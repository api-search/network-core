---
name: Configured
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/configured.png
url: https://example.com/apis/configured.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Configured
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
  - name: cleanroomsml
    description: >-
      <p>Welcome to the <i>Amazon Web Services Clean Rooms ML API
      Reference</i>.</p> <p>Amazon Web Services Clean Rooms ML provides a
      privacy-enhancing method for two parties to identify similar users in
      their data without the need to share their data with each other. The first
      party brings the training data to Clean Rooms so that they can create and
      configure an audience model (lookalike model) and associate it with a
      collaboration. The second party then brings their seed data to Clean Rooms
      and generates an audience (lookalike segment) that resembles the training
      data.</p> <p>To learn more about Amazon Web Services Clean Rooms ML
      concepts, procedures, and best practices, see the <a
      href="https://docs.aws.amazon.com/clean-rooms/latest/userguide/machine-learning.html">Clean
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
            title: cleanroomsml
          paths:
            /audience-model:
              GET:
                summary: ListAudienceModels
                description: <p>Returns a list of audience models.</p>
                tags:
                  - Lists
                  - Audience
                  - Models
                  - Audience
                  - Models
            /configured-audience-model:
              GET:
                summary: ListConfiguredAudienceModels
                description: <p>Returns a list of the configured audience models.</p>
                tags:
                  - Lists
                  - Configured
                  - Audience
                  - Models
                  - Audience
                  - Models
                  - Configured
            /training-dataset:
              GET:
                summary: ListTrainingDatasets
                description: <p>Returns a list of training datasets.</p>
                tags:
                  - Lists
                  - Training
                  - Datasets
                  - Audience
                  - Models
                  - Configured
                  - Training
                  - Datasets
            /audience-generation-job/{audienceGenerationJobArn}:
              GET:
                summary: GetAudienceGenerationJob
                description: <p>Returns information about an audience generation job.</p>
                tags:
                  - Get
                  - Audience
                  - Generation
                  - Jobs
                  - Audience
                  - Models
                  - Configured
                  - Training
                  - Datasets
                  - Generation
                  - Jobs
                  - ARN
            /audience-model/{audienceModelArn}:
              GET:
                summary: GetAudienceModel
                description: <p>Returns information about an audience model</p>
                tags:
                  - Get
                  - Audience
                  - Models
                  - Audience
                  - Models
                  - Configured
                  - Training
                  - Datasets
                  - Generation
                  - Jobs
                  - ARN
            /configured-audience-model/{configuredAudienceModelArn}:
              PATCH:
                summary: UpdateConfiguredAudienceModel
                description: >-
                  <p>Provides the information necessary to update a configured
                  audience model. Updates that impact audience generation jobs
                  take effect when a new job starts, but do not impact currently
                  running jobs.</p>
                tags:
                  - Update
                  - Configured
                  - Audience
                  - Models
                  - Audience
                  - Models
                  - Configured
                  - Training
                  - Datasets
                  - Generation
                  - Jobs
                  - ARN
            /configured-audience-model/{configuredAudienceModelArn}/policy:
              PUT:
                summary: PutConfiguredAudienceModelPolicy
                description: >-
                  <p>Create or update the resource policy for a configured
                  audience model.</p>
                tags:
                  - Put
                  - Configured
                  - Audience
                  - Models
                  - Policies
                  - Audience
                  - Models
                  - Configured
                  - Training
                  - Datasets
                  - Generation
                  - Jobs
                  - ARN
                  - Policies
            /training-dataset/{trainingDatasetArn}:
              GET:
                summary: GetTrainingDataset
                description: <p>Returns information about a training dataset.</p>
                tags:
                  - Get
                  - Training
                  - Datasets
                  - Audience
                  - Models
                  - Configured
                  - Training
                  - Datasets
                  - Generation
                  - Jobs
                  - ARN
                  - Policies
            /audience-export-job:
              POST:
                summary: StartAudienceExportJob
                description: >-
                  <p>Export an audience of a specified size after you have
                  generated an audience.</p>
                tags:
                  - Start
                  - Audience
                  - Export
                  - Jobs
                  - Audience
                  - Models
                  - Configured
                  - Training
                  - Datasets
                  - Generation
                  - Jobs
                  - ARN
                  - Policies
                  - Export
            /audience-generation-job:
              POST:
                summary: StartAudienceGenerationJob
                description: >-
                  <p>Information necessary to start the audience generation
                  job.</p>
                tags:
                  - Start
                  - Audience
                  - Generation
                  - Jobs
                  - Audience
                  - Models
                  - Configured
                  - Training
                  - Datasets
                  - Generation
                  - Jobs
                  - ARN
                  - Policies
                  - Export
            /tags/{resourceArn}:
              DELETE:
                summary: UntagResource
                description: <p>Removes metadata tags from a specified res
                tags:
                  - Untag
                  - Resources
                  - Audience
                  - Models
                  - Configured
                  - Training
                  - Datasets
                  - Generation
                  - Jobs
                  - ARN
                  - Policies
                  - Expo
    overlays:
      - type: APIs.io Search
        url: overlays/cleanroomsml-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/cleanroomsml-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:cleanroomsml
  - name: FactSet IRN Configuration API
    description: >-
      Config API allows users to read and update configuration and settings of
      the Internal Research Notes.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.factset.com/api-catalog/irn-configuration-api
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: >-
          https://developer.factset.com/api-catalog/irn-configuration-api#overview
      - type: SDKs
        url: >-
          https://developer.factset.com/api-catalog/irn-configuration-api#sdkLibrary
      - type: Jupyter Notebooks
        url: >-
          https://developer.factset.com/api-catalog/irn-configuration-api#notebooks
      - type: Code Snippets
        url: >-
          https://developer.factset.com/api-catalog/irn-configuration-api#codeSnippet
      - type: Change Log
        url: >-
          https://developer.factset.com/api-catalog/irn-configuration-api#changelog
      - type: OpenAPI
        data:
          openapi: 3.0.1
          info:
            title: IRN API v1
          paths:
            /v1/authors:
              get:
                tags:
                  - Get
                  - All
                  - Authors
                  - V1
                  - Authors
                summary: Get all Authors
            /v1/contact-custom-fields:
              get:
                tags:
                  - Get
                  - All
                  - The
                  - Contact
                  - Custom
                  - Fields
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                summary: Get all the contact custom fields
              post:
                tags:
                  - Create
                  - Contact
                  - Custom
                  - Field
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                summary: Create a contact custom field
            /v1/contact-custom-fields/{contactCustomFieldId}:
              get:
                tags:
                  - Get
                  - Specific
                  - Contact
                  - Custom
                  - Field's
                  - Details
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                summary: Get a specific Contact custom field's details
              patch:
                tags:
                  - Edit
                  - Contact
                  - Custom
                  - Field
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                summary: Edit a contact custom field
              delete:
                tags:
                  - Delete
                  - Contact
                  - Custom
                  - Field
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                summary: Delete a contact custom field
            /v1/contact-roles:
              get:
                tags:
                  - Get
                  - List
                  - Of
                  - The
                  - Contact
                  - Roles
                  - Configured
                  - In
                  - Your
                  - Group
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                summary: Get list of the contact roles configured in your group
              post:
                tags:
                  - Create
                  - Contact
                  - Roles
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                summary: Create contact roles
            /v1/contact-types:
              get:
                tags:
                  - Get
                  - List
                  - Of
                  - The
                  - Contact
                  - Types
                  - Configured
                  - In
                  - Your
                  - Group
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                  - Types
                summary: Get list of the contact types configured in your group
              post:
                tags:
                  - Create
                  - Contact
                  - Types
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                  - Types
                summary: Create contact types
            /v1/custom-fields:
              get:
                tags:
                  - Get
                  - All
                  - Custom
                  - Fields
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                  - Types
                summary: Get all Custom Fields
            /v1/custom-symbol-custom-fields:
              get:
                tags:
                  - Get
                  - All
                  - The
                  - Custom
                  - Symbol
                  - Fields
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                  - Types
                  - Symbol
                summary: Get all the Custom symbol custom fields
              post:
                tags:
                  - Create
                  - Custom
                  - Symbol
                  - Field
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                  - Types
                  - Symbol
                summary: Create a Custom symbol custom field
            /v1/custom-symbol-custom-fields/{customSymbolCustomFieldId}:
              get:
                tags:
                  - Get
                  - Specific
                  - Custom
                  - Symbol
                  - Field's
                  - Details
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                  - Types
                  - Symbol
                summary: Get a specific Custom symbol custom field's details
              patch:
                tags:
                  - Edit
                  - Custom
                  - Symbol
                  - Field
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                  - Types
                  - Symbol
                summary: Edit a Custom symbol custom field
              delete:
                tags:
                  - Delete
                  - Custom
                  - Symbol
                  - Field
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                  - Types
                  - Symbol
                summary: Delete a Custom symbol custom field
            /v1/custom-symbol-types:
              get:
                tags:
                  - Get
                  - All
                  - The
                  - Custom
                  - Symbol
                  - Types
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                  - Types
                  - Symbol
                summary: Get all the custom symbol types
              post:
                tags:
                  - Create
                  - Custom
                  - Symbol
                  - Type
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                  - Types
                  - Symbol
                summary: Create a Custom symbol type
            /v1/custom-symbol-types/{customSymbolTypeId}:
              get:
                tags:
                  - Get
                  - Specific
                  - Custom
                  - Symbol
                  - Type's
                  - Details
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                  - Types
                  - Symbol
                  - Type
                summary: Get a specific Custom symbol type's details
              put:
                tags:
                  - Edit
                  - Custom
                  - Symbol
                  - Type
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                  - Types
                  - Symbol
                  - Type
                summary: Edit a Custom symbol type
              delete:
                tags:
                  - Delete
                  - Custom
                  - Symbol
                  - Type
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                  - Types
                  - Symbol
                  - Type
                summary: Delete a Custom symbol type
            /v1/custom-symbol-types/{customSymbolTypeId}/custom-fields:
              get:
                tags:
                  - Get
                  - Custom
                  - Fields
                  - For
                  - Symbol
                  - Type
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                  - Types
                  - Symbol
                  - Type
                summary: Get Custom fields for Custom Symbol type
            /v1/group:
              get:
                tags:
                  - Get
                  - Group
                  - Details
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                  - Types
                  - Symbol
                  - Type
                  - Group
                summary: Get Group details
            /v1/group/client-sales-representative:
              get:
                tags:
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                  - Types
                  - Symbol
                  - Type
                  - Group
                  - Client
                  - Sales
                  - Representative
            /v1/phone-number-types:
              get:
                tags:
                  - Get
                  - List
                  - Of
                  - The
                  - Phone
                  - Types
                  - Configured
                  - In
                  - Your
                  - Group
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                  - Types
                  - Symbol
                  - Type
                  - Group
                  - Client
                  - Sales
                  - Representative
                  - Phone
                  - Number
                summary: Get list of the phone types configured in your group
              post:
                tags:
                  - Create
                  - Phone
                  - Type
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                  - Types
                  - Symbol
                  - Type
                  - Group
                  - Client
                  - Sales
                  - Representative
                  - Phone
                  - Number
                summary: Create a phone type
            /v1/recommendations:
              get:
                tags:
                  - Get
                  - All
                  - Recommendations
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                  - Types
                  - Symbol
                  - Type
                  - Group
                  - Client
                  - Sales
                  - Representative
                  - Phone
                  - Number
                  - Recommendations
                summary: Get all Recommendations
            /v1/relationship-categories:
              get:
                tags:
                  - Get
                  - List
                  - Of
                  - The
                  - Relationship
                  - Categories
                  - Configured
                  - In
                  - Your
                  - Group
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                  - Types
                  - Symbol
                  - Type
                  - Group
                  - Client
                  - Sales
                  - Representative
                  - Phone
                  - Number
                  - Recommendations
                  - Relationship
                  - Categories
                summary: >-
                  Get list of the relationship categories configured in your
                  group
              post:
                tags:
                  - Create
                  - Relationship
                  - Category
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                  - Types
                  - Symbol
                  - Type
                  - Group
                  - Client
                  - Sales
                  - Representative
                  - Phone
                  - Number
                  - Recommendations
                  - Relationship
                  - Categories
                summary: Create a relationship category
            /v1/relationships:
              get:
                tags:
                  - Get
                  - List
                  - Of
                  - The
                  - Relationships
                  - Configured
                  - In
                  - Your
                  - Group
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                  - Types
                  - Symbol
                  - Type
                  - Group
                  - Client
                  - Sales
                  - Representative
                  - Phone
                  - Number
                  - Recommendations
                  - Relationship
                  - Categories
                  - Relationships
                summary: Get list of the relationships configured in your group
              post:
                tags:
                  - Create
                  - Relationship
                  - Type
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                  - Types
                  - Symbol
                  - Type
                  - Group
                  - Client
                  - Sales
                  - Representative
                  - Phone
                  - Number
                  - Recommendations
                  - Relationship
                  - Categories
                  - Relationships
                summary: Create a relationship type
            /v1/sentiments:
              get:
                tags:
                  - Get
                  - All
                  - Sentiments
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                  - Types
                  - Symbol
                  - Type
                  - Group
                  - Client
                  - Sales
                  - Representative
                  - Phone
                  - Number
                  - Recommendations
                  - Relationship
                  - Categories
                  - Relationships
                  - Sentiments
                summary: Get all Sentiments
            /v1/subjects:
              get:
                tags:
                  - Get
                  - All
                  - Subjects
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                  - Types
                  - Symbol
                  - Type
                  - Group
                  - Client
                  - Sales
                  - Representative
                  - Phone
                  - Number
                  - Recommendations
                  - Relationship
                  - Categories
                  - Relationships
                  - Sentiments
                  - Subjects
                summary: Get all Subjects
            /v1/subjects/{subjectId}:
              get:
                tags:
                  - Get
                  - Subject
                  - Details
                  - For
                  - The
                  - Given
                  - Id
                  - Provided
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                  - Types
                  - Symbol
                  - Type
                  - Group
                  - Client
                  - Sales
                  - Representative
                  - Phone
                  - Number
                  - Recommendations
                  - Relationship
                  - Categories
                  - Relationships
                  - Sentiments
                  - Subjects
                summary: Get Subject details for the given Id provided
            /v1/symbols-relationships:
              get:
                tags:
                  - Get
                  - All
                  - The
                  - Symbols
                  - Relationships
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                  - Types
                  - Symbol
                  - Type
                  - Group
                  - Client
                  - Sales
                  - Representative
                  - Phone
                  - Number
                  - Recommendations
                  - Relationship
                  - Categories
                  - Relationships
                  - Sentiments
                  - Subjects
                  - Symbols
                summary: Get all the Symbols Relationships
              post:
                tags:
                  - Create
                  - Symbol
                  - Relationship
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                  - Types
                  - Symbol
                  - Type
                  - Group
                  - Client
                  - Sales
                  - Representative
                  - Phone
                  - Number
                  - Recommendations
                  - Relationship
                  - Categories
                  - Relationships
                  - Sentiments
                  - Subjects
                  - Symbols
                summary: Create a symbol relationship
            /v1/teams:
              get:
                tags:
                  - Get
                  - All
                  - Teams
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                  - Types
                  - Symbol
                  - Type
                  - Group
                  - Client
                  - Sales
                  - Representative
                  - Phone
                  - Number
                  - Recommendations
                  - Relationship
                  - Categories
                  - Relationships
                  - Sentiments
                  - Subjects
                  - Symbols
                  - Teams
                summary: Get all Teams
            /v1/teams/{teamId}:
              get:
                tags:
                  - Get
                  - Team
                  - Details
                  - For
                  - The
                  - Given
                  - Id
                  - Provided
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                  - Types
                  - Symbol
                  - Type
                  - Group
                  - Client
                  - Sales
                  - Representative
                  - Phone
                  - Number
                  - Recommendations
                  - Relationship
                  - Categories
                  - Relationships
                  - Sentiments
                  - Subjects
                  - Symbols
                  - Teams
                summary: Get Team details for the given Id provided
            /v1/users:
              get:
                tags:
                  - Get
                  - All
                  - Assigned
                  - Fact
                  - Set
                  - Users
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                  - Types
                  - Symbol
                  - Type
                  - Group
                  - Client
                  - Sales
                  - Representative
                  - Phone
                  - Number
                  - Recommendations
                  - Relationship
                  - Categories
                  - Relationships
                  - Sentiments
                  - Subjects
                  - Symbols
                  - Teams
                  - Users
                summary: Get all assigned FactSet users
            /v1/custom-symbol-types/reorder:
              post:
                tags:
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                  - Types
                  - Symbol
                  - Type
                  - Group
                  - Client
                  - Sales
                  - Representative
                  - Phone
                  - Number
                  - Recommendations
                  - Relationship
                  - Categories
                  - Relationships
                  - Sentiments
                  - Subjects
                  - Symbols
                  - Teams
                  - Users
                  - Reorder
            /v1/relationship-categories/reorder:
              post:
                tags:
                  - Reorder
                  - Relationship
                  - Categories
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                  - Types
                  - Symbol
                  - Type
                  - Group
                  - Client
                  - Sales
                  - Representative
                  - Phone
                  - Number
                  - Recommendations
                  - Relationship
                  - Categories
                  - Relationships
                  - Sentiments
                  - Subjects
                  - Symbols
                  - Teams
                  - Users
                  - Reorder
                summary: Reorder relationship categories
            /v1/contact-roles/{contactRoleId}:
              put:
                tags:
                  - Edit
                  - Contact
                  - Role
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                  - Types
                  - Symbol
                  - Type
                  - Group
                  - Client
                  - Sales
                  - Representative
                  - Phone
                  - Number
                  - Recommendations
                  - Relationship
                  - Categories
                  - Relationships
                  - Sentiments
                  - Subjects
                  - Symbols
                  - Teams
                  - Users
                  - Reorder
                  - Role
                summary: Edit a contact role
              delete:
                tags:
                  - Delete
                  - Contact
                  - Role
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                  - Types
                  - Symbol
                  - Type
                  - Group
                  - Client
                  - Sales
                  - Representative
                  - Phone
                  - Number
                  - Recommendations
                  - Relationship
                  - Categories
                  - Relationships
                  - Sentiments
                  - Subjects
                  - Symbols
                  - Teams
                  - Users
                  - Reorder
                  - Role
                summary: Delete a contact role
            /v1/contact-types/{contactTypeId}:
              put:
                tags:
                  - Edit
                  - Contact
                  - Type
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                  - Types
                  - Symbol
                  - Type
                  - Group
                  - Client
                  - Sales
                  - Representative
                  - Phone
                  - Number
                  - Recommendations
                  - Relationship
                  - Categories
                  - Relationships
                  - Sentiments
                  - Subjects
                  - Symbols
                  - Teams
                  - Users
                  - Reorder
                  - Role
                summary: Edit a contact type
              delete:
                tags:
                  - Delete
                  - Contact
                  - Type
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                  - Types
                  - Symbol
                  - Type
                  - Group
                  - Client
                  - Sales
                  - Representative
                  - Phone
                  - Number
                  - Recommendations
                  - Relationship
                  - Categories
                  - Relationships
                  - Sentiments
                  - Subjects
                  - Symbols
                  - Teams
                  - Users
                  - Reorder
                  - Role
                summary: Delete a contact type
            /v1/phone-number-types/{phoneNumberTypeId}:
              put:
                tags:
                  - Edit
                  - Phone
                  - Type
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                  - Types
                  - Symbol
                  - Type
                  - Group
                  - Client
                  - Sales
                  - Representative
                  - Phone
                  - Number
                  - Recommendations
                  - Relationship
                  - Categories
                  - Relationships
                  - Sentiments
                  - Subjects
                  - Symbols
                  - Teams
                  - Users
                  - Reorder
                  - Role
                summary: Edit a phone type
              delete:
                tags:
                  - Delete
                  - Phone
                  - Type
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                  - Types
                  - Symbol
                  - Type
                  - Group
                  - Client
                  - Sales
                  - Representative
                  - Phone
                  - Number
                  - Recommendations
                  - Relationship
                  - Categories
                  - Relationships
                  - Sentiments
                  - Subjects
                  - Symbols
                  - Teams
                  - Users
                  - Reorder
                  - Role
                summary: Delete a phone type
            /v1/relationship-categories/{relationshipCategoryId}:
              put:
                tags:
                  - Edit
                  - Relationship
                  - Category
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                  - Types
                  - Symbol
                  - Type
                  - Group
                  - Client
                  - Sales
                  - Representative
                  - Phone
                  - Number
                  - Recommendations
                  - Relationship
                  - Categories
                  - Relationships
                  - Sentiments
                  - Subjects
                  - Symbols
                  - Teams
                  - Users
                  - Reorder
                  - Role
                  - Category
                summary: Edit a relationship category
              delete:
                tags:
                  - Delete
                  - Relationship
                  - Category
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                  - Types
                  - Symbol
                  - Type
                  - Group
                  - Client
                  - Sales
                  - Representative
                  - Phone
                  - Number
                  - Recommendations
                  - Relationship
                  - Categories
                  - Relationships
                  - Sentiments
                  - Subjects
                  - Symbols
                  - Teams
                  - Users
                  - Reorder
                  - Role
                  - Category
                summary: Delete a relationship category
            /v1/relationships/{relationshipId}:
              put:
                tags:
                  - Edit
                  - Relationship
                  - Type
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                  - Types
                  - Symbol
                  - Type
                  - Group
                  - Client
                  - Sales
                  - Representative
                  - Phone
                  - Number
                  - Recommendations
                  - Relationship
                  - Categories
                  - Relationships
                  - Sentiments
                  - Subjects
                  - Symbols
                  - Teams
                  - Users
                  - Reorder
                  - Role
                  - Category
                summary: Edit a relationship type
              delete:
                tags:
                  - Delete
                  - Relationship
                  - Type
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                  - Types
                  - Symbol
                  - Type
                  - Group
                  - Client
                  - Sales
                  - Representative
                  - Phone
                  - Number
                  - Recommendations
                  - Relationship
                  - Categories
                  - Relationships
                  - Sentiments
                  - Subjects
                  - Symbols
                  - Teams
                  - Users
                  - Reorder
                  - Role
                  - Category
                summary: Delete a relationship type
            /v1/symbols-relationships/{symbolsRelationshipId}:
              put:
                tags:
                  - Edit
                  - Symbol
                  - Relationship
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                  - Types
                  - Symbol
                  - Type
                  - Group
                  - Client
                  - Sales
                  - Representative
                  - Phone
                  - Number
                  - Recommendations
                  - Relationship
                  - Categories
                  - Relationships
                  - Sentiments
                  - Subjects
                  - Symbols
                  - Teams
                  - Users
                  - Reorder
                  - Role
                  - Category
                summary: Edit a symbol relationship
              delete:
                tags:
                  - Delete
                  - Symbol
                  - Relationship
                  - V1
                  - Authors
                  - Contact
                  - Custom
                  - Fields
                  - Field
                  - Id
                  - Roles
                  - Types
                  - Symbol
                  - Type
                  - Group
                  - Client
                  - Sales
                  - Representative
                  - Phone
                  - Number
                  - Recommendations
                  - Relationship
                  - Categories
                  - Relationships
                  - Sentiments
                  - Subjects
                  - Symbols
                  - Teams
                  - Users
                  - Reorder
                  - Role
                  - Category
                summary: Delete a symbol relationship
          tags:
            - name: Contacts - CustomFields
            - name: Contacts - PhoneNumberTypes
            - name: Contacts - Relationship Category
            - name: Contacts - Relationships
            - name: Contacts - Roles
            - name: Contacts - Types
            - name: CustomSymbols - CustomFields
            - name: CustomSymbols - Relationships
            - name: CustomSymbols - Types
            - name: 'N'
    overlays:
      - type: APIs.io Search
        url: overlays/irn-configuration-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/irn-configuration-openapi-api-evangelist-ratings.yml
    aid: factset:factset-irn-configuration-api
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---