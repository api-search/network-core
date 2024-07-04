---
name: Collaboration
description: Needs a description.
image: >-
  https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/collaboration.png
url: https://example.com/apis/collaboration.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Collaboration
apis:
  - name: cleanrooms
    description: >-
      <p>Welcome to the <i>Clean Rooms API Reference</i>.</p> <p>Clean Rooms is
      an Amazon Web Services service that helps multiple parties to join their
      data together in a secure collaboration workspace. In the collaboration,
      members who can query and receive results can get insights into the
      collective datasets without either party getting access to the other
      party's raw data.</p> <p>To learn more about Clean Rooms concepts,
      procedures, and best practices, see the <a
      href="https://docs.aws.amazon.com/clean-rooms/latest/userguide/what-is.html">Clean
      Rooms User Guide</a>.</p> <p>To learn more about SQL commands, functions,
      and conditions supported in Clean Rooms, see the <a
      href="https://docs.aws.amazon.com/clean-rooms/latest/sql-reference/sql-reference.html">Clean
      Rooms SQL Reference</a>.</p>
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
            title: cleanrooms
          paths:
            /collaborations/{collaborationIdentifier}/batch-analysistemplates:
              POST:
                summary: BatchGetCollaborationAnalysisTemplate
                description: >-
                  <p>Retrieves multiple analysis templates within a
                  collaboration by their Amazon Resource Names (ARNs).</p>
                tags:
                  - Batches
                  - Get
                  - Collaboration
                  - Analysis
                  - Templates
                  - Identifiers
                  - Batches
                  - Analysis Templates
            /collaborations/{collaborationIdentifier}/batch-schema:
              POST:
                summary: BatchGetSchema
                description: <p>Retrieves multiple schemas by their identifiers.</p>
                tags:
                  - Batches
                  - Get
                  - Schemas
                  - Identifiers
                  - Batches
                  - Analysis Templates
                  - Schemas
            /memberships/{membershipIdentifier}/analysistemplates:
              GET:
                summary: ListAnalysisTemplates
                description: <p>Lists analysis templates that the caller owns.</p>
                tags:
                  - Lists
                  - Analysis
                  - Templates
                  - Identifiers
                  - Batches
                  - Analysis Templates
                  - Schemas
            /collaborations:
              GET:
                summary: ListCollaborations
                description: >-
                  <p>Lists collaborations the caller owns, is active in, or has
                  been invited to.</p>
                tags:
                  - Lists
                  - Collaborations
                  - Identifiers
                  - Batches
                  - Analysis Templates
                  - Schemas
                  - Collaborations
            /memberships/{membershipIdentifier}/configuredaudiencemodelassociations:
              GET:
                summary: ListConfiguredAudienceModelAssociations
                description: >-
                  <p>Lists information about requested configured audience model
                  associations.</p>
                tags:
                  - Lists
                  - Configured
                  - Audience
                  - Models
                  - Associations
                  - Identifiers
                  - Batches
                  - Analysis Templates
                  - Schemas
                  - Collaborations
                  - Configuration Audience Model Associations
            /configuredTables:
              GET:
                summary: ListConfiguredTables
                description: <p>Lists configured tables.</p>
                tags:
                  - Lists
                  - Configured
                  - Tables
                  - Identifiers
                  - Batches
                  - Analysis Templates
                  - Schemas
                  - Collaborations
                  - Configuration Audience Model Associations
                  - Tables
            /configuredTables/{configuredTableIdentifier}/analysisRule:
              POST:
                summary: CreateConfiguredTableAnalysisRule
                description: >-
                  <p>Creates a new analysis rule for a configured table.
                  Currently, only one analysis rule can be created for a given
                  configured table.</p>
                tags:
                  - Create
                  - Configured
                  - Tables
                  - Analysis
                  - Rules
                  - Identifiers
                  - Batches
                  - Analysis Templates
                  - Schemas
                  - Collaborations
                  - Configuration Audience Model Associations
                  - Tables
                  - Configured
                  - Tables
                  - Analysis
                  - Rules
            /memberships/{membershipIdentifier}/configuredTableAssociations:
              GET:
                summary: ListConfiguredTableAssociations
                description: <p>Lists configured table associations for a membership.</p>
                tags:
                  - Lists
                  - Configured
                  - Tables
                  - Associations
                  - Identifiers
                  - Batches
                  - Analysis Templates
                  - Schemas
                  - Collaborations
                  - Configuration Audience Model Associations
                  - Tables
                  - Configured
                  - Tables
                  - Analysis
                  - Rules
                  - Associations
            /memberships:
              GET:
                summary: ListMemberships
                description: >-
                  <p>Lists all memberships resources within the caller's
                  account.</p>
                tags:
                  - Lists
                  - Memberships
                  - Identifiers
                  - Batches
                  - Analysis Templates
                  - Schemas
                  - Collaborations
                  - Configuration Audience Model Associations
                  - Tables
                  - Configured
                  - Tables
                  - Analysis
                  - Rules
                  - Associations
                  - Memberships
            /memberships/{membershipIdentifier}/privacybudgettemplates:
              GET:
                summary: ListPrivacyBudgetTemplates
                description: >-
                  <p>Returns detailed information about the privacy budget
                  templates in a specified membership.</p>
                tags:
                  - Lists
                  - Privacy
                  - Budgets
                  - Templates
                  - Identifiers
                  - Batches
                  - Analysis Templates
                  - Schemas
                  - Collaborations
                  - Configuration Audience Model Associations
                  - Tables
                  - Configured
                  - Tables
                  - Analysis
                  - Rules
                  - Associations
                  - Memberships
                  - Privacy Budget Templates
            /memberships/{membershipIdentifier}/analysistemplates/{analysisTemplateIdentifier}:
              PATCH:
                summary: UpdateAnalysisTemplate
                description: <p>Updates the analysis template metadata.</p>
                tags:
                  - Update
                  - Analysis
                  - Templates
                  - Identifiers
                  - Batches
                  - Analysis Templates
                  - Schemas
                  - Collaborations
                  - Configuration Audience Model Associations
                  - Tables
                  - Configured
                  - Tables
                  - Analysis
                  - Rules
                  - Associations
                  - Memberships
                  - Privacy Budget Templates
                  - Templates
            /collaborations/{collaborationIdentifier}:
              PATCH:
                summary: UpdateCollaboration
                description: >-
                  <p>Updates collaboration metadata and can only be called by
                  the collaboration owner.</p>
                tags:
                  - Update
                  - Collaboration
                  - Identifiers
                  - Batches
                  - Analysis Templates
                  - Schemas
                  - Collaborations
                  - Configuration Audience Model Associations
                  - Tables
                  - Configured
                  - Tables
                  - Analysis
                  - Rules
                  - Associations
                  - Memberships
                  - Privacy Budget Templates
                  - Templates
            /memberships/{membershipIdentifier}/configuredaudiencemodelassociations/{configuredAudienceModelAssociationIdentifier}:
              PATCH:
                summary: UpdateConfiguredAudienceModelAssociation
                description: >-
                  <p>Provides the details necessary to update a configured
                  audience model association.</p>
                tags:
                  - Update
                  - Configured
                  - Audience
                  - Models
                  - Association
                  - Identifiers
                  - Batches
                  - Analysis Templates
                  - Schemas
                  - Collaborations
                  - Configuration Audience Model Associations
                  - Tables
                  - Configured
                  - Tables
                  - Analysis
                  - Rules
                  - Associations
                  - Memberships
                  - Privacy Budget Templates
                  - Templates
                  - Audience
                  - Models
                  - Association
            /configuredTables/{configuredTableIdentifier}:
              PATCH:
                summary: UpdateConfiguredTable
                description: <p>Updates a configured table.</p>
                tags:
                  - Update
                  - Configured
                  - Tables
                  - Identifiers
                  - Batches
                  - Analysis Templates
                  - Schemas
                  - Collaborations
                  - Configuration Audience Model Associations
                  - Tables
                  - Configured
                  - Tables
                  - Analysis
                  - Rules
                  - Associations
                  - Memberships
                  - Privacy Budget Templates
                  - Templates
                  - Audience
                  - Models
                  - Association
            /configuredTables/{configuredTableIdentifier}/analysisRule/{analysisRuleType}:
              PATCH:
                summary: UpdateConfiguredTableAnalysisRule
                description: <p>Updates a configured table analysis rule.</p>
                tags:
                  - Update
                  - Configured
                  - Tables
                  - Analysis
                  - Rules
                  - Identifiers
                  - Batches
                  - Analysis Templates
                  - Schemas
                  - Collaborations
                  - Configuration Audience Model Associations
                  - Tables
                  - Configured
                  - Tables
                  - Analysis
                  - Rules
                  - Associations
                  - Memberships
                  - Privacy Budget Templates
                  - Templates
                  - Audience
                  - Models
                  - Association
                  - Types
            /memberships/{membershipIdentifier}/configuredTableAssociations/{configuredTableAssociationIdentifier}:
              PATCH:
                summary: UpdateConfiguredTableAssociation
                description: <p>Updates a configured table association.</p>
                tags:
                  - Update
                  - Configured
                  - Tables
                  - Association
                  - Identifiers
                  - Batches
                  - Analysis Templates
                  - Schemas
                  - Collaborations
                  - Configuration Audience Model Associations
                  - Tables
                  - Configured
                  - Tables
                  - Analysis
                  - Rules
                  - Associations
                  - Memberships
                  - Privacy Budget Templates
                  - Templates
                  - Audience
                  - Models
                  - Association
                  - Types
            /collaborations/{collaborationIdentifier}/member/{accountId}:
              DELETE:
                summary: DeleteMember
                description: >-
                  <p>Removes the specified member from a collaboration. The
                  removed member is placed in the Removed status and can't
                  interact with the collaboration. The removed member's data is
                  inaccessible to active members of the collaboration.</p>
                tags:
                  - Delete
                  - Members
                  - Identifiers
                  - Batches
                  - Analysis Templates
                  - Schemas
                  - Collaborations
                  - Configuration Audience Model Associations
                  - Tables
                  - Configured
                  - Tables
                  - Analysis
                  - Rules
                  - Associations
                  - Memberships
                  - Privacy Budget Templates
                  - Templates
                  - Audience
                  - Models
                  - Association
                  - Types
                  - Members
                  - Account
                  - Identifiers
            /memberships/{membershipIdentifier}:
              PATCH:
                summary: UpdateMembership
                description: <p>Updates a membership.</p>
                tags:
                  - Update
                  - Membership
                  - Identifiers
                  - Batches
                  - Analysis Templates
                  - Schemas
                  - Collaborations
                  - Configuration Audience Model Associations
                  - Tables
                  - Configured
                  - Tables
                  - Analysis
                  - Rules
                  - Associations
                  - Memberships
                  - Privacy Budget Templates
                  - Templates
                  - Audience
                  - Models
                  - Association
                  - Types
                  - Members
                  - Account
                  - Identifiers
            /memberships/{membershipIdentifier}/privacybudgettemplates/{privacyBudgetTemplateIdentifier}:
              PATCH:
                summary: UpdatePrivacyBudgetTemplate
                description: >-
                  <p>Updates the privacy budget template for the specified
                  membership.</p>
                tags:
                  - Update
                  - Privacy
                  - Budgets
                  - Templates
                  - Identifiers
                  - Batches
                  - Analysis Templates
                  - Schemas
                  - Collaborations
                  - Configuration Audience Model Associations
                  - Tables
                  - Configured
                  - Tables
                  - Analysis
                  - Rules
                  - Associations
                  - Memberships
                  - Privacy Budget Templates
                  - Templates
                  - Audience
                  - Models
                  - Association
                  - Types
                  - Members
                  - Account
                  - Identifiers
                  - Privacy
                  - Budgets
            /collaborations/{collaborationIdentifier}/analysistemplates/{analysisTemplateArn}:
              GET:
                summary: GetCollaborationAnalysisTemplate
                description: <p>Retrieves an analysis template within a collaboration.</p>
                tags:
                  - Get
                  - Collaboration
                  - Analysis
                  - Templates
                  - Identifiers
                  - Batches
                  - Analysis Templates
                  - Schemas
                  - Collaborations
                  - Configuration Audience Model Associations
                  - Tables
                  - Configured
                  - Tables
                  - Analysis
                  - Rules
                  - Associations
                  - Memberships
                  - Privacy Budget Templates
                  - Templates
                  - Audience
                  - Models
                  - Association
                  - Types
                  - Members
                  - Account
                  - Identifiers
                  - Privacy
                  - Budgets
                  - ARN
            /collaborations/{collaborationIdentifier}/configuredaudiencemodelassociations/{configuredAudienceModelAssociationIdentifier}:
              GET:
                summary: GetCollaborationConfiguredAudienceModelAssociation
                description: >-
                  <p>Retrieves a configured audience model association within a
                  collaboration.</p>
                tags:
                  - Get
                  - Collaboration
                  - Configured
                  - Audience
                  - Models
                  - Association
                  - Identifiers
                  - Batches
                  - Analysis Templates
                  - Schemas
                  - Collaborations
                  - Configuration Audience Model Associations
                  - Tables
                  - Configured
                  - Tables
                  - Analysis
                  - Rules
                  - Associations
                  - Memberships
                  - Privacy Budget Templates
                  - Templates
                  - Audience
                  - Models
                  - Association
                  - Types
                  - Members
                  - Account
                  - Identifiers
                  - Privacy
                  - Budgets
                  - ARN
            /collaborations/{collaborationIdentifier}/privacybudgettemplates/{privacyBudgetTemplateIdentifier}:
              GET:
                summary: GetCollaborationPrivacyBudgetTemplate
                description: >-
                  <p>Returns details about a specified privacy budget
                  template.</p>
                tags:
                  - Get
                  - Collaboration
                  - Privacy
                  - Budgets
                  - Templates
                  - Identifiers
                  - Batches
                  - Analysis Templates
                  - Schemas
                  - Collaborations
                  - Configuration Audience Model Associations
                  - Tables
                  - Configured
                  - Tables
                  - Analysis
                  - Rules
                  - Associations
                  - Memberships
                  - Privacy Budget Templates
                  - Templates
                  - Audience
                  - Models
                  - Association
                  - Types
                  - Members
                  - Account
                  - Identifiers
                  - Privacy
                  - Budgets
                  - ARN
            /memberships/{membershipIdentifier}/protectedQueries/{protectedQueryIdentifier}:
              PATCH:
                summary: UpdateProtectedQuery
                description: <p>Updates the processing of a currently running query.</p>
                tags:
                  - Update
                  - Protected
                  - Queries
                  - Identifiers
                  - Batches
                  - Analysis Templates
                  - Schemas
                  - Collaborations
                  - Configuration Audience Model Associations
                  - Tables
                  - Configured
                  - Tables
                  - Analysis
                  - Rules
                  - Associations
                  - Memberships
                  - Privacy Budget Templates
                  - Templates
                  - Audience
                  - Models
                  - Association
                  - Types
                  - Members
                  - Account
                  - Identifiers
                  - Privacy
                  - Budgets
                  - ARN
                  - Protected
                  - Queries
                  - Queries
            /collaborations/{collaborationIdentifier}/schemas/{name}:
              GET:
                summary: GetSchema
                description: >-
                  <p>Retrieves the schema for a relation within a
                  collaboration.</p>
                tags:
                  - Get
                  - Schemas
                  - Identifiers
                  - Batches
                  - Analysis Templates
                  - Schemas
                  - Collaborations
                  - Configuration Audience Model Associations
                  - Tables
                  - Configured
                  - Tables
                  - Analysis
                  - Rules
                  - Associations
                  - Memberships
                  - Privacy Budget Templates
                  - Templates
                  - Audience
                  - Models
                  - Association
                  - Types
                  - Members
                  - Account
                  - Identifiers
                  - Privacy
                  - Budgets
                  - ARN
                  - Protected
                  - Queries
                  - Queries
                  - Schemas
                  - Names
            /collaborations/{collaborationIdentifier}/schemas/{name}/analysisRule/{type}:
              GET:
                summary: GetSchemaAnalysisRule
                description: <p>Retrieves a schema analysis rule.</p>
                tags:
                  - Get
                  - Schemas
                  - Analysis
                  - Rules
                  - Identifiers
                  - Batches
                  - Analysis Templates
                  - Schemas
                  - Collaborations
                  - Configuration Audience Model Associations
                  - Tables
                  - Configured
                  - Tables
                  - Analysis
                  - Rules
                  - Associations
                  - Memberships
                  - Privacy Budget Templates
                  - Templates
                  - Audience
                  - Models
                  - Association
                  - Types
                  - Members
                  - Account
                  - Identifiers
                  - Privacy
                  - Budgets
                  - ARN
                  - Protected
                  - Queries
                  - Queries
                  - Schemas
                  - Names
            /collaborations/{collaborationIdentifier}/analysistemplates:
              GET:
                summary: ListCollaborationAnalysisTemplates
                description: <p>Lists analysis templates within a collaboration.</p>
                tags:
                  - Lists
                  - Collaboration
                  - Analysis
                  - Templates
                  - Identifiers
                  - Batches
                  - Analysis Templates
                  - Schemas
                  - Collaborations
                  - Configuration Audience Model Associations
                  - Tables
                  - Configured
                  - Tables
                  - Analysis
                  - Rules
                  - Associations
                  - Memberships
                  - Privacy Budget Templates
                  - Templates
                  - Audience
                  - Models
                  - Association
                  - Types
                  - Members
                  - Account
                  - Identifiers
                  - Privacy
                  - Budgets
                  - ARN
                  - Protected
                  - Queries
                  - Queries
                  - Schemas
                  - Names
            /collaborations/{collaborationIdentifier}/configuredaudiencemodelassociations:
              GET:
                summary: ListCollaborationConfiguredAudienceModelAssociations
                description: >-
                  <p>Lists configured audience model associations within a
                  collaboration.</p>
                tags:
                  - Lists
                  - Collaboration
                  - Configured
                  - Audience
                  - Models
                  - Associations
                  - Identifiers
                  - Batches
                  - Analysis Templates
                  - Schemas
                  - Collaborations
                  - Configuration Audience Model Associations
                  - Tables
                  - Configured
                  - Tables
                  - Analysis
                  - Rules
                  - Associations
                  - Memberships
                  - Privacy Budget Templates
                  - Templates
                  - Audience
                  - Models
                  - Association
                  - Types
                  - Members
                  - Account
                  - Identifiers
                  - Privacy
                  - Budgets
                  - ARN
                  - Protected
                  - Queries
                  - Queries
                  - Schemas
                  - Names
            /collaborations/{collaborationIdentifier}/privacybudgettemplates:
              GET:
                summary: ListCollaborationPrivacyBudgetTemplates
                description: >-
                  <p>Returns an array that summarizes each privacy budget
                  template in a specified collaboration.</p>
                tags:
                  - Lists
                  - Collaboration
                  - Privacy
                  - Budgets
                  - Templates
                  - Identifiers
                  - Batches
                  - Analysis Templates
                  - Schemas
                  - Collaborations
                  - Configuration Audience Model Associations
                  - Tables
                  - Configured
                  - Tables
                  - Analysis
                  - Rules
                  - Associations
                  - Memberships
                  - Privacy Budget Templates
                  - Templates
                  - Audience
                  - Models
                  - Association
                  - Types
                  - Members
                  - Account
                  - Identifiers
                  - Privacy
                  - Budgets
                  - ARN
                  - Protected
                  - Queries
                  - Queries
                  - Schemas
                  - Names
            /collaborations/{collaborationIdentifier}/privacybudgets:
              GET:
                summary: ListCollaborationPrivacyBudgets
                description: >-
                  <p>Returns an array that summarizes each privacy budget in a
                  specified collaboration. The summary includes the
                  collaboration ARN, creation time, creating account, and
                  privacy budget details.</p>
                tags:
                  - Lists
                  - Collaboration
                  - Privacy
                  - Budgets
                  - Identifiers
                  - Batches
                  - Analysis Templates
                  - Schemas
                  - Collaborations
                  - Configuration Audience Model Associations
                  - Tables
                  - Configured
                  - Tables
                  - Analysis
                  - Rules
                  - Associations
                  - Memberships
                  - Privacy Budget Templates
                  - Templates
                  - Audience
                  - Models
                  - Association
                  - Types
                  - Members
                  - Account
                  - Identifiers
                  - Privacy
                  - Budgets
                  - ARN
                  - Protected
                  - Queries
                  - Queries
                  - Schemas
                  - Names
                  - Privacy Budgets
            /collaborations/{collaborationIdentifier}/members:
              GET:
                summary: ListMembers
                description: <p>Lists all members within a collaboration.</p>
                tags:
                  - Lists
                  - Members
                  - Identifiers
                  - Batches
                  - Analysis Templates
                  - Schemas
                  - Collaborations
                  - Configuration Audience Model Associations
                  - Tables
                  - Configured
                  - Tables
                  - Analysis
                  - Rules
                  - Associations
                  - Memberships
                  - Privacy Budget Templates
                  - Templates
                  - Audience
                  - Models
                  - Association
                  - Types
                  - Members
                  - Account
                  - Identifiers
                  - Privacy
                  - Budgets
                  - ARN
                  - Protected
                  - Queries
                  - Queries
                  - Schemas
                  - Names
                  - Privacy Budgets
                  - Members
            /memberships/{membershipIdentifier}/privacybudgets:
              GET:
                summary: ListPrivacyBudgets
                description: >-
                  <p>Returns detailed information about the privacy budgets in a
                  specified membership.</p>
                tags:
                  - Lists
                  - Privacy
                  - Budgets
                  - Identifiers
                  - Batches
                  - Analysis Templates
                  - Schemas
                  - Collaborations
                  - Configuration Audience Model Associations
                  - Tables
                  - Configured
                  - Tables
                  - Analysis
                  - Rules
                  - Associations
                  - Memberships
                  - Privacy Budget Templates
                  - Templates
                  - Audience
                  - Models
                  - Association
                  - Types
                  - Members
                  - Account
                  - Identifiers
                  - Privacy
                  - Budgets
                  - ARN
                  - Protected
                  - Queries
                  - Queries
                  - Schemas
                  - Names
                  - Privacy Budgets
                  - Members
            /memberships/{membershipIdentifier}/protectedQueries:
              POST:
                summary: StartProtectedQuery
                description: >-
                  <p>Creates a protected query that is started by Clean
                  Rooms.</p>
                tags:
                  - Start
                  - Protected
                  - Queries
                  - Identifiers
                  - Batches
                  - Analysis Templates
                  - Schemas
                  - Collaborations
                  - Configuration Audience Model Associations
                  - Tables
                  - Configured
                  - Tables
                  - Analysis
                  - Rules
                  - Associations
                  - Memberships
                  - Privacy Budget Templates
                  - Templates
                  - Audience
                  - Models
                  - Association
                  - Types
                  - Members
                  - Account
                  - Identifiers
                  - Privacy
                  - Budgets
                  - ARN
                  - Protected
                  - Queries
                  - Queries
                  - Schemas
                  - Names
                  - Privacy Budgets
                  - Members
            /collaborations/{collaborationIdentifier}/schemas:
              GET:
                summary: ListSchemas
                description: <p>Lists the schemas for relations within a collaboration.</p>
                tags:
                  - Lists
                  - Schemas
                  - Identifiers
                  - Batches
                  - Analysis Templates
                  - Schemas
                  - Collaborations
                  - Configuration Audience Model Associations
                  - Tables
                  - Configured
                  - Tables
                  - Analysis
                  - Rules
                  - Associations
                  - Memberships
                  - Privacy Budget Templates
                  - Templates
                  - Audience
                  - Models
                  - Association
                  - Types
                  - Members
                  - Account
                  - Identifiers
                  - Privacy
                  - Budgets
                  - ARN
                  - Protected
                  - Queries
                  - Queries
                  - Schemas
                  - Names
                  - Privacy Budgets
                  - Members
            /tags/{resourceArn}:
              DELETE:
                summary: UntagResource
                description: <p>Removes a tag or list of tags from a resource.</p>
                tags:
                  - Untag
                  - Resources
                  - Identifiers
                  - Batches
                  - Analysis Templates
                  - Schemas
                  - Collaborations
                  - Configuration Audience Model Associations
                  - Tables
                  - Configured
                  - Tables
                  - Analysis
                  - Rules
                  - Associations
                  - Memberships
                  - Privacy Budget Templates
                  - Templates
                  - Audience
                  - Models
                  - Association
                  - Types
                  - Members
                  - Account
                  - Identifiers
                  - Privacy
                  - Budgets
                  - ARN
                  - Protected
                  - Queries
                  - Queries
                  - Schemas
                  - Names
                  - Privacy Budgets
                  - Members
            /memberships/{membershipIdentifier}/previewprivacyimpact:
              POST:
                summary: PreviewPrivacyImpact
                description: >-
                  <p>An estimate of the number of aggregation functions that the
                  member who can query can run given epsilon and noise param
                tags:
                  - Preview
                  - Privacy
                  - Impact
                  - Identifiers
                  - Batches
                  - Analysis Templates
                  - Schemas
                  - Collaborations
                  - Configuration Audience Model Associations
                  - Tables
                  - Configured
                  - Tables
                  - Analysis
                  - Rules
                  - Associations
                  - Memberships
                  - Privacy Budget Templates
                  - Templates
                  - Audience
                  - Models
                  - Association
                  - Types
                  - Members
                  - Account
                  - Identifiers
                  - Privacy
                  - Budgets
                  - ARN
                  - Protected
                  - Queries
                  - Queries
                  - Schemas
                  - Names
                  - Privacy Budgets
                  - Members
                  - Preview Privacy
    overlays:
      - type: APIs.io Search
        url: overlays/cleanrooms-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/cleanrooms-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:cleanrooms
  - aid: box:box-collaborations-api
    name: Box Collaborations API
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
            title: Box Collaborations API
          paths:
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
                  - Collaborations
            /folders/{folder_id}/collaborations:
              get:
                summary: List folder collaborations
                description: >-
                  Retrieves a list of pending and active collaborations for a

                  folder. This returns all the users that have access to the
                  folder

                  or have been invited to the folder.
                tags:
                  - List
                  - Folder
                  - Collaborations
                  - Files
                  - File_id
                  - Collaborations
                  - Folders
                  - Folder_id
            /collaborations/{collaboration_id}:
              get:
                summary: Get collaboration
                tags:
                  - Get
                  - Collaboration
                  - Files
                  - File_id
                  - Collaborations
                  - Folders
                  - Folder_id
                  - Collaboration_id
                description: Retrieves a single collaboration.
              put:
                tags:
                  - Update
                  - Collaboration
                  - Files
                  - File_id
                  - Collaborations
                  - Folders
                  - Folder_id
                  - Collaboration_id
                summary: Update collaboration
                description: |-
                  Updates a collaboration.
                  Can be used to change the owner of an item, or to
                  accept collaboration invites.
              delete:
                summary: Remove collaboration
                tags:
                  - Remove
                  - Collaboration
                  - Files
                  - File_id
                  - Collaborations
                  - Folders
                  - Folder_id
                  - Collaboration_id
                description: Deletes a single collaboration.
            /collaborations:
              get:
                summary: List pending collaborations
                tags:
                  - List
                  - Pending
                  - Collaborations
                  - Files
                  - File_id
                  - Collaborations
                  - Folders
                  - Folder_id
                  - Collaboration_id
                description: Retrieves all pending collaboration invites for this user.
              post:
                tags:
                  - Create
                  - Collaboration
                  - Files
                  - File_id
                  - Collaborations
                  - Folders
                  - Folder_id
                  - Collaboration_id
                summary: Create collaboration
                description: >-
                  Adds a collaboration for a single user or a single group to a
                  file

                  or folder.


                  Collaborations can be created using email address, user IDs,
                  or a

                  group IDs.


                  If a collaboration is being created with a group, access to

                  this endpoint is dependent on the group's ability to be
                  invited.


                  If collaboration is in `pending` status, the following fields

                  are redacted:

                  - `login` and `name` are hidden if a collaboration was created

                  using `user_id`,

                  -  `name` is hidden if a collaboration was created using
                  `login`.
            /groups/{group_id}/collaborations:
              get:
                summary: List group collaborations
                tags:
                  - List
                  - Group
                  - Collaborations
                  - Files
                  - File_id
                  - Collaborations
                  - Folders
                  - Folder_id
                  - Collaboration_id
                  - Groups
                  - Group_id
                description: |-
                  Retrieves all the collaborations for a group. The user
                  must have admin permissions to inspect enterprise's groups.

                  Each collaboration object has details on which files or
                  folders the group has access to and wit
    overlays:
      - type: APIs.io Search
        url: overlays/collaborations-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/collaborations-openapi-api-evangelist-ratings.yml
  - aid: box:box-collaboration-whitelist-entries-api
    name: Box Collaboration Whitelist Entries API
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
            title: Box Collaboration Whitelist Entries API
          paths:
            /collaboration_whitelist_entries:
              get:
                summary: List allowed collaboration domains
                tags:
                  - List
                  - Allowed
                  - Collaboration
                  - Domains
                  - Collaboration_whitelist_entries
                description: >-
                  Returns the list domains that have been deemed safe to create
                  collaborations

                  for within the current enterprise.
              post:
                summary: Add domain to list of allowed collaboration domains
                tags:
                  - Add
                  - Domain
                  - To
                  - List
                  - Of
                  - Allowed
                  - Collaboration
                  - Domains
                  - Collaboration_whitelist_entries
                description: |-
                  Creates a new entry in the list of allowed domains to allow
                  collaboration for.
            /collaboration_whitelist_entries/{collaboration_whitelist_entry_id}:
              get:
                summary: Get allowed collaboration domain
                tags:
                  - Get
                  - Allowed
                  - Collaboration
                  - Domain
                  - Collaboration_whitelist_entries
                  - Collaboration_whitelist_entry_id
                description: >-
                  Returns a domain that has been deemed safe to create
                  collaborations

                  for within the current enterprise.
              delete:
                summary: Remove domain from list of allowed collaboration domains
                tags:
                  - Remove
                  - Domain
                  - From
                  - List
                  - Of
                  - Allowed
                  - Collaboration
                  - Domains
                  - Collaboration_whitelist_entries
                  - Collaboration_whitelist_entry_id
                description: >-
                  Removes a domain from the list of domains that have been
                  deemed safe to create

                  collaborations for within the current
    overlays:
      - type: APIs.io Search
        url: overlays/collaboration-whitelist-entries-openapi-search.yml
      - type: API Evangelist Ratings
        url: >-
          overlays/collaboration-whitelist-entries-openapi-api-evangelist-ratings.yml
  - aid: box:box-collaboration-whitelist-exempt-targets-api
    name: Box Collaboration Whitelist Exempt Targets API
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
            title: Box Collaboration Whitelist Exempt Targets API
          paths:
            /collaboration_whitelist_exempt_targets:
              get:
                summary: List users exempt from collaboration domain restrictions
                tags:
                  - List
                  - Users
                  - Exempt
                  - From
                  - Collaboration
                  - Domain
                  - Restrictions
                  - Collaboration_whitelist_exempt_targets
                description: >-
                  Returns a list of users who have been exempt from the
                  collaboration

                  domain restrictions.
              post:
                summary: Create user exemption from collaboration domain restrictions
                tags:
                  - Create
                  - User
                  - Exemption
                  - From
                  - Collaboration
                  - Domain
                  - Restrictions
                  - Collaboration_whitelist_exempt_targets
                description: >-
                  Exempts a user from the restrictions set out by the allowed
                  list of domains

                  for collaborations.
            /collaboration_whitelist_exempt_targets/{collaboration_whitelist_exempt_target_id}:
              get:
                summary: Get user exempt from collaboration domain restrictions
                tags:
                  - Get
                  - User
                  - Exempt
                  - From
                  - Collaboration
                  - Domain
                  - Restrictions
                  - Collaboration_whitelist_exempt_targets
                  - Collaboration_whitelist_exempt_target_id
                description: |-
                  Returns a users who has been exempt from the collaboration
                  domain restrictions.
              delete:
                summary: Remove user from list of users exempt from domain restrictions
                tags:
                  - Remove
                  - User
                  - From
                  - List
                  - Of
                  - Users
                  - Exempt
                  - Domain
                  - Restrictions
                  - Collaboration_whitelist_exempt_targets
                  - Collaboration_whitelist_exempt_target_id
                description: >-
                  Removes a user's exemption from the restrictions set out by
                  the allowed list

                  of domains for col
    overlays:
      - type: APIs.io Search
        url: overlays/collaboration-whitelist-exempt-targets-openapi-search.yml
      - type: API Evangelist Ratings
        url: >-
          overlays/collaboration-whitelist-exempt-targets-openapi-api-evangelist-ratings.yml
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---