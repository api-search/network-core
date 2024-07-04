---
name: Agents
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/agents.png
url: https://example.com/apis/agents.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Agents
apis:
  - name: bedrock-agent
    description: >-
      <p>An example service, deployed with the Octane Service creator, which
      will echo the string</p>
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
            title: bedrock-agent
          paths:
            /agents/{agentId}/agentversions/{agentVersion}/knowledgebases/:
              POST:
                summary: ListAgentKnowledgeBases
                description: >-
                  <p>List of Knowledge Bases associated to an existing Amazon
                  Bedrock Agent Version</p>
                tags:
                  - Lists
                  - Agent
                  - Knowledge
                  - Bases
                  - Identifiers
                  - Agent Versions
                  - Agent
                  - Versions
                  - Knowledgebases
            /agents/:
              POST:
                summary: ListAgents
                description: <p>Lists Agents</p>
                tags:
                  - Lists
                  - Agents
                  - Identifiers
                  - Agent Versions
                  - Agent
                  - Versions
                  - Knowledgebases
                  - Agents
            /agents/{agentId}/agentversions/{agentVersion}/actiongroups/:
              POST:
                summary: ListAgentActionGroups
                description: >-
                  <p>Lists an Action Group for existing Amazon Bedrock Agent
                  Version</p>
                tags:
                  - Lists
                  - Agent
                  - Actions
                  - Groups
                  - Identifiers
                  - Agent Versions
                  - Agent
                  - Versions
                  - Knowledgebases
                  - Agents
                  - Action Groups
            /agents/{agentId}/agentaliases/:
              POST:
                summary: ListAgentAliases
                description: <p>Lists all the Aliases for an Amazon Bedrock Agent</p>
                tags:
                  - Lists
                  - Agent
                  - Aliases
                  - Identifiers
                  - Agent Versions
                  - Agent
                  - Versions
                  - Knowledgebases
                  - Agents
                  - Action Groups
                  - Agent Aliases
            /knowledgebases/{knowledgeBaseId}/datasources/:
              POST:
                summary: ListDataSources
                description: <p>List data sources</p>
                tags:
                  - Lists
                  - Data
                  - Sources
                  - Identifiers
                  - Agent Versions
                  - Agent
                  - Versions
                  - Knowledgebases
                  - Agents
                  - Action Groups
                  - Agent Aliases
                  - Base
                  - Data Source
            /knowledgebases/:
              POST:
                summary: ListKnowledgeBases
                description: <p>List Knowledge Bases</p>
                tags:
                  - Lists
                  - Knowledge
                  - Bases
                  - Identifiers
                  - Agent Versions
                  - Agent
                  - Versions
                  - Knowledgebases
                  - Agents
                  - Action Groups
                  - Agent Aliases
                  - Base
                  - Data Source
            /agents/{agentId}/:
              PUT:
                summary: UpdateAgent
                description: <p>Updates an existing Amazon Bedrock Agent</p>
                tags:
                  - Update
                  - Agent
                  - Identifiers
                  - Agent Versions
                  - Agent
                  - Versions
                  - Knowledgebases
                  - Agents
                  - Action Groups
                  - Agent Aliases
                  - Base
                  - Data Source
            /agents/{agentId}/agentversions/{agentVersion}/actiongroups/{actionGroupId}/:
              PUT:
                summary: UpdateAgentActionGroup
                description: >-
                  <p>Updates an existing Action Group for Amazon Bedrock
                  Agent</p>
                tags:
                  - Update
                  - Agent
                  - Actions
                  - Group
                  - Identifiers
                  - Agent Versions
                  - Agent
                  - Versions
                  - Knowledgebases
                  - Agents
                  - Action Groups
                  - Agent Aliases
                  - Base
                  - Data Source
                  - Actions
                  - Group
            /agents/{agentId}/agentaliases/{agentAliasId}/:
              PUT:
                summary: UpdateAgentAlias
                description: <p>Updates an existing Alias for an Amazon Bedrock Agent</p>
                tags:
                  - Update
                  - Agent
                  - Alias
                  - Identifiers
                  - Agent Versions
                  - Agent
                  - Versions
                  - Knowledgebases
                  - Agents
                  - Action Groups
                  - Agent Aliases
                  - Base
                  - Data Source
                  - Actions
                  - Group
                  - Alias
            /agents/{agentId}/agentversions/{agentVersion}/:
              GET:
                summary: GetAgentVersion
                description: <p>Gets an Agent version for existing Amazon Bedrock Agent</p>
                tags:
                  - Get
                  - Agent
                  - Versions
                  - Identifiers
                  - Agent Versions
                  - Agent
                  - Versions
                  - Knowledgebases
                  - Agents
                  - Action Groups
                  - Agent Aliases
                  - Base
                  - Data Source
                  - Actions
                  - Group
                  - Alias
            /knowledgebases/{knowledgeBaseId}/datasources/{dataSourceId}:
              PUT:
                summary: UpdateDataSource
                description: <p>Update an existing data source</p>
                tags:
                  - Update
                  - Data
                  - Source
                  - Identifiers
                  - Agent Versions
                  - Agent
                  - Versions
                  - Knowledgebases
                  - Agents
                  - Action Groups
                  - Agent Aliases
                  - Base
                  - Data Source
                  - Actions
                  - Group
                  - Alias
                  - Data
                  - Source
            /knowledgebases/{knowledgeBaseId}:
              PUT:
                summary: UpdateKnowledgeBase
                description: <p>Update an existing knowledge base</p>
                tags:
                  - Update
                  - Knowledge
                  - Base
                  - Identifiers
                  - Agent Versions
                  - Agent
                  - Versions
                  - Knowledgebases
                  - Agents
                  - Action Groups
                  - Agent Aliases
                  - Base
                  - Data Source
                  - Actions
                  - Group
                  - Alias
                  - Data
                  - Source
            /agents/{agentId}/agentversions/{agentVersion}/knowledgebases/{knowledgeBaseId}/:
              PUT:
                summary: UpdateAgentKnowledgeBase
                description: >-
                  <p>Updates an existing Knowledge Base associated to an Amazon
                  Bedrock Agent</p>
                tags:
                  - Update
                  - Agent
                  - Knowledge
                  - Base
                  - Identifiers
                  - Agent Versions
                  - Agent
                  - Versions
                  - Knowledgebases
                  - Agents
                  - Action Groups
                  - Agent Aliases
                  - Base
                  - Data Source
                  - Actions
                  - Group
                  - Alias
                  - Data
                  - Source
                  - Knowledge
            /knowledgebases/{knowledgeBaseId}/datasources/{dataSourceId}/ingestionjobs/{ingestionJobId}:
              GET:
                summary: GetIngestionJob
                description: <p>Get an ingestion job</p>
                tags:
                  - Get
                  - Ingestion
                  - Jobs
                  - Identifiers
                  - Agent Versions
                  - Agent
                  - Versions
                  - Knowledgebases
                  - Agents
                  - Action Groups
                  - Agent Aliases
                  - Base
                  - Data Source
                  - Actions
                  - Group
                  - Alias
                  - Data
                  - Source
                  - Knowledge
                  - Ingestion Jobs
                  - Ingestion
                  - Jobs
            /agents/{agentId}/agentversions/:
              POST:
                summary: ListAgentVersions
                description: <p>Lists Agent Versions</p>
                tags:
                  - Lists
                  - Agent
                  - Versions
                  - Identifiers
                  - Agent Versions
                  - Agent
                  - Versions
                  - Knowledgebases
                  - Agents
                  - Action Groups
                  - Agent Aliases
                  - Base
                  - Data Source
                  - Actions
                  - Group
                  - Alias
                  - Data
                  - Source
                  - Knowledge
                  - Ingestion Jobs
                  - Ingestion
                  - Jobs
            /knowledgebases/{knowledgeBaseId}/datasources/{dataSourceId}/ingestionjobs/:
              PUT:
                summary: StartIngestionJob
                description: <p>Start a new ingestion job</p>
                tags:
                  - Start
                  - Ingestion
                  - Jobs
                  - Identifiers
                  - Agent Versions
                  - Agent
                  - Versions
                  - Knowledgebases
                  - Agents
                  - Action Groups
                  - Agent Aliases
                  - Base
                  - Data Source
                  - Actions
                  - Group
                  - Alias
                  - Data
                  - Source
                  - Knowledge
                  - Ingestion Jobs
                  - Ingestion
                  - Jobs
            /tags/{resourceArn}:
              DELETE:
                summary: UntagResource
                description: <p>Untag a re
                tags:
                  - Untag
                  - Resources
                  - Identifiers
                  - Agent Versions
                  - Agent
                  - Versions
                  - Knowledgebases
                  - Agents
                  - Action Groups
                  - Agent Aliases
                  - Base
                  - Data Source
                  - Actions
                  - Group
                  - Alias
                  - Data
                  - Source
                  - Knowledge
                  - Ingestion Jobs
                  - Ingestion
                  - Jobs
                  - A
    overlays:
      - type: APIs.io Search
        url: overlays/bedrock-agent-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/bedrock-agent-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:bedrock-agent
  - name: FactSet Terms and Conditions API
    description: FactSet Security Reference - Fixed Income Terms & Conditions
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.factset.com/api-catalog/factset-terms-and-conditions-api
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: >-
          https://developer.factset.com/api-catalog/factset-terms-and-conditions-api#overview
      - type: SDKs
        url: >-
          https://developer.factset.com/api-catalog/factset-terms-and-conditions-api#sdkLibrary
      - type: Jupyter Notebooks
        url: >-
          https://developer.factset.com/api-catalog/factset-terms-and-conditions-api#notebooks
      - type: Code Snippets
        url: >-
          https://developer.factset.com/api-catalog/factset-terms-and-conditions-api#codeSnippet
      - type: Change Log
        url: >-
          https://developer.factset.com/api-catalog/factset-terms-and-conditions-api#changelog
      - type: OpenAPI
        data:
          openapi: 3.0.0
          info:
            title: FactSet Terms & Conditions API
            license:
              name: License Information
              url: http://www.factset.com/api/license.html
          tags:
            - name: Terms & Conditions
              description: >-
                Select specific Terms & Conditions fields for a list of Fixed
                Income Security identifiers.
            - name: Issue Size
              description: >-
                Fetch the Fixed Income Issue Details, such as Amount
                Outstanding, Change, and Type.
            - name: Coupons
              description: Coupon History and Schedules
            - name: Covenants
              description: Covenant Details and Negative Covenants
            - name: Redemptions
              description: Redemption Prices
            - name: Agents
              description: Agency Details
            - name: Use of Proceeds
              description: Use of Proceeds raised from Fixed Income Issues
            - name: Underwriters
              description: Lead Underwriter Details
            - name: Convertibles
              description: Convertible Details, History, and Triggers
          paths:
            /factset-terms-and-conditions/v1/terms-and-conditions:
              get:
                summary: >-
                  Return select Terms and Conditions items for a Fixed Income
                  security.
                description: >
                  Returns Terms and Conditions data items for the Fixed Income
                  security. Includes items for Conditional Redemptions,
                  Redemption Options, Security Details, and Coupon Details.

                  Use the `fields` parameter to request specific items only or
                  request an entire category of items to fetch all available
                  fields matching that category(s).

                  <p>*For T&C data related to Agency, Coupon History, Issue
                  Size, Negative Covenants, or Redemption Prices, Lead
                  Underwriters, and Use of Proceeds, please use respective
                  endpoints optimized for that content.*</p>
                tags:
                  - Return
                  - Select
                  - Terms
                  - And
                  - Conditions
                  - Items
                  - For
                  - Fixed
                  - Income
                  - Security.
                  - Factset
                  - Terms
                  - And
                  - Conditions
                  - V1
              post:
                summary: >-
                  Return Terms and Conditions for a list of Fixed Income
                  securities.
                description: >
                  Returns Terms and Conditions data items for the Fixed Income
                  security. Includes reference items for Conditional
                  Redemptions, Redemption Options, Security Details, Convertible
                  Features, and Coupon Details.

                  Use the `fields` parameter to request specific items only or
                  request an entire category of items to fetch all available
                  fields matching that category(s).

                  <p>*For T&C data related to Agency, Coupon History, Issue
                  Size, Negative Covenants, or Redemption Prices, Lead
                  Underwriters, and Use of Proceeds, please use respective
                  endpoints optimized for that content.*</p>
                tags:
                  - Return
                  - Terms
                  - And
                  - Conditions
                  - For
                  - List
                  - Of
                  - Fixed
                  - Income
                  - Securities.
                  - Factset
                  - Terms
                  - And
                  - Conditions
                  - V1
            /factset-terms-and-conditions/v1/fields:
              get:
                summary: Available fields for /terms-and-conditions endpoint
                tags:
                  - Available
                  - Fields
                  - For
                  - /terms-and-conditions
                  - Endpoint
                  - Factset
                  - Terms
                  - And
                  - Conditions
                  - V1
                  - Fields
                description: >
                  Returns a list of available fields that can be used in the
                  `fields`

                  parameter of the **/terms-and-conditions** endpoint.

                  Leave _category_ blank to request all available items.

                  Make Note, this does not represent all available fields within
                  the Terms and Conditions API and all other endpoints.
            /factset-terms-and-conditions/v1/issue-size:
              get:
                summary: Return Issue Size data for a list of Fixed Income securities.
                description: |
                  Returns Issue Size data for the Fixed Income security.
                tags:
                  - Return
                  - Issue
                  - Size
                  - Data
                  - For
                  - List
                  - Of
                  - Fixed
                  - Income
                  - Securities.
                  - Factset
                  - Terms
                  - And
                  - Conditions
                  - V1
                  - Fields
                  - Issue
                  - Size
              post:
                summary: >-
                  Return Issue Size data for a large list of Fixed Income
                  securities.
                description: |
                  Returns Issue Size data for a list of Fixed Income securities.
                tags:
                  - Return
                  - Issue
                  - Size
                  - Data
                  - For
                  - Large
                  - List
                  - Of
                  - Fixed
                  - Income
                  - Securities.
                  - Factset
                  - Terms
                  - And
                  - Conditions
                  - V1
                  - Fields
                  - Issue
                  - Size
            /factset-terms-and-conditions/v1/coupon-history:
              get:
                summary: >-
                  Return historical Coupon information for a Fixed Income
                  security.
                description: >
                  Returns historical Coupon information for the Fixed Income
                  security.
                tags:
                  - Return
                  - Historical
                  - Coupon
                  - Information
                  - For
                  - Fixed
                  - Income
                  - Security.
                  - Factset
                  - Terms
                  - And
                  - Conditions
                  - V1
                  - Fields
                  - Issue
                  - Size
                  - Coupon
                  - History
              post:
                summary: >-
                  Return historical Coupon information for a list of Fixed
                  Income securities.
                description: >
                  Returns historical Coupon information for a list of Fixed
                  Income securities.
                tags:
                  - Return
                  - Historical
                  - Coupon
                  - Information
                  - For
                  - List
                  - Of
                  - Fixed
                  - Income
                  - Securities.
                  - Factset
                  - Terms
                  - And
                  - Conditions
                  - V1
                  - Fields
                  - Issue
                  - Size
                  - Coupon
                  - History
            /factset-terms-and-conditions/v1/coupon-schedules:
              get:
                summary: Return Coupon Sechedules for a Fixed Income security.
                description: >
                  Returns Coupon Schedules information for the Fixed Income
                  security.
                tags:
                  - Return
                  - Coupon
                  - Sechedules
                  - For
                  - Fixed
                  - Income
                  - Security.
                  - Factset
                  - Terms
                  - And
                  - Conditions
                  - V1
                  - Fields
                  - Issue
                  - Size
                  - Coupon
                  - History
                  - Schedules
              post:
                summary: >-
                  Return Coupon Schedules information for a list of Fixed Income
                  securities.
                description: >
                  Returns historical Coupon Schedules information for a list of
                  Fixed Income securities.
                tags:
                  - Return
                  - Coupon
                  - Schedules
                  - Information
                  - For
                  - List
                  - Of
                  - Fixed
                  - Income
                  - Securities.
                  - Factset
                  - Terms
                  - And
                  - Conditions
                  - V1
                  - Fields
                  - Issue
                  - Size
                  - Coupon
                  - History
                  - Schedules
            /factset-terms-and-conditions/v1/covenant-details:
              get:
                summary: Return Covenant Details for a Fixed Income security.
                description: |
                  Returns Covenant Details for the Fixed Income security.
                tags:
                  - Return
                  - Covenant
                  - Details
                  - For
                  - Fixed
                  - Income
                  - Security.
                  - Factset
                  - Terms
                  - And
                  - Conditions
                  - V1
                  - Fields
                  - Issue
                  - Size
                  - Coupon
                  - History
                  - Schedules
                  - Covenant
                  - Details
              post:
                summary: Return Covenant Details for a list of Fixed Income securities.
                description: >
                  Returns Covenant Details for a list of Fixed Income
                  securities.
                tags:
                  - Return
                  - Covenant
                  - Details
                  - For
                  - List
                  - Of
                  - Fixed
                  - Income
                  - Securities.
                  - Factset
                  - Terms
                  - And
                  - Conditions
                  - V1
                  - Fields
                  - Issue
                  - Size
                  - Coupon
                  - History
                  - Schedules
                  - Covenant
                  - Details
            /factset-terms-and-conditions/v1/redemption-prices:
              get:
                summary: Return Redemption Prices for a Fixed Income security.
                description: |
                  Returns Redemption Prices for the Fixed Income security.
                tags:
                  - Return
                  - Redemption
                  - Prices
                  - For
                  - Fixed
                  - Income
                  - Security.
                  - Factset
                  - Terms
                  - And
                  - Conditions
                  - V1
                  - Fields
                  - Issue
                  - Size
                  - Coupon
                  - History
                  - Schedules
                  - Covenant
                  - Details
                  - Redemption
                  - Prices
              post:
                summary: >-
                  Return Redemption Prices for a list of Fixed Income
                  securities.
                description: >
                  Returns Redemption Prices for a list of Fixed Income
                  securities.
                tags:
                  - Return
                  - Redemption
                  - Prices
                  - For
                  - List
                  - Of
                  - Fixed
                  - Income
                  - Securities.
                  - Factset
                  - Terms
                  - And
                  - Conditions
                  - V1
                  - Fields
                  - Issue
                  - Size
                  - Coupon
                  - History
                  - Schedules
                  - Covenant
                  - Details
                  - Redemption
                  - Prices
            /factset-terms-and-conditions/v1/agents:
              get:
                summary: Return Agents items for a Fixed Income security.
                description: |
                  Returns Agents data items for the Fixed Income security.
                tags:
                  - Return
                  - Agents
                  - Items
                  - For
                  - Fixed
                  - Income
                  - Security.
                  - Factset
                  - Terms
                  - And
                  - Conditions
                  - V1
                  - Fields
                  - Issue
                  - Size
                  - Coupon
                  - History
                  - Schedules
                  - Covenant
                  - Details
                  - Redemption
                  - Prices
                  - Agents
              post:
                summary: Return Agents items for a list of Fixed Income securities.
                description: >
                  Returns Agents data items for a list of Fixed Income
                  securities.
                tags:
                  - Return
                  - Agents
                  - Items
                  - For
                  - List
                  - Of
                  - Fixed
                  - Income
                  - Securities.
                  - Factset
                  - Terms
                  - And
                  - Conditions
                  - V1
                  - Fields
                  - Issue
                  - Size
                  - Coupon
                  - History
                  - Schedules
                  - Covenant
                  - Details
                  - Redemption
                  - Prices
                  - Agents
            /factset-terms-and-conditions/v1/lead-underwriters:
              get:
                summary: Return Lead Underwriters for a Fixed Income security.
                description: |
                  Returns Lead Underwriters for the Fixed Income security.
                tags:
                  - Return
                  - Lead
                  - Underwriters
                  - For
                  - Fixed
                  - Income
                  - Security.
                  - Factset
                  - Terms
                  - And
                  - Conditions
                  - V1
                  - Fields
                  - Issue
                  - Size
                  - Coupon
                  - History
                  - Schedules
                  - Covenant
                  - Details
                  - Redemption
                  - Prices
                  - Agents
                  - Lead
                  - Underwriters
              post:
                summary: >-
                  Return Lead Underwriters for a list of Fixed Income
                  securities.
                description: >
                  Returns Lead Underwriters for a list of Fixed Income
                  securities.
                tags:
                  - Return
                  - Lead
                  - Underwriters
                  - For
                  - List
                  - Of
                  - Fixed
                  - Income
                  - Securities.
                  - Factset
                  - Terms
                  - And
                  - Conditions
                  - V1
                  - Fields
                  - Issue
                  - Size
                  - Coupon
                  - History
                  - Schedules
                  - Covenant
                  - Details
                  - Redemption
                  - Prices
                  - Agents
                  - Lead
                  - Underwriters
            /factset-terms-and-conditions/v1/use-of-proceeds:
              get:
                summary: Return Use of Proceeds for a Fixed Income security.
                description: |
                  Returns Use of Proceeds for the Fixed Income security.
                tags:
                  - Return
                  - Use
                  - Of
                  - Proceeds
                  - For
                  - Fixed
                  - Income
                  - Security.
                  - Factset
                  - Terms
                  - And
                  - Conditions
                  - V1
                  - Fields
                  - Issue
                  - Size
                  - Coupon
                  - History
                  - Schedules
                  - Covenant
                  - Details
                  - Redemption
                  - Prices
                  - Agents
                  - Lead
                  - Underwriters
                  - Use
                  - Of
                  - Proceeds
              post:
                summary: Return Use of Proceeds for a list of Fixed Income securities.
                description: |
                  Returns Use of Proceeds for a list of Fixed Income securities.
                tags:
                  - Return
                  - Use
                  - Of
                  - Proceeds
                  - For
                  - List
                  - Fixed
                  - Income
                  - Securities.
                  - Factset
                  - Terms
                  - And
                  - Conditions
                  - V1
                  - Fields
                  - Issue
                  - Size
                  - Coupon
                  - History
                  - Schedules
                  - Covenant
                  - Details
                  - Redemption
                  - Prices
                  - Agents
                  - Lead
                  - Underwriters
                  - Use
                  - Of
                  - Proceeds
            /factset-terms-and-conditions/v1/convertible-details:
              get:
                summary: >-
                  Return Convertible Details for a list of Convertible Fixed
                  Income securities.
                description: >
                  Returns Convertible Details for a list of securities, such as
                  -
                    * Convertible Currency
                    * Convertible Effective Date
                    * Convertible Notice Days Max and Min
                    * Convertible Payment Form
                    * Convertible Payment Details
                    * Convertible Payment Form Election
                    * Convertible Price Method
                    * Convertible Type
                    * Convertibles Ratio
                    * More
                tags:
                  - Return
                  - Convertible
                  - Details
                  - For
                  - List
                  - Of
                  - Fixed
                  - Income
                  - Securities.
                  - Factset
                  - Terms
                  - And
                  - Conditions
                  - V1
                  - Fields
                  - Issue
                  - Size
                  - Coupon
                  - History
                  - Schedules
                  - Covenant
                  - Details
                  - Redemption
                  - Prices
                  - Agents
                  - Lead
                  - Underwriters
                  - Use
                  - Of
                  - Proceeds
                  - Convertible
              post:
                summary: >-
                  Return Convertible Details data for a large list of Fixed
                  Income securities.
                description: >
                  Returns Convertible Details for a list of securities, such as
                  -
                    * Convertible Currency
                    * Convertible Effective Date
                    * Convertible Notice Days Max and Min
                    * Convertible Payment Form
                    * Convertible Payment Details
                    * Convertible Payment Form Election
                    * Convertible Price Method
                    * Convertible Type
                    * Convertibles Ratio
                    * More
                tags:
                  - Return
                  - Convertible
                  - Details
                  - Data
                  - For
                  - Large
                  - List
                  - Of
                  - Fixed
                  - Income
                  - Securities.
                  - Factset
                  - Terms
                  - And
                  - Conditions
                  - V1
                  - Fields
                  - Issue
                  - Size
                  - Coupon
                  - History
                  - Schedules
                  - Covenant
                  - Details
                  - Redemption
                  - Prices
                  - Agents
                  - Lead
                  - Underwriters
                  - Use
                  - Of
                  - Proceeds
                  - Convertible
            /factset-terms-and-conditions/v1/convertible-history:
              get:
                summary: >-
                  Return Convertible History data for a list of Fixed Income
                  securities.
                description: >
                  Returns Convertible History data for the Fixed Income
                  security, including - * Convertibles Price * Convertibles
                  Effective Date
                tags:
                  - Return
                  - Convertible
                  - History
                  - Data
                  - For
                  - List
                  - Of
                  - Fixed
                  - Income
                  - Securities.
                  - Factset
                  - Terms
                  - And
                  - Conditions
                  - V1
                  - Fields
                  - Issue
                  - Size
                  - Coupon
                  - History
                  - Schedules
                  - Covenant
                  - Details
                  - Redemption
                  - Prices
                  - Agents
                  - Lead
                  - Underwriters
                  - Use
                  - Of
                  - Proceeds
                  - Convertible
              post:
                summary: >-
                  Return Convertible History data for a large list of Fixed
                  Income securities.
                description: >
                  Returns Convertible History data for a list of Fixed Income
                  securities.
                tags:
                  - Return
                  - Convertible
                  - History
                  - Data
                  - For
                  - Large
                  - List
                  - Of
                  - Fixed
                  - Income
                  - Securities.
                  - Factset
                  - Terms
                  - And
                  - Conditions
                  - V1
                  - Fields
                  - Issue
                  - Size
                  - Coupon
                  - History
                  - Schedules
                  - Covenant
                  - Details
                  - Redemption
                  - Prices
                  - Agents
                  - Lead
                  - Underwriters
                  - Use
                  - Of
                  - Proceeds
                  - Convertible
            /factset-terms-and-conditions/v1/convertible-triggers:
              get:
                summary: >-
                  Return Convertible Triggers data for a list of Fixed Income
                  securities.
                description: >
                  Returns Convertible Triggers data for the Fixed Income
                  security including the Convertible Trigger Id, Event, and
                  Description.
                tags:
                  - Return
                  - Convertible
                  - Triggers
                  - Data
                  - For
                  - List
                  - Of
                  - Fixed
                  - Income
                  - Securities.
                  - Factset
                  - Terms
                  - And
                  - Conditions
                  - V1
                  - Fields
                  - Issue
                  - Size
                  - Coupon
                  - History
                  - Schedules
                  - Covenant
                  - Details
                  - Redemption
                  - Prices
                  - Agents
                  - Lead
                  - Underwriters
                  - Use
                  - Of
                  - Proceeds
                  - Convertible
                  - Triggers
              post:
                summary: >-
                  Return Convertible Trigger data for a large list of Fixed
                  Income securities.
                description: >
                  Returns Convertible Triggers data for the Fixed Income
                  security including the Convertible Trigger Id, Event, and
                  Description.
                tags:
                  - Return
                  - Convertible
                  - Trigger
                  - Data
                  - For
                  - Large
                  - List
                  - Of
                  - Fixed
                  - Income
                  - Securities.
                  - Factset
                  - Terms
                  - And
                  - Conditions
                  - V1
                  - Fields
                  - Issue
                  - Size
                  - Coupon
                  - History
                  - Schedules
                  - Covenant
                  - Details
                  - Redemption
                  - Prices
                  - Agents
                  - Lead
                  - Underwriters
                  - Use
                  - Of
                  - Proceeds
                  - Convertible
                  - Trigge
    overlays:
      - type: APIs.io Search
        url: overlays/terms-and-conditions-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/terms-and-conditions-openapi-api-evangelist-ratings.yml
    aid: factset:factset-terms-and-conditions-api
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---