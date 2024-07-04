---
name: Assignment
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/assignment.png
url: https://example.com/apis/assignment.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Assignment
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
  - name: sso
    description: >-
      <p>AWS IAM Identity Center (successor to AWS Single Sign-On) Portal is a
      web service that makes it easy for you to assign user access to IAM
      Identity Center resources such as the AWS access portal. Users can get AWS
      account applications and roles assigned to them and get federated into the
      application.</p> <note> <p>Although AWS Single Sign-On was renamed, the
      <code>sso</code> and <code>identitystore</code> API namespaces will
      continue to retain their original name for backward compatibility
      purposes. For more information, see <a
      href="https://docs.aws.amazon.com/singlesignon/latest/userguide/what-is.html#renamed">IAM
      Identity Center rename</a>.</p> </note> <p>This reference guide describes
      the IAM Identity Center Portal operations that you can call
      programatically and includes detailed information on data types and
      errors.</p> <note> <p>AWS provides SDKs that consist of libraries and
      sample code for various programming languages and platforms, such as Java,
      Ruby, .Net, iOS, or Android. The SDKs provide a convenient way to create
      programmatic access to IAM Identity Center and other AWS services. For
      more information about the AWS SDKs, including how to download and install
      them, see <a href="http://aws.amazon.com/tools/">Tools for Amazon Web
      Services</a>.</p> </note>
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
            title: sso
          paths:
            /federation/credentials:
              GET:
                summary: GetRoleCredentials
                description: >-
                  <p>Returns the STS short-term credentials for a given role
                  name that is assigned to the user.</p>
                tags:
                  - Get
                  - Roles
                  - Credentials
                  - Federation
                  - Credentials
            /assignment/roles:
              GET:
                summary: ListAccountRoles
                description: >-
                  <p>Lists all roles that are assigned to the user for a given
                  AWS account.</p>
                tags:
                  - Lists
                  - Account
                  - Roles
                  - Federation
                  - Credentials
                  - Assignment
                  - Roles
            /assignment/accounts:
              GET:
                summary: ListAccounts
                description: >-
                  <p>Lists all AWS accounts assigned to the user. These AWS
                  accounts are assigned by the administrator of the account. For
                  more information, see <a
                  href="https://docs.aws.amazon.com/singlesignon/latest/userguide/useraccess.html#assignusers">Assign
                  User Access</a> in the <i>IAM Identity Center User Guide</i>.
                  This operation returns a paginated response.</p>
                tags:
                  - Lists
                  - Accounts
                  - Federation
                  - Credentials
                  - Assignment
                  - Roles
                  - Accounts
            /logout:
              POST:
                summary: Logout
                description: >-
                  <p>Removes the locally stored SSO tokens from the client-side
                  cache and sends an API call to the IAM Identity Center service
                  to invalidate the corresponding server-side IAM Identity
                  Center sign in session.</p> <note> <p>If a user uses IAM
                  Identity Center to access the AWS CLI, the user’s IAM Identity
                  Center sign in session is used to obtain an IAM session, as
                  specified in the corresponding IAM Identity Center permission
                  set. More specifically, IAM Identity Center assumes an IAM
                  role in the target account on behalf of the user, and the
                  corresponding temporary AWS credentials are returned to the
                  client.</p> <p>After user logout, any existing IAM role
                  sessions that were created by using IAM Identity Center
                  permission sets continue based on the duration configured in
                  the permission set. For more information, see <a
                  href="https://docs.aws.amazon.com/singlesignon/latest/userguide/authconcept.html">User
                  authentications</a> in the <i>IAM Identity Center User
                  Guide</i>.</
                tags:
                  - Logout
                  - Federation
                  - Credentials
                  - Assignment
                  - Roles
                  - Accounts
                  - Logo
    overlays:
      - type: APIs.io Search
        url: overlays/sso-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/sso-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:sso
  - aid: box:box-files-api
    name: Box Files API
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
            title: Box Files API
          paths:
            /files/{file_id}:
              get:
                summary: Get file information
                tags:
                  - Get
                  - File
                  - Information
                  - Files
                  - File_id
                description: Retrieves the details about a file.
              post:
                summary: Restore file
                tags:
                  - Restore
                  - File
                  - Files
                  - File_id
                description: >-
                  Restores a file that has been moved to the trash.


                  An optional new parent ID can be provided to restore the file
                  to in case the

                  original folder has been deleted.
              put:
                summary: Update file
                tags:
                  - Update
                  - File
                  - Files
                  - File_id
                description: |-
                  Updates a file. This can be used to rename or move a file,
                  create a shared link, or lock a file.
              delete:
                summary: Delete file
                tags:
                  - Delete
                  - File
                  - Files
                  - File_id
                description: |-
                  Deletes a file, either permanently or by moving it to
                  the trash.

                  The the enterprise settings determine whether the item will
                  be permanently deleted from Box or moved to the trash.
            /files/{file_id}/content:
              get:
                summary: Download file
                tags:
                  - Download
                  - File
                  - Files
                  - File_id
                  - Content
                description: Returns the contents of a file in binary format.
              post:
                tags:
                  - Upload
                  - File
                  - Version
                  - Files
                  - File_id
                  - Content
                summary: Upload file version
                description: |-
                  Update a file's content. For file sizes over 50MB we recommend
                  using the Chunk Upload APIs.

                  # Request body order

                  The `attributes` part of the body must come **before** the
                  `file` part. Requests that do not follow this format when
                  uploading the file will receive a HTTP `400` error with a
                  `metadata_after_file_contents` error code.
            /files/content:
              options:
                summary: Preflight check before upload
                tags:
                  - Preflight
                  - Check
                  - Before
                  - Upload
                  - Files
                  - File_id
                  - Content
                description: |-
                  Performs a check to verify that a file will be accepted by Box
                  before you upload the entire file.
              post:
                tags:
                  - Upload
                  - File
                  - Files
                  - File_id
                  - Content
                summary: Upload file
                description: >-
                  Uploads a small file to Box. For file sizes over 50MB we
                  recommend

                  using the Chunk Upload APIs.


                  # Request body order


                  The `attributes` part of the body must come **before** the

                  `file` part. Requests that do not follow this format when

                  uploading the file will receive a HTTP `400` error with a

                  `metadata_after_file_contents` error code.
            /files/upload_sessions:
              post:
                summary: Create upload session
                tags:
                  - Create
                  - Upload
                  - Session
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                description: Creates an upload session for a new file.
            /files/{file_id}/upload_sessions:
              post:
                summary: Create upload session for existing file
                tags:
                  - Create
                  - Upload
                  - Session
                  - For
                  - Existing
                  - File
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                description: Creates an upload session for an existing file.
            /files/upload_sessions/{upload_session_id}:
              get:
                summary: Get upload session
                tags:
                  - Get
                  - Upload
                  - Session
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                description: Return information about an upload session.
              put:
                summary: Upload part of file
                tags:
                  - Upload
                  - Part
                  - Of
                  - File
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                description: Updates a chunk of an upload session for a file.
              delete:
                summary: Remove upload session
                tags:
                  - Remove
                  - Upload
                  - Session
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                description: |-
                  Abort an upload session and discard all data uploaded.

                  This cannot be reversed.
            /files/upload_sessions/{upload_session_id}/parts:
              get:
                summary: List parts
                tags:
                  - List
                  - Parts
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                description: |-
                  Return a list of the chunks uploaded to the upload
                  session so far.
            /files/upload_sessions/{upload_session_id}/commit:
              post:
                summary: Commit upload session
                tags:
                  - Commit
                  - Upload
                  - Session
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                description: |-
                  Close an upload session and create a file from the
                  uploaded chunks.
            /files/{file_id}/copy:
              post:
                summary: Copy file
                description: Creates a copy of a file.
                tags:
                  - Copy
                  - File
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
            /files/{file_id}/thumbnail.{extension}:
              get:
                summary: Get file thumbnail
                description: >-
                  Retrieves a thumbnail, or smaller image representation, of a
                  file.


                  Sizes of `32x32`,`64x64`, `128x128`, and `256x256` can be
                  returned in

                  the `.png` format and sizes of `32x32`, `160x160`, and
                  `320x320`

                  can be returned in the `.jpg` format.


                  Thumbnails can be generated for the image and video file
                  formats listed

                  [found on our community site][1].


                  [1]:
                  https://community.box.com/t5/Migrating-and-Previewing-Content/File-Types-and-Fonts-Supported-in-Box-Content-Preview/ta-p/327
                tags:
                  - Get
                  - File
                  - Thumbnail
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
            /files/{file_id}/collaborations:
              get:
                summary: List file collaborations
                description: |-
                  Retrieves a list of pending and active collaborations for a
                  file. This returns all the users that have access to the file
                  or have been invited to the file.
                tags:
                  - List
                  - File
                  - Collaborations
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
            /files/{file_id}/comments:
              get:
                summary: List file comments
                description: Retrieves a list of comments for a file.
                tags:
                  - List
                  - File
                  - Comments
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
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
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
                  - Tasks
            /files/{file_id}/trash:
              get:
                summary: Get trashed file
                tags:
                  - Get
                  - Trashed
                  - File
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
                  - Tasks
                  - Trash
                description: >-
                  Retrieves a file that has been moved to the trash.


                  Please note that only if the file itself has been moved to the

                  trash can it be retrieved with this API call. If instead one
                  of

                  its parent folders was moved to the trash, only that folder

                  can be inspected using the

                  [`GET /folders/:id/trash`](e://get_folders_id_trash) API.


                  To list all items that have been moved to the trash, please

                  use the [`GET
                  /folders/trash/items`](e://get-folders-trash-items/)

                  API.
              delete:
                summary: Permanently remove file
                tags:
                  - Permanently
                  - Remove
                  - File
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
                  - Tasks
                  - Trash
                description: |-
                  Permanently deletes a file that is in the trash.
                  This action cannot be undone.
            /files/{file_id}/versions:
              get:
                summary: List all file versions
                tags:
                  - List
                  - All
                  - File
                  - Versions
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
                  - Tasks
                  - Trash
                  - Versions
                description: >-
                  Retrieve a list of the past versions for a file.


                  Versions are only tracked by Box users with premium accounts.
                  To fetch the ID

                  of the current version of a file, use the `GET /file/:id` API.
            /files/{file_id}/versions/{file_version_id}:
              get:
                summary: Get file version
                tags:
                  - Get
                  - File
                  - Version
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
                  - Tasks
                  - Trash
                  - Versions
                  - File_version_id
                description: |-
                  Retrieve a specific version of a file.

                  Versions are only tracked for Box users with premium accounts.
              delete:
                summary: Remove file version
                tags:
                  - Remove
                  - File
                  - Version
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
                  - Tasks
                  - Trash
                  - Versions
                  - File_version_id
                description: |-
                  Move a file version to the trash.

                  Versions are only tracked for Box users with premium accounts.
              put:
                summary: Restore file version
                tags:
                  - Restore
                  - File
                  - Version
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
                  - Tasks
                  - Trash
                  - Versions
                  - File_version_id
                description: |-
                  Restores a specific version of a file after it was deleted.
                  Don't use this endpoint to restore Box Notes,
                  as it works with file formats such as PDF, DOC,
                  PPTX or similar.
            /files/{file_id}/versions/current:
              post:
                summary: Promote file version
                tags:
                  - Promote
                  - File
                  - Version
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
                  - Tasks
                  - Trash
                  - Versions
                  - File_version_id
                  - Current
                description: >-
                  Promote a specific version of a file.


                  If previous versions exist, this method can be used to

                  promote one of the older versions to the top of the version
                  history.


                  This creates a new copy of the old version and puts it at the

                  top of the versions history. The file will have the exact same
                  contents

                  as the older version, with the the same hash digest, `etag`,
                  and

                  name as the original.


                  Other properties such as comments do not get updated to their

                  former values.


                  Don't use this endpoint to restore Box Notes,

                  as it works with file formats such as PDF, DOC,

                  PPTX or similar.
            /files/{file_id}/metadata:
              get:
                summary: List metadata instances on file
                tags:
                  - List
                  - Metadata
                  - Instances
                  - 'On'
                  - File
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
                  - Tasks
                  - Trash
                  - Versions
                  - File_version_id
                  - Current
                  - Metadata
                description: Retrieves all metadata for a given file.
            /files/{file_id}/metadata/enterprise/securityClassification-6VMVochwUWo:
              get:
                summary: Get classification on file
                tags:
                  - Get
                  - Classification
                  - 'On'
                  - File
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
                  - Tasks
                  - Trash
                  - Versions
                  - File_version_id
                  - Current
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                description: >-
                  Retrieves the classification metadata instance that

                  has been applied to a file.


                  This API can also be called by including the enterprise ID in
                  the

                  URL explicitly, for example

                  `/files/:id//enterprise_12345/securityClassification-6VMVochwUWo`.
              post:
                summary: Add classification to file
                tags:
                  - Add
                  - Classification
                  - To
                  - File
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
                  - Tasks
                  - Trash
                  - Versions
                  - File_version_id
                  - Current
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                description: >-
                  Adds a classification to a file by specifying the label of the

                  classification to add.


                  This API can also be called by including the enterprise ID in
                  the

                  URL explicitly, for example

                  `/files/:id//enterprise_12345/securityClassification-6VMVochwUWo`.
              put:
                summary: Update classification on file
                tags:
                  - Update
                  - Classification
                  - 'On'
                  - File
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
                  - Tasks
                  - Trash
                  - Versions
                  - File_version_id
                  - Current
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                description: >-
                  Updates a classification on a file.


                  The classification can only be updated if a classification has
                  already been

                  applied to the file before. When editing classifications, only
                  values are

                  defined for the enterprise will be accepted.
              delete:
                summary: Remove classification from file
                tags:
                  - Remove
                  - Classification
                  - From
                  - File
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
                  - Tasks
                  - Trash
                  - Versions
                  - File_version_id
                  - Current
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                description: >-
                  Removes any classifications from a file.


                  This API can also be called by including the enterprise ID in
                  the

                  URL explicitly, for example

                  `/files/:id//enterprise_12345/securityClassification-6VMVochwUWo`.
            /files/{file_id}/metadata/{scope}/{template_key}:
              get:
                summary: Get metadata instance on file
                tags:
                  - Get
                  - Metadata
                  - Instance
                  - 'On'
                  - File
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
                  - Tasks
                  - Trash
                  - Versions
                  - File_version_id
                  - Current
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                  - Scope
                  - Template_key
                description: >-
                  Retrieves the instance of a metadata template that has been
                  applied to a

                  file.
              post:
                summary: Create metadata instance on file
                tags:
                  - Create
                  - Metadata
                  - Instance
                  - 'On'
                  - File
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
                  - Tasks
                  - Trash
                  - Versions
                  - File_version_id
                  - Current
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                  - Scope
                  - Template_key
                description: >-
                  Applies an instance of a metadata template to a file.


                  In most cases only values that are present in the metadata
                  template

                  will be accepted, except for the `global.properties` template
                  which accepts

                  any key-value pair.
              put:
                summary: Update metadata instance on file
                tags:
                  - Update
                  - Metadata
                  - Instance
                  - 'On'
                  - File
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
                  - Tasks
                  - Trash
                  - Versions
                  - File_version_id
                  - Current
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                  - Scope
                  - Template_key
                description: >-
                  Updates a piece of metadata on a file.


                  The metadata instance can only be updated if the template has
                  already been

                  applied to the file before. When editing metadata, only values
                  that match

                  the metadata template schema will be accepted.


                  The update is applied atomically. If any errors occur during
                  the

                  application of the operations, the metadata instance will not
                  be changed.
              delete:
                summary: Remove metadata instance from file
                tags:
                  - Remove
                  - Metadata
                  - Instance
                  - From
                  - File
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
                  - Tasks
                  - Trash
                  - Versions
                  - File_version_id
                  - Current
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                  - Scope
                  - Template_key
                description: Deletes a piece of file metadata.
            /files/{file_id}/metadata/global/boxSkillsCards:
              get:
                summary: List Box Skill cards on file
                tags:
                  - List
                  - Box
                  - Skill
                  - Cards
                  - 'On'
                  - File
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
                  - Tasks
                  - Trash
                  - Versions
                  - File_version_id
                  - Current
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                  - Scope
                  - Template_key
                  - Skills
                  - Cards
                description: >-
                  List the Box Skills metadata cards that are attached to a
                  file.
              post:
                summary: Create Box Skill cards on file
                tags:
                  - Create
                  - Box
                  - Skill
                  - Cards
                  - 'On'
                  - File
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
                  - Tasks
                  - Trash
                  - Versions
                  - File_version_id
                  - Current
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                  - Scope
                  - Template_key
                  - Skills
                  - Cards
                description: Applies one or more Box Skills metadata cards to a file.
              put:
                summary: Update Box Skill cards on file
                tags:
                  - Update
                  - Box
                  - Skill
                  - Cards
                  - 'On'
                  - File
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
                  - Tasks
                  - Trash
                  - Versions
                  - File_version_id
                  - Current
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                  - Scope
                  - Template_key
                  - Skills
                  - Cards
                description: Updates one or more Box Skills metadata cards to a file.
              delete:
                summary: Remove Box Skill cards from file
                tags:
                  - Remove
                  - Box
                  - Skill
                  - Cards
                  - From
                  - File
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
                  - Tasks
                  - Trash
                  - Versions
                  - File_version_id
                  - Current
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                  - Scope
                  - Template_key
                  - Skills
                  - Cards
                description: Removes any Box Skills cards metadata from a file.
            /files/{file_id}/watermark:
              get:
                summary: Get watermark on file
                tags:
                  - Get
                  - Watermark
                  - 'On'
                  - File
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
                  - Tasks
                  - Trash
                  - Versions
                  - File_version_id
                  - Current
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                  - Scope
                  - Template_key
                  - Skills
                  - Cards
                  - Watermark
                description: Retrieve the watermark for a file.
              put:
                summary: Apply watermark to file
                tags:
                  - Apply
                  - Watermark
                  - To
                  - File
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
                  - Tasks
                  - Trash
                  - Versions
                  - File_version_id
                  - Current
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                  - Scope
                  - Template_key
                  - Skills
                  - Cards
                  - Watermark
                description: Applies or update a watermark on a file.
              delete:
                summary: Remove watermark from file
                tags:
                  - Remove
                  - Watermark
                  - From
                  - File
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
                  - Tasks
                  - Trash
                  - Versions
                  - File_version_id
                  - Current
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                  - Scope
                  - Template_key
                  - Skills
                  - Cards
                  - Watermark
                description: Removes the watermark from a file.
            /files/{file_id}#get_shared_link:
              get:
                summary: Get shared link for file
                tags:
                  - Get
                  - Shared
                  - Link
                  - For
                  - File
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
                  - Tasks
                  - Trash
                  - Versions
                  - File_version_id
                  - Current
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                  - Scope
                  - Template_key
                  - Skills
                  - Cards
                  - Watermark
                  - '#get_shared_link'
                description: Gets the information for a shared link on a file.
            /files/{file_id}#add_shared_link:
              put:
                summary: Add shared link to file
                tags:
                  - Add
                  - Shared
                  - Link
                  - To
                  - File
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
                  - Tasks
                  - Trash
                  - Versions
                  - File_version_id
                  - Current
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                  - Scope
                  - Template_key
                  - Skills
                  - Cards
                  - Watermark
                  - '#get_shared_link'
                  - '#add_shared_link'
                description: Adds a shared link to a file.
            /files/{file_id}#update_shared_link:
              put:
                summary: Update shared link on file
                tags:
                  - Update
                  - Shared
                  - Link
                  - 'On'
                  - File
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
                  - Tasks
                  - Trash
                  - Versions
                  - File_version_id
                  - Current
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                  - Scope
                  - Template_key
                  - Skills
                  - Cards
                  - Watermark
                  - '#get_shared_link'
                  - '#add_shared_link'
                  - '#update_shared_link'
                description: Updates a shared link on a file.
            /files/{file_id}#remove_shared_link:
              put:
                summary: Remove shared link from file
                tags:
                  - Remove
                  - Shared
                  - Link
                  - From
                  - File
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
                  - Tasks
                  - Trash
                  - Versions
                  - File_version_id
                  - Current
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                  - Scope
                  - Template_key
                  - Skills
                  - Cards
                  - Watermark
                  - '#get_shared_link'
                  - '#add_shared_link'
                  - '#update_shared_link'
                  - '#remove_shared_link'
                description: Removes a shared link from a file.
            /retention_policy_assignments/{retention_policy_assignment_id}/files_under_retention:
              get:
                summary: Get files under retention
                tags:
                  - Get
                  - Files
                  - Under
                  - Retention
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
                  - Tasks
                  - Trash
                  - Versions
                  - File_version_id
                  - Current
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                  - Scope
                  - Template_key
                  - Skills
                  - Cards
                  - Watermark
                  - '#get_shared_link'
                  - '#add_shared_link'
                  - '#update_shared_link'
                  - '#remove_shared_link'
                  - Retention_policy_assignments
                  - Retention_policy_assignment_id
                  - Files_under_retention
                description: >-
                  Returns a list of files under retention for a retention policy
                  assignment.
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
                  - Files
                  - File_id
                  - Content
                  - Upload_sessions
                  - Upload_session_id
                  - Parts
                  - Commit
                  - Copy
                  - Thumbnail.
                  - Extension
                  - Collaborations
                  - Comments
                  - Tasks
                  - Trash
                  - Versions
                  - File_version_id
                  - Current
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                  - Scope
                  - Template_key
                  - Skills
                  - Cards
                  - Watermark
                  - '#get_shared_link'
                  - '#add_shared_link'
                  - '#update_shared_link'
                  - '#remove_shared_link'
                  - Retention_policy_assignments
                  - Retention_policy_assignment_id
                  - Files_under_retention
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

                  find a list of policy assignments for a give
    overlays:
      - type: APIs.io Search
        url: overlays/files-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/files-openapi-api-evangelist-ratings.yml
  - aid: box:box-task-assignments-api
    name: Box Task Assignments API
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
            title: Box Task Assignments API
          paths:
            /task_assignments:
              post:
                summary: Assign task
                tags:
                  - Assign
                  - Task
                  - Task_assignments
                description: >-
                  Assigns a task to a user.


                  A task can be assigned to more than one user by creating
                  multiple

                  assignments.
            /task_assignments/{task_assignment_id}:
              get:
                summary: Get task assignment
                tags:
                  - Get
                  - Task
                  - Assignment
                  - Task_assignments
                  - Task_assignment_id
                description: Retrieves information about a task assignment.
              put:
                summary: Update task assignment
                tags:
                  - Update
                  - Task
                  - Assignment
                  - Task_assignments
                  - Task_assignment_id
                description: |-
                  Updates a task assignment. This endpoint can be
                  used to update the state of a task assigned to a user.
              delete:
                summary: Unassign task
                tags:
                  - Unassign
                  - Task
                  - Task_assignments
                  - Task_assignment_id
                description: Deletes a specific task
    overlays:
      - type: APIs.io Search
        url: overlays/task-assignments-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/task-assignments-openapi-api-evangelist-ratings.yml
  - aid: box:box-retention-policy-assignments-api
    name: Box Retention Policy Assignments API
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
            title: Box Retention Policy Assignments API
          paths:
            /retention_policy_assignments:
              post:
                summary: Assign retention policy
                tags:
                  - Assign
                  - Retention
                  - Policy
                  - Retention_policy_assignments
                description: Assigns a retention policy to an item.
            /retention_policy_assignments/{retention_policy_assignment_id}:
              get:
                summary: Get retention policy assignment
                tags:
                  - Get
                  - Retention
                  - Policy
                  - Assignment
                  - Retention_policy_assignments
                  - Retention_policy_assignment_id
                description: Retrieves a retention policy assignment
              delete:
                summary: Remove retention policy assignment
                tags:
                  - Remove
                  - Retention
                  - Policy
                  - Assignment
                  - Retention_policy_assignments
                  - Retention_policy_assignment_id
                description: |-
                  Removes a retention policy assignment
                  applied to content.
            /retention_policy_assignments/{retention_policy_assignment_id}/files_under_retention:
              get:
                summary: Get files under retention
                tags:
                  - Get
                  - Files
                  - Under
                  - Retention
                  - Retention_policy_assignments
                  - Retention_policy_assignment_id
                  - Files_under_retention
                description: >-
                  Returns a list of files under retention for a retention policy
                  assignment.
            /retention_policy_assignments/{retention_policy_assignment_id}/file_versions_under_retention:
              get:
                summary: Get file versions under retention
                tags:
                  - Get
                  - File
                  - Versions
                  - Under
                  - Retention
                  - Retention_policy_assignments
                  - Retention_policy_assignment_id
                  - Files_under_retention
                  - File_versions_under_retention
                description: >-
                  Returns a list of file versions under retention for a
                  retention policy
    overlays:
      - type: APIs.io Search
        url: overlays/retention-policy-assignments-openapi-search.yml
      - type: API Evangelist Ratings
        url: >-
          overlays/retention-policy-assignments-openapi-api-evangelist-ratings.yml
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
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---