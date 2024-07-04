---
name: Assignments
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/assignments.png
url: https://example.com/apis/assignments.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Assignments
apis:
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
  - aid: bigcommerce:channels
    name: Channels
    description: Needs a description
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.bigcommerce.com/
    baseURL: https://api.example.com
    tags: []
    properties:
      - type: Documentation
        url: https://developer.bigcommerce.com/
      - type: OpenAPI
        data:
          openapi: 3.0.0
          info:
            version: ''
            title: Channels
          tags:
            - name: Batch metafields
            - name: Channels
            - name: Metafields
            - name: Menus
            - name: Active Theme
            - name: Currency Assignments
            - name: Listings
            - name: Site
            - name: Site Checkout URL
          paths:
            /channels:
              parameters:
                - null
              get:
                tags:
                  - Get
                  - All
                  - Channels
                  - Channels
                summary: Get All Channels
                description: >-
                  Returns a list of *Channels*.


                  Will always return the default BigCommerce storefront with an
                  ID of `1`. This storefront is created by default when you
                  provision a BigCommerce store.
              post:
                tags:
                  - Create
                  - Channel
                  - Channels
                summary: Create a Channel
                description: Creates a *Channel*.
            /channels/{channel_id}:
              parameters:
                - null
                - null
              get:
                tags:
                  - Get
                  - Channel
                  - Channels
                  - Channel_id
                summary: Get a Channel
                description: >-
                  Returns a *Channel*. Channel ID `1` returns the default
                  BigCommerce storefront.
              put:
                tags:
                  - Update
                  - Channel
                  - Channels
                  - Channel_id
                summary: Update a Channel
                description: >-
                  Updates a *Channel*.


                  ## Updatable Fields


                  The following fields can be updated.

                  * `name`

                  * `external_id`

                  * `status`

                  * `is_listable_from_ui`

                  * `is_visible`

                  * `config_meta`



                  > #### Note

                  > * Partial updates are supported. In most cases, if a field
                  that *cannot* be updated is passed in, the API **will not**
                  respond with an error. It returns a 200 response with the
                  object, in which you will see the field(s) were not updated.

                  > * `platform` and `type` cannot be updated after a channel is
                  created.

                  > * A channel with status `deleted` or `terminated` cannot be
                  updated.
            /channels/{channel_id}/active-theme:
              parameters:
                - null
                - null
              get:
                tags:
                  - Get
                  - Channel
                  - Active
                  - Theme
                  - Channels
                  - Channel_id
                  - Active
                  - Theme
                summary: Get a Channel Active Theme
                description: |-
                  Returns details of the theme active on the specified channel.
                  Does not support active Blueprint (legacy) themes.
            /channels/currency-assignments:
              parameters:
                - null
              get:
                tags:
                  - Get
                  - All
                  - Channels
                  - Currency
                  - Assignments
                  - Channels
                  - Channel_id
                  - Active
                  - Theme
                  - Currency
                  - Assignments
                summary: Get All Channels Currency Assignments
                description: Returns a list of currency assignments for all channels.
              post:
                tags:
                  - Create
                  - Multiple
                  - Channels
                  - Currency
                  - Assignments
                  - Channels
                  - Channel_id
                  - Active
                  - Theme
                  - Currency
                  - Assignments
                summary: Create Multiple Channels Currency Assignments
                description: >-
                  Sets enabled currencies and default currency for multiple
                  channels. Note that currencies must be added first in the
                  **Settings > Setup > Currencies** settings from an active
                  MSF-enabled BigCommerce store control panel before the
                  currencies can be assigned to a channel.
              put:
                tags:
                  - Update
                  - Multiple
                  - Channels
                  - Currency
                  - Assignments
                  - Channels
                  - Channel_id
                  - Active
                  - Theme
                  - Currency
                  - Assignments
                summary: Update Multiple Channels Currency Assignments
                description: >-
                  Updates enabled currencies and default currency for multiple
                  channels. Note that currencies must be added first in the
                  **Settings > Setup > Currencies** settings from an active
                  MSF-enabled BigCommerce store control panel before the
                  currencies can be assigned to a channel.
            /channels/{channel_id}/currency-assignments:
              parameters:
                - null
                - null
              get:
                tags:
                  - Get
                  - Channel
                  - Currency
                  - Assignments
                  - Channels
                  - Channel_id
                  - Active
                  - Theme
                  - Currency
                  - Assignments
                summary: Get Channel Currency Assignments
                description: Returns a list of currency assignments for a specific channel.
              post:
                tags:
                  - Create
                  - Channel
                  - Currency
                  - Assignments
                  - Channels
                  - Channel_id
                  - Active
                  - Theme
                  - Currency
                  - Assignments
                summary: Create Channel Currency Assignments
                description: >-
                  Sets enabled currencies and default currency for a specific
                  channel. Note that currencies must be added first in the
                  **Settings > Setup > Currencies** settings from an active
                  MSF-enabled BigCommerce store control panel before the
                  currencies can be assigned to a channel.
              put:
                tags:
                  - Update
                  - Channel
                  - Currency
                  - Assignments
                  - Channels
                  - Channel_id
                  - Active
                  - Theme
                  - Currency
                  - Assignments
                summary: Update Channel Currency Assignments
                description: >-
                  Updates enabled currencies and default currency for a specific
                  channel. Note that currencies must be added first in the
                  **Settings > Setup > Currencies** settings from an active
                  MSF-enabled BigCommerce store control panel before the
                  currencies can be assigned to a channel.
              delete:
                tags:
                  - Delete
                  - Channel
                  - Currency
                  - Assignments
                  - Channels
                  - Channel_id
                  - Active
                  - Theme
                  - Currency
                  - Assignments
                summary: Delete Channel Currency Assignments
                description: >-
                  Deletes currency assignments for a specific channel. Once
                  done, this channel will inherit the store’s currency settings.
            /channels/{channel_id}/listings:
              parameters:
                - null
                - null
              get:
                tags:
                  - Get
                  - Channel
                  - Listings
                  - Channels
                  - Channel_id
                  - Active
                  - Theme
                  - Currency
                  - Assignments
                  - Listings
                summary: Get Channel Listings
                description: >-
                  Returns a list of all *Channel Listings* for a specific
                  channel. Note that if the *Channel* is not found or there is
                  no listing associated to the *Channel*, it will return a 200
                  response with empty data.
              post:
                tags:
                  - Create
                  - Channel
                  - Listings
                  - Channels
                  - Channel_id
                  - Active
                  - Theme
                  - Currency
                  - Assignments
                  - Listings
                summary: Create Channel Listings
                description: Creates one or more *Channel Listings* for a specific channel.
              put:
                tags:
                  - Update
                  - Channel
                  - Listings
                  - Channels
                  - Channel_id
                  - Active
                  - Theme
                  - Currency
                  - Assignments
                  - Listings
                summary: Update Channel Listings
                description: >-
                  Updates one or more *Channel Listings* for a specific channel.


                  > #### Note

                  > * Partial updates are supported. In most cases, if a field
                  that *cannot* be updated is passed in, the API **will not**
                  respond with an error. It returns a 200 response with the
                  object, in which you will see the field(s) were not updated.

                  > * If a new variant is provided, the API will append the
                  variant to the list. If a variant already exists, the API will
                  update the existing variant. Other variants that are not
                  provided in the payload remains unchanged.

                  > * If `listing_id` does not exist, the API will return a 200
                  response with empty data.

                  > * `listing_id` is required and cannot be less than or equal
                  to zero.

                  > * `product_id` cannot be updated after a channel listing is
                  created.

                  > * `product_id` of a variant must match the `product_id` of
                  the channel listing.
            /channels/{channel_id}/listings/{listing_id}:
              parameters:
                - null
                - null
                - null
              get:
                tags:
                  - Get
                  - Channel
                  - Listing
                  - Channels
                  - Channel_id
                  - Active
                  - Theme
                  - Currency
                  - Assignments
                  - Listings
                  - Listing_id
                summary: Get a Channel Listing
                description: Returns a *Channel Listing* for a specific channel.
            /channels/{channel_id}/site/checkout-url:
              parameters:
                - null
                - null
              put:
                summary: Upsert a Siteʼs Checkout URL
                tags:
                  - Upsert
                  - Siteʼs
                  - Checkout
                  - Channels
                  - Channel_id
                  - Active
                  - Theme
                  - Currency
                  - Assignments
                  - Listings
                  - Listing_id
                  - Site
                  - Checkout
                  - Url
                description: Creates or updates (upserts) a siteʼs checkout URL
              delete:
                summary: Delete a Siteʼs Checkout URL
                description: >-
                  Deletes a siteʼs checkout URL. After deletion, a shared
                  checkout URL is used.
                tags:
                  - Delete
                  - Siteʼs
                  - Checkout
                  - Channels
                  - Channel_id
                  - Active
                  - Theme
                  - Currency
                  - Assignments
                  - Listings
                  - Listing_id
                  - Site
                  - Checkout
                  - Url
            /channels/{channel_id}/site:
              parameters:
                - null
                - null
              get:
                summary: Get a Channel Site
                description: |
                  Alias of `GET /sites?channel_id=channel_id`

                  Returns site data for the specified channel.
                tags:
                  - Get
                  - Channel
                  - Site
                  - Channels
                  - Channel_id
                  - Active
                  - Theme
                  - Currency
                  - Assignments
                  - Listings
                  - Listing_id
                  - Site
                  - Checkout
                  - Url
              put:
                summary: Update a Channel Site
                tags:
                  - Update
                  - Channel
                  - Site
                  - Channels
                  - Channel_id
                  - Active
                  - Theme
                  - Currency
                  - Assignments
                  - Listings
                  - Listing_id
                  - Site
                  - Checkout
                  - Url
                description: Updates a site for provided channel.
              post:
                summary: Create a Channel Site
                tags:
                  - Create
                  - Channel
                  - Site
                  - Channels
                  - Channel_id
                  - Active
                  - Theme
                  - Currency
                  - Assignments
                  - Listings
                  - Listing_id
                  - Site
                  - Checkout
                  - Url
                description: Alias of POST `/sites`. Creates a site for provided channel.
              delete:
                description: Deletes the Channelʼs site.
                tags:
                  - Delete
                  - Channel
                  - Site
                  - Channels
                  - Channel_id
                  - Active
                  - Theme
                  - Currency
                  - Assignments
                  - Listings
                  - Listing_id
                  - Site
                  - Checkout
                  - Url
                summary: Delete a Channel Site
            /channels/{channel_id}/channel-menus:
              parameters:
                - null
                - null
              get:
                summary: Get Channel Menus
                description: >
                  Returns list of Control Panel side navigation menus for a
                  channel.
                tags:
                  - Get
                  - Channel
                  - Menus
                  - Channels
                  - Channel_id
                  - Active
                  - Theme
                  - Currency
                  - Assignments
                  - Listings
                  - Listing_id
                  - Site
                  - Checkout
                  - Url
                  - Channel
                  - Menus
              post:
                summary: Create Channel Menus
                tags:
                  - Create
                  - Channel
                  - Menus
                  - Channels
                  - Channel_id
                  - Active
                  - Theme
                  - Currency
                  - Assignments
                  - Listings
                  - Listing_id
                  - Site
                  - Checkout
                  - Url
                  - Channel
                  - Menus
                description: >-
                  Creates or replaces list of control panel side navigation
                  menus for a channel.
              delete:
                description: Deletes control panel side navigation menus for a channel.
                tags:
                  - Delete
                  - Channel
                  - Menus
                  - Channels
                  - Channel_id
                  - Active
                  - Theme
                  - Currency
                  - Assignments
                  - Listings
                  - Listing_id
                  - Site
                  - Checkout
                  - Url
                  - Channel
                  - Menus
                summary: Delete Channel Menus
            /channels/{channel_id}/metafields:
              parameters:
                - null
                - null
              get:
                summary: Get Channel Metafields
                tags:
                  - Get
                  - Channel
                  - Metafields
                  - Channels
                  - Channel_id
                  - Active
                  - Theme
                  - Currency
                  - Assignments
                  - Listings
                  - Listing_id
                  - Site
                  - Checkout
                  - Url
                  - Channel
                  - Menus
                  - Metafields
                description: >-
                  Returns a list of metafields on a channel. Optional filter
                  parameters can be passed in.
              post:
                summary: Create a Channel Metafield
                tags:
                  - Create
                  - Channel
                  - Metafield
                  - Channels
                  - Channel_id
                  - Active
                  - Theme
                  - Currency
                  - Assignments
                  - Listings
                  - Listing_id
                  - Site
                  - Checkout
                  - Url
                  - Channel
                  - Menus
                  - Metafields
                description: >-
                  Creates a channel metafield.


                  **Note:** The maxiumum number of metafields allowed on each
                  order, product, category, variant, channel, or brand is 250
                  per client ID. For more information, see [Platform
                  Limits](https://support.bigcommerce.com/s/article/Platform-Limits)
                  in the Help Center.
            /channels/{channel_id}/metafields/{metafield_id}:
              parameters:
                - null
                - null
                - null
              get:
                summary: Get a Channel Metafield
                tags:
                  - Get
                  - Channel
                  - Metafield
                  - Channels
                  - Channel_id
                  - Active
                  - Theme
                  - Currency
                  - Assignments
                  - Listings
                  - Listing_id
                  - Site
                  - Checkout
                  - Url
                  - Channel
                  - Menus
                  - Metafields
                  - Metafield_id
                description: Returns a single channel metafield.
              put:
                summary: Update a Channel Metafield
                tags:
                  - Update
                  - Channel
                  - Metafield
                  - Channels
                  - Channel_id
                  - Active
                  - Theme
                  - Currency
                  - Assignments
                  - Listings
                  - Listing_id
                  - Site
                  - Checkout
                  - Url
                  - Channel
                  - Menus
                  - Metafields
                  - Metafield_id
                description: >-
                  Updates a single channel metafield.


                  **Usage Notes**

                  * Attempting to modify `namespace`, `key`, and
                  `permission_set` fields using a client ID different from the
                  one used to create those metafields will result in a `403`
                  error message. 
              delete:
                summary: Delete a Channel Metafield
                tags:
                  - Delete
                  - Channel
                  - Metafield
                  - Channels
                  - Channel_id
                  - Active
                  - Theme
                  - Currency
                  - Assignments
                  - Listings
                  - Listing_id
                  - Site
                  - Checkout
                  - Url
                  - Channel
                  - Menus
                  - Metafields
                  - Metafield_id
                description: Deletes a single channel metafield.
            /channels/metafields:
              get:
                summary: Get All Channel Metafields
                tags:
                  - Get
                  - All
                  - Channel
                  - Metafields
                  - Channels
                  - Channel_id
                  - Active
                  - Theme
                  - Currency
                  - Assignments
                  - Listings
                  - Listing_id
                  - Site
                  - Checkout
                  - Url
                  - Channel
                  - Menus
                  - Metafields
                  - Metafield_id
                description: Get all channel metafields.
              post:
                summary: Create multiple Metafields
                tags:
                  - Create
                  - Multiple
                  - Metafields
                  - Channels
                  - Channel_id
                  - Active
                  - Theme
                  - Currency
                  - Assignments
                  - Listings
                  - Listing_id
                  - Site
                  - Checkout
                  - Url
                  - Channel
                  - Menus
                  - Metafields
                  - Metafield_id
                description: Create multiple metafields.
              put:
                summary: Update multiple Metafields
                tags:
                  - Update
                  - Multiple
                  - Metafields
                  - Channels
                  - Channel_id
                  - Active
                  - Theme
                  - Currency
                  - Assignments
                  - Listings
                  - Listing_id
                  - Site
                  - Checkout
                  - Url
                  - Channel
                  - Menus
                  - Metafields
                  - Metafield_id
                description: Update multiple metafields.
              delete:
                summary: Delete All Metafields
                tags:
                  - Delete
                  - All
                  - Metafields
                  - Channels
                  - Channel_id
                  - Active
                  - Theme
                  - Currency
                  - Assignments
                  - Listings
                  - Listing_id
                  - Site
                  - Checkout
                  - Url
                  - Channel
                  - Menus
                  - Metafields
                  - Metafield_id
                description: Delete all channel
    overlays:
      - type: APIs.io Search
        url: overlays/channels-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/channels-openapi-api-evangelist-ratings.yml
  - aid: bigcommerce:price-lists
    name: Price Lists
    description: Needs a description
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.bigcommerce.com/
    baseURL: https://api.example.com
    tags: []
    properties:
      - type: Documentation
        url: https://developer.bigcommerce.com/
      - type: OpenAPI
        data:
          openapi: 3.0.1
          info:
            title: Price Lists
            version: ''
          tags:
            - name: Price Lists
            - name: Price Lists Assignments
            - name: Price Lists Records
          paths:
            /pricelists:
              parameters:
                - null
              get:
                tags:
                  - Get
                  - All
                  - Price
                  - Lists
                  - Pricelists
                summary: Get All Price Lists
                description: >-
                  Returns a list of *Price Lists*. Optional parameters can be
                  passed in.
              post:
                tags:
                  - Create
                  - Price
                  - List
                  - Pricelists
                summary: Create a Price List
                description: |-
                  Creates a *Price List*.

                  **Required Fields**
                  * name
              delete:
                tags:
                  - Delete
                  - All
                  - Price
                  - Lists
                  - Pricelists
                summary: Delete All Price Lists
                description: >-
                  Deletes a *Price List*. All associated price records are also
                  removed. Optional parameters can be passed in.
            /pricelists/{price_list_id}:
              parameters:
                - null
              get:
                tags:
                  - Get
                  - Price
                  - List
                  - Pricelists
                  - Price_list_id
                summary: Get a Price List
                description: ' Returns a single *Price List*.'
              put:
                tags:
                  - Update
                  - Price
                  - List
                  - Pricelists
                  - Price_list_id
                summary: Update a Price List
                description: Updates a *Price List*.
              delete:
                tags:
                  - Delete
                  - Price
                  - List
                  - Pricelists
                  - Price_list_id
                summary: Delete a Price List
                description: >-
                  Deletes a *Price List*. All associated price records are also
                  removed.

                  **Limits**

                  * Limit of 1 concurrent request.
            /pricelists/records:
              parameters:
                - null
              put:
                tags:
                  - Create
                  - Batch
                  - Of
                  - Price
                  - Lists
                  - Records
                  - Pricelists
                  - Price_list_id
                  - Records
                summary: Create Batch of Price Lists Records
                description: >-
                  Creates a batch of `Price Lists Records`; may include price
                  list records from more than one price list.  Concurrency limit
                  of 1.
            /pricelists/{price_list_id}/records:
              parameters:
                - null
              get:
                tags:
                  - Get
                  - All
                  - Price
                  - List
                  - Records
                  - Pricelists
                  - Price_list_id
                  - Records
                summary: Get All Price List Records
                description: >-
                  Returns a list of *Price List Records* associated with a
                  *Price List*.


                  **Notes**

                  * Supports up to 10 simultaneous GET requests. Running more
                  than the allowed number of requests concurrently on the same
                  store will result in a `429` status error and your additional
                  requests will fail.

                  * Store Pricelist Records data to reduce the number of calls
                  and maximize performance.
              put:
                tags:
                  - Upsert
                  - Price
                  - List
                  - Records
                  - Pricelists
                  - Price_list_id
                  - Records
                summary: Upsert Price List Records
                description: >-
                  Creates or updates *Price List Records*. 


                  **Required Fields**

                  * currency


                  **Notes**

                  * Batch requests support up to 1,000 items per request.

                  * Up to 2 concurrent batch upsert requests are supported with
                  this API. Running more than the allowed concurrent requests in
                  parallel on the **same store** will cause a `429` error, and
                  your additional requests will fail. You are encouraged to run
                  requests sequentially with as many records per request as
                  possible to maximize performance.

                  * When updating a product with variants, or multiple SKUs,
                  don't include records for the parent product SKU.
              delete:
                tags:
                  - Delete
                  - Price
                  - List
                  - Record
                  - Pricelists
                  - Price_list_id
                  - Records
                summary: Delete a Price List Record
                description: >-
                  Deletes a *Price List Record*. Deleting the records does not
                  delete the Price List. Optional parameters can be passed in.
            /pricelists/{price_list_id}/records/{variant_id}:
              parameters:
                - null
              get:
                tags:
                  - Get
                  - Price
                  - Records
                  - By
                  - Variant
                  - Pricelists
                  - Price_list_id
                  - Records
                  - Variant_id
                summary: Get Price Records by Variant
                description: >
                  Returns *Price List Records* using the variant ID. Will also
                  contain currency records.


                  **Notes**

                  * Supports up to 40 simultaneous GET requests. Running more
                  than the allowed number of requests concurrently on the same
                  store will result in a `429` status error, and your additional
                  requests will fail.

                  * Store Pricelist Records data to reduce the number of calls
                  and maximize performance.
            /pricelists/{price_list_id}/records/{variant_id}/{currency_code}:
              parameters:
                - null
              get:
                tags:
                  - Get
                  - Price
                  - Record
                  - By
                  - Currency
                  - Code
                  - Pricelists
                  - Price_list_id
                  - Records
                  - Variant_id
                  - Currency_code
                summary: Get a Price Record by Currency Code
                description: >-
                  Returns a *Price List Record* using the currency code. You can
                  use optional parameters.

                  **Notes**

                  * Supports up to 50 simultaneous GET requests. Running more
                  than the allowed number of requests concurrently on the same
                  store will result in a `429` status error, and your additional
                  requests will fail.
              put:
                tags:
                  - Set
                  - Price
                  - List
                  - Record
                  - By
                  - Currency
                  - Code
                  - Pricelists
                  - Price_list_id
                  - Records
                  - Variant_id
                  - Currency_code
                summary: Set Price List Record by Currency Code
                description: >-
                  Creates or updates a *Price List Record* using the currency
                  code.

                  **Notes**

                  * Supports up to 40 simultaneous PUT requests. Running more
                  than the allowed number of requests concurrently on the same
                  store will result in a `429` status error, and your additional
                  requests will fail.
              delete:
                tags:
                  - Delete
                  - Price
                  - Record
                  - By
                  - Currency
                  - Code
                  - Pricelists
                  - Price_list_id
                  - Records
                  - Variant_id
                  - Currency_code
                summary: Delete a Price Record by Currency Code
                description: >-
                  Deletes a *Price List Record* using the currency code.

                  **Note:**

                  * Supports up to 25 simultaneous DELETE requests. Running more
                  than the allowed number of requests concurrently on the same
                  store will result in a `429` status error, and your additional
                  requests will fail.
            /pricelists/assignments:
              parameters:
                - null
              get:
                tags:
                  - Get
                  - Price
                  - List
                  - Assignments
                  - Pricelists
                  - Price_list_id
                  - Records
                  - Variant_id
                  - Currency_code
                  - Assignments
                summary: Get Price List Assignments
                description: >-
                  Fetches an array of `Price List Assignments` matching a
                  particular Customer Group and Price List and Channel.
              post:
                tags:
                  - Create
                  - Price
                  - List
                  - Assignments
                  - Pricelists
                  - Price_list_id
                  - Records
                  - Variant_id
                  - Currency_code
                  - Assignments
                description: |-
                  Creates a batch of `Price List Assignments`. 
                  **Note:** The batch limit for `Price List Assignments` is 25.
                summary: Create Price List Assignments
              delete:
                tags:
                  - Delete
                  - Price
                  - List
                  - Assignments
                  - Pricelists
                  - Price_list_id
                  - Records
                  - Variant_id
                  - Currency_code
                  - Assignments
                summary: Delete Price List Assignments
                description: >-
                  Deletes one or more `Price List Assignments` objects from
                  BigCommerce using a query parameter. You must use at least one
                  query parameter. 
            /pricelists/{price_list_id}/assignments:
              parameters:
                - null
              put:
                tags:
                  - Upsert
                  - Price
                  - List
                  - Pricelists
                  - Price_list_id
                  - Records
                  - Variant_id
                  - Currency_code
                  - Assignments
                description: >-
                  Upsert a single `Price List Assignment` for a `Price List`.

                  **Note:**

                  * Supports up to 25 simultaneous PUT requests. Running more
                  than the allowed number of requests concurrently on the same
                  store will result in a `429` status error and your additional
                  requests will fail.        
                summary: Upsert Price Li
    overlays:
      - type: APIs.io Search
        url: overlays/price-lists-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/price-lists-openapi-api-evangelist-ratings.yml
  - aid: bigcommerce:catalog-products
    name: Catalog - Products
    description: Needs a description
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.bigcommerce.com/
    baseURL: https://api.example.com
    tags: []
    properties:
      - type: Documentation
        url: https://developer.bigcommerce.com/
      - type: OpenAPI
        data:
          openapi: 3.0.3
          info:
            title: Catalog - Products
            version: ''
          tags:
            - name: Batch metafields
            - name: Products
            - name: Bulk Pricing Rules
            - name: Complex Rules
            - name: Custom Fields
            - name: Images
            - name: Metafields
            - name: Reviews
            - name: Videos
            - name: Channel Assignments
            - name: Category Assignments
            - name: Summary
          paths:
            /catalog/products:
              get:
                tags:
                  - Get
                  - All
                  - Products
                  - Catalog
                  - Products
                summary: Get All Products
                description: >-
                  Returns a list of **Products**. Optional filter parameters can
                  be passed in.
              put:
                tags:
                  - Update
                  - Products
                  - Batch)
                  - Catalog
                  - Products
                summary: Update Products (Batch)
                description: >-
                  Updates products in batches. Batches are limited to 10
                  products.


                  **Required Fields**

                  * `id` - product `id` is required for batch updates to
                  products.


                  **Read-Only Fields**

                  - `id`

                  - `date_created`

                  - `date_modified`

                  - `calculated_price`

                  - `base_variant_id`
              post:
                tags:
                  - Create
                  - Product
                  - Catalog
                  - Products
                summary: Create a Product
                description: >-
                  Creates a *Product*. Only one product can be created at a
                  time; however, you can create multiple product variants using
                  the `variants` array.


                  **Required Fields:**

                  - `name`

                  - `type`

                  - `weight`

                  - `price`


                  **Read-Only Fields**

                  - `id`

                  - `date_created`

                  - `date_modified`

                  - `calculated_price`

                  - `base_variant_id`


                  **Limits**

                  - 250 characters product name length.

                  - A product can have up to 1000 images. Each image file or
                  image uploaded by URL can be up to 8 MB.


                  **Usage Notes**

                  * You can create multiple product variants using the
                  `variants` array.

                  * This endpoint accepts a `video` array. To create a product
                  video that accepts a `video` object, see [Create a Product
                  Video](/docs/rest-catalog/products/videos#create-a-product-video)
                  for information.
              delete:
                tags:
                  - Delete
                  - Products
                  - Catalog
                  - Products
                summary: Delete Products
                description: >-
                  To delete *Product* objects, you must include a filter. This
                  prevents inadvertently deleting all *Product* objects in a
                  store.


                  > #### Note

                  > The maximum number of products you can delete at one time is
                  250.


                  **Example**:

                  To delete products with IDs 1,2 and 3, use `DELETE
                  /v3/catalog/products?id:in=1,2,3`.
              parameters:
                - null
            /catalog/products/{product_id}:
              get:
                tags:
                  - Get
                  - Product
                  - Catalog
                  - Products
                  - Product_id
                summary: Get a Product
                description: >-
                  Returns a single *Product*. Optional parameters can be passed
                  in.
              put:
                tags:
                  - Update
                  - Product
                  - Catalog
                  - Products
                  - Product_id
                summary: Update a Product
                description: >
                  Updates a *Product*.


                  **Limits**

                  - A product can have up to 1000 images. Each image file or
                  image uploaded by URL can be up to 8 MB.


                  **Read-Only Fields**

                  - id

                  - date_created

                  - date_modified

                  - calculated_price

                  - base_variant_id
              delete:
                tags:
                  - Delete
                  - Product
                  - Catalog
                  - Products
                  - Product_id
                summary: Delete a Product
                description: Deletes a *Product*.
              parameters:
                - null
                - null
            /catalog/products/{product_id}/images:
              get:
                tags:
                  - Get
                  - All
                  - Product
                  - Images
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                summary: Get All Product Images
                description: >-
                  Returns a list of *Product Images*. Optional parameters can be
                  passed in.
              post:
                tags:
                  - Create
                  - Product
                  - Image
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                summary: Create a Product Image
                description: >-
                  Creates a *Product Image*.

                   **Required Fields**
                  - `image_file`, or

                  - `image_url`


                  **Usage Notes**

                  - `image_url` - `255` character limit

                  - For file uploads, use the `multipart/form-data` media type.

                  - You can create only one image at a time. A product can have
                  up to 1000 images.

                  - Supported image file types are BMP, GIF, JPEG, PNG, WBMP,
                  XBM, and WEBP.

                  - Each image file or image uploaded by URL can be up to 8 MB.
              parameters:
                - null
                - null
            /catalog/products/{product_id}/images/{image_id}:
              get:
                tags:
                  - Get
                  - Product
                  - Image
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                summary: Get a Product Image
                description: >-
                  Returns a single *Product Image*. Optional parameters can be
                  passed in.
              put:
                tags:
                  - Update
                  - Product
                  - Image
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                summary: Update a Product Image
                description: >-
                  Updates a *Product Image*.


                  **Usage Notes**

                  - `image_url` - `255` character limit

                  - Each image file or image uploaded by URL can be up to 8 MB.

                  - For file uploads, send a POST request using the
                  `multipart/form-data` media type
              delete:
                tags:
                  - Delete
                  - Product
                  - Image
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                summary: Delete a Product Image
                description: Deletes a *Product Image*.
              parameters:
                - null
                - null
                - null
            /catalog/products/{product_id}/videos:
              get:
                tags:
                  - Get
                  - All
                  - Product
                  - Videos
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                summary: Get All Product Videos
                description: >-
                  Returns a list of *Product Videos*. Optional parameters can be
                  passed in.
              post:
                tags:
                  - Create
                  - Product
                  - Video
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                summary: Create a Product Video
                description: |-
                  Creates a *Product Video*.

                  **Required Fields**
                  * video_id

                  **Read-Only Fields**
                  * id

                  Publicly accessible URLs are valid parameters.
                  Videos must be loaded through YouTube at this time.
              parameters:
                - null
                - null
            /catalog/products/{product_id}/videos/{id}:
              get:
                tags:
                  - Get
                  - Product
                  - Video
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                summary: Get a Product Video
                description: >-
                  Returns a single *Product Video*. Optional parameters can be
                  passed in.
              put:
                tags:
                  - Update
                  - Product
                  - Video
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                summary: Update a Product Video
                description: |-
                  Updates a *Product Video.

                  **Required Fields**
                  * none

                  **Read-Only Fields**
                  * id
              delete:
                tags:
                  - Delete
                  - Product
                  - Video
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                summary: Delete a Product Video
                description: Deletes a *Product Video*.
              parameters:
                - null
                - null
                - null
            /catalog/products/{product_id}/complex-rules:
              get:
                tags:
                  - Get
                  - Complex
                  - Rules
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                summary: Get Complex Rules
                description: >-
                  Returns a list of all product *Complex Rules*. Optional
                  parameters may be passed in.
              post:
                tags:
                  - Create
                  - Complex
                  - Rule
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                summary: Create a Complex Rule
                description: |-
                  Creates a product *Complex Rule*.

                  **Required Fields**
                  - modifier_id
                  - modifier_value_id
                  - variant_id

                  **Read-Only Fields**
                  - complex_rule_id
                  - conditions_id
                  - rule_id
                  - combination_id
                  - id
              parameters:
                - null
                - null
            /catalog/products/{product_id}/complex-rules/{complex_rule_id}:
              get:
                tags:
                  - Get
                  - Product
                  - Complex
                  - Rule
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                summary: Get a Product Complex Rule
                description: >-
                  Returns a single *Complex Rule*. Optional parameters can be
                  passed in.
              put:
                tags:
                  - Update
                  - Product
                  - Complex
                  - Rule
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                summary: Update a Product Complex Rule
                description: |-
                  Updates a *Complex Rule*.

                  **Required Fields**:
                  - none

                  **Read-Only Fields**:
                  - complex_rule_id
                  - conditions_id
                  - rule_id
                  - combination_id
                  - id
              delete:
                tags:
                  - Delete
                  - Product
                  - Complex
                  - Rule
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                summary: Delete a Product Complex Rule
                description: Deletes a product *Complex Rule*.
              parameters:
                - null
                - null
                - null
            /catalog/products/{product_id}/custom-fields:
              get:
                tags:
                  - Get
                  - Product
                  - Custom
                  - Fields
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                  - Custom
                  - Fields
                summary: Get Product Custom Fields
                description: >-
                  Returns a list of product *Custom Fields*. You can pass in
                  optional parameters.


                  **Note:**

                  The default rate limit for this endpoint is 40 concurrent
                  requests.
              post:
                tags:
                  - Create
                  - Product
                  - Custom
                  - Field
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                  - Custom
                  - Fields
                summary: Create a Product Custom Field
                description: >-
                  Creates a *Custom Field*.


                  **Required Fields:**

                  - name

                  - value


                  **Name-Value Pair Uniqueness**

                  - Every name-value pair must be unique inside a product.


                  **Read-Only:**

                  - id


                  **Limits**

                  - 200 custom fields per product limit.

                  - 250 characters per custom field limit.


                  **Note:**

                  The default rate limit for this endpoint is 40 concurrent
                  requests.
              parameters:
                - null
            /catalog/products/{product_id}/custom-fields/{custom_field_id}:
              get:
                tags:
                  - Get
                  - Product
                  - Custom
                  - Field
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                  - Custom
                  - Fields
                  - Custom_field_id
                summary: Get a Product Custom Field
                description: >
                  Returns a *Custom Field*.


                  **Note:**

                  The default rate limit for this endpoint is 40 concurrent
                  requests.
              put:
                tags:
                  - Update
                  - Product
                  - Custom
                  - Field
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                  - Custom
                  - Fields
                  - Custom_field_id
                summary: Update a Product Custom Field
                description: |-
                  Updates a *Custom Field*.

                  **Required Fields**
                  - none

                  **Name-Value Pair Uniqueness**
                  - Every name-value pair must be unique inside a product.

                  **Read-Only**
                  - id

                   **Limits**
                  - 200 custom fields per product limit.
                  - 250 characters per custom field limit.
                  - 40 concurrent requests default rate limit.
              delete:
                tags:
                  - Delete
                  - Product
                  - Custom
                  - Field
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                  - Custom
                  - Fields
                  - Custom_field_id
                summary: Delete a Product Custom Field
                description: >-
                  Deletes a product *Custom Field*.


                  **Note:**

                  The default rate limit for this endpoint is 40 concurrent
                  requests.
              parameters:
                - null
                - null
            /catalog/products/{product_id}/bulk-pricing-rules/{bulk_pricing_rule_id}:
              get:
                tags:
                  - Get
                  - Bulk
                  - Pricing
                  - Rule
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                  - Custom
                  - Fields
                  - Custom_field_id
                  - Bulk
                  - Pricing
                  - Bulk_pricing_rule_id
                summary: Get a Bulk Pricing Rule
                description: >-
                  Returns a single *Bulk Pricing Rule*. Optional parameters can
                  be passed in.
              put:
                tags:
                  - Update
                  - Bulk
                  - Pricing
                  - Rule
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                  - Custom
                  - Fields
                  - Custom_field_id
                  - Bulk
                  - Pricing
                  - Bulk_pricing_rule_id
                summary: Update a Bulk Pricing Rule
                description: |-
                  Updates a *Bulk Pricing Rule*.

                  **Required Fields**
                  * none

                  **Read-Only Fields**
                  - id
              delete:
                tags:
                  - Delete
                  - Bulk
                  - Pricing
                  - Rule
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                  - Custom
                  - Fields
                  - Custom_field_id
                  - Bulk
                  - Pricing
                  - Bulk_pricing_rule_id
                summary: Delete a Bulk Pricing Rule
                description: Deletes a *Bulk Pricing Rule*.
              parameters:
                - null
                - null
                - null
            /catalog/products/{product_id}/metafields:
              get:
                tags:
                  - Get
                  - Product
                  - Metafields
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                  - Custom
                  - Fields
                  - Custom_field_id
                  - Bulk
                  - Pricing
                  - Bulk_pricing_rule_id
                  - Metafields
                summary: Get Product Metafields
                description: >-
                  Returns a list of *Product Metafields*. Optional parameters
                  can be passed in.
              post:
                tags:
                  - Create
                  - Product
                  - Metafield
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                  - Custom
                  - Fields
                  - Custom_field_id
                  - Bulk
                  - Pricing
                  - Bulk_pricing_rule_id
                  - Metafields
                summary: Create a Product Metafield
                description: >-
                  Creates a *Product Metafield*.


                  **Required Fields:**

                  * permission_set

                  * namespace

                  * key

                  * value


                  **Note:** The maxiumum number of metafields allowed on each
                  order, product, category, variant, or brand is 250 per client
                  ID. For more information, see [Platform
                  Limits](https://support.bigcommerce.com/s/article/Platform-Limits)
                  in the Help Center.
              parameters:
                - null
                - null
            /catalog/products/{product_id}/metafields/{metafield_id}:
              get:
                tags:
                  - Get
                  - Product
                  - Metafield
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                  - Custom
                  - Fields
                  - Custom_field_id
                  - Bulk
                  - Pricing
                  - Bulk_pricing_rule_id
                  - Metafields
                  - Metafield_id
                summary: Get a Product Metafield
                description: >-
                  Returns a single *Product Metafield*. Optional parameters can
                  be passed in.
              put:
                tags:
                  - Update
                  - Product
                  - Metafield
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                  - Custom
                  - Fields
                  - Custom_field_id
                  - Bulk
                  - Pricing
                  - Bulk_pricing_rule_id
                  - Metafields
                  - Metafield_id
                summary: Update a Product Metafield
                description: "Updates a *Product Metafield*.\n\n**Required Fields**\n* none\n\n**Read-Only Fields**\n* id\n* These fields can only be modified using the API account that created the metafield:\n\t* `namespace`\n\t* `key`\n\t* `permission_set`\n\t* `value`\n\n**Usage Notes**\n* Attempting to modify the `namespace`, `key`, `permission_set`, or `value` field using an API account different from the one used to create those metafields will result in a `403` error message. "
              delete:
                tags:
                  - Delete
                  - Product
                  - Metafield
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                  - Custom
                  - Fields
                  - Custom_field_id
                  - Bulk
                  - Pricing
                  - Bulk_pricing_rule_id
                  - Metafields
                  - Metafield_id
                summary: Delete a Product Metafield
                description: Deletes a *Product Metafield*.
              parameters:
                - null
                - null
                - null
            /catalog/products/{product_id}/reviews:
              get:
                tags:
                  - Get
                  - Product
                  - Reviews
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                  - Custom
                  - Fields
                  - Custom_field_id
                  - Bulk
                  - Pricing
                  - Bulk_pricing_rule_id
                  - Metafields
                  - Metafield_id
                  - Reviews
                summary: Get Product Reviews
                description: >-
                  Returns a list of all *Product Reviews*. Optional parameters
                  can be passed in.
              post:
                tags:
                  - Create
                  - Product
                  - Review
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                  - Custom
                  - Fields
                  - Custom_field_id
                  - Bulk
                  - Pricing
                  - Bulk_pricing_rule_id
                  - Metafields
                  - Metafield_id
                  - Reviews
                summary: Create a Product Review
                description: |-
                  Creates a *Product Review*.

                  **Required Fields**
                  - title
                  - date_reviewed

                  **Read-Only Fields**
                  * id
              parameters:
                - null
                - null
            /catalog/products/{product_id}/reviews/{review_id}:
              get:
                tags:
                  - Get
                  - Product
                  - Review
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                  - Custom
                  - Fields
                  - Custom_field_id
                  - Bulk
                  - Pricing
                  - Bulk_pricing_rule_id
                  - Metafields
                  - Metafield_id
                  - Reviews
                  - Review_id
                summary: Get a Product Review
                description: >-
                  Returns a single *Product Review*. Optional parameters maybe
                  passed in.
              put:
                tags:
                  - Update
                  - Product
                  - Review
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                  - Custom
                  - Fields
                  - Custom_field_id
                  - Bulk
                  - Pricing
                  - Bulk_pricing_rule_id
                  - Metafields
                  - Metafield_id
                  - Reviews
                  - Review_id
                summary: Update a Product Review
                description: |-
                  Updates a *Product Review*.

                  **Required Fields**
                  * none

                  **Read-Only Fields**
                  * id
              delete:
                tags:
                  - Delete
                  - Product
                  - Review
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                  - Custom
                  - Fields
                  - Custom_field_id
                  - Bulk
                  - Pricing
                  - Bulk_pricing_rule_id
                  - Metafields
                  - Metafield_id
                  - Reviews
                  - Review_id
                summary: Delete a Product Review
                description: Deletes a *Product Review*.
              parameters:
                - null
                - null
                - null
            /catalog/products/channel-assignments:
              get:
                summary: Get Products Channel Assignments
                description: Returns a list of products channel assignments.
                tags:
                  - Get
                  - Products
                  - Channel
                  - Assignments
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                  - Custom
                  - Fields
                  - Custom_field_id
                  - Bulk
                  - Pricing
                  - Bulk_pricing_rule_id
                  - Metafields
                  - Metafield_id
                  - Reviews
                  - Review_id
                  - Channel
                  - Assignments
              put:
                summary: Create Products Channel Assignments
                description: Creates products channel assignments.
                tags:
                  - Create
                  - Products
                  - Channel
                  - Assignments
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                  - Custom
                  - Fields
                  - Custom_field_id
                  - Bulk
                  - Pricing
                  - Bulk_pricing_rule_id
                  - Metafields
                  - Metafield_id
                  - Reviews
                  - Review_id
                  - Channel
                  - Assignments
              delete:
                summary: Delete Products Channel Assignments
                description: >-
                  Delete products channel assignments. A filter must be
                  supplied.
                tags:
                  - Delete
                  - Products
                  - Channel
                  - Assignments
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                  - Custom
                  - Fields
                  - Custom_field_id
                  - Bulk
                  - Pricing
                  - Bulk_pricing_rule_id
                  - Metafields
                  - Metafield_id
                  - Reviews
                  - Review_id
                  - Channel
                  - Assignments
              parameters:
                - null
            /catalog/products/category-assignments:
              get:
                summary: Get Products Category Assignments
                description: Returns a list of products category assignments.
                tags:
                  - Get
                  - Products
                  - Category
                  - Assignments
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                  - Custom
                  - Fields
                  - Custom_field_id
                  - Bulk
                  - Pricing
                  - Bulk_pricing_rule_id
                  - Metafields
                  - Metafield_id
                  - Reviews
                  - Review_id
                  - Channel
                  - Assignments
                  - Category
              put:
                summary: Create Products Category Assignments.
                description: Creates products category assignments.
                tags:
                  - Create
                  - Products
                  - Category
                  - Assignments.
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                  - Custom
                  - Fields
                  - Custom_field_id
                  - Bulk
                  - Pricing
                  - Bulk_pricing_rule_id
                  - Metafields
                  - Metafield_id
                  - Reviews
                  - Review_id
                  - Channel
                  - Assignments
                  - Category
              delete:
                summary: Delete Products Category Assignments
                description: >-
                  Deletes products category assignments. A filter must be
                  supplied.
                tags:
                  - Delete
                  - Products
                  - Category
                  - Assignments
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                  - Custom
                  - Fields
                  - Custom_field_id
                  - Bulk
                  - Pricing
                  - Bulk_pricing_rule_id
                  - Metafields
                  - Metafield_id
                  - Reviews
                  - Review_id
                  - Channel
                  - Assignments
                  - Category
              parameters:
                - null
            /catalog/summary:
              get:
                tags:
                  - Get
                  - Catalog
                  - Summary
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                  - Custom
                  - Fields
                  - Custom_field_id
                  - Bulk
                  - Pricing
                  - Bulk_pricing_rule_id
                  - Metafields
                  - Metafield_id
                  - Reviews
                  - Review_id
                  - Channel
                  - Assignments
                  - Category
                  - Summary
                summary: Get a Catalog Summary
                description: >-
                  Returns a lightweight inventory summary from the BigCommerce
                  Catalog.


                  The inventory summary includes:

                  * "inventory_count"

                  * "variant_count"

                  * "inventory_value"

                  * "highest_variant_price"

                  * "average_variant_price"

                  * "lowest_variant_price"

                  * "oldest_variant_date"

                  * "newest_variant_date"

                  * "primary_category_id"

                  * "primary_category_name"
              parameters:
                - null
            /catalog/products/metafields:
              get:
                summary: Get All Product Metafields
                tags:
                  - Get
                  - All
                  - Product
                  - Metafields
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                  - Custom
                  - Fields
                  - Custom_field_id
                  - Bulk
                  - Pricing
                  - Bulk_pricing_rule_id
                  - Metafields
                  - Metafield_id
                  - Reviews
                  - Review_id
                  - Channel
                  - Assignments
                  - Category
                  - Summary
                description: Get all product metafields.
              post:
                summary: Create multiple Metafields
                tags:
                  - Create
                  - Multiple
                  - Metafields
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                  - Custom
                  - Fields
                  - Custom_field_id
                  - Bulk
                  - Pricing
                  - Bulk_pricing_rule_id
                  - Metafields
                  - Metafield_id
                  - Reviews
                  - Review_id
                  - Channel
                  - Assignments
                  - Category
                  - Summary
                description: Create multiple metafields.
              put:
                summary: Update multiple Metafields
                tags:
                  - Update
                  - Multiple
                  - Metafields
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                  - Custom
                  - Fields
                  - Custom_field_id
                  - Bulk
                  - Pricing
                  - Bulk_pricing_rule_id
                  - Metafields
                  - Metafield_id
                  - Reviews
                  - Review_id
                  - Channel
                  - Assignments
                  - Category
                  - Summary
                description: Update multiple metafields.
              delete:
                summary: Delete All Metafields
                tags:
                  - Delete
                  - All
                  - Metafields
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                  - Custom
                  - Fields
                  - Custom_field_id
                  - Bulk
                  - Pricing
                  - Bulk_pricing_rule_id
                  - Metafields
                  - Metafield_id
                  - Reviews
                  - Review_id
                  - Channel
                  - Assignments
                  - Category
                  - Summary
                description: Delete all product
    overlays:
      - type: APIs.io Search
        url: overlays/catalog-products-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/catalog-products-openapi-api-evangelist-ratings.yml
  - aid: box:box-tasks-api
    name: Box Tasks API
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
            title: Box Tasks API
          paths:
            /files/{file_id}/tasks:
              get:
                summary: List tasks on file
                description: |-
                  Retrieves a list of all the tasks for a file. This
                  endpoint does not support pagination.
                tags:
                  - List
                  - Tasks
                  - 'On'
                  - File
                  - Files
                  - File_id
                  - Tasks
            /tasks:
              post:
                tags:
                  - Create
                  - Task
                  - Files
                  - File_id
                  - Tasks
                summary: Create task
                description: >-
                  Creates a single task on a file. This task is not assigned to
                  any user and

                  will need to be assigned separately.
            /tasks/{task_id}:
              get:
                summary: Get task
                tags:
                  - Get
                  - Task
                  - Files
                  - File_id
                  - Tasks
                  - Task_id
                description: Retrieves information about a specific task.
              put:
                tags:
                  - Update
                  - Task
                  - Files
                  - File_id
                  - Tasks
                  - Task_id
                summary: Update task
                description: >-
                  Updates a task. This can be used to update a task's
                  configuration, or to

                  update its completion state.
              delete:
                tags:
                  - Remove
                  - Task
                  - Files
                  - File_id
                  - Tasks
                  - Task_id
                summary: Remove task
                description: Removes a task from a file.
            /tasks/{task_id}/assignments:
              get:
                summary: List task assignments
                tags:
                  - List
                  - Task
                  - Assignments
                  - Files
                  - File_id
                  - Tasks
                  - Task_id
                  - Assignments
                description: Lists all of the assignments for a
    overlays:
      - type: APIs.io Search
        url: overlays/tasks-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/tasks-openapi-api-evangelist-ratings.yml
  - aid: box:box-retention-policies-api
    name: Box Retention Policies API
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
            title: Box Retention Policies API
          paths:
            /retention_policies:
              get:
                summary: List retention policies
                tags:
                  - List
                  - Retention
                  - Policies
                  - Retention_policies
                description: Retrieves all of the retention policies for an enterprise.
              post:
                summary: Create retention policy
                tags:
                  - Create
                  - Retention
                  - Policy
                  - Retention_policies
                description: Creates a retention policy.
            /retention_policies/{retention_policy_id}:
              get:
                summary: Get retention policy
                tags:
                  - Get
                  - Retention
                  - Policy
                  - Retention_policies
                  - Retention_policy_id
                description: Retrieves a retention policy.
              put:
                summary: Update retention policy
                tags:
                  - Update
                  - Retention
                  - Policy
                  - Retention_policies
                  - Retention_policy_id
                description: Updates a retention policy.
              delete:
                summary: Delete retention policy
                tags:
                  - Delete
                  - Retention
                  - Policy
                  - Retention_policies
                  - Retention_policy_id
                description: Permanently deletes a retention policy.
            /retention_policies/{retention_policy_id}/assignments:
              get:
                summary: List retention policy assignments
                tags:
                  - List
                  - Retention
                  - Policy
                  - Assignments
                  - Retention_policies
                  - Retention_policy_id
                  - Assignments
                description: >-
                  Returns a list of all retention policy assignments associated
                  with a specified

                  reten
    overlays:
      - type: APIs.io Search
        url: overlays/retention-policies-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/retention-policies-openapi-api-evangelist-ratings.yml
  - aid: box:box-legal-hold-policy-assignments-api
    name: Box Legal Hold Policy Assignments API
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
            title: Box Legal Hold Policy Assignments API
          paths:
            /legal_hold_policy_assignments:
              get:
                summary: List legal hold policy assignments
                tags:
                  - List
                  - Legal
                  - Hold
                  - Policy
                  - Assignments
                  - Legal_hold_policy_assignments
                description: >-
                  Retrieves a list of items a legal hold policy has been
                  assigned to.
              post:
                summary: Assign legal hold policy
                tags:
                  - Assign
                  - Legal
                  - Hold
                  - Policy
                  - Legal_hold_policy_assignments
                description: Assign a legal hold to a file, file version, folder, or user.
            /legal_hold_policy_assignments/{legal_hold_policy_assignment_id}:
              get:
                summary: Get legal hold policy assignment
                tags:
                  - Get
                  - Legal
                  - Hold
                  - Policy
                  - Assignment
                  - Legal_hold_policy_assignments
                  - Legal_hold_policy_assignment_id
                description: Retrieve a legal hold policy assignment.
              delete:
                tags:
                  - Unassign
                  - Legal
                  - Hold
                  - Policy
                  - Legal_hold_policy_assignments
                  - Legal_hold_policy_assignment_id
                summary: Unassign legal hold policy
                description: |-
                  Remove a legal hold from an item.

                  This is an asynchronous process. The policy will not be
                  fully removed yet when the response returns.
            /legal_hold_policy_assignments/{legal_hold_policy_assignment_id}/files_on_hold:
              get:
                summary: List current file versions for legal hold policy assignment
                tags:
                  - List
                  - Current
                  - File
                  - Versions
                  - For
                  - Legal
                  - Hold
                  - Policy
                  - Assignment
                  - Legal_hold_policy_assignments
                  - Legal_hold_policy_assignment_id
                  - Files_on_hold
                description: >-
                  Get a list of current file versions for a legal hold

                  assignment.


                  In some cases you may want to get previous file versions
                  instead. In these

                  cases, use the `GET 
                  /legal_hold_policy_assignments/:id/file_versions_on_hold`

                  API instead to return any previous versions of a file for this
                  legal hold

                  policy assignment.


                  Due to ongoing re-architecture efforts this API might not
                  return all file

                  versions held for this policy ID. Instead, this API will only
                  return the

                  latest file version held in the newly developed architecture.
                  The `GET

                  /file_version_legal_holds` API can be used to fetch current
                  and past versions

                  of files held within the legacy architecture.


                  The `GET /legal_hold_policy_assignments?policy_id={id}` API
                  can be used to

                  find a list of policy assignments for a given policy ID.
            /legal_hold_policy_assignments/{legal_hold_policy_assignment_id}/file_versions_on_hold:
              get:
                summary: List previous file versions for legal hold policy assignment
                tags:
                  - List
                  - Previous
                  - File
                  - Versions
                  - For
                  - Legal
                  - Hold
                  - Policy
                  - Assignment
                  - Legal_hold_policy_assignments
                  - Legal_hold_policy_assignment_id
                  - Files_on_hold
                  - File_versions_on_hold
                description: >-
                  Get a list of previous file versions for a legal hold

                  assignment.


                  In some cases you may only need the latest file versions
                  instead. In these

                  cases, use the `GET 
                  /legal_hold_policy_assignments/:id/files_on_hold` API

                  instead to return any current (latest) versions of a file for
                  this legal hold

                  policy assignment.


                  Due to ongoing re-architecture efforts this API might not
                  return all files

                  held for this policy ID. Instead, this API will only return
                  past file versions

                  held in the newly developed architecture. The `GET
                  /file_version_legal_holds`

                  API can be used to fetch current and past versions of files
                  held within the

                  legacy architecture.


                  The `GET /legal_hold_policy_assignments?policy_id={id}` API
                  can be used to

                  find a list of policy assignments for a give
    overlays:
      - type: APIs.io Search
        url: overlays/legal-hold-policy-assignments-openapi-search.yml
      - type: API Evangelist Ratings
        url: >-
          overlays/legal-hold-policy-assignments-openapi-api-evangelist-ratings.yml
  - aid: box:box-storage-policy-assignments-api
    name: Box Storage Policy Assignments API
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
            title: Box Storage Policy Assignments API
          paths:
            /storage_policy_assignments:
              get:
                summary: List storage policy assignments
                tags:
                  - List
                  - Storage
                  - Policy
                  - Assignments
                  - Storage_policy_assignments
                description: >-
                  Fetches all the storage policy assignment for an enterprise or
                  user.
              post:
                summary: Assign storage policy
                tags:
                  - Assign
                  - Storage
                  - Policy
                  - Storage_policy_assignments
                description: Creates a storage policy assignment for an enterprise or user.
            /storage_policy_assignments/{storage_policy_assignment_id}:
              get:
                summary: Get storage policy assignment
                tags:
                  - Get
                  - Storage
                  - Policy
                  - Assignment
                  - Storage_policy_assignments
                  - Storage_policy_assignment_id
                description: Fetches a specific storage policy assignment.
              put:
                summary: Update storage policy assignment
                tags:
                  - Update
                  - Storage
                  - Policy
                  - Assignment
                  - Storage_policy_assignments
                  - Storage_policy_assignment_id
                description: Updates a specific storage policy assignment.
              delete:
                summary: Unassign storage policy
                tags:
                  - Unassign
                  - Storage
                  - Policy
                  - Storage_policy_assignments
                  - Storage_policy_assignment_id
                description: |-
                  Delete a storage policy assignment.

                  Deleting a storage policy assignment on a user
                  will have the user inherit the enterprise's default
                  storage policy.

                  There is a rate limit for calling this endpoint of only
                  twice per user in a 24 hour
    overlays:
      - type: APIs.io Search
        url: overlays/storage-policy-assignments-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/storage-policy-assignments-openapi-api-evangelist-ratings.yml
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
  - aid: twilio:twilio-trust-hub-api
    name: Twilio Trust Hub API
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
            title: Twilio - Trusthub
            license:
              name: Apache 2.0
              url: https://www.apache.org/licenses/LICENSE-2.0.html
          openapi: 3.0.1
          paths:
            /v1/ComplianceInquiries/Customers/Initialize:
              description: 'TODO: Resource-level docs'
              post:
                description: >-
                  Create a new Compliance Inquiry for the authenticated account.
                  This is necessary to start a new embedded session.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
            /v1/ComplianceInquiries/Customers/{CustomerId}/Initialize:
              description: 'TODO: Resource-level docs'
              post:
                description: >-
                  Resume a specific Compliance Inquiry that has expired, or
                  re-open a rejected Compliance Inquiry for editing.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
            /v1/ComplianceInquiries/Tollfree/Initialize:
              description: 'TODO: Resource-level docs'
              post:
                description: >-
                  Create a new Compliance Tollfree Verification Inquiry for the
                  authenticated account. This is necessary to start a new
                  embedded session.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
            /v1/CustomerProfiles:
              description: 'TODO: Resource-level docs'
              post:
                description: Create a new Customer-Profile.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
              get:
                description: Retrieve a list of all Customer-Profiles for an account.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
            /v1/CustomerProfiles/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: Fetch a specific Customer-Profile instance.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
              post:
                description: Updates a Customer-Profile in an account.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
              delete:
                description: Delete a specific Customer-Profile.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
            /v1/CustomerProfiles/{CustomerProfileSid}/ChannelEndpointAssignments:
              description: 'TODO: Resource-level docs'
              post:
                description: Create a new Assigned Item.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
                  - Profile
                  - Channel
                  - Endpoint
                  - Assignments
              get:
                description: Retrieve a list of all Assigned Items for an account.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
                  - Profile
                  - Channel
                  - Endpoint
                  - Assignments
            /v1/CustomerProfiles/{CustomerProfileSid}/ChannelEndpointAssignments/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: Fetch specific Assigned Item Instance.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
                  - Profile
                  - Channel
                  - Endpoint
                  - Assignments
              delete:
                description: Remove an Assignment Item Instance.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
                  - Profile
                  - Channel
                  - Endpoint
                  - Assignments
            /v1/CustomerProfiles/{CustomerProfileSid}/EntityAssignments:
              description: 'TODO: Resource-level docs'
              post:
                description: Create a new Assigned Item.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
                  - Profile
                  - Channel
                  - Endpoint
                  - Assignments
                  - Entity
              get:
                description: Retrieve a list of all Assigned Items for an account.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
                  - Profile
                  - Channel
                  - Endpoint
                  - Assignments
                  - Entity
            /v1/CustomerProfiles/{CustomerProfileSid}/EntityAssignments/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: Fetch specific Assigned Item Instance.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
                  - Profile
                  - Channel
                  - Endpoint
                  - Assignments
                  - Entity
              delete:
                description: Remove an Assignment Item Instance.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
                  - Profile
                  - Channel
                  - Endpoint
                  - Assignments
                  - Entity
            /v1/CustomerProfiles/{CustomerProfileSid}/Evaluations:
              description: 'TODO: Resource-level docs'
              post:
                description: Create a new Evaluation
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
                  - Profile
                  - Channel
                  - Endpoint
                  - Assignments
                  - Entity
                  - Evaluations
              get:
                description: >-
                  Retrieve a list of Evaluations associated to the
                  customer_profile resource.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
                  - Profile
                  - Channel
                  - Endpoint
                  - Assignments
                  - Entity
                  - Evaluations
            /v1/CustomerProfiles/{CustomerProfileSid}/Evaluations/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: Fetch specific Evaluation Instance.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
                  - Profile
                  - Channel
                  - Endpoint
                  - Assignments
                  - Entity
                  - Evaluations
            /v1/EndUsers:
              description: 'TODO: Resource-level docs'
              post:
                description: Create a new End User.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
                  - Profile
                  - Channel
                  - Endpoint
                  - Assignments
                  - Entity
                  - Evaluations
                  - End
                  - Users
              get:
                description: Retrieve a list of all End User for an account.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
                  - Profile
                  - Channel
                  - Endpoint
                  - Assignments
                  - Entity
                  - Evaluations
                  - End
                  - Users
            /v1/EndUsers/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: Fetch specific End User Instance.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
                  - Profile
                  - Channel
                  - Endpoint
                  - Assignments
                  - Entity
                  - Evaluations
                  - End
                  - Users
              post:
                description: Update an existing End User.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
                  - Profile
                  - Channel
                  - Endpoint
                  - Assignments
                  - Entity
                  - Evaluations
                  - End
                  - Users
              delete:
                description: Delete a specific End User.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
                  - Profile
                  - Channel
                  - Endpoint
                  - Assignments
                  - Entity
                  - Evaluations
                  - End
                  - Users
            /v1/EndUserTypes:
              description: 'TODO: Resource-level docs'
              get:
                description: Retrieve a list of all End-User Types.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
                  - Profile
                  - Channel
                  - Endpoint
                  - Assignments
                  - Entity
                  - Evaluations
                  - End
                  - Users
                  - User
                  - Types
            /v1/EndUserTypes/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: Fetch a specific End-User Type Instance.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
                  - Profile
                  - Channel
                  - Endpoint
                  - Assignments
                  - Entity
                  - Evaluations
                  - End
                  - Users
                  - User
                  - Types
            /v1/Policies:
              description: 'TODO: Resource-level docs'
              get:
                description: Retrieve a list of all Policys.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
                  - Profile
                  - Channel
                  - Endpoint
                  - Assignments
                  - Entity
                  - Evaluations
                  - End
                  - Users
                  - User
                  - Types
                  - Policies
            /v1/Policies/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: Fetch specific Policy Instance.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
                  - Profile
                  - Channel
                  - Endpoint
                  - Assignments
                  - Entity
                  - Evaluations
                  - End
                  - Users
                  - User
                  - Types
                  - Policies
            /v1/SupportingDocuments:
              description: 'TODO: Resource-level docs'
              post:
                description: Create a new Supporting Document.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
                  - Profile
                  - Channel
                  - Endpoint
                  - Assignments
                  - Entity
                  - Evaluations
                  - End
                  - Users
                  - User
                  - Types
                  - Policies
                  - Supporting
                  - Documents
              get:
                description: Retrieve a list of all Supporting Document for an account.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
                  - Profile
                  - Channel
                  - Endpoint
                  - Assignments
                  - Entity
                  - Evaluations
                  - End
                  - Users
                  - User
                  - Types
                  - Policies
                  - Supporting
                  - Documents
            /v1/SupportingDocuments/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: Fetch specific Supporting Document Instance.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
                  - Profile
                  - Channel
                  - Endpoint
                  - Assignments
                  - Entity
                  - Evaluations
                  - End
                  - Users
                  - User
                  - Types
                  - Policies
                  - Supporting
                  - Documents
              post:
                description: Update an existing Supporting Document.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
                  - Profile
                  - Channel
                  - Endpoint
                  - Assignments
                  - Entity
                  - Evaluations
                  - End
                  - Users
                  - User
                  - Types
                  - Policies
                  - Supporting
                  - Documents
              delete:
                description: Delete a specific Supporting Document.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
                  - Profile
                  - Channel
                  - Endpoint
                  - Assignments
                  - Entity
                  - Evaluations
                  - End
                  - Users
                  - User
                  - Types
                  - Policies
                  - Supporting
                  - Documents
            /v1/SupportingDocumentTypes:
              description: 'TODO: Resource-level docs'
              get:
                description: Retrieve a list of all Supporting Document Types.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
                  - Profile
                  - Channel
                  - Endpoint
                  - Assignments
                  - Entity
                  - Evaluations
                  - End
                  - Users
                  - User
                  - Types
                  - Policies
                  - Supporting
                  - Documents
                  - Document
            /v1/SupportingDocumentTypes/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: Fetch a specific Supporting Document Type Instance.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
                  - Profile
                  - Channel
                  - Endpoint
                  - Assignments
                  - Entity
                  - Evaluations
                  - End
                  - Users
                  - User
                  - Types
                  - Policies
                  - Supporting
                  - Documents
                  - Document
            /v1/TrustProducts:
              description: 'TODO: Resource-level docs'
              post:
                description: Create a new Customer-Profile.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
                  - Profile
                  - Channel
                  - Endpoint
                  - Assignments
                  - Entity
                  - Evaluations
                  - End
                  - Users
                  - User
                  - Types
                  - Policies
                  - Supporting
                  - Documents
                  - Document
                  - Trust
                  - Products
              get:
                description: Retrieve a list of all Customer-Profiles for an account.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
                  - Profile
                  - Channel
                  - Endpoint
                  - Assignments
                  - Entity
                  - Evaluations
                  - End
                  - Users
                  - User
                  - Types
                  - Policies
                  - Supporting
                  - Documents
                  - Document
                  - Trust
                  - Products
            /v1/TrustProducts/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: Fetch a specific Customer-Profile instance.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
                  - Profile
                  - Channel
                  - Endpoint
                  - Assignments
                  - Entity
                  - Evaluations
                  - End
                  - Users
                  - User
                  - Types
                  - Policies
                  - Supporting
                  - Documents
                  - Document
                  - Trust
                  - Products
              post:
                description: Updates a Customer-Profile in an account.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
                  - Profile
                  - Channel
                  - Endpoint
                  - Assignments
                  - Entity
                  - Evaluations
                  - End
                  - Users
                  - User
                  - Types
                  - Policies
                  - Supporting
                  - Documents
                  - Document
                  - Trust
                  - Products
              delete:
                description: Delete a specific Customer-Profile.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
                  - Profile
                  - Channel
                  - Endpoint
                  - Assignments
                  - Entity
                  - Evaluations
                  - End
                  - Users
                  - User
                  - Types
                  - Policies
                  - Supporting
                  - Documents
                  - Document
                  - Trust
                  - Products
            /v1/TrustProducts/{TrustProductSid}/ChannelEndpointAssignments:
              description: 'TODO: Resource-level docs'
              post:
                description: Create a new Assigned Item.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
                  - Profile
                  - Channel
                  - Endpoint
                  - Assignments
                  - Entity
                  - Evaluations
                  - End
                  - Users
                  - User
                  - Types
                  - Policies
                  - Supporting
                  - Documents
                  - Document
                  - Trust
                  - Products
                  - Product
              get:
                description: Retrieve a list of all Assigned Items for an account.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
                  - Profile
                  - Channel
                  - Endpoint
                  - Assignments
                  - Entity
                  - Evaluations
                  - End
                  - Users
                  - User
                  - Types
                  - Policies
                  - Supporting
                  - Documents
                  - Document
                  - Trust
                  - Products
                  - Product
            /v1/TrustProducts/{TrustProductSid}/ChannelEndpointAssignments/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: Fetch specific Assigned Item Instance.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
                  - Profile
                  - Channel
                  - Endpoint
                  - Assignments
                  - Entity
                  - Evaluations
                  - End
                  - Users
                  - User
                  - Types
                  - Policies
                  - Supporting
                  - Documents
                  - Document
                  - Trust
                  - Products
                  - Product
              delete:
                description: Remove an Assignment Item Instance.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
                  - Profile
                  - Channel
                  - Endpoint
                  - Assignments
                  - Entity
                  - Evaluations
                  - End
                  - Users
                  - User
                  - Types
                  - Policies
                  - Supporting
                  - Documents
                  - Document
                  - Trust
                  - Products
                  - Product
            /v1/TrustProducts/{TrustProductSid}/EntityAssignments:
              description: 'TODO: Resource-level docs'
              post:
                description: Create a new Assigned Item.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
                  - Profile
                  - Channel
                  - Endpoint
                  - Assignments
                  - Entity
                  - Evaluations
                  - End
                  - Users
                  - User
                  - Types
                  - Policies
                  - Supporting
                  - Documents
                  - Document
                  - Trust
                  - Products
                  - Product
              get:
                description: Retrieve a list of all Assigned Items for an account.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
                  - Profile
                  - Channel
                  - Endpoint
                  - Assignments
                  - Entity
                  - Evaluations
                  - End
                  - Users
                  - User
                  - Types
                  - Policies
                  - Supporting
                  - Documents
                  - Document
                  - Trust
                  - Products
                  - Product
            /v1/TrustProducts/{TrustProductSid}/EntityAssignments/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: Fetch specific Assigned Item Instance.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
                  - Profile
                  - Channel
                  - Endpoint
                  - Assignments
                  - Entity
                  - Evaluations
                  - End
                  - Users
                  - User
                  - Types
                  - Policies
                  - Supporting
                  - Documents
                  - Document
                  - Trust
                  - Products
                  - Product
              delete:
                description: Remove an Assignment Item Instance.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
                  - Profile
                  - Channel
                  - Endpoint
                  - Assignments
                  - Entity
                  - Evaluations
                  - End
                  - Users
                  - User
                  - Types
                  - Policies
                  - Supporting
                  - Documents
                  - Document
                  - Trust
                  - Products
                  - Product
            /v1/TrustProducts/{TrustProductSid}/Evaluations:
              description: 'TODO: Resource-level docs'
              post:
                description: Create a new Evaluation
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
                  - Profile
                  - Channel
                  - Endpoint
                  - Assignments
                  - Entity
                  - Evaluations
                  - End
                  - Users
                  - User
                  - Types
                  - Policies
                  - Supporting
                  - Documents
                  - Document
                  - Trust
                  - Products
                  - Product
              get:
                description: >-
                  Retrieve a list of Evaluations associated to the trust_product
                  resource.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
                  - Profile
                  - Channel
                  - Endpoint
                  - Assignments
                  - Entity
                  - Evaluations
                  - End
                  - Users
                  - User
                  - Types
                  - Policies
                  - Supporting
                  - Documents
                  - Document
                  - Trust
                  - Products
                  - Product
            /v1/TrustProducts/{TrustProductSid}/Evaluations/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: Fetch specific Evaluation Instance.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
                  - Profile
                  - Channel
                  - Endpoint
                  - Assignments
                  - Entity
                  - Evaluations
                  - End
                  - Users
                  - User
                  - Types
                  - Policies
                  - Supporting
                  - Documents
                  - Document
                  - Trust
                  - Products
                  - Product
          tags:
            - name: TrusthubV1ComplianceInquiries
            - name: TrusthubV1ComplianceTollfreeInquiries
            - name: TrusthubV1CustomerProfiles
            - name: TrusthubV1CustomerProfilesChannelEndpointAssignment
            - name: TrusthubV1CustomerProfilesEntityAssignments
            - name: TrusthubV1CustomerProfilesEvaluations
            - name: TrusthubV1EndUser
            - name: TrusthubV1EndUserType
            - name: TrusthubV1Policies
            - name: TrusthubV1SupportingDocument
            - name: TrusthubV1SupportingDocumentType
            - name: TrusthubV1TrustProducts
            - name: TrusthubV1TrustProductsChannelEndpointAssignment
            - name: TrusthubV1TrustProductsEntityAssignments
            - name: TrusthubV1TrustProductsEvaluations
          x-maturity:
            - name: GA
              description: This product is G
    overlays:
      - type: APIs.io Search
        url: overlays/trust-hub-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/trust-hub-openapi-api-evangelist-ratings.yml
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---