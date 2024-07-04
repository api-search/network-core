---
name: Bases
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/bases.png
url: https://example.com/apis/bases.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Bases
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
  - name: qconnect
    description: >-
      <note> <p> <b>Powered by Amazon Bedrock</b>: Amazon Web Services
      implements <a
      href="https://docs.aws.amazon.com/bedrock/latest/userguide/abuse-detection.html">automated
      abuse detection</a>. Because Amazon Q in Connect is built on Amazon
      Bedrock, users can take full advantage of the controls implemented in
      Amazon Bedrock to enforce safety, security, and the responsible use of
      artificial intelligence (AI).</p> </note> <p>Amazon Q in Connect is a
      generative AI customer service assistant. It is an LLM-enhanced evolution
      of Amazon Connect Wisdom that delivers real-time recommendations to help
      contact center agents resolve customer issues quickly and accurately.</p>
      <p>Amazon Q automatically detects customer intent during calls and chats
      using conversational analytics and natural language understanding (NLU).
      It then provides agents with immediate, real-time generative responses and
      suggested actions, and links to relevant documents and articles. Agents
      can also query Amazon Q directly using natural language or keywords to
      answer customer requests.</p> <p>Use the Amazon Q in Connect APIs to
      create an assistant and a knowledge base, for example, or manage content
      by uploading custom files.</p> <p>For more information, see <a
      href="https://docs.aws.amazon.com/connect/latest/adminguide/amazon-q-connect.html">Use
      Amazon Q in Connect for generative AI powered agent assistance in
      real-time</a> in the <i>Amazon Connect Administrator Guide</i>.</p>
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
            title: qconnect
          paths:
            /assistants:
              GET:
                summary: ListAssistants
                description: <p>Lists information about assistants.</p>
                tags:
                  - Lists
                  - Assistants
                  - Assistants
            /assistants/{assistantId}/associations:
              GET:
                summary: ListAssistantAssociations
                description: <p>Lists information about assistant associations.</p>
                tags:
                  - Lists
                  - Assistants
                  - Associations
                  - Assistants
                  - Identifiers
                  - Associations
            /knowledgeBases/{knowledgeBaseId}/contents:
              GET:
                summary: ListContents
                description: <p>Lists the content.</p>
                tags:
                  - Lists
                  - Contents
                  - Assistants
                  - Identifiers
                  - Associations
                  - Bases
                  - Knowledge
                  - Base
                  - Contents
            /knowledgeBases:
              GET:
                summary: ListKnowledgeBases
                description: <p>Lists the knowledge bases.</p>
                tags:
                  - Lists
                  - Knowledge
                  - Bases
                  - Assistants
                  - Identifiers
                  - Associations
                  - Bases
                  - Knowledge
                  - Base
                  - Contents
            /knowledgeBases/{knowledgeBaseId}/quickResponses:
              GET:
                summary: ListQuickResponses
                description: <p>Lists information about quick response.</p>
                tags:
                  - Lists
                  - Quick
                  - Responses
                  - Assistants
                  - Identifiers
                  - Associations
                  - Bases
                  - Knowledge
                  - Base
                  - Contents
                  - Quick
                  - Responses
            /assistants/{assistantId}/sessions:
              POST:
                summary: CreateSession
                description: >-
                  <p>Creates a session. A session is a contextual container used
                  for generating recommendations. Amazon Connect creates a new
                  Amazon Q session for each contact on which Amazon Q is
                  enabled.</p>
                tags:
                  - Create
                  - Sessions
                  - Assistants
                  - Identifiers
                  - Associations
                  - Bases
                  - Knowledge
                  - Base
                  - Contents
                  - Quick
                  - Responses
                  - Sessions
            /assistants/{assistantId}:
              GET:
                summary: GetAssistant
                description: <p>Retrieves information about an assistant.</p>
                tags:
                  - Get
                  - Assistants
                  - Assistants
                  - Identifiers
                  - Associations
                  - Bases
                  - Knowledge
                  - Base
                  - Contents
                  - Quick
                  - Responses
                  - Sessions
            /assistants/{assistantId}/associations/{assistantAssociationId}:
              GET:
                summary: GetAssistantAssociation
                description: <p>Retrieves information about an assistant association.</p>
                tags:
                  - Get
                  - Assistants
                  - Association
                  - Assistants
                  - Identifiers
                  - Associations
                  - Bases
                  - Knowledge
                  - Base
                  - Contents
                  - Quick
                  - Responses
                  - Sessions
                  - Assistants
                  - Association
            /knowledgeBases/{knowledgeBaseId}/contents/{contentId}:
              POST:
                summary: UpdateContent
                description: <p>Updates information about the content.</p>
                tags:
                  - Update
                  - Content
                  - Assistants
                  - Identifiers
                  - Associations
                  - Bases
                  - Knowledge
                  - Base
                  - Contents
                  - Quick
                  - Responses
                  - Sessions
                  - Assistants
                  - Association
                  - Content
            /knowledgeBases/{knowledgeBaseId}/importJobs/{importJobId}:
              GET:
                summary: GetImportJob
                description: <p>Retrieves the started import job.</p>
                tags:
                  - Get
                  - Import
                  - Jobs
                  - Assistants
                  - Identifiers
                  - Associations
                  - Bases
                  - Knowledge
                  - Base
                  - Contents
                  - Quick
                  - Responses
                  - Sessions
                  - Assistants
                  - Association
                  - Content
                  - Import
                  - Jobs
                  - Jobs
            /knowledgeBases/{knowledgeBaseId}:
              GET:
                summary: GetKnowledgeBase
                description: <p>Retrieves information about the knowledge base.</p>
                tags:
                  - Get
                  - Knowledge
                  - Base
                  - Assistants
                  - Identifiers
                  - Associations
                  - Bases
                  - Knowledge
                  - Base
                  - Contents
                  - Quick
                  - Responses
                  - Sessions
                  - Assistants
                  - Association
                  - Content
                  - Import
                  - Jobs
                  - Jobs
            /knowledgeBases/{knowledgeBaseId}/quickResponses/{quickResponseId}:
              POST:
                summary: UpdateQuickResponse
                description: <p>Updates an existing Amazon Q quick response.</p>
                tags:
                  - Update
                  - Quick
                  - Responses
                  - Assistants
                  - Identifiers
                  - Associations
                  - Bases
                  - Knowledge
                  - Base
                  - Contents
                  - Quick
                  - Responses
                  - Sessions
                  - Assistants
                  - Association
                  - Content
                  - Import
                  - Jobs
                  - Jobs
                  - Responses
            /knowledgeBases/{knowledgeBaseId}/contents/{contentId}/summary:
              GET:
                summary: GetContentSummary
                description: <p>Retrieves summary information about the content.</p>
                tags:
                  - Get
                  - Content
                  - Summaries
                  - Assistants
                  - Identifiers
                  - Associations
                  - Bases
                  - Knowledge
                  - Base
                  - Contents
                  - Quick
                  - Responses
                  - Sessions
                  - Assistants
                  - Association
                  - Content
                  - Import
                  - Jobs
                  - Jobs
                  - Responses
                  - Summaries
            /assistants/{assistantId}/sessions/{sessionId}/recommendations:
              GET:
                summary: GetRecommendations
                description: >-
                  <p>Retrieves recommendations for the specified session. To
                  avoid retrieving the same recommendations in subsequent calls,
                  use <a
                  href="https://docs.aws.amazon.com/amazon-q-connect/latest/APIReference/API_NotifyRecommendationsReceived.html">NotifyRecommendationsReceived</a>.
                  This API supports long-polling behavior with the
                  <code>waitTimeSeconds</code> parameter. Short poll is the
                  default behavior and only returns recommendations already
                  available. To perform a manual query against an assistant, use
                  <a
                  href="https://docs.aws.amazon.com/amazon-q-connect/latest/APIReference/API_QueryAssistant.html">QueryAssistant</a>.</p>
                tags:
                  - Get
                  - Recommendations
                  - Assistants
                  - Identifiers
                  - Associations
                  - Bases
                  - Knowledge
                  - Base
                  - Contents
                  - Quick
                  - Responses
                  - Sessions
                  - Assistants
                  - Association
                  - Content
                  - Import
                  - Jobs
                  - Jobs
                  - Responses
                  - Summaries
                  - Sessions
                  - Recommendations
            /assistants/{assistantId}/sessions/{sessionId}:
              GET:
                summary: GetSession
                description: <p>Retrieves information for a specified session.</p>
                tags:
                  - Get
                  - Sessions
                  - Assistants
                  - Identifiers
                  - Associations
                  - Bases
                  - Knowledge
                  - Base
                  - Contents
                  - Quick
                  - Responses
                  - Sessions
                  - Assistants
                  - Association
                  - Content
                  - Import
                  - Jobs
                  - Jobs
                  - Responses
                  - Summaries
                  - Sessions
                  - Recommendations
            /knowledgeBases/{knowledgeBaseId}/importJobs:
              POST:
                summary: StartImportJob
                description: >-
                  <p>Start an asynchronous job to import Amazon Q resources from
                  an uploaded source file. Before calling this API, use <a
                  href="https://docs.aws.amazon.com/wisdom/latest/APIReference/API_StartContentUpload.html">StartContentUpload</a>
                  to upload an asset that contains the resource data.</p> <ul>
                  <li> <p>For importing Amazon Q quick responses, you need to
                  upload a csv file including the quick responses. For
                  information about how to format the csv file for importing
                  quick responses, see <a
                  href="https://docs.aws.amazon.com/console/connect/quick-responses/add-data">Import
                  quick responses</a>.</p> </li> </ul>
                tags:
                  - Start
                  - Import
                  - Jobs
                  - Assistants
                  - Identifiers
                  - Associations
                  - Bases
                  - Knowledge
                  - Base
                  - Contents
                  - Quick
                  - Responses
                  - Sessions
                  - Assistants
                  - Association
                  - Content
                  - Import
                  - Jobs
                  - Jobs
                  - Responses
                  - Summaries
                  - Sessions
                  - Recommendations
            /tags/{resourceArn}:
              DELETE:
                summary: UntagResource
                description: <p>Removes the specified tags from the specified resource.</p>
                tags:
                  - Untag
                  - Resources
                  - Assistants
                  - Identifiers
                  - Associations
                  - Bases
                  - Knowledge
                  - Base
                  - Contents
                  - Quick
                  - Responses
                  - Sessions
                  - Assistants
                  - Association
                  - Content
                  - Import
                  - Jobs
                  - Jobs
                  - Responses
                  - Summaries
                  - Sessions
                  - Recommendations
                  - ARN
            /assistants/{assistantId}/sessions/{sessionId}/recommendations/notify:
              POST:
                summary: NotifyRecommendationsReceived
                description: >-
                  <p>Removes the specified recommendations from the specified
                  assistant's queue of newly available recommendations. You can
                  use this API in conjunction with <a
                  href="https://docs.aws.amazon.com/amazon-q-connect/latest/APIReference/API_GetRecommendations.html">GetRecommendations</a>
                  and a <code>waitTimeSeconds</code> input for long-polling
                  behavior and avoiding duplicate recommendations.</p>
                tags:
                  - Notify
                  - Recommendations
                  - Received
                  - Assistants
                  - Identifiers
                  - Associations
                  - Bases
                  - Knowledge
                  - Base
                  - Contents
                  - Quick
                  - Responses
                  - Sessions
                  - Assistants
                  - Association
                  - Content
                  - Import
                  - Jobs
                  - Jobs
                  - Responses
                  - Summaries
                  - Sessions
                  - Recommendations
                  - ARN
                  - Notify
            /assistants/{assistantId}/feedback:
              PUT:
                summary: PutFeedback
                description: >-
                  <p>Provides feedback against the specified assistant for the
                  specified target. This API only supports generative
                  targets.</p>
                tags:
                  - Put
                  - Feedback
                  - Assistants
                  - Identifiers
                  - Associations
                  - Bases
                  - Knowledge
                  - Base
                  - Contents
                  - Quick
                  - Responses
                  - Sessions
                  - Assistants
                  - Association
                  - Content
                  - Import
                  - Jobs
                  - Jobs
                  - Responses
                  - Summaries
                  - Sessions
                  - Recommendations
                  - ARN
                  - Notify
                  - Feedback
            /assistants/{assistantId}/query:
              POST:
                summary: QueryAssistant
                description: >-
                  <p>Performs a manual search against the specified assistant.
                  To retrieve recommendations for an assistant, use <a
                  href="https://docs.aws.amazon.com/amazon-q-connect/latest/APIReference/API_GetRecommendations.html">GetRecommendations</a>.
                  </p>
                tags:
                  - Queries
                  - Assistants
                  - Assistants
                  - Identifiers
                  - Associations
                  - Bases
                  - Knowledge
                  - Base
                  - Contents
                  - Quick
                  - Responses
                  - Sessions
                  - Assistants
                  - Association
                  - Content
                  - Import
                  - Jobs
                  - Jobs
                  - Responses
                  - Summaries
                  - Sessions
                  - Recommendations
                  - ARN
                  - Notify
                  - Feedback
                  - Queries
            /knowledgeBases/{knowledgeBaseId}/templateUri:
              POST:
                summary: UpdateKnowledgeBaseTemplateUri
                description: >-
                  <p>Updates the template URI of a knowledge base. This is only
                  supported for knowledge bases of type EXTERNAL. Include a
                  single variable in <code>${variable}</code> format; this
                  interpolated by Amazon Q using ingested content. For example,
                  if you ingest a Salesforce article, it has an <code>Id</code>
                  value, and you can set the template URI to
                  <code>https://myInstanceName.lightning.force.com/lightning/r/Knowledge__kav/*${Id}*/view</code>.
                  </p>
                tags:
                  - Update
                  - Knowledge
                  - Base
                  - Templates
                  - URI
                  - Assistants
                  - Identifiers
                  - Associations
                  - Bases
                  - Knowledge
                  - Base
                  - Contents
                  - Quick
                  - Responses
                  - Sessions
                  - Assistants
                  - Association
                  - Content
                  - Import
                  - Jobs
                  - Jobs
                  - Responses
                  - Summaries
                  - Sessions
                  - Recommendations
                  - ARN
                  - Notify
                  - Feedback
                  - Queries
                  - Templates
                  - URI
            /knowledgeBases/{knowledgeBaseId}/search:
              POST:
                summary: SearchContent
                description: >-
                  <p>Searches for content in a specified knowledge base. Can be
                  used to get a specific content resource by its name.</p>
                tags:
                  - Search
                  - Content
                  - Assistants
                  - Identifiers
                  - Associations
                  - Bases
                  - Knowledge
                  - Base
                  - Contents
                  - Quick
                  - Responses
                  - Sessions
                  - Assistants
                  - Association
                  - Content
                  - Import
                  - Jobs
                  - Jobs
                  - Responses
                  - Summaries
                  - Sessions
                  - Recommendations
                  - ARN
                  - Notify
                  - Feedback
                  - Queries
                  - Templates
                  - URI
                  - Search
            /knowledgeBases/{knowledgeBaseId}/search/quickResponses:
              POST:
                summary: SearchQuickResponses
                description: >-
                  <p>Searches existing Amazon Q quick responses in an Amazon Q
                  knowledge base.</p>
                tags:
                  - Search
                  - Quick
                  - Responses
                  - Assistants
                  - Identifiers
                  - Associations
                  - Bases
                  - Knowledge
                  - Base
                  - Contents
                  - Quick
                  - Responses
                  - Sessions
                  - Assistants
                  - Association
                  - Content
                  - Import
                  - Jobs
                  - Jobs
                  - Responses
                  - Summaries
                  - Sessions
                  - Recommendations
                  - ARN
                  - Notify
                  - Feedback
                  - Queries
                  - Templates
                  - URI
                  - Search
            /assistants/{assistantId}/searchSessions:
              POST:
                summary: SearchSessions
                description: <p>Searches for sessions.</p>
                tags:
                  - Search
                  - Sessions
                  - Assistants
                  - Identifiers
                  - Associations
                  - Bases
                  - Knowledge
                  - Base
                  - Contents
                  - Quick
                  - Responses
                  - Sessions
                  - Assistants
                  - Association
                  - Content
                  - Import
                  - Jobs
                  - Jobs
                  - Responses
                  - Summaries
                  - Sessions
                  - Recommendations
                  - ARN
                  - Notify
                  - Feedback
                  - Queries
                  - Templates
                  - URI
                  - Search
            /knowledgeBases/{knowledgeBaseId}/upload:
              POST:
                summary: StartContentUpload
                description: >-
                  <p>Get a URL to upload content to a knowledge base. To upload
                  content, first make a PUT request to the returned URL with
                  your file, making sure to include the required headers. Then
                  use <a
                  href="https://docs.aws.amazon.com/amazon-q-connect/latest/APIReference/API_CreateContent.html">CreateContent</a>
                  to finalize the content creation process or <a
                  href="https://docs.aws.amazon.com/amazon-q-connect/latest/APIReference/API_UpdateContent.html">UpdateContent</a>
                  to modify an existing resource. You can only upload content to
                  a knowledge base of type C
                tags:
                  - Start
                  - Content
                  - Uploads
                  - Assistants
                  - Identifiers
                  - Associations
                  - Bases
                  - Knowledge
                  - Base
                  - Contents
                  - Quick
                  - Responses
                  - Sessions
                  - Assistants
                  - Association
                  - Content
                  - Import
                  - Jobs
                  - Jobs
                  - Responses
                  - Summaries
                  - Sessions
                  - Recommendations
                  - ARN
                  - Notify
                  - Feedback
                  - Queries
                  - Templates
                  - URI
                  - Search
                  - Uplo
    overlays:
      - type: APIs.io Search
        url: overlays/qconnect-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/qconnect-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:qconnect
  - name: wisdom
    description: >-
      <p>Amazon Connect Wisdom delivers agents the information they need to
      solve customer issues as they're actively speaking with customers. Agents
      can search across connected repositories from within their agent desktop
      to find answers quickly. Use Amazon Connect Wisdom to create an assistant
      and a knowledge base, for example, or manage content by uploading custom
      files.</p>
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
            title: wisdom
          paths:
            /assistants:
              GET:
                summary: ListAssistants
                description: <p>Lists information about assistants.</p>
                tags:
                  - Lists
                  - Assistants
                  - Assistants
            /assistants/{assistantId}/associations:
              GET:
                summary: ListAssistantAssociations
                description: <p>Lists information about assistant associations.</p>
                tags:
                  - Lists
                  - Assistants
                  - Associations
                  - Assistants
                  - Identifiers
                  - Associations
            /knowledgeBases/{knowledgeBaseId}/contents:
              GET:
                summary: ListContents
                description: <p>Lists the content.</p>
                tags:
                  - Lists
                  - Contents
                  - Assistants
                  - Identifiers
                  - Associations
                  - Bases
                  - Knowledge
                  - Base
                  - Contents
            /knowledgeBases:
              GET:
                summary: ListKnowledgeBases
                description: <p>Lists the knowledge bases.</p>
                tags:
                  - Lists
                  - Knowledge
                  - Bases
                  - Assistants
                  - Identifiers
                  - Associations
                  - Bases
                  - Knowledge
                  - Base
                  - Contents
            /knowledgeBases/{knowledgeBaseId}/quickResponses:
              GET:
                summary: ListQuickResponses
                description: <p>Lists information about quick response.</p>
                tags:
                  - Lists
                  - Quick
                  - Responses
                  - Assistants
                  - Identifiers
                  - Associations
                  - Bases
                  - Knowledge
                  - Base
                  - Contents
                  - Quick
                  - Responses
            /assistants/{assistantId}/sessions:
              POST:
                summary: CreateSession
                description: >-
                  <p>Creates a session. A session is a contextual container used
                  for generating recommendations. Amazon Connect creates a new
                  Wisdom session for each contact on which Wisdom is
                  enabled.</p>
                tags:
                  - Create
                  - Sessions
                  - Assistants
                  - Identifiers
                  - Associations
                  - Bases
                  - Knowledge
                  - Base
                  - Contents
                  - Quick
                  - Responses
                  - Sessions
            /assistants/{assistantId}:
              GET:
                summary: GetAssistant
                description: <p>Retrieves information about an assistant.</p>
                tags:
                  - Get
                  - Assistants
                  - Assistants
                  - Identifiers
                  - Associations
                  - Bases
                  - Knowledge
                  - Base
                  - Contents
                  - Quick
                  - Responses
                  - Sessions
            /assistants/{assistantId}/associations/{assistantAssociationId}:
              GET:
                summary: GetAssistantAssociation
                description: <p>Retrieves information about an assistant association.</p>
                tags:
                  - Get
                  - Assistants
                  - Association
                  - Assistants
                  - Identifiers
                  - Associations
                  - Bases
                  - Knowledge
                  - Base
                  - Contents
                  - Quick
                  - Responses
                  - Sessions
                  - Assistants
                  - Association
            /knowledgeBases/{knowledgeBaseId}/contents/{contentId}:
              POST:
                summary: UpdateContent
                description: <p>Updates information about the content.</p>
                tags:
                  - Update
                  - Content
                  - Assistants
                  - Identifiers
                  - Associations
                  - Bases
                  - Knowledge
                  - Base
                  - Contents
                  - Quick
                  - Responses
                  - Sessions
                  - Assistants
                  - Association
                  - Content
            /knowledgeBases/{knowledgeBaseId}/importJobs/{importJobId}:
              GET:
                summary: GetImportJob
                description: <p>Retrieves the started import job.</p>
                tags:
                  - Get
                  - Import
                  - Jobs
                  - Assistants
                  - Identifiers
                  - Associations
                  - Bases
                  - Knowledge
                  - Base
                  - Contents
                  - Quick
                  - Responses
                  - Sessions
                  - Assistants
                  - Association
                  - Content
                  - Import
                  - Jobs
                  - Jobs
            /knowledgeBases/{knowledgeBaseId}:
              GET:
                summary: GetKnowledgeBase
                description: <p>Retrieves information about the knowledge base.</p>
                tags:
                  - Get
                  - Knowledge
                  - Base
                  - Assistants
                  - Identifiers
                  - Associations
                  - Bases
                  - Knowledge
                  - Base
                  - Contents
                  - Quick
                  - Responses
                  - Sessions
                  - Assistants
                  - Association
                  - Content
                  - Import
                  - Jobs
                  - Jobs
            /knowledgeBases/{knowledgeBaseId}/quickResponses/{quickResponseId}:
              POST:
                summary: UpdateQuickResponse
                description: <p>Updates an existing Wisdom quick response.</p>
                tags:
                  - Update
                  - Quick
                  - Responses
                  - Assistants
                  - Identifiers
                  - Associations
                  - Bases
                  - Knowledge
                  - Base
                  - Contents
                  - Quick
                  - Responses
                  - Sessions
                  - Assistants
                  - Association
                  - Content
                  - Import
                  - Jobs
                  - Jobs
                  - Responses
            /knowledgeBases/{knowledgeBaseId}/contents/{contentId}/summary:
              GET:
                summary: GetContentSummary
                description: <p>Retrieves summary information about the content.</p>
                tags:
                  - Get
                  - Content
                  - Summaries
                  - Assistants
                  - Identifiers
                  - Associations
                  - Bases
                  - Knowledge
                  - Base
                  - Contents
                  - Quick
                  - Responses
                  - Sessions
                  - Assistants
                  - Association
                  - Content
                  - Import
                  - Jobs
                  - Jobs
                  - Responses
                  - Summaries
            /assistants/{assistantId}/sessions/{sessionId}/recommendations:
              GET:
                summary: GetRecommendations
                description: >-
                  <p>Retrieves recommendations for the specified session. To
                  avoid retrieving the same recommendations in subsequent calls,
                  use <a
                  href="https://docs.aws.amazon.com/wisdom/latest/APIReference/API_NotifyRecommendationsReceived.html">NotifyRecommendationsReceived</a>.
                  This API supports long-polling behavior with the
                  <code>waitTimeSeconds</code> parameter. Short poll is the
                  default behavior and only returns recommendations already
                  available. To perform a manual query against an assistant, use
                  <a
                  href="https://docs.aws.amazon.com/wisdom/latest/APIReference/API_QueryAssistant.html">QueryAssistant</a>.</p>
                tags:
                  - Get
                  - Recommendations
                  - Assistants
                  - Identifiers
                  - Associations
                  - Bases
                  - Knowledge
                  - Base
                  - Contents
                  - Quick
                  - Responses
                  - Sessions
                  - Assistants
                  - Association
                  - Content
                  - Import
                  - Jobs
                  - Jobs
                  - Responses
                  - Summaries
                  - Sessions
                  - Recommendations
            /assistants/{assistantId}/sessions/{sessionId}:
              GET:
                summary: GetSession
                description: <p>Retrieves information for a specified session.</p>
                tags:
                  - Get
                  - Sessions
                  - Assistants
                  - Identifiers
                  - Associations
                  - Bases
                  - Knowledge
                  - Base
                  - Contents
                  - Quick
                  - Responses
                  - Sessions
                  - Assistants
                  - Association
                  - Content
                  - Import
                  - Jobs
                  - Jobs
                  - Responses
                  - Summaries
                  - Sessions
                  - Recommendations
            /knowledgeBases/{knowledgeBaseId}/importJobs:
              POST:
                summary: StartImportJob
                description: >-
                  <p>Start an asynchronous job to import Wisdom resources from
                  an uploaded source file. Before calling this API, use <a
                  href="https://docs.aws.amazon.com/wisdom/latest/APIReference/API_StartContentUpload.html">StartContentUpload</a>
                  to upload an asset that contains the resource data.</p> <ul>
                  <li> <p>For importing Wisdom quick responses, you need to
                  upload a csv file including the quick responses. For
                  information about how to format the csv file for importing
                  quick responses, see <a
                  href="https://docs.aws.amazon.com/console/connect/quick-responses/add-data">Import
                  quick responses</a>.</p> </li> </ul>
                tags:
                  - Start
                  - Import
                  - Jobs
                  - Assistants
                  - Identifiers
                  - Associations
                  - Bases
                  - Knowledge
                  - Base
                  - Contents
                  - Quick
                  - Responses
                  - Sessions
                  - Assistants
                  - Association
                  - Content
                  - Import
                  - Jobs
                  - Jobs
                  - Responses
                  - Summaries
                  - Sessions
                  - Recommendations
            /tags/{resourceArn}:
              DELETE:
                summary: UntagResource
                description: <p>Removes the specified tags from the specified resource.</p>
                tags:
                  - Untag
                  - Resources
                  - Assistants
                  - Identifiers
                  - Associations
                  - Bases
                  - Knowledge
                  - Base
                  - Contents
                  - Quick
                  - Responses
                  - Sessions
                  - Assistants
                  - Association
                  - Content
                  - Import
                  - Jobs
                  - Jobs
                  - Responses
                  - Summaries
                  - Sessions
                  - Recommendations
                  - ARN
            /assistants/{assistantId}/sessions/{sessionId}/recommendations/notify:
              POST:
                summary: NotifyRecommendationsReceived
                description: >-
                  <p>Removes the specified recommendations from the specified
                  assistant's queue of newly available recommendations. You can
                  use this API in conjunction with <a
                  href="https://docs.aws.amazon.com/wisdom/latest/APIReference/API_GetRecommendations.html">GetRecommendations</a>
                  and a <code>waitTimeSeconds</code> input for long-polling
                  behavior and avoiding duplicate recommendations.</p>
                tags:
                  - Notify
                  - Recommendations
                  - Received
                  - Assistants
                  - Identifiers
                  - Associations
                  - Bases
                  - Knowledge
                  - Base
                  - Contents
                  - Quick
                  - Responses
                  - Sessions
                  - Assistants
                  - Association
                  - Content
                  - Import
                  - Jobs
                  - Jobs
                  - Responses
                  - Summaries
                  - Sessions
                  - Recommendations
                  - ARN
                  - Notify
            /assistants/{assistantId}/query:
              POST:
                summary: QueryAssistant
                description: >-
                  <p>Performs a manual search against the specified assistant.
                  To retrieve recommendations for an assistant, use <a
                  href="https://docs.aws.amazon.com/wisdom/latest/APIReference/API_GetRecommendations.html">GetRecommendations</a>.
                  </p>
                tags:
                  - Queries
                  - Assistants
                  - Assistants
                  - Identifiers
                  - Associations
                  - Bases
                  - Knowledge
                  - Base
                  - Contents
                  - Quick
                  - Responses
                  - Sessions
                  - Assistants
                  - Association
                  - Content
                  - Import
                  - Jobs
                  - Jobs
                  - Responses
                  - Summaries
                  - Sessions
                  - Recommendations
                  - ARN
                  - Notify
                  - Queries
            /knowledgeBases/{knowledgeBaseId}/templateUri:
              POST:
                summary: UpdateKnowledgeBaseTemplateUri
                description: >-
                  <p>Updates the template URI of a knowledge base. This is only
                  supported for knowledge bases of type EXTERNAL. Include a
                  single variable in <code>${variable}</code> format; this
                  interpolated by Wisdom using ingested content. For example, if
                  you ingest a Salesforce article, it has an <code>Id</code>
                  value, and you can set the template URI to
                  <code>https://myInstanceName.lightning.force.com/lightning/r/Knowledge__kav/*${Id}*/view</code>.
                  </p>
                tags:
                  - Update
                  - Knowledge
                  - Base
                  - Templates
                  - URI
                  - Assistants
                  - Identifiers
                  - Associations
                  - Bases
                  - Knowledge
                  - Base
                  - Contents
                  - Quick
                  - Responses
                  - Sessions
                  - Assistants
                  - Association
                  - Content
                  - Import
                  - Jobs
                  - Jobs
                  - Responses
                  - Summaries
                  - Sessions
                  - Recommendations
                  - ARN
                  - Notify
                  - Queries
                  - Templates
                  - URI
            /knowledgeBases/{knowledgeBaseId}/search:
              POST:
                summary: SearchContent
                description: >-
                  <p>Searches for content in a specified knowledge base. Can be
                  used to get a specific content resource by its name.</p>
                tags:
                  - Search
                  - Content
                  - Assistants
                  - Identifiers
                  - Associations
                  - Bases
                  - Knowledge
                  - Base
                  - Contents
                  - Quick
                  - Responses
                  - Sessions
                  - Assistants
                  - Association
                  - Content
                  - Import
                  - Jobs
                  - Jobs
                  - Responses
                  - Summaries
                  - Sessions
                  - Recommendations
                  - ARN
                  - Notify
                  - Queries
                  - Templates
                  - URI
                  - Search
            /knowledgeBases/{knowledgeBaseId}/search/quickResponses:
              POST:
                summary: SearchQuickResponses
                description: >-
                  <p>Searches existing Wisdom quick responses in a Wisdom
                  knowledge base.</p>
                tags:
                  - Search
                  - Quick
                  - Responses
                  - Assistants
                  - Identifiers
                  - Associations
                  - Bases
                  - Knowledge
                  - Base
                  - Contents
                  - Quick
                  - Responses
                  - Sessions
                  - Assistants
                  - Association
                  - Content
                  - Import
                  - Jobs
                  - Jobs
                  - Responses
                  - Summaries
                  - Sessions
                  - Recommendations
                  - ARN
                  - Notify
                  - Queries
                  - Templates
                  - URI
                  - Search
            /assistants/{assistantId}/searchSessions:
              POST:
                summary: SearchSessions
                description: <p>Searches for sessions.</p>
                tags:
                  - Search
                  - Sessions
                  - Assistants
                  - Identifiers
                  - Associations
                  - Bases
                  - Knowledge
                  - Base
                  - Contents
                  - Quick
                  - Responses
                  - Sessions
                  - Assistants
                  - Association
                  - Content
                  - Import
                  - Jobs
                  - Jobs
                  - Responses
                  - Summaries
                  - Sessions
                  - Recommendations
                  - ARN
                  - Notify
                  - Queries
                  - Templates
                  - URI
                  - Search
            /knowledgeBases/{knowledgeBaseId}/upload:
              POST:
                summary: StartContentUpload
                description: >-
                  <p>Get a URL to upload content to a knowledge base. To upload
                  content, first make a PUT request to the returned URL with
                  your file, making sure to include the required headers. Then
                  use <a
                  href="https://docs.aws.amazon.com/wisdom/latest/APIReference/API_CreateContent.html">CreateContent</a>
                  to finalize the content creation process or <a
                  href="https://docs.aws.amazon.com/wisdom/latest/APIReference/API_UpdateContent.html">UpdateContent</a>
                  to modify an existing resource. You can only upload content to
                  a knowledge base of type C
                tags:
                  - Start
                  - Content
                  - Uploads
                  - Assistants
                  - Identifiers
                  - Associations
                  - Bases
                  - Knowledge
                  - Base
                  - Contents
                  - Quick
                  - Responses
                  - Sessions
                  - Assistants
                  - Association
                  - Content
                  - Import
                  - Jobs
                  - Jobs
                  - Responses
                  - Summaries
                  - Sessions
                  - Recommendations
                  - ARN
                  - Notify
                  - Queries
                  - Templates
                  - URI
                  - Search
                  - Uplo
    overlays:
      - type: APIs.io Search
        url: overlays/wisdom-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/wisdom-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:wisdom
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---