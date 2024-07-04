---
name: Anonymous
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/anonymous.png
url: https://example.com/apis/anonymous.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Anonymous
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
  - name: Confluence API
    description: >-
      This is the reference for the Confluence Cloud REST API. This API is the
      primary way to get and modify data in Confluence Cloud, whether you are
      developing an app or any other integration. Use it to interact with
      Confluence entities, like pages and blog posts, spaces, users, groups, and
      more.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.atlassian.com/cloud/confluence/rest/v1/intro/
    baseURL: https://api.example.com
    tags: []
    properties:
      - type: Documentation
        url: https://developer.atlassian.com/cloud/confluence/rest/v1/intro/
      - type: OpenAPI
        data:
          openapi: 3.0.1
          info:
            title: The Confluence Cloud REST API
          externalDocs:
            description: >-
              The online and complete version of the Confluence Cloud REST API
              docs.
            url: https://developer.atlassian.com/cloud/confluence/rest/
          tags:
            - name: Audit
              description: ''
            - name: Analytics
              description: ''
            - name: Content
              description: ''
            - name: Content - attachments
              description: ''
            - name: Content body
              description: ''
            - name: Content - children and descendants
              description: ''
            - name: Content - macro body
              description: ''
            - name: Content comments
              description: ''
            - name: Content labels
              description: ''
            - name: Content permissions
              description: ''
            - name: Content properties
              description: ''
            - name: Content restrictions
              description: ''
            - name: Content states
              description: ''
            - name: Content versions
              description: ''
            - name: Content watches
              description: ''
            - name: Dynamic modules
              description: ''
            - name: Experimental
              description: >-
                APIs in this section can change without any prior deprecation
                notice.
            - name: Group
              description: >-
                **[WARNING](https://support.atlassian.com/user-management/docs/create-and-update-groups/)
                The standard Atlassian group names are default names only and
                can be edited or deleted.**  For example, an admin or Atlassian
                support could delete the default group jira-software-users or
                rename it to jsw-users at any point.
            - name: Inline tasks
              description: ''
            - name: Label info
              description: ''
            - name: Long-running task
              description: ''
            - name: Relation
              description: ''
            - name: Search
              description: ''
            - name: Settings
              description: ''
            - name: Space
              description: ''
            - name: Space permissions
              description: ''
            - name: Space properties
              description: ''
            - name: Space settings
              description: ''
            - name: Templates
              description: ''
            - name: Themes
              description: ''
            - name: Users
              description: ''
            - name: User properties
              description: ''
          paths:
            /wiki/rest/api/audit:
              get:
                tags:
                  - Get
                  - Audit
                  - Records
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                summary: Get audit records
                description: >-
                  Returns all records in the audit log, optionally for a certain
                  date range.

                  This contains information about events like space exports,
                  group membership

                  changes, app installations, etc. For more information, see

                  [Audit
                  log](https://confluence.atlassian.com/confcloud/audit-log-802164269.html)

                  in the Confluence administrator's guide.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Confluence Administrator' global permission.
              post:
                tags:
                  - Create
                  - Audit
                  - Record
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                summary: Create audit record
                description: >-
                  Creates a record in the audit log.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Confluence Administrator' global permission.
            /wiki/rest/api/audit/export:
              get:
                tags:
                  - Export
                  - Audit
                  - Records
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                summary: Export audit records
                description: >-
                  Exports audit records as a CSV file or ZIP file.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Confluence Administrator' global permission.
            /wiki/rest/api/audit/retention:
              get:
                tags:
                  - Get
                  - Retention
                  - Period
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                summary: Get retention period
                description: >-
                  Returns the retention period for records in the audit log. The
                  retention

                  period is how long an audit record is kept for, from creation
                  date until

                  it is deleted.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Confluence Administrator' global permission.
              put:
                tags:
                  - Sets
                  - Retention
                  - Period
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                summary: Set retention period
                description: >-
                  Sets the retention period for records in the audit log. The
                  retention period

                  can be set to a maximum of 1 year.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Confluence Administrator' global permission.
            /wiki/rest/api/audit/since:
              get:
                tags:
                  - Get
                  - Audit
                  - Records
                  - For
                  - Time
                  - Period
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                summary: Get audit records for time period
                description: >-
                  Returns records from the audit log, for a time period back
                  from the current

                  date. For example, you can use this method to get the last 3
                  months of records.


                  This contains information about events like space exports,
                  group membership

                  changes, app installations, etc. For more information, see

                  [Audit
                  log](https://confluence.atlassian.com/confcloud/audit-log-802164269.html)

                  in the Confluence administrator's guide.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Confluence Administrator' global permission.
            /wiki/rest/api/content:
              get:
                tags:
                  - Get
                  - Content
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                summary: Get content
                description: >-
                  Deprecated, use [Confluence's v2
                  API](https://developer.atlassian.com/cloud/confluence/rest/v2/intro/).


                  Returns all content in a Confluence instance.


                  By default, the following objects are expanded: `space`,
                  `history`, `version`.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission).

                  Only content that the user has permission to view will be
                  returned.
              post:
                tags:
                  - Create
                  - Content
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                summary: Create content
                description: >-
                  Deprecated, use [Confluence's v2
                  API](https://developer.atlassian.com/cloud/confluence/rest/v2/intro/).


                  Creates a new piece of content or publishes an existing draft.


                  To publish a draft, add the `id` and `status` properties to
                  the body of the request.

                  Set the `id` to the ID of the draft and set the `status` to
                  'current'. When the

                  request is sent, a new piece of content will be created and
                  the metadata from the

                  draft will be transferred into it.


                  By default, the following objects are expanded: `space`,
                  `history`, `version`.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**: 'Add' permission for the

                  space that the content will be created in, and permission to
                  view the draft if publishing a draft.
            /wiki/rest/api/content/archive:
              post:
                tags:
                  - Archive
                  - Pages
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                summary: Archive pages
                description: >-
                  Archives a list of pages. The pages to be archived are
                  specified as a list of content IDs.

                  This API accepts the archival request and returns a task ID.

                  The archival process happens asynchronously.

                  Use the /longtask/<taskId> REST API to get the copy task
                  status.


                  Each content ID needs to resolve to page objects that are not
                  already in an archived state.

                  The content IDs need not belong to the same space.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Archive' permission for each of the pages in the
                  corresponding space it belongs to.
            /wiki/rest/api/content/blueprint/instance/{draftId}:
              put:
                tags:
                  - Publish
                  - Shared
                  - Draft
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                summary: Publish shared draft
                description: >-
                  Publishes a shared draft of a page created from a blueprint.


                  By default, the following objects are expanded:
                  `body.storage`, `history`, `space`, `version`, `ancestors`.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to view the draft and 'Add' permission for the
                  space that

                  the content will be created in.
              post:
                tags:
                  - Publish
                  - Legacy
                  - Draft
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                summary: Publish legacy draft
                description: >-
                  Publishes a legacy draft of a page created from a blueprint.
                  Legacy drafts

                  will eventually be removed in favor of shared drafts. For now,
                  this method

                  works the same as [Publish shared
                  draft](#api-content-blueprint-instance-draftId-put).


                  By default, the following objects are expanded:
                  `body.storage`, `history`, `space`, `version`, `ancestors`.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to view the draft and 'Add' permission for the
                  space that

                  the content will be created in.
            /wiki/rest/api/content/search:
              get:
                tags:
                  - Search
                  - Content
                  - By
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                summary: Search content by CQL
                description: >-
                  Returns the list of content that matches a Confluence Query
                  Language

                  (CQL) query. For information on CQL, see:

                  [Advanced searching using
                  CQL](https://developer.atlassian.com/cloud/confluence/advanced-searching-using-cql/).


                  Example initial call:

                  ```

                  /wiki/rest/api/content/search?cql=type=page&limit=25

                  ```


                  Example response:

                  ```

                  {
                    "results": [
                      { ... },
                      { ... },
                      ...
                      { ... }
                    ],
                    "limit": 25,
                    "size": 25,
                    ...
                    "_links": {
                      "base": "<url>",
                      "context": "<url>",
                      "next": "/rest/api/content/search?cql=type=page&limit=25&cursor=raNDoMsTRiNg",
                      "self": "<url>"
                    }
                  }

                  ```


                  When additional results are available, returns `next` and
                  `prev` URLs to retrieve them in subsequent calls. The URLs
                  each contain a cursor that points to the appropriate set of
                  results. Use `limit` to specify the number of results returned
                  in each call.

                  Example subsequent call (taken from example response):

                  ```

                  /wiki/rest/api/content/search?cql=type=page&limit=25&cursor=raNDoMsTRiNg

                  ```

                  The response to this will have a `prev` URL similar to the
                  `next` in the example response.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission).

                  Only content that the user has permission to view will be
                  returned.
            /wiki/rest/api/content/{id}:
              get:
                tags:
                  - Get
                  - Content
                  - By
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                summary: Get content by ID
                description: >-
                  Deprecated, use [Confluence's v2
                  API](https://developer.atlassian.com/cloud/confluence/rest/v2/intro/).


                  Returns a single piece of content, like a page or a blog post.


                  By default, the following objects are expanded: `space`,
                  `history`, `version`.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to view the content. If the content is a blog post,
                  'View' permission

                  for the space is required.
              put:
                tags:
                  - Update
                  - Content
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                summary: Update content
                description: >-
                  Deprecated, use [Confluence's v2
                  API](https://developer.atlassian.com/cloud/confluence/rest/v2/intro/).


                  Updates a piece of content. Use this method to update the
                  title or body

                  of a piece of content, change the status, change the parent
                  page, and more.


                  Note, updating draft content is currently not supported.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to update the content.
              delete:
                tags:
                  - Delete
                  - Content
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                summary: Delete content
                description: >-
                  Deprecated, use [Confluence's v2
                  API](https://developer.atlassian.com/cloud/confluence/rest/v2/intro/).


                  Moves a piece of content to the space's trash or purges it
                  from the trash,

                  depending on the content's type and status:


                  - If the content's type is `page`,`blogpost`, or `attachment`
                  and its status is `current`,

                  it will be trashed.

                  - If the content's type is `page`,`blogpost`, or `attachment`
                  and its status is `trashed`,

                  the content will be purged from the trash and deleted
                  permanently. Note,

                  you must also set the `status` query parameter to `trashed` in
                  your request.

                  - If the content's type is `comment`, it will be deleted

                  permanently without being trashed.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Delete' permission for the space that the content is in.
            /wiki/rest/api/content/{id}/pageTree:
              delete:
                tags:
                  - Delete
                  - Page
                  - Trees
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                summary: Delete page tree
                description: >-
                  Moves a pagetree rooted at a page to the space's trash:


                  - If the content's type is `page` and its status is `current`,
                  it will be trashed including

                  all its descendants.

                  - For every other combination of content type and status, this
                  API is not supported.


                  This API accepts the pageTree delete request and returns a
                  task ID.

                  The delete process happens asynchronously.

                   Response example:
                   <pre><code>
                   {
                        "id" : "1180606",
                        "links" : {
                             "status" : "/rest/api/longtask/1180606"
                        }
                   }
                   </code></pre>
                   Use the `/longtask/<taskId>` REST API to get the copy task status.

                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Delete' permission for the space that the content is in.
            /wiki/rest/api/content/{id}/child:
              get:
                tags:
                  - Get
                  - Content
                  - Children
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                summary: Get content children
                description: >-
                  Deprecated, use [Confluence's v2
                  API](https://developer.atlassian.com/cloud/confluence/rest/v2/intro/).


                  Returns a map of the direct children of a piece of content. A
                  piece of content

                  has different types of child content, depending on its type.
                  These are

                  the default parent-child content type relationships:


                  - `page`: child content is `page`, `comment`, `attachment`

                  - `blogpost`: child content is `comment`, `attachment`

                  - `attachment`: child content is `comment`

                  - `comment`: child content is `attachment`


                  Apps can override these default relationships. Apps can also
                  introduce

                  new content types that create new parent-child content
                  relationships.


                  Note, the map will always include all child content types that
                  are valid

                  for the content. However, if the content has no instances of a
                  child content

                  type, the map will contain an empty array for that child
                  content type.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**: 'View' permission for the space,

                  and permission to view the content if it is a page.
            /wiki/rest/api/content/{pageId}/move/{position}/{targetId}:
              put:
                tags:
                  - Move
                  - Page
                  - To
                  - New
                  - Locations
                  - Relative
                  - Target
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                summary: Move a page to a new location relative to a target page
                description: >-
                  Move a page to a new location relative to a target page:


                  * `before` - move the page under the same parent as the
                  target, before the target in the list of children

                  * `after` - move the page under the same parent as the target,
                  after the target in the list of children

                  * `append` - move the page to be a child of the target


                  Caution: This API can move pages to the top level of a space.
                  Top-level pages are difficult to find in the UI

                  because they do not show up in the page tree display. To avoid
                  this, never use `before` or `after` positions

                  when the `targetId` is a top-level page.
            /wiki/rest/api/content/{id}/child/attachment:
              get:
                tags:
                  - Get
                  - Attachments
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                summary: Get attachments
                description: >-
                  Deprecated, use [Confluence's v2
                  API](https://developer.atlassian.com/cloud/confluence/rest/v2/intro/).


                  Returns the attachments for a piece of content.


                  By default, the following objects are expanded: `metadata`.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to view the content. If the content is a blog post,
                  'View' permission

                  for the space is required.
              put:
                tags:
                  - Create
                  - Or
                  - Update
                  - Attachment
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                summary: Create or update attachment
                description: >-
                  Adds an attachment to a piece of content. If the attachment
                  already exists

                  for the content, then the attachment is updated (i.e. a new
                  version of the

                  attachment is created).


                  Note, you must set a `X-Atlassian-Token: nocheck` header on
                  the request

                  for this method, otherwise it will be blocked. This protects
                  against XSRF

                  attacks, which is necessary as this method accepts
                  multipart/form-data.


                  The media type 'multipart/form-data' is defined in [RFC
                  7578](https://www.ietf.org/rfc/rfc7578.txt).

                  Most client libraries have classes that make it easier to
                  implement

                  multipart posts, like the
                  [MultipartEntityBuilder](https://hc.apache.org/httpcomponents-client-5.1.x/current/httpclient5/apidocs/)

                  Java class provided by Apache HTTP Components.


                  Note, according to [RFC
                  7578](https://tools.ietf.org/html/rfc7578#section-4.5),

                  in the case where the form data is text,

                  the charset parameter for the "text/plain" Content-Type may be
                  used to

                  indicate the character encoding used in that part. In the case
                  of this

                  API endpoint, the `comment` body parameter should be sent with
                  `type=text/plain`

                  and `charset=utf-8` values. This will force the charset to be
                  UTF-8.


                  Example: This curl command attaches a file ('example.txt') to
                  a piece of

                  content (id='123') with a comment and `minorEdits`=true. If
                  the 'example.txt'

                  file already exists, it will update it with a new version of
                  the attachment.


                  ``` bash

                  curl -D- \
                    -u admin:admin \
                    -X PUT \
                    -H 'X-Atlassian-Token: nocheck' \
                    -F 'file=@"example.txt"' \
                    -F 'minorEdit="true"' \
                    -F 'comment="Example attachment comment"; type=text/plain; charset=utf-8' \
                    http://myhost/rest/api/content/123/child/attachment
                  ```

                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to update the content.
              post:
                tags:
                  - Create
                  - Attachment
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                summary: Create attachment
                description: >-
                  Adds an attachment to a piece of content. This method only
                  adds a new

                  attachment. If you want to update an existing attachment, use

                  [Create or update
                  attachments](#api-content-id-child-attachment-put).


                  Note, you must set a `X-Atlassian-Token: nocheck` header on
                  the request

                  for this method, otherwise it will be blocked. This protects
                  against XSRF

                  attacks, which is necessary as this method accepts
                  multipart/form-data.


                  The media type 'multipart/form-data' is defined in [RFC
                  7578](https://www.ietf.org/rfc/rfc7578.txt).

                  Most client libraries have classes that make it easier to
                  implement

                  multipart posts, like the
                  [MultipartEntityBuilder](https://hc.apache.org/httpcomponents-client-5.1.x/current/httpclient5/apidocs/)

                  Java class provided by Apache HTTP Components.


                  Note, according to [RFC
                  7578](https://tools.ietf.org/html/rfc7578#section-4.5),

                  in the case where the form data is text,

                  the charset parameter for the "text/plain" Content-Type may be
                  used to

                  indicate the character encoding used in that part. In the case
                  of this

                  API endpoint, the `comment` body parameter should be sent with
                  `type=text/plain`

                  and `charset=utf-8` values. This will force the charset to be
                  UTF-8.


                  Example: This curl command attaches a file ('example.txt') to
                  a container

                  (id='123') with a comment and `minorEdits`=true.


                  ``` bash

                  curl -D- \
                    -u admin:admin \
                    -X POST \
                    -H 'X-Atlassian-Token: nocheck' \
                    -F 'file=@"example.txt"' \
                    -F 'minorEdit="true"' \
                    -F 'comment="Example attachment comment"; type=text/plain; charset=utf-8' \
                    http://myhost/rest/api/content/123/child/attachment
                  ```

                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to update the content.
            /wiki/rest/api/content/{id}/child/attachment/{attachmentId}:
              put:
                tags:
                  - Update
                  - Attachment
                  - Properties
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                summary: Update attachment properties
                description: >-
                  Updates the attachment properties, i.e. the non-binary data of
                  an attachment

                  like the filename, media-type, comment, and parent container.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to update the content.
            /wiki/rest/api/content/{id}/child/attachment/{attachmentId}/data:
              post:
                tags:
                  - Update
                  - Attachment
                  - Data
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                summary: Update attachment data
                description: >-
                  Updates the binary data of an attachment, given the attachment
                  ID, and

                  optionally the comment and the minor edit field.


                  This method is essentially the same as [Create or update
                  attachments](#api-content-id-child-attachment-put),

                  except that it matches the attachment ID rather than the name.


                  Note, you must set a `X-Atlassian-Token: nocheck` header on
                  the request

                  for this method, otherwise it will be blocked. This protects
                  against XSRF

                  attacks, which is necessary as this method accepts
                  multipart/form-data.


                  The media type 'multipart/form-data' is defined in [RFC
                  7578](https://www.ietf.org/rfc/rfc7578.txt).

                  Most client libraries have classes that make it easier to
                  implement

                  multipart posts, like the
                  [MultipartEntityBuilder](https://hc.apache.org/httpcomponents-client-5.1.x/current/httpclient5/apidocs/)

                  Java class provided by Apache HTTP Components.


                  Note, according to [RFC
                  7578](https://tools.ietf.org/html/rfc7578#section-4.5),

                  in the case where the form data is text,

                  the charset parameter for the "text/plain" Content-Type may be
                  used to

                  indicate the character encoding used in that part. In the case
                  of this

                  API endpoint, the `comment` body parameter should be sent with
                  `type=text/plain`

                  and `charset=utf-8` values. This will force the charset to be
                  UTF-8.


                  Example: This curl command updates an attachment (id='att456')
                  that is attached

                  to a piece of content (id='123') with a comment and
                  `minorEdits`=true.


                  ``` bash

                  curl -D- \
                    -u admin:admin \
                    -X POST \
                    -H 'X-Atlassian-Token: nocheck' \
                    -F 'file=@"example.txt"' \
                    -F 'minorEdit="true"' \
                    -F 'comment="Example attachment comment"; type=text/plain; charset=utf-8' \
                    http://myhost/rest/api/content/123/child/attachment/att456/data
                  ```

                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to update the content.
            /wiki/rest/api/content/{id}/child/attachment/{attachmentId}/download:
              get:
                tags:
                  - Get
                  - To
                  - Download
                  - Attachment
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                summary: Get URI to download attachment
                description: >-
                  Redirects the client to a URL that serves an attachment's
                  binary data.
            /wiki/rest/api/content/{id}/child/comment:
              get:
                tags:
                  - Get
                  - Content
                  - Comments
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                summary: Get content comments
                description: >-
                  Deprecated, use [Confluence's v2
                  API](https://developer.atlassian.com/cloud/confluence/rest/v2/intro/).


                  Returns the comments on a piece of content.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**: 'View' permission for the space,

                  and permission to view the content if it is a page.
            /wiki/rest/api/content/{id}/child/{type}:
              get:
                tags:
                  - Get
                  - Content
                  - Children
                  - By
                  - Types
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                summary: Get content children by type
                description: >-
                  Deprecated, use [Confluence's v2
                  API](https://developer.atlassian.com/cloud/confluence/rest/v2/intro/).


                  Returns all children of a given type, for a piece of content.

                  A piece of content has different types of child content,
                  depending on its type:


                  - `page`: child content is `page`, `comment`, `attachment`

                  - `blogpost`: child content is `comment`, `attachment`

                  - `attachment`: child content is `comment`

                  - `comment`: child content is `attachment`


                  Custom content types that are provided by apps can also be
                  returned.


                  Note, this method only returns direct children. To return
                  children at all

                  levels, use [Get descendants by
                  type](#api-content-id-descendant-type-get).


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**: 'View' permission for the space,

                  and permission to view the content if it is a page.
            /wiki/rest/api/content/{id}/descendant:
              get:
                tags:
                  - Get
                  - Content
                  - Descendants
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                summary: Get content descendants
                description: >-
                  Returns a map of the descendants of a piece of content. This
                  is similar

                  to [Get content children](#api-content-id-child-get), except
                  that this

                  method returns child pages at all levels, rather than just the
                  direct

                  child pages.


                  A piece of content has different types of descendants,
                  depending on its type:


                  - `page`: descendant is `page`, `comment`, `attachment`

                  - `blogpost`: descendant is `comment`, `attachment`

                  - `attachment`: descendant is `comment`

                  - `comment`: descendant is `attachment`


                  The map will always include all descendant types that are
                  valid for the content.

                  However, if the content has no instances of a descendant type,
                  the map will

                  contain an empty array for that descendant type.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'View' permission for the space, and permission to view the
                  content if it

                  is a page.
            /wiki/rest/api/content/{id}/descendant/{type}:
              get:
                tags:
                  - Get
                  - Content
                  - Descendants
                  - By
                  - Types
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                summary: Get content descendants by type
                description: >-
                  Returns all descendants of a given type, for a piece of
                  content. This is

                  similar to [Get content children by
                  type](#api-content-id-child-type-get),

                  except that this method returns child pages at all levels,
                  rather than just

                  the direct child pages.


                  A piece of content has different types of descendants,
                  depending on its type:


                  - `page`: descendant is `page`, `comment`, `attachment`

                  - `blogpost`: descendant is `comment`, `attachment`

                  - `attachment`: descendant is `comment`

                  - `comment`: descendant is `attachment`


                  Custom content types that are provided by apps can also be
                  returned.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'View' permission for the space, and permission to view the
                  content if it

                  is a page.
            /wiki/rest/api/content/{id}/history:
              get:
                tags:
                  - Get
                  - Content
                  - History
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                summary: Get content history
                description: >-
                  Deprecated, use [Confluence's v2
                  API](https://developer.atlassian.com/cloud/confluence/rest/v2/intro/).


                  Returns the most recent update for a piece of content.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**: Permission to view the content.
            /wiki/rest/api/content/{id}/history/{version}/macro/id/{macroId}:
              get:
                tags:
                  - Get
                  - Macro
                  - Body
                  - By
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                summary: Get macro body by macro ID
                description: >-
                  Returns the body of a macro in storage format, for the given
                  macro ID.

                  This includes information like the name of the macro, the body
                  of the macro,

                  and any macro parameters. This method is mainly used by Cloud
                  apps.


                  About the macro ID: When a macro is created in a new version
                  of content,

                  Confluence will generate a random ID for it, unless an ID is
                  specified

                  (by an app). The macro ID will look similar to this:
                  '50884bd9-0cb8-41d5-98be-f80943c14f96'.

                  The ID is then persisted as new versions of content are
                  created, and is

                  only modified by Confluence if there are conflicting IDs.


                  Note, to preserve backwards compatibility this resource will
                  also match on

                  the hash of the macro body, even if a macro ID is found. This
                  check will

                  eventually become redundant, as macro IDs are generated for
                  pages and

                  transparently propagate out to all instances.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to view the content that the macro is in.
            /wiki/rest/api/content/{id}/history/{version}/macro/id/{macroId}/convert/{to}:
              get:
                tags:
                  - Get
                  - Macro
                  - Body
                  - By
                  - And
                  - Convert
                  - The
                  - Representation
                  - Synchronously
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                summary: >-
                  Get macro body by macro ID and convert the representation
                  synchronously
                description: >-
                  Returns the body of a macro in format specified in path, for
                  the given macro ID.

                  This includes information like the name of the macro, the body
                  of the macro,

                  and any macro parameters.


                  About the macro ID: When a macro is created in a new version
                  of content,

                  Confluence will generate a random ID for it, unless an ID is
                  specified

                  (by an app). The macro ID will look similar to this:
                  '50884bd9-0cb8-41d5-98be-f80943c14f96'.

                  The ID is then persisted as new versions of content are
                  created, and is

                  only modified by Confluence if there are conflicting IDs.


                  Note, to preserve backwards compatibility this resource will
                  also match on

                  the hash of the macro body, even if a macro ID is found. This
                  check will

                  eventually become redundant, as macro IDs are generated for
                  pages and

                  transparently propagate out to all instances.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to view the content that the macro is in.
            /wiki/rest/api/content/{id}/history/{version}/macro/id/{macroId}/convert/async/{to}:
              get:
                tags:
                  - Get
                  - Macro
                  - Body
                  - By
                  - And
                  - Convert
                  - Representation
                  - Asynchronously
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                summary: >-
                  Get macro body by macro ID and convert representation
                  Asynchronously
                description: >-
                  Returns Async Id of the conversion task which will convert the
                  macro into a content body of the desired format.

                  The result will be available for 5 minutes after completion of
                  the conversion.


                  About the macro ID: When a macro is created in a new version
                  of content,

                  Confluence will generate a random ID for it, unless an ID is
                  specified

                  (by an app). The macro ID will look similar to this:
                  '884bd9-0cb8-41d5-98be-f80943c14f96'.

                  The ID is then persisted as new versions of content are
                  created, and is

                  only modified by Confluence if there are conflicting IDs.


                  Note, to preserve backwards compatibility this resource will
                  also match on

                  the hash of the macro body, even if a macro ID is found. This
                  check will

                  eventually become redundant, as macro IDs are generated for
                  pages and

                  transparently propagate out to all instances.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to view the content that the macro is in.
            /wiki/rest/api/content/{id}/label:
              get:
                tags:
                  - Get
                  - Labels
                  - For
                  - Content
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                summary: Get labels for content
                description: >-
                  Deprecated, use [Confluence's v2
                  API](https://developer.atlassian.com/cloud/confluence/rest/v2/intro/).


                  Returns the labels on a piece of content.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'View' permission for the space and permission to view the
                  content if it is a page.
              post:
                tags:
                  - Add
                  - Labels
                  - To
                  - Content
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                summary: Add labels to content
                description: >-
                  Adds labels to a piece of content. Does not modify the
                  existing labels.


                  Notes:


                  - Labels can also be added when creating content ([Create
                  content](#api-content-post)).

                  - Labels can be updated when updating content ([Update
                  content](#api-content-id-put)).

                  This will delete the existing labels and replace them with the
                  labels in

                  the request.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to update the content.
              delete:
                tags:
                  - Removes
                  - Labels
                  - From
                  - Content
                  - Using
                  - Queries
                  - Parameters
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                summary: Remove label from content using query parameter
                description: >-
                  Removes a label from a piece of content. Labels can't be
                  deleted from archived content.

                  This is similar to [Remove label from
                  content](#api-content-id-label-label-delete)

                  except that the label name is specified via a query parameter.


                  Use this method if the label name has "/" characters, as

                  [Remove label from content using query
                  parameter](#api-content-id-label-delete)

                  does not accept "/" characters for the label name.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to update the content.
            /wiki/rest/api/content/{id}/label/{label}:
              delete:
                tags:
                  - Removes
                  - Labels
                  - From
                  - Content
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                summary: Remove label from content
                description: >-
                  Removes a label from a piece of content. Labels can't be
                  deleted from archived content.

                  This is similar to [Remove label from content using query
                  parameter](#api-content-id-label-delete)

                  except that the label name is specified via a path parameter.


                  Use this method if the label name does not have "/"
                  characters, as the path

                  parameter does not accept "/" characters for security reasons.
                  Otherwise,

                  use [Remove label from content using query
                  parameter](#api-content-id-label-delete).


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to update the content.
            /wiki/rest/api/content/{id}/notification/child-created:
              get:
                tags:
                  - Get
                  - Watches
                  - For
                  - Page
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                summary: Get watches for page
                description: >-
                  Returns the watches for a page. A user that watches a page
                  will receive

                  receive notifications when the page is updated.


                  If you want to manage watches for a page, use the following
                  `user` methods:


                  - [Get content watch status for
                  user](#api-user-watch-content-contentId-get)

                  - [Add content watch](#api-user-watch-content-contentId-post)

                  - [Remove content
                  watch](#api-user-watch-content-contentId-delete)


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission).
            /wiki/rest/api/content/{id}/notification/created:
              get:
                tags:
                  - Get
                  - Watches
                  - For
                  - Space
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                summary: Get watches for space
                description: >-
                  Returns all space watches for the space that the content is
                  in. A user that

                  watches a space will receive receive notifications when any
                  content in the

                  space is updated.


                  If you want to manage watches for a space, use the following
                  `user` methods:


                  - [Get space watch status for
                  user](#api-user-watch-space-spaceKey-get)

                  - [Add space watch](#api-user-watch-space-spaceKey-post)

                  - [Remove space watch](#api-user-watch-space-spaceKey-delete)


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission).
            /wiki/rest/api/content/{id}/pagehierarchy/copy:
              post:
                tags:
                  - Copy
                  - Page
                  - Hierarchy
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                summary: Copy page hierarchy
                description: >-
                  Copy page hierarchy allows the copying of an entire hierarchy
                  of pages and their associated properties, permissions and
                  attachments.
                   The id path parameter refers to the content id of the page to copy, and the new parent of this copied page is defined using the destinationPageId in the request body.
                   The titleOptions object defines the rules of renaming page titles during the copy;
                   for example, search and replace can be used in conjunction to rewrite the copied page titles.

                   Response example:
                   <pre><code>
                   {
                        "id" : "1180606",
                        "links" : {
                             "status" : "/rest/api/longtask/1180606"
                        }
                   }
                   </code></pre>
                   Use the /longtask/<taskId> REST API to get the copy task status.
            /wiki/rest/api/content/{id}/copy:
              post:
                tags:
                  - Copy
                  - Single
                  - Page
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                summary: Copy single page
                description: >-
                  Copies a single page and its associated properties,
                  permissions, attachments, and custom contents.
                   The `id` path parameter refers to the content ID of the page to copy. The target of the page to be copied
                   is defined using the `destination` in the request body and can be one of the following types.

                    - `space`: page will be copied to the specified space as a root page on the space
                    - `parent_page`: page will be copied as a child of the specified parent page
                    - `existing_page`: page will be copied and replace the specified page

                  By default, the following objects are expanded: `space`,
                  `history`, `version`.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**: 'Add' permission for the space that the content
                  will be copied in and permission to update the content if
                  copying to an `existing_page`.
            /wiki/rest/api/content/{id}/permission/check:
              post:
                tags:
                  - Checks
                  - Content
                  - Permissions
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                summary: Check content permissions
                description: >-
                  Check if a user or a group can perform an operation to the
                  specified content. The `operation` to check

                  must be provided. The user’s account ID or the ID of the group
                  can be provided in the `subject` to check

                  permissions against a specified user or group. The following
                  permission checks are done to make sure that the

                  user or group has the proper access:


                  - site permissions

                  - space permissions

                  - content restrictions


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission) if checking permission for self,

                  otherwise 'Confluence Administrator' global permission is
                  required.
            /wiki/rest/api/content/{id}/property:
              get:
                tags:
                  - Get
                  - Content
                  - Properties
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                summary: Get content properties
                description: >-
                  Returns the properties for a piece of content. For more
                  information

                  about content properties, see [Confluence entity
                  properties](https://developer.atlassian.com/cloud/confluence/confluence-entity-properties/).


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'View' permission for the space, and permission to view the
                  content if it is a page.
              post:
                tags:
                  - Create
                  - Content
                  - Properties
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                summary: Create content property
                description: >-
                  Creates a property for an existing piece of content. For more
                  information

                  about content properties, see [Confluence entity
                  properties](https://developer.atlassian.com/cloud/confluence/confluence-entity-properties/).


                  This is the same as [Create content property for
                  key](#api-content-id-property-key-post)

                  except that the key is specified in the request body instead
                  of as a

                  path parameter.


                  Content properties can also be added when creating a new piece
                  of content

                  by including them in the `metadata.properties` of the request.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to update the content.
            /wiki/rest/api/content/{id}/property/{key}:
              get:
                tags:
                  - Get
                  - Content
                  - Properties
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                summary: Get content property
                description: >-
                  Returns a content property for a piece of content. For more
                  information, see

                  [Confluence entity
                  properties](https://developer.atlassian.com/cloud/confluence/confluence-entity-properties/).


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'View' permission for the space, and permission to view the
                  content if it is a page.
              put:
                tags:
                  - Update
                  - Content
                  - Properties
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                summary: Update content property
                description: >-
                  Updates an existing content property. This method will also
                  create a new

                  property for a piece of content, if the property key does not
                  exist and

                  the property version is 1. For more information about content
                  properties, see

                  [Confluence entity
                  properties](https://developer.atlassian.com/cloud/confluence/confluence-entity-properties/).


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to update the content.
              post:
                tags:
                  - Create
                  - Content
                  - Properties
                  - For
                  - Keys
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                summary: Create content property for key
                description: >-
                  Creates a property for an existing piece of content. For more
                  information

                  about content properties, see [Confluence entity
                  properties](https://developer.atlassian.com/cloud/confluence/confluence-entity-properties/).


                  This is the same as [Create content
                  property](#api-content-id-property-post)

                  except that the key is specified as a path parameter instead
                  of in the

                  request body.


                  Content properties can also be added when creating a new piece
                  of content

                  by including them in the `metadata.properties` of the request.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to update the content.
              delete:
                tags:
                  - Delete
                  - Content
                  - Properties
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                summary: Delete content property
                description: >-
                  Deletes a content property. For more information about content
                  properties, see

                  [Confluence entity
                  properties](https://developer.atlassian.com/cloud/confluence/confluence-entity-properties/).


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to update the content.
            /wiki/rest/api/content/{id}/restriction:
              get:
                tags:
                  - Get
                  - Restrictions
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                summary: Get restrictions
                description: >-
                  Returns the restrictions on a piece of content.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to view the content.
              put:
                tags:
                  - Update
                  - Restrictions
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                summary: Update restrictions
                description: >-
                  Updates restrictions for a piece of content. For each
                  operation specified in the request, it removes

                  any existing restrictions on the content for that operation,
                  and replaces them with the restrictions in the request.

                  Note: Not specifying an operation will ignore restrictions of
                  that type, and passing an empty list for an operation

                  will remove all existing restrictions of that type.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to edit the content.
              post:
                tags:
                  - Add
                  - Restrictions
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                summary: Add restrictions
                description: >-
                  Adds restrictions to a piece of content. Note, this does not
                  change any

                  existing restrictions on the content.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to edit the content.
              delete:
                tags:
                  - Delete
                  - Restrictions
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                summary: Delete restrictions
                description: >-
                  Removes all restrictions (read and update) on a piece of
                  content.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to edit the content.
            /wiki/rest/api/content/{id}/restriction/byOperation:
              get:
                tags:
                  - Get
                  - Restrictions
                  - By
                  - Operation
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                summary: Get restrictions by operation
                description: >-
                  Returns restrictions on a piece of content by operation. This
                  method is

                  similar to [Get restrictions](#api-content-id-restriction-get)
                  except that

                  the operations are properties of the return object, rather
                  than items in

                  a results array.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to view the content.
            /wiki/rest/api/content/{id}/restriction/byOperation/{operationKey}:
              get:
                tags:
                  - Get
                  - Restrictions
                  - For
                  - Operation
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                summary: Get restrictions for operation
                description: >-
                  Returns the restictions on a piece of content for a given
                  operation (read

                  or update).


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to view the content.
            /wiki/rest/api/content/{id}/restriction/byOperation/{operationKey}/group/{groupName}:
              get:
                tags:
                  - Get
                  - Content
                  - Restrictions
                  - Status
                  - For
                  - Group
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                summary: Get content restriction status for group
                description: >-
                  Deprecated, use [Get content restriction status for group via
                  groupId](https://developer.atlassian.com/cloud/confluence/rest/v1/api-group-content-restrictions/#api-wiki-rest-api-content-id-restriction-byoperation-operationkey-bygroupid-groupid-get).

                  Returns whether the specified content restriction applies to a
                  group.

                  For example, if a page with `id=123` has a `read` restriction
                  for the `admins` group,

                  the following request will return `true`:


                  `/wiki/rest/api/content/123/restriction/byOperation/read/group/admins`


                  Note that a response of `true` does not guarantee that the
                  group can view the page, as it does not account for

                  account-inherited restrictions, space permissions, or even
                  product access. For more

                  information, see [Confluence
                  permissions](https://confluence.atlassian.com/x/_AozKw).


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to view the content.
              put:
                tags:
                  - Add
                  - Group
                  - To
                  - Content
                  - Restrictions
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                summary: Add group to content restriction
                description: >-
                  Deprecated, use [Add group to content restriction via
                  groupId](https://developer.atlassian.com/cloud/confluence/rest/v1/api-group-content-restrictions/#api-wiki-rest-api-content-id-restriction-byoperation-operationkey-bygroupid-groupid-put).

                  Adds a group to a content restriction. That is, grant read or
                  update

                  permission to the group for a piece of content.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to edit the content.
              delete:
                tags:
                  - Removes
                  - Group
                  - From
                  - Content
                  - Restrictions
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                summary: Remove group from content restriction
                description: >-
                  Deprecated, use [Remove group from content restriction by
                  groupId](https://developer.atlassian.com/cloud/confluence/rest/v1/api-group-content-restrictions/#api-wiki-rest-api-content-id-restriction-byoperation-operationkey-user-delete).

                  Removes a group from a content restriction. That is, remove
                  read or update

                  permission for the group for a piece of content.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to edit the content.
            /wiki/rest/api/content/{id}/restriction/byOperation/{operationKey}/byGroupId/{groupId}:
              get:
                tags:
                  - Get
                  - Content
                  - Restrictions
                  - Status
                  - For
                  - Group
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                summary: Get content restriction status for group
                description: >-
                  Returns whether the specified content restriction applies to a
                  group.

                  For example, if a page with `id=123` has a `read` restriction
                  for the `123456` group id,

                  the following request will return `true`:


                  `/wiki/rest/api/content/123/restriction/byOperation/read/byGroupId/123456`


                  Note that a response of `true` does not guarantee that the
                  group can view the page, as it does not account for

                  account-inherited restrictions, space permissions, or even
                  product access. For more

                  information, see [Confluence
                  permissions](https://confluence.atlassian.com/x/_AozKw).


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to view the content.
              put:
                tags:
                  - Add
                  - Group
                  - To
                  - Content
                  - Restrictions
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                summary: Add group to content restriction
                description: >-
                  Adds a group to a content restriction by Group Id. That is,
                  grant read or update

                  permission to the group for a piece of content.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to edit the content.
              delete:
                tags:
                  - Removes
                  - Group
                  - From
                  - Content
                  - Restrictions
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                summary: Remove group from content restriction
                description: >-
                  Removes a group from a content restriction. That is, remove
                  read or update

                  permission for the group for a piece of content.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to edit the content.
            /wiki/rest/api/content/{id}/restriction/byOperation/{operationKey}/user:
              get:
                tags:
                  - Get
                  - Content
                  - Restrictions
                  - Status
                  - For
                  - Users
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                summary: Get content restriction status for user
                description: >-
                  Returns whether the specified content restriction applies to a
                  user.

                  For example, if a page with `id=123` has a `read` restriction
                  for a user with an account ID of

                  `384093:32b4d9w0-f6a5-3535-11a3-9c8c88d10192`, the following
                  request will return `true`:


                  `/wiki/rest/api/content/123/restriction/byOperation/read/user?accountId=384093:32b4d9w0-f6a5-3535-11a3-9c8c88d10192`


                  Note that a response of `true` does not guarantee that the
                  user can view the page, as it does not account for

                  account-inherited restrictions, space permissions, or even
                  product access. For more

                  information, see [Confluence
                  permissions](https://confluence.atlassian.com/x/_AozKw).


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to view the content.
              put:
                tags:
                  - Add
                  - Users
                  - To
                  - Content
                  - Restrictions
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                summary: Add user to content restriction
                description: >-
                  Adds a user to a content restriction. That is, grant read or
                  update

                  permission to the user for a piece of content.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to edit the content.
              delete:
                tags:
                  - Removes
                  - Users
                  - From
                  - Content
                  - Restrictions
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                summary: Remove user from content restriction
                description: >-
                  Removes a group from a content restriction. That is, remove
                  read or update

                  permission for the group for a piece of content.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to edit the content.
            /wiki/rest/api/content/{id}/state:
              get:
                tags:
                  - Get
                  - Content
                  - States
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                summary: Get content state
                description: >-
                  Gets the current content state of the draft or current version
                  of content. To specify the draft version, set

                  the parameter status to draft, otherwise archived or current
                  will get the relevant published state.

                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to view the content.
              put:
                tags:
                  - Sets
                  - The
                  - Content
                  - States
                  - Of
                  - And
                  - Publishes
                  - New
                  - Versions
                  - Content
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                summary: >-
                  Set the content state of a content and publishes a new version
                  of the content.
                description: >-
                  Sets the content state of the content specified and creates a
                  new version

                  (publishes the content without changing the body) of the
                  content with the new state.


                  You may pass in either an id of a state, or the name and color
                  of a desired new state.

                  If all 3 are passed in, id will be used.

                  If the name and color passed in already exist under the
                  current user's existing custom states, the existing state will
                  be reused.

                  If custom states are disabled in the space of the content
                  (which can be determined by getting the content state space
                  settings of the content's space)

                  then this set will fail.


                  You may not remove a content state via this PUT request. You
                  must use the DELETE method. A specified state is required in
                  the body of this request.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to edit the content.
              delete:
                tags:
                  - Removes
                  - The
                  - Content
                  - States
                  - Of
                  - And
                  - Publishes
                  - New
                  - Versions
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                summary: >-
                  Removes the content state of a content and publishes a new
                  version.
                description: >-
                  Removes the content state of the content specified and creates
                  a new version

                  (publishes the content without changing the body) of the
                  content with the new status.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to edit the content.
            /wiki/rest/api/content/{id}/state/available:
              get:
                tags:
                  - Gets
                  - Available
                  - Content
                  - States
                  - For
                  - Content
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                summary: Gets available content states for content.
                description: >-
                  Gets content states that are available for the content to be
                  set as.

                  Will return all enabled Space Content States.

                  Will only return most the 3 most recently published custom
                  content states to match UI editor list.

                  To get all custom content states, use the /content-states
                  endpoint.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to edit the content.
            /wiki/rest/api/content/{id}/version:
              get:
                tags:
                  - Get
                  - Content
                  - Versions
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                summary: Get content versions
                description: >-
                  Deprecated, use [Confluence's v2
                  API](https://developer.atlassian.com/cloud/confluence/rest/v2/intro/).


                  Returns the versions for a piece of content in descending
                  order.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to view the content. If the content is a blog post,
                  'View' permission

                  for the space is required.
              post:
                tags:
                  - Restore
                  - Content
                  - Versions
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                summary: Restore content version
                description: >-
                  Restores a historical version to be the latest version. That
                  is, a new version

                  is created with the content of the historical version.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to update the content.
            /wiki/rest/api/content/{id}/version/{versionNumber}:
              get:
                tags:
                  - Get
                  - Content
                  - Versions
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                summary: Get content version
                description: >-
                  Deprecated, use [Confluence's v2
                  API](https://developer.atlassian.com/cloud/confluence/rest/v2/intro/).


                  Returns a version for a piece of content.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to view the content. If the content is a blog post,
                  'View' permission

                  for the space is required.
              delete:
                tags:
                  - Delete
                  - Content
                  - Versions
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                summary: Delete content version
                description: >-
                  Delete a historical version. This does not delete the changes
                  made to the

                  content in that version, rather the changes for the deleted
                  version are

                  rolled up into the next version. Note, you cannot delete the
                  current version.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to update the content.
            /wiki/rest/api/content-states:
              put:
                tags:
                  - Bulk
                  - Sets
                  - Content
                  - States
                  - Of
                  - Many
                  - Contents
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                summary: Bulk set content state of many contents
                description: >-
                  Creates a long running task that sets content state of draft
                  or published versions of pages specified.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**

                  Content Edit Permission for a content to have its state set
                  via this endpoint.
              get:
                tags:
                  - Get
                  - Custom
                  - Content
                  - States
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                summary: Get Custom Content States
                description: >-
                  Get custom content states that authenticated user has created.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**

                  Must have user authentication.
            /wiki/rest/api/content-states/delete:
              post:
                tags:
                  - Bulk
                  - Removes
                  - Content
                  - States
                  - From
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                summary: Bulk remove content states from content
                description: >-
                  Creates a long running task that Removes content state from
                  draft or published versions of pages specified.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**

                  Content Edit Permission for a content to have its state
                  removed via this endpoint.
            /wiki/rest/api/content-states/task/{taskId}:
              get:
                tags:
                  - Get
                  - Update
                  - 'On'
                  - Long
                  - Running
                  - Tasks
                  - For
                  - Settings
                  - Of
                  - Content
                  - States
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                summary: Get update on long running task for setting of content state.
                description: >-
                  Get Status of long running task that was previously created to
                  set or remove content states from content.

                  User must first create a task by passing in details to
                  /wiki/rest/api/content-states PUT or DELETE endpoints.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**

                  Must have created long running task
            /wiki/rest/api/contentbody/convert/{to}:
              post:
                tags:
                  - Convert
                  - Content
                  - Body
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                summary: Convert content body
                description: >-
                  Converts a content body from one format to another format.


                  Supported conversions:


                  - storage: view, export_view, styled_view, editor

                  - editor: storage

                  - view: none

                  - export_view: none

                  - styled_view: none


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  If request specifies 'contentIdContext', 'View' permission for
                  the space, and permission to view the content.
            /wiki/rest/api/contentbody/convert/async/{to}:
              post:
                tags:
                  - Asynchronously
                  - Convert
                  - Content
                  - Body
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                summary: Asynchronously convert content body
                description: >-
                  Converts a content body from one format to another format
                  asynchronously.

                  Returns the asyncId for the asynchronous task.


                  Supported conversions:


                  - storage: export_view


                  No other conversions are supported at the moment.

                  Once a conversion is completed, it will be available for 5
                  minutes at the result endpoint.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  If request specifies 'contentIdContext', 'View' permission for
                  the space, and permission to view the content.
            /wiki/rest/api/contentbody/convert/async/{id}:
              get:
                tags:
                  - Get
                  - Asynchronously
                  - Converted
                  - Content
                  - Body
                  - From
                  - The
                  - Identifiers
                  - Or
                  - Current
                  - Status
                  - Of
                  - Tasks
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                summary: >-
                  Get asynchronously converted content body from the id or the
                  current status of the task.
                description: >-
                  Returns the asynchronous content body for the corresponding id
                  if the task is complete 

                  or returns the status of the task.


                  After the task is completed, the result can be obtained for 5
                  minutes, or until an identical conversion request is made
                  again,

                  with allowCache query param set to false.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  If request specifies 'contentIdContext', 'View' permission for
                  the space, and permission to view the content.
            /wiki/rest/api/inlinetasks/search:
              get:
                tags:
                  - Get
                  - Inline
                  - Tasks
                  - Based
                  - 'On'
                  - Search
                  - Parameters
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                summary: Get inline tasks based on search parameters
                description: >-
                  Deprecated, use [Confluence's v2
                  API](https://developer.atlassian.com/cloud/confluence/rest/v2/intro/).


                  Returns inline tasks based on the search query.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission). Only tasks

                  in contents that the user has permission to view are returned.
            /wiki/rest/api/inlinetasks/{inlineTaskId}:
              get:
                tags:
                  - Get
                  - Inline
                  - Tasks
                  - Based
                  - 'On'
                  - Global
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                summary: Get inline task based on global ID
                description: >-
                  Deprecated, use [Confluence's v2
                  API](https://developer.atlassian.com/cloud/confluence/rest/v2/intro/).


                  Returns inline task based on the global ID.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to view the content associated with the task.
              put:
                tags:
                  - Update
                  - Inline
                  - Tasks
                  - Given
                  - Global
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                summary: Update inline task given global ID
                description: >-
                  Updates an inline tasks status given its global ID


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to update the content associated with the task.
            /wiki/rest/api/label:
              get:
                tags:
                  - Get
                  - Labels
                  - Information
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                summary: Get label information
                description: >-
                  Returns label information and a list of contents associated
                  with the label.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission). Only contents

                  that the user is permitted to view is returned.
            /wiki/rest/api/group:
              get:
                tags:
                  - Get
                  - Groups
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                summary: Get groups
                description: >-
                  Returns all user groups. The returned groups are ordered
                  alphabetically in

                  ascending order by group name.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission).
              post:
                tags:
                  - Create
                  - New
                  - Users
                  - Group
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                summary: Create new user group
                description: >-
                  Creates a new user group.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  User must be a site admin.
              delete:
                tags:
                  - Delete
                  - Users
                  - Group
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                summary: Delete user group
                description: >-
                  Delete user group.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  User must be a site admin.
            /wiki/rest/api/group/by-name:
              get:
                tags:
                  - Get
                  - Group
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                summary: Get group
                description: >-
                  Returns a user group for a given group name.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission).
            /wiki/rest/api/group/by-id:
              get:
                tags:
                  - Get
                  - Group
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                summary: Get group
                description: >-
                  Returns a user group for a given group id.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission).
              delete:
                tags:
                  - Delete
                  - Users
                  - Group
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                summary: Delete user group
                description: >-
                  Delete user group.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  User must be a site admin.
            /wiki/rest/api/group/{groupName}:
              get:
                tags:
                  - Get
                  - Group
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                summary: Get group
                description: >-
                  Returns a user group for a given group name.


                  Use updated Get group API


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission).
            /wiki/rest/api/group/member:
              get:
                tags:
                  - Get
                  - Group
                  - Members
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                summary: Get group members
                description: >-
                  Returns the users that are members of a group.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission).
            /wiki/rest/api/group/{groupName}/member:
              get:
                tags:
                  - Get
                  - Group
                  - Members
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                summary: Get group members
                description: >-
                  Returns the users that are members of a group.


                  Use updated Get group API


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission).
            /wiki/rest/api/group/picker:
              get:
                tags:
                  - Search
                  - Groups
                  - By
                  - Partial
                  - Queries
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                summary: Search groups by partial query
                description: Get search results of groups by partial query provided.
            /wiki/rest/api/group/userByGroupId:
              post:
                tags:
                  - Add
                  - Members
                  - To
                  - Group
                  - By
                  - Identifiers
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                summary: Add member to group by groupId
                description: >-
                  Adds a user as a member in a group represented by its groupId


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  User must be a site admin.
              delete:
                tags:
                  - Removes
                  - Members
                  - From
                  - Group
                  - Using
                  - Identifiers
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                summary: Remove member from group using group id
                description: >-
                  Remove user as a member from a group.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  User must be a site admin.
            /wiki/rest/api/group/{groupId}/membersByGroupId:
              get:
                tags:
                  - Get
                  - Group
                  - Members
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                summary: Get group members
                description: >-
                  Returns the users that are members of a group.


                  Use updated Get group API


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission).
            /wiki/rest/api/group/user:
              post:
                tags:
                  - Add
                  - Members
                  - To
                  - Group
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                summary: Add member to group
                description: >-
                  Adds a user as a member in a group.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  User must be a site admin.
              delete:
                tags:
                  - Removes
                  - Members
                  - From
                  - Group
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                summary: Remove member from group
                description: >-
                  Remove user as a member from a group.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  User must be a site admin.
            /wiki/rest/api/longtask:
              get:
                tags:
                  - Get
                  - Long-running
                  - Tasks
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                summary: Get long-running tasks
                description: >-
                  Returns information about all active long-running tasks (e.g.
                  space export),

                  such as how long each task has been running and the percentage
                  of each task

                  that has completed.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission).
            /wiki/rest/api/longtask/{id}:
              get:
                tags:
                  - Get
                  - Long-running
                  - Tasks
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                summary: Get long-running task
                description: >-
                  Returns information about an active long-running task (e.g.
                  space export),

                  such as how long it has been running and the percentage of the
                  task that

                  has completed.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission).
            /wiki/rest/api/relation/{relationName}/from/{sourceType}/{sourceKey}/to/{targetType}:
              get:
                tags:
                  - Find
                  - Target
                  - Entities
                  - Related
                  - To
                  - Source
                  - Entities
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                summary: Find target entities related to a source entity
                description: >-
                  Returns all target entities that have a particular
                  relationship to the

                  source entity. Note, relationships are one way.


                  For example, the following method finds all content that the
                  current user

                  has an 'ignore' relationship with:

                  `GET
                  /wiki/rest/api/relation/ignore/from/user/current/to/content`

                  Note, 'ignore' is an example custom relationship type.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to view both the target entity and source entity.
            /wiki/rest/api/relation/{relationName}/from/{sourceType}/{sourceKey}/to/{targetType}/{targetKey}:
              get:
                tags:
                  - Find
                  - Relationships
                  - From
                  - Source
                  - To
                  - Target
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                summary: Find relationship from source to target
                description: >-
                  Find whether a particular type of relationship exists from a
                  source

                  entity to a target entity. Note, relationships are one way.


                  For example, you can use this method to find whether the
                  current user has

                  selected a particular page as a favorite (i.e. 'save for
                  later'):

                  `GET
                  /wiki/rest/api/relation/favourite/from/user/current/to/content/123`


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to view both the target entity and source entity.
              put:
                tags:
                  - Create
                  - Relationships
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                summary: Create relationship
                description: >-
                  Creates a relationship between two entities (user, space,
                  content). The

                  'favourite' relationship is supported by default, but you can
                  use this method

                  to create any type of relationship between two entities.


                  For example, the following method creates a 'sibling'
                  relationship between

                  two pieces of content:

                  `GET
                  /wiki/rest/api/relation/sibling/from/content/123/to/content/456`


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission).
              delete:
                tags:
                  - Delete
                  - Relationships
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                summary: Delete relationship
                description: >-
                  Deletes a relationship between two entities (user, space,
                  content).


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission).

                  For favourite relationships, the current user can only delete
                  their own

                  favourite relationships. A space administrator can delete
                  favourite

                  relationships for any user.
            /wiki/rest/api/relation/{relationName}/to/{targetType}/{targetKey}/from/{sourceType}:
              get:
                tags:
                  - Find
                  - Source
                  - Entities
                  - Related
                  - To
                  - Target
                  - Entities
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                summary: Find source entities related to a target entity
                description: >-
                  Returns all target entities that have a particular
                  relationship to the

                  source entity. Note, relationships are one way.


                  For example, the following method finds all users that have a
                  'collaborator'

                  relationship to a piece of content with an ID of '1234':

                  `GET
                  /wiki/rest/api/relation/collaborator/to/content/1234/from/user`

                  Note, 'collaborator' is an example custom relationship type.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to view both the target entity and source entity.
            /wiki/rest/api/search:
              get:
                tags:
                  - Search
                  - Content
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                summary: Search content
                description: >-
                  Searches for content using the

                  [Confluence Query Language
                  (CQL)](https://developer.atlassian.com/cloud/confluence/advanced-searching-using-cql/).


                  **Note that CQL input queries submitted through the
                  `/wiki/rest/api/search` endpoint no longer support
                  user-specific fields like `user`, `user.fullname`,
                  `user.accountid`, and `user.userkey`.** 

                  See this [deprecation
                  notice](https://developer.atlassian.com/cloud/confluence/deprecation-notice-search-api/)
                  for more details.


                  Example initial call:

                  ```

                  /wiki/rest/api/search?cql=type=page&limit=25

                  ```


                  Example response:

                  ```

                  {
                    "results": [
                      { ... },
                      { ... },
                      ...
                      { ... }
                    ],
                    "limit": 25,
                    "size": 25,
                    ...
                    "_links": {
                      "base": "<url>",
                      "context": "<url>",
                      "next": "/rest/api/search?cql=type=page&limit=25&cursor=raNDoMsTRiNg",
                      "self": "<url>"
                    }
                  }

                  ```


                  When additional results are available, returns `next` and
                  `prev` URLs to retrieve them in subsequent calls. The URLs
                  each contain a cursor that points to the appropriate set of
                  results. Use `limit` to specify the number of results returned
                  in each call.


                  Example subsequent call (taken from example response):

                  ```

                  /wiki/rest/api/search?cql=type=page&limit=25&cursor=raNDoMsTRiNg

                  ```

                  The response to this will have a `prev` URL similar to the
                  `next` in the example response.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to view the entities. Note, only entities that the
                  user has

                  permission to view will be returned.
            /wiki/rest/api/search/user:
              get:
                tags:
                  - Search
                  - Users
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                summary: Search users
                description: >-
                  Searches for users using user-specific queries from the

                  [Confluence Query Language
                  (CQL)](https://developer.atlassian.com/cloud/confluence/advanced-searching-using-cql/).


                  Note that CQL input queries submitted through the
                  `/wiki/rest/api/search/user` endpoint only support
                  user-specific fields like `user`, `user.fullname`,
                  `user.accountid`, and `user.userkey`.


                  Note that some user fields may be set to null depending on the
                  user's privacy settings.

                  These are: email, profilePicture, displayName, and timeZone.
            /wiki/rest/api/settings/lookandfeel:
              get:
                tags:
                  - Get
                  - Look
                  - And
                  - Feel
                  - Settings
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                summary: Get look and feel settings
                description: >-
                  Returns the look and feel settings for the site or a single
                  space. This

                  includes attributes such as the color scheme, padding, and
                  border radius.


                  The look and feel settings for a space can be inherited from
                  the global

                  look and feel settings or provided by a theme.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  None
              put:
                tags:
                  - Select
                  - Look
                  - And
                  - Feel
                  - Settings
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                summary: Select look and feel settings
                description: >-
                  Sets the look and feel settings to the default (global)
                  settings, the

                  custom settings, or the current theme's settings for a space.

                  The custom and theme settings can only be selected if there is
                  already

                  a theme set for a space. Note, the default space settings are
                  inherited

                  from the current global settings.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Admin' permission for the space.
            /wiki/rest/api/settings/lookandfeel/custom:
              post:
                tags:
                  - Update
                  - Look
                  - And
                  - Feel
                  - Settings
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                summary: Update look and feel settings
                description: >-
                  Updates the look and feel settings for the site or for a
                  single space.

                  If custom settings exist, they are updated. If no custom
                  settings exist,

                  then a set of custom settings is created.


                  Note, if a theme is selected for a space, the space look and
                  feel settings

                  are provided by the theme and cannot be overridden.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Admin' permission for the space.
              delete:
                tags:
                  - Reset
                  - Look
                  - And
                  - Feel
                  - Settings
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                summary: Reset look and feel settings
                description: >-
                  Resets the custom look and feel settings for the site or a
                  single space.

                  This changes the values of the custom settings to be the same
                  as the

                  default settings. It does not change which settings (default
                  or custom)

                  are selected. Note, the default space settings are inherited
                  from the

                  current global settings.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Admin' permission for the space.
            /wiki/rest/api/settings/lookandfeel/selected:
              put:
                tags:
                  - Sets
                  - Look
                  - And
                  - Feel
                  - Settings
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                summary: Set look and feel settings
                description: >-
                  Sets the look and feel settings to either the default settings
                  or the

                  custom settings, for the site or a single space. Note, the
                  default

                  space settings are inherited from the current global settings.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Admin' permission for the space.
            /wiki/rest/api/settings/systemInfo:
              get:
                tags:
                  - Get
                  - Systems
                  - Info
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                summary: Get system info
                description: >-
                  Returns the system information for the Confluence Cloud
                  tenant. This

                  information is used by Atlassian.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission).
            /wiki/rest/api/settings/theme:
              get:
                tags:
                  - Get
                  - Themes
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                summary: Get themes
                description: >-
                  Returns all themes, not including the default theme.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**: None
            /wiki/rest/api/settings/theme/selected:
              get:
                tags:
                  - Get
                  - Global
                  - Theme
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                summary: Get global theme
                description: >-
                  Returns the globally assigned theme.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**: None
            /wiki/rest/api/settings/theme/{themeKey}:
              get:
                tags:
                  - Get
                  - Theme
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                summary: Get theme
                description: >-
                  Returns a theme. This includes information about the theme
                  name,

                  description, and icon.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**: None
            /wiki/rest/api/space:
              get:
                tags:
                  - Get
                  - Spaces
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                summary: Get spaces
                description: >-
                  Deprecated, use [Confluence's v2
                  API](https://developer.atlassian.com/cloud/confluence/rest/v2/intro/).


                  Returns all spaces. The returned spaces are ordered
                  alphabetically in

                  ascending order by space key.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission).

                  Note, the returned list will only contain spaces that the
                  current user

                  has permission to view.
              post:
                tags:
                  - Create
                  - Space
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                summary: Create space
                description: >-
                  Creates a new space. Note, currently you cannot set space
                  labels when

                  creating a space.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Create Space(s)' global permission.
            /wiki/rest/api/space/_private:
              post:
                tags:
                  - Create
                  - Private
                  - Space
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                summary: Create private space
                description: >-
                  Creates a new space that is only visible to the creator. This
                  method is

                  the same as the [Create space](#api-space-post) method with
                  permissions

                  set to the current user only. Note, currently you cannot set
                  space

                  labels when creating a space.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Create Space(s)' global permission.
            /wiki/rest/api/space/{spaceKey}:
              get:
                tags:
                  - Get
                  - Space
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                summary: Get space
                description: >-
                  Deprecated, use [Confluence's v2
                  API](https://developer.atlassian.com/cloud/confluence/rest/v2/intro/).


                  Returns a space. This includes information like the name,
                  description,

                  and permissions, but not the content in the space.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'View' permission for the space.
              put:
                tags:
                  - Update
                  - Space
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                summary: Update space
                description: >-
                  Updates the name, description, or homepage of a space.


                  -   For security reasons, permissions cannot be updated via
                  the API and

                  must be changed via the user interface instead.

                  -   Currently you cannot set space labels when updating a
                  space.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Admin' permission for the space.
              delete:
                tags:
                  - Delete
                  - Space
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                summary: Delete space
                description: >-
                  Deletes a space. Note, the space will be deleted in a long
                  running task.

                  Therefore, the space may not be deleted yet when this method
                  has

                  returned. Clients should poll the status link that is returned
                  in the

                  response until the task completes.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Admin' permission for the space.
            /wiki/rest/api/space/{spaceKey}/content:
              get:
                tags:
                  - Get
                  - Content
                  - For
                  - Space
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                summary: Get content for space
                description: >-
                  Deprecated, use [Confluence's v2
                  API](https://developer.atlassian.com/cloud/confluence/rest/v2/intro/).


                  Returns all content in a space. The returned content is
                  grouped by type

                  (pages then blogposts), then ordered by content ID in
                  ascending order.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'View' permission for the space. Note, the returned list will
                  only

                  contain content that the current user has permission to view.
            /wiki/rest/api/space/{spaceKey}/permission:
              post:
                tags:
                  - Add
                  - New
                  - Permission
                  - To
                  - Space
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                summary: Add new permission to space
                description: >-
                  Adds new permission to space.


                  If the permission to be added is a group permission, the group
                  can be identified

                  by its group name or group id.


                  Note: Apps cannot access this REST resource - including when
                  utilizing user impersonation.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Admin' permission for the space.
            /wiki/rest/api/space/{spaceKey}/permission/custom-content:
              post:
                tags:
                  - Add
                  - New
                  - Custom
                  - Content
                  - Permission
                  - To
                  - Space
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                summary: Add new custom content permission to space
                description: >-
                  Adds new custom content permission to space.


                  If the permission to be added is a group permission, the group
                  can be identified

                  by its group name or group id.


                  Note: Only apps can access this REST resource and only make
                  changes to the respective app permissions.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Admin' permission for the space.
            /wiki/rest/api/space/{spaceKey}/permission/{id}:
              delete:
                tags:
                  - Removes
                  - Space
                  - Permission
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                summary: Remove a space permission
                description: >-
                  Removes a space permission. Note that removing Read Space
                  permission for a user or group will remove all

                  the space permissions for that user or group.


                  Note: Apps cannot access this REST resource - including when
                  utilizing user impersonation.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Admin' permission for the space.
            /wiki/rest/api/space/{spaceKey}/content/{type}:
              get:
                tags:
                  - Get
                  - Content
                  - By
                  - Types
                  - For
                  - Space
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                summary: Get content by type for space
                description: >-
                  Deprecated, use [Confluence's v2
                  API](https://developer.atlassian.com/cloud/confluence/rest/v2/intro/).


                  Returns all content of a given type, in a space. The returned
                  content is

                  ordered by content ID in ascending order.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'View' permission for the space. Note, the returned list will
                  only

                  contain content that the current user has permission to view.
            /wiki/rest/api/space/{spaceKey}/property:
              get:
                tags:
                  - Get
                  - Space
                  - Properties
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                summary: Get space properties
                description: >-
                  Deprecated, use [Confluence's v2
                  API](https://developer.atlassian.com/cloud/confluence/rest/v2/intro/).


                  Returns all properties for the given space. Space properties
                  are a key-value storage associated with a space.


                  **[Permissions
                  required](https://confluence.atlassian.com/x/_AozKw)**: ‘View’
                  permission for the space.
              post:
                tags:
                  - Create
                  - Space
                  - Properties
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                summary: Create space property
                description: >-
                  Deprecated, use [Confluence's v2
                  API](https://developer.atlassian.com/cloud/confluence/rest/v2/intro/).


                  Creates a new space property.


                  **[Permissions
                  required](https://confluence.atlassian.com/x/_AozKw)**:

                  ‘Admin’ permission for the space.
            /wiki/rest/api/space/{spaceKey}/property/{key}:
              get:
                tags:
                  - Get
                  - Space
                  - Properties
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                summary: Get space property
                description: >-
                  Deprecated, use [Confluence's v2
                  API](https://developer.atlassian.com/cloud/confluence/rest/v2/intro/).


                  Returns a space property.


                  **[Permissions
                  required](https://confluence.atlassian.com/x/_AozKw)**: ‘View’
                  permission for the space.
              put:
                tags:
                  - Update
                  - Space
                  - Properties
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                summary: Update space property
                description: >-
                  Deprecated, use [Confluence's v2
                  API](https://developer.atlassian.com/cloud/confluence/rest/v2/intro/).


                  Updates a space property. Note, you cannot update the key of a
                  space

                  property, only the value.


                  **[Permissions
                  required](https://confluence.atlassian.com/x/_AozKw)**:

                  ‘Admin’ permission for the space.
              post:
                tags:
                  - Create
                  - Space
                  - Properties
                  - For
                  - Keys
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                summary: Create space property for key
                description: >-
                  Deprecated, use [Confluence's v2
                  API](https://developer.atlassian.com/cloud/confluence/rest/v2/intro/).


                  Creates a new space property. This is the same as `POST

                  /wiki/rest/api/space/{spaceKey}/property` but the key for the
                  property is passed as a

                  path parameter, rather than in the request body.


                  **[Permissions
                  required](https://confluence.atlassian.com/x/_AozKw)**:

                  ‘Admin’ permission for the space.
              delete:
                tags:
                  - Delete
                  - Space
                  - Properties
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                summary: Delete space property
                description: >-
                  Deprecated, use [Confluence's v2
                  API](https://developer.atlassian.com/cloud/confluence/rest/v2/intro/).


                  Deletes a space property.


                  **[Permissions
                  required](https://confluence.atlassian.com/x/_AozKw)**:

                  ‘Admin’ permission for the space.
            /wiki/rest/api/space/{spaceKey}/settings:
              get:
                tags:
                  - Get
                  - Space
                  - Settings
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                summary: Get space settings
                description: >-
                  Returns the settings of a space. Currently only the

                  `routeOverrideEnabled` setting can be returned.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'View' permission for the space.
              put:
                tags:
                  - Update
                  - Space
                  - Settings
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                summary: Update space settings
                description: >-
                  Updates the settings for a space. Currently only the

                  `routeOverrideEnabled` setting can be updated.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Admin' permission for the space.
            /wiki/rest/api/space/{spaceKey}/state:
              get:
                tags:
                  - Get
                  - Space
                  - Suggested
                  - Content
                  - States
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                summary: Get space suggested content states
                description: >-
                  Get content states that are suggested in the space.

                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Space view permission
            /wiki/rest/api/space/{spaceKey}/state/settings:
              get:
                tags:
                  - Get
                  - Content
                  - States
                  - Settings
                  - For
                  - Space
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                summary: Get content state settings for space
                description: >-
                  Get object describing whether content states are allowed at
                  all, if custom content states or space content states

                  are restricted, and a list of space content states allowed for
                  the space if they are not restricted.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Space admin permission
            /wiki/rest/api/space/{spaceKey}/state/content:
              get:
                tags:
                  - Get
                  - Content
                  - In
                  - Space
                  - With
                  - Given
                  - States
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                summary: Get content in space with given content state
                description: >-
                  Finds paginated content with 


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Space View Permission
            /wiki/rest/api/space/{spaceKey}/theme:
              get:
                tags:
                  - Get
                  - Space
                  - Theme
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                summary: Get space theme
                description: >-
                  Returns the theme selected for a space, if one is set. If no
                  space

                  theme is set, this means that the space is inheriting the
                  global look

                  and feel settings.


                  **[Permissions
                  required](https://confluence.atlassian.com/x/_AozKw)**: ‘View’
                  permission for the space.
              put:
                tags:
                  - Sets
                  - Space
                  - Theme
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                summary: Set space theme
                description: >-
                  Sets the theme for a space. Note, if you want to reset the
                  space theme to

                  the default Confluence theme, use the 'Reset space theme'
                  method instead

                  of this method.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Admin' permission for the space.
              delete:
                tags:
                  - Reset
                  - Space
                  - Theme
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                summary: Reset space theme
                description: >-
                  Resets the space theme. This means that the space will inherit
                  the

                  global look and feel settings


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Admin' permission for the space.
            /wiki/rest/api/space/{spaceKey}/watch:
              get:
                tags:
                  - Get
                  - Space
                  - Watchers
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                summary: Get space watchers
                description: Returns a list of watchers of a space
            /wiki/rest/api/space/{spaceKey}/label:
              get:
                tags:
                  - Get
                  - Space
                  - Labels
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                summary: Get Space Labels
                description: >-
                  Returns a list of labels associated with a space. Can provide
                  a prefix as well as other filters to

                  select different types of labels.
              post:
                tags:
                  - Add
                  - Labels
                  - To
                  - Space
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                summary: Add labels to a space
                description: >-
                  Adds labels to a piece of content. Does not modify the
                  existing labels.


                  Notes:


                  - Labels can also be added when creating content ([Create
                  content](#api-content-post)).

                  - Labels can be updated when updating content ([Update
                  content](#api-content-id-put)).

                  This will delete the existing labels and replace them with the
                  labels in

                  the request.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to update the content.
              delete:
                tags:
                  - Removes
                  - Labels
                  - From
                  - Space
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                summary: Remove label from a space
                description: ''
            /wiki/rest/api/template:
              put:
                tags:
                  - Update
                  - Content
                  - Templates
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                summary: Update content template
                description: >-
                  Updates a content template. Note, blueprint templates cannot
                  be updated

                  via the REST API.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Admin' permission for the space to update a space template or
                  'Confluence Administrator'

                  global permission to update a global template.
              post:
                tags:
                  - Create
                  - Content
                  - Templates
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                summary: Create content template
                description: >-
                  Creates a new content template. Note, blueprint templates
                  cannot be created via the REST API.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Admin' permission for the space to create a space template or
                  'Confluence Administrator'

                  global permission to create a global template.
            /wiki/rest/api/template/blueprint:
              get:
                tags:
                  - Get
                  - Blueprints
                  - Templates
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                  - Blueprints
                summary: Get blueprint templates
                description: >-
                  Returns all templates provided by blueprints. Use this method
                  to retrieve

                  all global blueprint templates or all blueprint templates in a
                  space.


                  Note, all global blueprints are inherited by each space. Space
                  blueprints

                  can be customised without affecting the global blueprints.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'View' permission for the space to view blueprints for the
                  space and permission

                  to access the Confluence site ('Can use' global permission) to
                  view global blueprints.
            /wiki/rest/api/template/page:
              get:
                tags:
                  - Get
                  - Content
                  - Templates
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                  - Blueprints
                  - Page
                summary: Get content templates
                description: >-
                  Returns all content templates. Use this method to retrieve all
                  global

                  content templates or all content templates in a space.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'View' permission for the space to view space templates and
                  permission to

                  access the Confluence site ('Can use' global permission) to
                  view global templates.
            /wiki/rest/api/template/{contentTemplateId}:
              get:
                tags:
                  - Get
                  - Content
                  - Templates
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                  - Blueprints
                  - Page
                summary: Get content template
                description: >-
                  Returns a content template. This includes information about
                  template,

                  like the name, the space or blueprint that the template is in,
                  the body

                  of the template, and more.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'View' permission for the space to view space templates and
                  permission to

                  access the Confluence site ('Can use' global permission) to
                  view global templates.
              delete:
                tags:
                  - Removes
                  - Templates
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                  - Blueprints
                  - Page
                summary: Remove template
                description: >-
                  Deletes a template. This results in different actions
                  depending on the

                  type of template:


                  - If the template is a content template, it is deleted.

                  - If the template is a modified space-level blueprint
                  template, it reverts

                  to the template inherited from the global-level blueprint
                  template.

                  - If the template is a modified global-level blueprint
                  template, it reverts

                  to the default global-level blueprint template.

                   Note, unmodified blueprint templates cannot be deleted.

                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:
                          'Admin' permission for the space to delete a space template or 'Confluence Administrator'
                          global permission to delete a global template.
            /wiki/rest/api/user:
              get:
                tags:
                  - Get
                  - Users
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                  - Blueprints
                  - Page
                summary: Get user
                description: >-
                  Returns a user. This includes information about the user, such
                  as the

                  display name, account ID, profile picture, and more. The
                  information returned may be

                  restricted by the user's profile visibility settings.


                  **Note:** to add, edit, or delete users in your organization,
                  see the

                  [user management REST
                  API](/cloud/admin/user-management/about/).


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission).
            /wiki/rest/api/user/anonymous:
              get:
                tags:
                  - Get
                  - Anonymous
                  - Users
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                  - Blueprints
                  - Page
                  - Anonymous
                summary: Get anonymous user
                description: >-
                  Returns information about how anonymous users are represented,
                  like the

                  profile picture and display name.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission).
            /wiki/rest/api/user/current:
              get:
                tags:
                  - Get
                  - Current
                  - Users
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                  - Blueprints
                  - Page
                  - Anonymous
                  - Current
                summary: Get current user
                description: >-
                  Returns the currently logged-in user. This includes
                  information about

                  the user, like the display name, userKey, account ID, profile
                  picture,

                  and more.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission).
            /wiki/rest/api/user/memberof:
              get:
                tags:
                  - Get
                  - Group
                  - Memberships
                  - For
                  - Users
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                  - Blueprints
                  - Page
                  - Anonymous
                  - Current
                  - Members
                summary: Get group memberships for user
                description: >-
                  Returns the groups that a user is a member of.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission).
            /wiki/rest/api/user/bulk:
              get:
                tags:
                  - Get
                  - Multiple
                  - Users
                  - Using
                  - Ids
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                  - Blueprints
                  - Page
                  - Anonymous
                  - Current
                  - Members
                  - Bulk
                summary: Get multiple users using ids
                description: >-
                  Returns user details for the ids provided in request.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission).
            /wiki/rest/api/user/watch/content/{contentId}:
              get:
                tags:
                  - Get
                  - Content
                  - Watch
                  - Status
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                  - Blueprints
                  - Page
                  - Anonymous
                  - Current
                  - Members
                  - Bulk
                summary: Get content watch status
                description: >-
                  Returns whether a user is watching a piece of content. Choose
                  the user by

                  doing one of the following:


                  - Specify a user via a query parameter: Use the `accountId` to
                  identify the user.

                  - Do not specify a user: The currently logged-in user will be
                  used.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Confluence Administrator' global permission if specifying a
                  user, otherwise

                  permission to access the Confluence site ('Can use' global
                  permission).
              post:
                tags:
                  - Add
                  - Content
                  - Watchers
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                  - Blueprints
                  - Page
                  - Anonymous
                  - Current
                  - Members
                  - Bulk
                summary: Add content watcher
                description: >-
                  Adds a user as a watcher to a piece of content. Choose the
                  user by doing

                  one of the following:


                  - Specify a user via a query parameter: Use the `accountId` to
                  identify the user.

                  - Do not specify a user: The currently logged-in user will be
                  used.


                  Note, you must add the `X-Atlassian-Token: no-check` header
                  when making a

                  request, as this operation has XSRF protection.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Confluence Administrator' global permission if specifying a
                  user, otherwise

                  permission to access the Confluence site ('Can use' global
                  permission).
              delete:
                tags:
                  - Removes
                  - Content
                  - Watchers
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                  - Blueprints
                  - Page
                  - Anonymous
                  - Current
                  - Members
                  - Bulk
                summary: Remove content watcher
                description: >-
                  Removes a user as a watcher from a piece of content. Choose
                  the user by

                  doing one of the following:


                  - Specify a user via a query parameter: Use the `accountId` to
                  identify the user.

                  - Do not specify a user: The currently logged-in user will be
                  used.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Confluence Administrator' global permission if specifying a
                  user, otherwise

                  permission to access the Confluence site ('Can use' global
                  permission).
            /wiki/rest/api/user/watch/label/{labelName}:
              get:
                tags:
                  - Get
                  - Labels
                  - Watch
                  - Status
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                  - Blueprints
                  - Page
                  - Anonymous
                  - Current
                  - Members
                  - Bulk
                summary: Get label watch status
                description: >-
                  Returns whether a user is watching a label. Choose the user by
                  doing one

                  of the following:


                  - Specify a user via a query parameter: Use the `accountId` to
                  identify the user.

                  - Do not specify a user: The currently logged-in user will be
                  used.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Confluence Administrator' global permission if specifying a
                  user, otherwise

                  permission to access the Confluence site ('Can use' global
                  permission).
              post:
                tags:
                  - Add
                  - Labels
                  - Watchers
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                  - Blueprints
                  - Page
                  - Anonymous
                  - Current
                  - Members
                  - Bulk
                summary: Add label watcher
                description: >-
                  Adds a user as a watcher to a label. Choose the user by doing
                  one of the

                  following:


                  - Specify a user via a query parameter: Use the `accountId` to
                  identify the user.

                  - Do not specify a user: The currently logged-in user will be
                  used.


                  Note, you must add the `X-Atlassian-Token: no-check` header
                  when making a

                  request, as this operation has XSRF protection.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Confluence Administrator' global permission if specifying a
                  user, otherwise

                  permission to access the Confluence site ('Can use' global
                  permission).
              delete:
                tags:
                  - Removes
                  - Labels
                  - Watchers
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                  - Blueprints
                  - Page
                  - Anonymous
                  - Current
                  - Members
                  - Bulk
                summary: Remove label watcher
                description: >-
                  Removes a user as a watcher from a label. Choose the user by
                  doing one of

                  the following:


                  - Specify a user via a query parameter: Use the `accountId` to
                  identify the user.

                  - Do not specify a user: The currently logged-in user will be
                  used.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Confluence Administrator' global permission if specifying a
                  user, otherwise

                  permission to access the Confluence site ('Can use' global
                  permission).
            /wiki/rest/api/user/watch/space/{spaceKey}:
              get:
                tags:
                  - Get
                  - Space
                  - Watch
                  - Status
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                  - Blueprints
                  - Page
                  - Anonymous
                  - Current
                  - Members
                  - Bulk
                summary: Get space watch status
                description: >-
                  Returns whether a user is watching a space. Choose the user by

                  doing one of the following:


                  - Specify a user via a query parameter: Use the `accountId` to
                  identify the user.

                  - Do not specify a user: The currently logged-in user will be
                  used.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Confluence Administrator' global permission if specifying a
                  user, otherwise

                  permission to access the Confluence site ('Can use' global
                  permission).
              post:
                tags:
                  - Add
                  - Space
                  - Watchers
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                  - Blueprints
                  - Page
                  - Anonymous
                  - Current
                  - Members
                  - Bulk
                summary: Add space watcher
                description: >-
                  Adds a user as a watcher to a space. Choose the user by doing
                  one of the

                  following:


                  - Specify a user via a query parameter: Use the `accountId` to
                  identify the user.

                  - Do not specify a user: The currently logged-in user will be
                  used.


                  Note, you must add the `X-Atlassian-Token: no-check` header
                  when making a

                  request, as this operation has XSRF protection.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Confluence Administrator' global permission if specifying a
                  user, otherwise

                  permission to access the Confluence site ('Can use' global
                  permission).
              delete:
                tags:
                  - Removes
                  - Space
                  - Watch
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                  - Blueprints
                  - Page
                  - Anonymous
                  - Current
                  - Members
                  - Bulk
                summary: Remove space watch
                description: >-
                  Removes a user as a watcher from a space. Choose the user by
                  doing one of

                  the following:


                  - Specify a user via a query parameter: Use the `accountId` to
                  identify the user.

                  - Do not specify a user: The currently logged-in user will be
                  used.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Confluence Administrator' global permission if specifying a
                  user, otherwise

                  permission to access the Confluence site ('Can use' global
                  permission).
            /wiki/rest/api/user/email:
              get:
                tags:
                  - Get
                  - Users
                  - Email
                  - Addresses
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                  - Blueprints
                  - Page
                  - Anonymous
                  - Current
                  - Members
                  - Bulk
                  - Email
                summary: Get user email address
                description: >-
                  Returns a user's email address. This API is only available to
                  apps approved by

                  Atlassian, according to these
                  [guidelines](https://community.developer.atlassian.com/t/guidelines-for-requesting-access-to-email-address/27603).


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission).
            /wiki/rest/api/user/email/bulk:
              get:
                tags:
                  - Get
                  - Users
                  - Email
                  - Addresses
                  - In
                  - Batches
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                  - Blueprints
                  - Page
                  - Anonymous
                  - Current
                  - Members
                  - Bulk
                  - Email
                summary: Get user email addresses in batch
                description: >-
                  Returns user email addresses for a set of accountIds. This API
                  is only available to apps approved by

                  Atlassian, according to these
                  [guidelines](https://community.developer.atlassian.com/t/guidelines-for-requesting-access-to-email-address/27603).


                  Any accounts which are not available will not be included in
                  the result.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission).
            /atlassian-connect/1/app/module/dynamic:
              get:
                tags:
                  - Get
                  - Modules
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                  - Blueprints
                  - Page
                  - Anonymous
                  - Current
                  - Members
                  - Bulk
                  - Email
                  - Atlassian
                  - Connect
                  - Applications
                  - Modules
                  - Dynamic
                summary: Get modules
                description: >-
                  Returns all modules registered dynamically by the calling app.


                  **[Permissions](#permissions) required:** Only Connect apps
                  can make this request.
              post:
                tags:
                  - Register
                  - Modules
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                  - Blueprints
                  - Page
                  - Anonymous
                  - Current
                  - Members
                  - Bulk
                  - Email
                  - Atlassian
                  - Connect
                  - Applications
                  - Modules
                  - Dynamic
                summary: Register modules
                description: >-
                  Registers a list of modules. For the list of modules that
                  support dynamic registration, see [Dynamic
                  modules](https://developer.atlassian.com/cloud/confluence/dynamic-modules/).


                  **[Permissions](#permissions) required:** Only Connect apps
                  can make this request.
              delete:
                tags:
                  - Removes
                  - Modules
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                  - Blueprints
                  - Page
                  - Anonymous
                  - Current
                  - Members
                  - Bulk
                  - Email
                  - Atlassian
                  - Connect
                  - Applications
                  - Modules
                  - Dynamic
                summary: Remove modules
                description: >-
                  Remove all or a list of modules registered by the calling app.


                  **[Permissions](#permissions) required:** Only Connect apps
                  can make this request.
            /wiki/rest/api/analytics/content/{contentId}/views:
              get:
                tags:
                  - Get
                  - Views
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                  - Blueprints
                  - Page
                  - Anonymous
                  - Current
                  - Members
                  - Bulk
                  - Email
                  - Atlassian
                  - Connect
                  - Applications
                  - Modules
                  - Dynamic
                  - Views
                summary: Get views
                description: Get the total number of views a piece of content has.
            /wiki/rest/api/analytics/content/{contentId}/viewers:
              get:
                tags:
                  - Get
                  - Viewers
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                  - Blueprints
                  - Page
                  - Anonymous
                  - Current
                  - Members
                  - Bulk
                  - Email
                  - Atlassian
                  - Connect
                  - Applications
                  - Modules
                  - Dynamic
                  - Views
                  - Viewers
                summary: Get viewers
                description: >-
                  Get the total number of distinct viewers a piece of content
                  has.
            /wiki/rest/api/user/{userId}/property:
              get:
                tags:
                  - Get
                  - Users
                  - Properties
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                  - Blueprints
                  - Page
                  - Anonymous
                  - Current
                  - Members
                  - Bulk
                  - Email
                  - Atlassian
                  - Connect
                  - Applications
                  - Modules
                  - Dynamic
                  - Views
                  - Viewers
                summary: Get user properties
                description: >-
                  Returns the properties for a user as list of property keys.
                  For more information

                  about user properties, see [Confluence entity
                  properties](https://developer.atlassian.com/cloud/confluence/confluence-entity-properties/).

                  `Note`, these properties stored against a user are on a
                  Confluence site level and not space/content level.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission).
            /wiki/rest/api/user/{userId}/property/{key}:
              get:
                tags:
                  - Get
                  - Users
                  - Properties
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                  - Blueprints
                  - Page
                  - Anonymous
                  - Current
                  - Members
                  - Bulk
                  - Email
                  - Atlassian
                  - Connect
                  - Applications
                  - Modules
                  - Dynamic
                  - Views
                  - Viewers
                summary: Get user property
                description: >-
                  Returns the property corresponding to `key` for a user. For
                  more information

                  about user properties, see [Confluence entity
                  properties](https://developer.atlassian.com/cloud/confluence/confluence-entity-properties/).

                  `Note`, these properties stored against a user are on a
                  Confluence site level and not space/content level.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission).
              put:
                tags:
                  - Update
                  - Users
                  - Properties
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                  - Blueprints
                  - Page
                  - Anonymous
                  - Current
                  - Members
                  - Bulk
                  - Email
                  - Atlassian
                  - Connect
                  - Applications
                  - Modules
                  - Dynamic
                  - Views
                  - Viewers
                summary: Update user property
                description: >-
                  Updates a property for the given user. Note, you cannot update
                  the key of a user property, only the value.

                  For more information about user properties, see

                  [Confluence entity
                  properties](https://developer.atlassian.com/cloud/confluence/confluence-entity-properties/).

                  `Note`, these properties stored against a user are on a
                  Confluence site level and not space/content level.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission).
              post:
                tags:
                  - Create
                  - Users
                  - Properties
                  - By
                  - Keys
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                  - Blueprints
                  - Page
                  - Anonymous
                  - Current
                  - Members
                  - Bulk
                  - Email
                  - Atlassian
                  - Connect
                  - Applications
                  - Modules
                  - Dynamic
                  - Views
                  - Viewers
                summary: Create user property by key
                description: >-
                  Creates a property for a user. For more information  about
                  user properties, see [Confluence entity properties]

                  (https://developer.atlassian.com/cloud/confluence/confluence-entity-properties/).

                  `Note`, these properties stored against a user are on a
                  Confluence site level and not space/content level.


                  `Note:` the number of properties which could be created per
                  app in a tenant for each user might be

                  restricted by fixed system limits.

                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission).
              delete:
                tags:
                  - Delete
                  - Users
                  - Properties
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                  - Blueprints
                  - Page
                  - Anonymous
                  - Current
                  - Members
                  - Bulk
                  - Email
                  - Atlassian
                  - Connect
                  - Applications
                  - Modules
                  - Dynamic
                  - Views
                  - Viewers
                summary: Delete user property
                description: >-
                  Deletes a property for the given user.

                  For more information about user properties, see

                  [Confluence entity
                  properties](https://developer.atlassian.com/cloud/confluence/confluence-entity-properties/).

                  `Note`, these properties stored against a user are on a
                  Confluence site level and not space/content level.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission).
          x-atlassian-narrative:
            documents:
              - title: About
                anchor: about
                body: >-
                  This is the reference for the Confluence Cloud REST API. This
                  API is the primary way to get and

                  modify data in Confluence Cloud, whether you are developing an
                  app or any other integration.

                  Use it to interact with Confluence entities, like pages and
                  blog posts, spaces, users, groups,

                  and more.
              - title: Authentication and authorization
                anchor: auth
                body: >-
                  **Authentication:** If you are building a Cloud app,
                  authentication is implemented via JWT or OAuth 2.0, depending
                  on what you are building (see [Security
                  overview](https://developer.atlassian.com/cloud/confluence/security-overview/)).
                  Otherwise, if you are authenticating directly against the REST
                  API, the REST API supports basic auth (see [Basic auth for
                  REST
                  APIs](https://developer.atlassian.com/cloud/confluence/basic-auth-for-rest-apis/)).


                  **Authorization:** If you are building a Cloud app,
                  authorization can be implemented by
                  [scopes](https://developer.atlassian.com/cloud/confluence/scopes/)
                  or by [OAuth 2.0 user
                  impersonation](https://developer.atlassian.com/cloud/confluence/oauth-2-jwt-bearer-tokens-for-apps).
                  Otherwise, if you are making calls directly against the REST
                  API, authorization is based on the user used in the
                  authentication process.


                  See [Security
                  overview](https://developer.atlassian.com/cloud/confluence/security-overview/)
                  for more details on authentication and authorization.
              - title: Status codes
                anchor: status-code
                body: >-
                  The Confluence REST API uses the [standard HTTP status
                  codes](https://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html).


                  Responses that return an error status code will also return a
                  response body, similar to the following:

                  ```json

                  {
                    "statusCode": 404,
                    "data": {
                      "authorized": false,
                      "valid": false,
                      "errors": [
                        {
                          "message": {
                            "translation": "This is an example error message.",
                            "args": []
                          }
                        }
                      ],
                      "successful": false
                    },
                    "message": "This is an example error message."
                  }

                  ```
              - title: Using the REST API
                anchor: using
                body: >-
                  **Expansion:** The Confluence REST API uses resource
                  expansion: some parts of a resource are not returned unless
                  explicitly specified. This simplifies responses and minimizes
                  network traffic.


                  To expand part of a resource in a request, use the `expand`
                  query parameter and specify the entities to be expanded. If
                  you need to expand nested entities, use the `.` dot notation.
                  For example, the following request will expand information
                  about the requested content's space and labels:

                  ```

                  GET /wiki/rest/api/content/{id}?expand=space,metadata.labels

                  ```

                  **Pagination:** The Confluence REST API uses pagination: a
                  method that returns a response with multiple objects can only
                  return a limited number at one time. This limits the size of
                  responses and conserves server resources.


                  Use the 'limit' and 'start' query parameters to specify
                  pagination:


                  - `limit` is the number of objects to return per page. This
                  may be restricted by system limits.

                  - `start` is the index of the first item returned in the page
                  of results. The base index is 0.


                  For example, the following request will return ten content
                  objects, starting from the fifth object.

                  ```

                  GET /wiki/rest/api/content?start=4&limit=10

                  ```

                  **Special headers:**


                  - `X-Atlassian-Token: no-check` request header must be
                  specified for methods

                  that are protected from Cross Site Request Forgery (XSRF/CSRF)
                  attacks. This is

                  stated in the method description, if required. For more
                  information, see this

                  [KB
                  article](https://confluence.atlassian.com/cloudkb/xsrf-check-failed-when-calling-cloud-apis-826874382.html).
              - title: Capabilities
                anchor: capabilities
                body: >-
                  **Webhooks:** A webhook is a user-defined callback over HTTP.
                  You can use Confluence webhooks to notify your app or web
                  application when certain events occur in Confluence. For
                  example, when a page is created or updated. To learn more, see
                  [Webhooks](https://developer.atlassian.com/cloud/confluence/modules/webhook/).


                  **Content properties:** Content properties are a key-value
                  storage associated with a piece of Confluence content. If you
                  are building an app, this is one form of persistence that you
                  can use. You can use the Confluence REST API to get, update,
                  and delete content properties. To learn more, see [Content
                  properties in the REST
                  API](https://developer.atlassian.com/cloud/confluence/content-properties/).


                  **CQL:** The Confluence Query Language (CQL) allows you to
                  perform complex searches for content using an SQL-like syntax
                  in the `search` resource. To learn more, see [Advanced
                  searching using
                  CQL](https://developer.atlassian.com/cloud/confluence/advanced-
      - type: Postman Collection
        url: >-
          https://developer.atlassian.com/cloud/confluence/confcloud.1.postman.json
      - type: Authentication
        url: https://developer.atlassian.com/cloud/confluence/rest/v1/intro/#auth
      - type: Status Codes
        url: >-
          https://developer.atlassian.com/cloud/confluence/rest/v1/intro/#status-code
      - type: Capabilities
        url: >-
          https://developer.atlassian.com/cloud/confluence/rest/v1/intro/#capabilities
    overlays:
      - type: APIs.io Search
        url: >-
          overlays/https://dac-static.atlassian.com/cloud/confluence/swagger.v3.json?_v=1.6660.0-0.1294.0-openapi-search.yml
      - type: APIs.io Search
        url: overlays/confluence-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/confluence-openapi-api-evangelist-ratings.yml
    aid: atlassian:confluence-api
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---