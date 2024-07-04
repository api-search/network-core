---
name: Collaborations
description: Needs a description.
image: >-
  https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/collaborations.png
url: https://example.com/apis/collaborations.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Collaborations
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
  - aid: box:box-folders-api
    name: Box Folders API
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
            title: Box Folders API
          paths:
            /folders/{folder_id}:
              get:
                summary: Get folder information
                tags:
                  - Get
                  - Folder
                  - Information
                  - Folders
                  - Folder_id
                description: >-
                  Retrieves details for a folder, including the first 100
                  entries

                  in the folder.


                  Passing `sort`, `direction`, `offset`, and `limit`

                  parameters in query allows you to manage the

                  list of returned

                  [folder items](r://folder--full#param-item-collection).


                  To fetch more items within the folder, use the

                  [Get items in a folder](e://get-folders-id-items) endpoint.
              post:
                summary: Restore folder
                tags:
                  - Restore
                  - Folder
                  - Folders
                  - Folder_id
                description: >-
                  Restores a folder that has been moved to the trash.


                  An optional new parent ID can be provided to restore the
                  folder to in case the

                  original folder has been deleted.


                  # Folder locking


                  During this operation, part of the file tree will be locked,
                  mainly

                  the source folder and all of its descendants, as well as the
                  destination

                  folder.


                  For the duration of the operation, no other move, copy,
                  delete, or restore

                  operation can performed on any of the locked folders.
              put:
                summary: Update folder
                description: |-
                  Updates a folder. This can be also be used to move the folder,
                  create shared links, update collaborations, and more.
                tags:
                  - Update
                  - Folder
                  - Folders
                  - Folder_id
              delete:
                summary: Delete folder
                description: |-
                  Deletes a folder, either permanently or by moving it to
                  the trash.
                tags:
                  - Delete
                  - Folder
                  - Folders
                  - Folder_id
            /folders/{folder_id}/items:
              get:
                summary: List items in folder
                tags:
                  - List
                  - Items
                  - In
                  - Folder
                  - Folders
                  - Folder_id
                  - Items
                description: >-
                  Retrieves a page of items in a folder. These items can be
                  files,

                  folders, and web links.


                  To request more information about the folder itself, like its
                  size,

                  use the [Get a folder](#get-folders-id) endpoint instead.
            /folders:
              post:
                summary: Create folder
                tags:
                  - Create
                  - Folder
                  - Folders
                  - Folder_id
                  - Items
                description: Creates a new empty folder within the specified parent folder.
            /folders/{folder_id}/copy:
              post:
                summary: Copy folder
                description: |-
                  Creates a copy of a folder within a destination folder.

                  The original folder will not be changed.
                tags:
                  - Copy
                  - Folder
                  - Folders
                  - Folder_id
                  - Items
                  - Copy
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
                  - Folders
                  - Folder_id
                  - Items
                  - Copy
                  - Collaborations
            /folders/{folder_id}/trash:
              get:
                summary: Get trashed folder
                tags:
                  - Get
                  - Trashed
                  - Folder
                  - Folders
                  - Folder_id
                  - Items
                  - Copy
                  - Collaborations
                  - Trash
                description: >-
                  Retrieves a folder that has been moved to the trash.


                  Please note that only if the folder itself has been moved to
                  the

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
                summary: Permanently remove folder
                tags:
                  - Permanently
                  - Remove
                  - Folder
                  - Folders
                  - Folder_id
                  - Items
                  - Copy
                  - Collaborations
                  - Trash
                description: |-
                  Permanently deletes a folder that is in the trash.
                  This action cannot be undone.
            /folders/{folder_id}/metadata:
              get:
                summary: List metadata instances on folder
                tags:
                  - List
                  - Metadata
                  - Instances
                  - 'On'
                  - Folder
                  - Folders
                  - Folder_id
                  - Items
                  - Copy
                  - Collaborations
                  - Trash
                  - Metadata
                description: >-
                  Retrieves all metadata for a given folder. This can not be
                  used on the root

                  folder with ID `0`.
            /folders/{folder_id}/metadata/enterprise/securityClassification-6VMVochwUWo:
              get:
                summary: Get classification on folder
                tags:
                  - Get
                  - Classification
                  - 'On'
                  - Folder
                  - Folders
                  - Folder_id
                  - Items
                  - Copy
                  - Collaborations
                  - Trash
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                description: >-
                  Retrieves the classification metadata instance that

                  has been applied to a folder.


                  This API can also be called by including the enterprise ID in
                  the

                  URL explicitly, for example

                  `/folders/:id//enterprise_12345/securityClassification-6VMVochwUWo`.
              post:
                summary: Add classification to folder
                tags:
                  - Add
                  - Classification
                  - To
                  - Folder
                  - Folders
                  - Folder_id
                  - Items
                  - Copy
                  - Collaborations
                  - Trash
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                description: >-
                  Adds a classification to a folder by specifying the label of
                  the

                  classification to add.


                  This API can also be called by including the enterprise ID in
                  the

                  URL explicitly, for example

                  `/folders/:id//enterprise_12345/securityClassification-6VMVochwUWo`.
              put:
                summary: Update classification on folder
                tags:
                  - Update
                  - Classification
                  - 'On'
                  - Folder
                  - Folders
                  - Folder_id
                  - Items
                  - Copy
                  - Collaborations
                  - Trash
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                description: >-
                  Updates a classification on a folder.


                  The classification can only be updated if a classification has
                  already been

                  applied to the folder before. When editing classifications,
                  only values are

                  defined for the enterprise will be accepted.
              delete:
                summary: Remove classification from folder
                tags:
                  - Remove
                  - Classification
                  - From
                  - Folder
                  - Folders
                  - Folder_id
                  - Items
                  - Copy
                  - Collaborations
                  - Trash
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                description: >-
                  Removes any classifications from a folder.


                  This API can also be called by including the enterprise ID in
                  the

                  URL explicitly, for example

                  `/folders/:id//enterprise_12345/securityClassification-6VMVochwUWo`.
            /folders/{folder_id}/metadata/{scope}/{template_key}:
              get:
                summary: Get metadata instance on folder
                tags:
                  - Get
                  - Metadata
                  - Instance
                  - 'On'
                  - Folder
                  - Folders
                  - Folder_id
                  - Items
                  - Copy
                  - Collaborations
                  - Trash
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                  - Scope
                  - Template_key
                description: >-
                  Retrieves the instance of a metadata template that has been
                  applied to a

                  folder. This can not be used on the root folder with ID `0`.
              post:
                summary: Create metadata instance on folder
                tags:
                  - Create
                  - Metadata
                  - Instance
                  - 'On'
                  - Folder
                  - Folders
                  - Folder_id
                  - Items
                  - Copy
                  - Collaborations
                  - Trash
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                  - Scope
                  - Template_key
                description: >-
                  Applies an instance of a metadata template to a folder.


                  In most cases only values that are present in the metadata
                  template

                  will be accepted, except for the `global.properties` template
                  which accepts

                  any key-value pair.


                  To display the metadata template in the Box web app the
                  enterprise needs to be

                  configured to enable **Cascading Folder Level Metadata** for
                  the user in the

                  admin console.
              put:
                summary: Update metadata instance on folder
                tags:
                  - Update
                  - Metadata
                  - Instance
                  - 'On'
                  - Folder
                  - Folders
                  - Folder_id
                  - Items
                  - Copy
                  - Collaborations
                  - Trash
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                  - Scope
                  - Template_key
                description: >-
                  Updates a piece of metadata on a folder.


                  The metadata instance can only be updated if the template has
                  already been

                  applied to the folder before. When editing metadata, only
                  values that match

                  the metadata template schema will be accepted.


                  The update is applied atomically. If any errors occur during
                  the

                  application of the operations, the metadata instance will not
                  be changed.
              delete:
                summary: Remove metadata instance from folder
                tags:
                  - Remove
                  - Metadata
                  - Instance
                  - From
                  - Folder
                  - Folders
                  - Folder_id
                  - Items
                  - Copy
                  - Collaborations
                  - Trash
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                  - Scope
                  - Template_key
                description: Deletes a piece of folder metadata.
            /folders/trash/items:
              get:
                summary: List trashed items
                tags:
                  - List
                  - Trashed
                  - Items
                  - Folders
                  - Folder_id
                  - Items
                  - Copy
                  - Collaborations
                  - Trash
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                  - Scope
                  - Template_key
                description: >-
                  Retrieves the files and folders that have been moved

                  to the trash.


                  Any attribute in the full files or folders objects can be
                  passed

                  in with the `fields` parameter to retrieve those specific

                  attributes that are not returned by default.


                  This endpoint defaults to use offset-based pagination, yet
                  also supports

                  marker-based pagination using the `marker` parameter.
            /folders/{folder_id}/watermark:
              get:
                summary: Get watermark for folder
                tags:
                  - Get
                  - Watermark
                  - For
                  - Folder
                  - Folders
                  - Folder_id
                  - Items
                  - Copy
                  - Collaborations
                  - Trash
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                  - Scope
                  - Template_key
                  - Watermark
                description: Retrieve the watermark for a folder.
              put:
                summary: Apply watermark to folder
                tags:
                  - Apply
                  - Watermark
                  - To
                  - Folder
                  - Folders
                  - Folder_id
                  - Items
                  - Copy
                  - Collaborations
                  - Trash
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                  - Scope
                  - Template_key
                  - Watermark
                description: Applies or update a watermark on a folder.
              delete:
                summary: Remove watermark from folder
                tags:
                  - Remove
                  - Watermark
                  - From
                  - Folder
                  - Folders
                  - Folder_id
                  - Items
                  - Copy
                  - Collaborations
                  - Trash
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                  - Scope
                  - Template_key
                  - Watermark
                description: Removes the watermark from a folder.
            /folders/{folder_id}#get_shared_link:
              get:
                summary: Get shared link for folder
                tags:
                  - Get
                  - Shared
                  - Link
                  - For
                  - Folder
                  - Folders
                  - Folder_id
                  - Items
                  - Copy
                  - Collaborations
                  - Trash
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                  - Scope
                  - Template_key
                  - Watermark
                  - '#get_shared_link'
                description: Gets the information for a shared link on a folder.
            /folders/{folder_id}#add_shared_link:
              put:
                summary: Add shared link to folder
                tags:
                  - Add
                  - Shared
                  - Link
                  - To
                  - Folder
                  - Folders
                  - Folder_id
                  - Items
                  - Copy
                  - Collaborations
                  - Trash
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                  - Scope
                  - Template_key
                  - Watermark
                  - '#get_shared_link'
                  - '#add_shared_link'
                description: Adds a shared link to a folder.
            /folders/{folder_id}#update_shared_link:
              put:
                summary: Update shared link on folder
                tags:
                  - Update
                  - Shared
                  - Link
                  - 'On'
                  - Folder
                  - Folders
                  - Folder_id
                  - Items
                  - Copy
                  - Collaborations
                  - Trash
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                  - Scope
                  - Template_key
                  - Watermark
                  - '#get_shared_link'
                  - '#add_shared_link'
                  - '#update_shared_link'
                description: Updates a shared link on a folder.
            /folders/{folder_id}#remove_shared_link:
              put:
                summary: Remove shared link from folder
                tags:
                  - Remove
                  - Shared
                  - Link
                  - From
                  - Folder
                  - Folders
                  - Folder_id
                  - Items
                  - Copy
                  - Collaborations
                  - Trash
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                  - Scope
                  - Template_key
                  - Watermark
                  - '#get_shared_link'
                  - '#add_shared_link'
                  - '#update_shared_link'
                  - '#remove_shared_link'
                description: Removes a shared link from a folder.
            /users/{user_id}/folders/0:
              put:
                summary: Transfer owned folders
                tags:
                  - Transfer
                  - Owned
                  - Folders
                  - Folders
                  - Folder_id
                  - Items
                  - Copy
                  - Collaborations
                  - Trash
                  - Metadata
                  - Classification
                  - Vochw
                  - Wo
                  - Scope
                  - Template_key
                  - Watermark
                  - '#get_shared_link'
                  - '#add_shared_link'
                  - '#update_shared_link'
                  - '#remove_shared_link'
                  - Users
                  - User_id
                description: >-
                  Move all of the items (files, folders and workflows) owned by
                  a user into

                  another user's account


                  Only the root folder (`0`) can be transferred.


                  Folders can only be moved across users by users with
                  administrative

                  permissions.


                  All existing shared links and folder-level collaborations are
                  transferred

                  during the operation. Please note that while collaborations at
                  the individual

                  file-level are transferred during the operation, the
                  collaborations are

                  deleted when the original user is deleted.


                  This call will be performed synchronously which might lead to
                  a slow response

                  when the source user has a large number of items in all of its
                  folders.


                  If the destination path has a metadata cascade policy attached
                  to any of

                  the parent folders, a metadata cascade operation will be
                  kicked off

                  asynchronously.


                  There is currently no way to check for when this operation is
                  finished.


                  The destination folder's name will be in the format `{User}'s
                  Files and

                  Folders`, where `{User}` is the display name of the user.


                  To make this API call your application will need to have the
                  "Read and write

                  all files and folders stored in Box" scope enabled.


                  Please make sure the destination user has access to `Relay` or
                  `Relay Lite`,

                  and has access to the files and folders involved in the
                  workflows being

                  transferred.


                  Admins will receive an email when the operation i
    overlays:
      - type: APIs.io Search
        url: overlays/folders-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/folders-openapi-api-evangelist-ratings.yml
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
  - aid: box:box-groups-api
    name: Box Groups API
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
            title: Box Groups API
          paths:
            /groups:
              get:
                summary: List groups for enterprise
                tags:
                  - List
                  - Groups
                  - For
                  - Enterprise
                  - Groups
                description: |-
                  Retrieves all of the groups for a given enterprise. The user
                  must have admin permissions to inspect enterprise's groups.
              post:
                summary: Create group
                tags:
                  - Create
                  - Group
                  - Groups
                description: >-
                  Creates a new group of users in an enterprise. Only users with
                  admin

                  permissions can create new groups.
            /groups/terminate_sessions:
              post:
                summary: Create jobs to terminate user group session
                tags:
                  - Create
                  - Jobs
                  - To
                  - Terminate
                  - User
                  - Group
                  - Session
                  - Groups
                  - Terminate_sessions
                description: |-
                  Validates the roles and permissions of the group,
                  and creates asynchronous jobs
                  to terminate the group's sessions.
                  Returns the status for the POST request.
            /groups/{group_id}:
              get:
                summary: Get group
                tags:
                  - Get
                  - Group
                  - Groups
                  - Terminate_sessions
                  - Group_id
                description: |-
                  Retrieves information about a group. Only members of this
                  group or users with admin-level permissions will be able to
                  use this API.
              put:
                summary: Update group
                tags:
                  - Update
                  - Group
                  - Groups
                  - Terminate_sessions
                  - Group_id
                description: |-
                  Updates a specific group. Only admins of this
                  group or users with admin-level permissions will be able to
                  use this API.
              delete:
                summary: Remove group
                tags:
                  - Remove
                  - Group
                  - Groups
                  - Terminate_sessions
                  - Group_id
                description: |-
                  Permanently deletes a group. Only users with
                  admin-level permissions will be able to use this API.
            /groups/{group_id}/memberships:
              get:
                summary: List members of group
                tags:
                  - List
                  - Members
                  - Of
                  - Group
                  - Groups
                  - Terminate_sessions
                  - Group_id
                  - Memberships
                description: |-
                  Retrieves all the members for a group. Only members of this
                  group or users with admin-level permissions will be able to
                  use this API.
            /groups/{group_id}/collaborations:
              get:
                summary: List group collaborations
                tags:
                  - List
                  - Group
                  - Collaborations
                  - Groups
                  - Terminate_sessions
                  - Group_id
                  - Memberships
                  - Collaborations
                description: |-
                  Retrieves all the collaborations for a group. The user
                  must have admin permissions to inspect enterprise's groups.

                  Each collaboration object has details on which files or
                  folders the group has access to and wit
    overlays:
      - type: APIs.io Search
        url: overlays/groups-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/groups-openapi-api-evangelist-ratings.yml
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---