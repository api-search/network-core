---
name: Assistants
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/assistants.png
url: https://example.com/apis/assistants.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Assistants
apis:
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
  - name: OpenAI Assistants API
    description: >-
      The Assistants API allows you to build AI assistants within your own
      applications. An Assistant has instructions and can leverage models,
      tools, and knowledge to respond to user queries. The Assistants API
      currently supports three types of tools - Code Interpreter, Retrieval, and
      Function calling. In the future, we plan to release more OpenAI-built
      tools, and allow you to provide your own tools on our platform.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://platform.openai.com/docs/assistants/overview
    baseURL: https://platform.openai.com/
    tags: []
    properties:
      - type: Documentation
        url: https://platform.openai.com/docs/api-reference
      - type: OpenAPI
        data:
          openapi: 3.0.0
          info:
            title: OpenAI Assistants
            license:
              name: MIT
              url: https://github.com/openai/openai-openapi/blob/master/LICENSE
          tags:
            - name: Assistants
              description: Build Assistants that can call models and use tools.
          paths:
            /assistants:
              get:
                tags:
                  - Returns
                  - List
                  - Of
                  - Assistants.
                  - Assistants
                summary: Returns a list of assistants.
              post:
                tags:
                  - Create
                  - An
                  - Assistant
                  - With
                  - Model
                  - And
                  - Instructions.
                  - Assistants
                summary: Create an assistant with a model and instructions.
            /assistants/{assistant_id}:
              get:
                tags:
                  - Retrieves
                  - An
                  - Assistant.
                  - Assistants
                  - Assistant_id
                summary: Retrieves an assistant.
              post:
                tags:
                  - Modifies
                  - An
                  - Assistant.
                  - Assistants
                  - Assistant_id
                summary: Modifies an assistant.
              delete:
                tags:
                  - Delete
                  - An
                  - Assistant.
                  - Assistants
                  - Assistant_id
                summary: Delete an assistant.
            /assistants/{assistant_id}/files:
              get:
                tags:
                  - Returns
                  - List
                  - Of
                  - Assistant
                  - Files.
                  - Assistants
                  - Assistant_id
                  - Files
                summary: Returns a list of assistant files.
              post:
                tags:
                  - Create
                  - An
                  - Assistant
                  - File
                  - By
                  - Attaching
                  - File](/docs/api-reference/files)
                  - To
                  - '[assistant](/docs/api-reference/assistants).'
                  - Assistants
                  - Assistant_id
                  - Files
                summary: >-
                  Create an assistant file by attaching a
                  [File](/docs/api-reference/files) to an
                  [assistant](/docs/api-reference/assistants).
            /assistants/{assistant_id}/files/{file_id}:
              get:
                tags:
                  - Retrieves
                  - An
                  - Assistant
                  - File.
                  - Assistants
                  - Assistant_id
                  - Files
                  - File_id
                summary: Retrieves an AssistantFile.
              delete:
                tags:
                  - Delete
                  - An
                  - Assistant
                  - File.
                  - Assistants
                  - Assistant_id
                  - Files
                  - File_id
                summary: Delete an assistant file.
          x-oaiMeta:
            groups:
              - id: audio
                title: Audio
                description: |
                  Learn how to turn audio into text or text into audio.

                  Related guide: [Speech to text](/docs/guides/speech-to-text)
                sections:
                  - type: endpoint
                    key: createSpeech
                    path: createSpeech
                  - type: endpoint
                    key: createTranscription
                    path: createTranscription
                  - type: endpoint
                    key: createTranslation
                    path: createTranslation
              - id: chat
                title: Chat
                description: >
                  Given a list of messages comprising a conversation, the model
                  will return a response.


                  Related guide: [Chat
                  Completions](/docs/guides/text-generation)
                sections:
                  - type: endpoint
                    key: createChatCompletion
                    path: create
                  - type: object
                    key: CreateChatCompletionResponse
                    path: object
                  - type: object
                    key: CreateChatCompletionStreamResponse
                    path: streaming
              - id: embeddings
                title: Embeddings
                description: >
                  Get a vector representation of a given input that can be
                  easily consumed by machine learning models and algorithms.


                  Related guide: [Embeddings](/docs/guides/embeddings)
                sections:
                  - type: endpoint
                    key: createEmbedding
                    path: create
                  - type: object
                    key: Embedding
                    path: object
              - id: fine-tuning
                title: Fine-tuning
                description: >
                  Manage fine-tuning jobs to tailor a model to your specific
                  training data.


                  Related guide: [Fine-tune models](/docs/guides/fine-tuning)
                sections:
                  - type: endpoint
                    key: createFineTuningJob
                    path: create
                  - type: endpoint
                    key: listPaginatedFineTuningJobs
                    path: list
                  - type: endpoint
                    key: listFineTuningEvents
                    path: list-events
                  - type: endpoint
                    key: retrieveFineTuningJob
                    path: retrieve
                  - type: endpoint
                    key: cancelFineTuningJob
                    path: cancel
                  - type: object
                    key: FineTuningJob
                    path: object
                  - type: object
                    key: FineTuningJobEvent
                    path: event-object
              - id: files
                title: Files
                description: >
                  Files are used to upload documents that can be used with
                  features like [Assistants](/docs/api-reference/assistants) and
                  [Fine-tuning](/docs/api-reference/fine-tuning).
                sections:
                  - type: endpoint
                    key: createFile
                    path: create
                  - type: endpoint
                    key: listFiles
                    path: list
                  - type: endpoint
                    key: retrieveFile
                    path: retrieve
                  - type: endpoint
                    key: deleteFile
                    path: delete
                  - type: endpoint
                    key: downloadFile
                    path: retrieve-contents
                  - type: object
                    key: OpenAIFile
                    path: object
              - id: images
                title: Images
                description: >
                  Given a prompt and/or an input image, the model will generate
                  a new image.


                  Related guide: [Image generation](/docs/guides/images)
                sections:
                  - type: endpoint
                    key: createImage
                    path: create
                  - type: endpoint
                    key: createImageEdit
                    path: createEdit
                  - type: endpoint
                    key: createImageVariation
                    path: createVariation
                  - type: object
                    key: Image
                    path: object
              - id: models
                title: Models
                description: >
                  List and describe the various models available in the API. You
                  can refer to the [Models](/docs/models) documentation to
                  understand what models are available and the differences
                  between them.
                sections:
                  - type: endpoint
                    key: listModels
                    path: list
                  - type: endpoint
                    key: retrieveModel
                    path: retrieve
                  - type: endpoint
                    key: deleteModel
                    path: delete
                  - type: object
                    key: Model
                    path: object
              - id: moderations
                title: Moderations
                description: >
                  Given a input text, outputs if the model classifies it as
                  violating OpenAI's content policy.


                  Related guide: [Moderations](/docs/guides/moderation)
                sections:
                  - type: endpoint
                    key: createModeration
                    path: create
                  - type: object
                    key: CreateModerationResponse
                    path: object
              - id: assistants
                title: Assistants
                beta: true
                description: >
                  Build assistants that can call models and use tools to perform
                  tasks.


                  [Get started with the Assistants API](/docs/assistants)
                sections:
                  - type: endpoint
                    key: createAssistant
                    path: createAssistant
                  - type: endpoint
                    key: createAssistantFile
                    path: createAssistantFile
                  - type: endpoint
                    key: listAssistants
                    path: listAssistants
                  - type: endpoint
                    key: listAssistantFiles
                    path: listAssistantFiles
                  - type: endpoint
                    key: getAssistant
                    path: getAssistant
                  - type: endpoint
                    key: getAssistantFile
                    path: getAssistantFile
                  - type: endpoint
                    key: modifyAssistant
                    path: modifyAssistant
                  - type: endpoint
                    key: deleteAssistant
                    path: deleteAssistant
                  - type: endpoint
                    key: deleteAssistantFile
                    path: deleteAssistantFile
                  - type: object
                    key: AssistantObject
                    path: object
                  - type: object
                    key: AssistantFileObject
                    path: file-object
              - id: threads
                title: Threads
                beta: true
                description: |
                  Create threads that assistants can interact with.

                  Related guide: [Assistants](/docs/assistants/overview)
                sections:
                  - type: endpoint
                    key: createThread
                    path: createThread
                  - type: endpoint
                    key: getThread
                    path: getThread
                  - type: endpoint
                    key: modifyThread
                    path: modifyThread
                  - type: endpoint
                    key: deleteThread
                    path: deleteThread
                  - type: object
                    key: ThreadObject
                    path: object
              - id: messages
                title: Messages
                beta: true
                description: |
                  Create messages within threads

                  Related guide: [Assistants](/docs/assistants/overview)
                sections:
                  - type: endpoint
                    key: createMessage
                    path: createMessage
                  - type: endpoint
                    key: listMessages
                    path: listMessages
                  - type: endpoint
                    key: listMessageFiles
                    path: listMessageFiles
                  - type: endpoint
                    key: getMessage
                    path: getMessage
                  - type: endpoint
                    key: getMessageFile
                    path: getMessageFile
                  - type: endpoint
                    key: modifyMessage
                    path: modifyMessage
                  - type: object
                    key: MessageObject
                    path: object
                  - type: object
                    key: MessageFileObject
                    path: file-object
              - id: runs
                title: Runs
                beta: true
                description: |
                  Represents an execution run on a thread.

                  Related guide: [Assistants](/docs/assistants/overview)
                sections:
                  - type: endpoint
                    key: createRun
                    path: createRun
                  - type: endpoint
                    key: createThreadAndRun
                    path: createThreadAndRun
                  - type: endpoint
                    key: listRuns
                    path: listRuns
                  - type: endpoint
                    key: listRunSteps
                    path: listRunSteps
                  - type: endpoint
                    key: getRun
                    path: getRun
                  - type: endpoint
                    key: getRunStep
                    path: getRunStep
                  - type: endpoint
                    key: modifyRun
                    path: modifyRun
                  - type: endpoint
                    key: submitToolOuputsToRun
                    path: submitToolOutputs
                  - type: endpoint
                    key: cancelRun
                    path: cancelRun
                  - type: object
                    key: RunObject
                    path: object
                  - type: object
                    key: RunStepObject
                    path: step-object
              - id: completions
                title: Completions
                legacy: true
                description: >
                  Given a prompt, the model will return one or more predicted
                  completions along with the probabilities of alternative tokens
                  at each position. Most developer should use our [Chat
                  Completions
                  API](/docs/guides/text-generation/text-generation-models) to
                  leverage our best and newest models. Most models that support
                  the legacy Completions endpoint [will be shut off on January
                  4th, 2024](/docs/deprecations/2023-07-06-gpt-and-embeddings).
                sections:
                  - type: endpoint
                    key: createCompletion
                    path: create
                  - type: object
                    key: CreateCompletionResponse
                    path: null
    overlays:
      - type: APIs.io Search
        url: >-
          overlays/https://github.com/apis-json/artisanal/tree/main/apis/openai/assistants-openapi-search.yml
      - type: APIs.io Search
        url: overlays/assistants-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/assistants-openapi-api-evangelist-ratings.yml
    aid: openai:openai-assistants-api
  - name: OpenAI Audio API
    description: >-
      The Audio API provides two speech to text endpoints, transcriptions and
      translations, based on our state-of-the-art open source large-v2 Whisper
      model.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://platform.openai.com/docs/guides/speech-to-text
    baseURL: https://platform.openai.com/
    tags: []
    properties:
      - type: Documentation
        url: https://platform.openai.com/docs/api-reference
      - type: OpenAPI
        data:
          openapi: 3.0.0
          info:
            title: ' audio'
            license:
              name: MIT
              url: https://github.com/openai/openai-openapi/blob/master/LICENSE
          tags:
            - name: Assistants
              description: Build Assistants that can call models and use tools.
            - name: Audio
              description: Learn how to turn audio into text or text into audio.
            - name: Chat
              description: >-
                Given a list of messages comprising a conversation, the model
                will return a response.
            - name: Completions
              description: >-
                Given a prompt, the model will return one or more predicted
                completions, and can also return the probabilities of
                alternative tokens at each position.
            - name: Embeddings
              description: >-
                Get a vector representation of a given input that can be easily
                consumed by machine learning models and algorithms.
            - name: Fine-tuning
              description: >-
                Manage fine-tuning jobs to tailor a model to your specific
                training data.
            - name: Files
              description: >-
                Files are used to upload documents that can be used with
                features like Assistants and Fine-tuning.
            - name: Images
              description: >-
                Given a prompt and/or an input image, the model will generate a
                new image.
            - name: Models
              description: List and describe the various models available in the API.
            - name: Moderations
              description: >-
                Given a input text, outputs if the model classifies it as
                violating OpenAI's content policy.
          paths:
            /audio/speech:
              post:
                tags:
                  - Generates
                  - Audio
                  - From
                  - The
                  - Input
                  - Text.
                  - Audio
                  - Speech
                summary: Generates audio from the input text.
            /audio/transcriptions:
              post:
                tags:
                  - Transcribes
                  - Audio
                  - Into
                  - The
                  - Input
                  - Language.
                  - Audio
                  - Speech
                  - Transcriptions
                summary: Transcribes audio into the input language.
            /audio/translations:
              post:
                tags:
                  - Translates
                  - Audio
                  - Into
                  - English.
                  - Audio
                  - Speech
                  - Transcriptions
                  - Translations
                summary: Translates audio into English.
          x-oaiMeta:
            groups:
              - id: audio
                title: Audio
                description: |
                  Learn how to turn audio into text or text into audio.

                  Related guide: [Speech to text](/docs/guides/speech-to-text)
                sections:
                  - type: endpoint
                    key: createSpeech
                    path: createSpeech
                  - type: endpoint
                    key: createTranscription
                    path: createTranscription
                  - type: endpoint
                    key: createTranslation
                    path: createTranslation
              - id: chat
                title: Chat
                description: >
                  Given a list of messages comprising a conversation, the model
                  will return a response.


                  Related guide: [Chat
                  Completions](/docs/guides/text-generation)
                sections:
                  - type: endpoint
                    key: createChatCompletion
                    path: create
                  - type: object
                    key: CreateChatCompletionResponse
                    path: object
                  - type: object
                    key: CreateChatCompletionStreamResponse
                    path: streaming
              - id: embeddings
                title: Embeddings
                description: >
                  Get a vector representation of a given input that can be
                  easily consumed by machine learning models and algorithms.


                  Related guide: [Embeddings](/docs/guides/embeddings)
                sections:
                  - type: endpoint
                    key: createEmbedding
                    path: create
                  - type: object
                    key: Embedding
                    path: object
              - id: fine-tuning
                title: Fine-tuning
                description: >
                  Manage fine-tuning jobs to tailor a model to your specific
                  training data.


                  Related guide: [Fine-tune models](/docs/guides/fine-tuning)
                sections:
                  - type: endpoint
                    key: createFineTuningJob
                    path: create
                  - type: endpoint
                    key: listPaginatedFineTuningJobs
                    path: list
                  - type: endpoint
                    key: listFineTuningEvents
                    path: list-events
                  - type: endpoint
                    key: retrieveFineTuningJob
                    path: retrieve
                  - type: endpoint
                    key: cancelFineTuningJob
                    path: cancel
                  - type: object
                    key: FineTuningJob
                    path: object
                  - type: object
                    key: FineTuningJobEvent
                    path: event-object
              - id: files
                title: Files
                description: >
                  Files are used to upload documents that can be used with
                  features like [Assistants](/docs/api-reference/assistants) and
                  [Fine-tuning](/docs/api-reference/fine-tuning).
                sections:
                  - type: endpoint
                    key: createFile
                    path: create
                  - type: endpoint
                    key: listFiles
                    path: list
                  - type: endpoint
                    key: retrieveFile
                    path: retrieve
                  - type: endpoint
                    key: deleteFile
                    path: delete
                  - type: endpoint
                    key: downloadFile
                    path: retrieve-contents
                  - type: object
                    key: OpenAIFile
                    path: object
              - id: images
                title: Images
                description: >
                  Given a prompt and/or an input image, the model will generate
                  a new image.


                  Related guide: [Image generation](/docs/guides/images)
                sections:
                  - type: endpoint
                    key: createImage
                    path: create
                  - type: endpoint
                    key: createImageEdit
                    path: createEdit
                  - type: endpoint
                    key: createImageVariation
                    path: createVariation
                  - type: object
                    key: Image
                    path: object
              - id: models
                title: Models
                description: >
                  List and describe the various models available in the API. You
                  can refer to the [Models](/docs/models) documentation to
                  understand what models are available and the differences
                  between them.
                sections:
                  - type: endpoint
                    key: listModels
                    path: list
                  - type: endpoint
                    key: retrieveModel
                    path: retrieve
                  - type: endpoint
                    key: deleteModel
                    path: delete
                  - type: object
                    key: Model
                    path: object
              - id: moderations
                title: Moderations
                description: >
                  Given a input text, outputs if the model classifies it as
                  violating OpenAI's content policy.


                  Related guide: [Moderations](/docs/guides/moderation)
                sections:
                  - type: endpoint
                    key: createModeration
                    path: create
                  - type: object
                    key: CreateModerationResponse
                    path: object
              - id: assistants
                title: Assistants
                beta: true
                description: >
                  Build assistants that can call models and use tools to perform
                  tasks.


                  [Get started with the Assistants API](/docs/assistants)
                sections:
                  - type: endpoint
                    key: createAssistant
                    path: createAssistant
                  - type: endpoint
                    key: createAssistantFile
                    path: createAssistantFile
                  - type: endpoint
                    key: listAssistants
                    path: listAssistants
                  - type: endpoint
                    key: listAssistantFiles
                    path: listAssistantFiles
                  - type: endpoint
                    key: getAssistant
                    path: getAssistant
                  - type: endpoint
                    key: getAssistantFile
                    path: getAssistantFile
                  - type: endpoint
                    key: modifyAssistant
                    path: modifyAssistant
                  - type: endpoint
                    key: deleteAssistant
                    path: deleteAssistant
                  - type: endpoint
                    key: deleteAssistantFile
                    path: deleteAssistantFile
                  - type: object
                    key: AssistantObject
                    path: object
                  - type: object
                    key: AssistantFileObject
                    path: file-object
              - id: threads
                title: Threads
                beta: true
                description: |
                  Create threads that assistants can interact with.

                  Related guide: [Assistants](/docs/assistants/overview)
                sections:
                  - type: endpoint
                    key: createThread
                    path: createThread
                  - type: endpoint
                    key: getThread
                    path: getThread
                  - type: endpoint
                    key: modifyThread
                    path: modifyThread
                  - type: endpoint
                    key: deleteThread
                    path: deleteThread
                  - type: object
                    key: ThreadObject
                    path: object
              - id: messages
                title: Messages
                beta: true
                description: |
                  Create messages within threads

                  Related guide: [Assistants](/docs/assistants/overview)
                sections:
                  - type: endpoint
                    key: createMessage
                    path: createMessage
                  - type: endpoint
                    key: listMessages
                    path: listMessages
                  - type: endpoint
                    key: listMessageFiles
                    path: listMessageFiles
                  - type: endpoint
                    key: getMessage
                    path: getMessage
                  - type: endpoint
                    key: getMessageFile
                    path: getMessageFile
                  - type: endpoint
                    key: modifyMessage
                    path: modifyMessage
                  - type: object
                    key: MessageObject
                    path: object
                  - type: object
                    key: MessageFileObject
                    path: file-object
              - id: runs
                title: Runs
                beta: true
                description: |
                  Represents an execution run on a thread.

                  Related guide: [Assistants](/docs/assistants/overview)
                sections:
                  - type: endpoint
                    key: createRun
                    path: createRun
                  - type: endpoint
                    key: createThreadAndRun
                    path: createThreadAndRun
                  - type: endpoint
                    key: listRuns
                    path: listRuns
                  - type: endpoint
                    key: listRunSteps
                    path: listRunSteps
                  - type: endpoint
                    key: getRun
                    path: getRun
                  - type: endpoint
                    key: getRunStep
                    path: getRunStep
                  - type: endpoint
                    key: modifyRun
                    path: modifyRun
                  - type: endpoint
                    key: submitToolOuputsToRun
                    path: submitToolOutputs
                  - type: endpoint
                    key: cancelRun
                    path: cancelRun
                  - type: object
                    key: RunObject
                    path: object
                  - type: object
                    key: RunStepObject
                    path: step-object
              - id: completions
                title: Completions
                legacy: true
                description: >
                  Given a prompt, the model will return one or more predicted
                  completions along with the probabilities of alternative tokens
                  at each position. Most developer should use our [Chat
                  Completions
                  API](/docs/guides/text-generation/text-generation-models) to
                  leverage our best and newest models. Most models that support
                  the legacy Completions endpoint [will be shut off on January
                  4th, 2024](/docs/deprecations/2023-07-06-gpt-and-embeddings).
                sections:
                  - type: endpoint
                    key: createCompletion
                    path: create
                  - type: object
                    key: CreateCompletionResponse
                    path: null
    overlays:
      - type: APIs.io Search
        url: >-
          overlays/https://github.com/apis-json/artisanal/tree/main/apis/openai/audio-openapi-search.yml
      - type: APIs.io Search
        url: overlays/audio-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/audio-openapi-api-evangelist-ratings.yml
    aid: openai:openai-audio-api
  - name: OpenAI Chat API
    description: >-
      Given a list of messages comprising a conversation, the model will return
      a response., providing an AI chat interface you can use to engage with
      users.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://platform.openai.com/docs/api-reference/chat
    baseURL: https://platform.openai.com/
    tags: []
    properties:
      - type: Documentation
        url: https://platform.openai.com/docs/api-reference
      - type: OpenAPI
        data:
          openapi: 3.0.0
          info:
            title: OpenAI Chat
            license:
              name: MIT
              url: https://github.com/openai/openai-openapi/blob/master/LICENSE
          tags:
            - name: Assistants
              description: Build Assistants that can call models and use tools.
            - name: Audio
              description: Learn how to turn audio into text or text into audio.
            - name: Chat
              description: >-
                Given a list of messages comprising a conversation, the model
                will return a response.
            - name: Completions
              description: >-
                Given a prompt, the model will return one or more predicted
                completions, and can also return the probabilities of
                alternative tokens at each position.
            - name: Embeddings
              description: >-
                Get a vector representation of a given input that can be easily
                consumed by machine learning models and algorithms.
            - name: Fine-tuning
              description: >-
                Manage fine-tuning jobs to tailor a model to your specific
                training data.
            - name: Files
              description: >-
                Files are used to upload documents that can be used with
                features like Assistants and Fine-tuning.
            - name: Images
              description: >-
                Given a prompt and/or an input image, the model will generate a
                new image.
            - name: Models
              description: List and describe the various models available in the API.
            - name: Moderations
              description: >-
                Given a input text, outputs if the model classifies it as
                violating OpenAI's content policy.
          paths:
            /chat/completions:
              post:
                tags:
                  - Creates
                  - Model
                  - Response
                  - For
                  - The
                  - Given
                  - Chat
                  - Conversation.
                  - Chat
                  - Completions
                summary: Creates a model response for the given chat conversation.
          x-oaiMeta:
            groups:
              - id: audio
                title: Audio
                description: |
                  Learn how to turn audio into text or text into audio.

                  Related guide: [Speech to text](/docs/guides/speech-to-text)
                sections:
                  - type: endpoint
                    key: createSpeech
                    path: createSpeech
                  - type: endpoint
                    key: createTranscription
                    path: createTranscription
                  - type: endpoint
                    key: createTranslation
                    path: createTranslation
              - id: chat
                title: Chat
                description: >
                  Given a list of messages comprising a conversation, the model
                  will return a response.


                  Related guide: [Chat
                  Completions](/docs/guides/text-generation)
                sections:
                  - type: endpoint
                    key: createChatCompletion
                    path: create
                  - type: object
                    key: CreateChatCompletionResponse
                    path: object
                  - type: object
                    key: CreateChatCompletionStreamResponse
                    path: streaming
              - id: embeddings
                title: Embeddings
                description: >
                  Get a vector representation of a given input that can be
                  easily consumed by machine learning models and algorithms.


                  Related guide: [Embeddings](/docs/guides/embeddings)
                sections:
                  - type: endpoint
                    key: createEmbedding
                    path: create
                  - type: object
                    key: Embedding
                    path: object
              - id: fine-tuning
                title: Fine-tuning
                description: >
                  Manage fine-tuning jobs to tailor a model to your specific
                  training data.


                  Related guide: [Fine-tune models](/docs/guides/fine-tuning)
                sections:
                  - type: endpoint
                    key: createFineTuningJob
                    path: create
                  - type: endpoint
                    key: listPaginatedFineTuningJobs
                    path: list
                  - type: endpoint
                    key: listFineTuningEvents
                    path: list-events
                  - type: endpoint
                    key: retrieveFineTuningJob
                    path: retrieve
                  - type: endpoint
                    key: cancelFineTuningJob
                    path: cancel
                  - type: object
                    key: FineTuningJob
                    path: object
                  - type: object
                    key: FineTuningJobEvent
                    path: event-object
              - id: files
                title: Files
                description: >
                  Files are used to upload documents that can be used with
                  features like [Assistants](/docs/api-reference/assistants) and
                  [Fine-tuning](/docs/api-reference/fine-tuning).
                sections:
                  - type: endpoint
                    key: createFile
                    path: create
                  - type: endpoint
                    key: listFiles
                    path: list
                  - type: endpoint
                    key: retrieveFile
                    path: retrieve
                  - type: endpoint
                    key: deleteFile
                    path: delete
                  - type: endpoint
                    key: downloadFile
                    path: retrieve-contents
                  - type: object
                    key: OpenAIFile
                    path: object
              - id: images
                title: Images
                description: >
                  Given a prompt and/or an input image, the model will generate
                  a new image.


                  Related guide: [Image generation](/docs/guides/images)
                sections:
                  - type: endpoint
                    key: createImage
                    path: create
                  - type: endpoint
                    key: createImageEdit
                    path: createEdit
                  - type: endpoint
                    key: createImageVariation
                    path: createVariation
                  - type: object
                    key: Image
                    path: object
              - id: models
                title: Models
                description: >
                  List and describe the various models available in the API. You
                  can refer to the [Models](/docs/models) documentation to
                  understand what models are available and the differences
                  between them.
                sections:
                  - type: endpoint
                    key: listModels
                    path: list
                  - type: endpoint
                    key: retrieveModel
                    path: retrieve
                  - type: endpoint
                    key: deleteModel
                    path: delete
                  - type: object
                    key: Model
                    path: object
              - id: moderations
                title: Moderations
                description: >
                  Given a input text, outputs if the model classifies it as
                  violating OpenAI's content policy.


                  Related guide: [Moderations](/docs/guides/moderation)
                sections:
                  - type: endpoint
                    key: createModeration
                    path: create
                  - type: object
                    key: CreateModerationResponse
                    path: object
              - id: assistants
                title: Assistants
                beta: true
                description: >
                  Build assistants that can call models and use tools to perform
                  tasks.


                  [Get started with the Assistants API](/docs/assistants)
                sections:
                  - type: endpoint
                    key: createAssistant
                    path: createAssistant
                  - type: endpoint
                    key: createAssistantFile
                    path: createAssistantFile
                  - type: endpoint
                    key: listAssistants
                    path: listAssistants
                  - type: endpoint
                    key: listAssistantFiles
                    path: listAssistantFiles
                  - type: endpoint
                    key: getAssistant
                    path: getAssistant
                  - type: endpoint
                    key: getAssistantFile
                    path: getAssistantFile
                  - type: endpoint
                    key: modifyAssistant
                    path: modifyAssistant
                  - type: endpoint
                    key: deleteAssistant
                    path: deleteAssistant
                  - type: endpoint
                    key: deleteAssistantFile
                    path: deleteAssistantFile
                  - type: object
                    key: AssistantObject
                    path: object
                  - type: object
                    key: AssistantFileObject
                    path: file-object
              - id: threads
                title: Threads
                beta: true
                description: |
                  Create threads that assistants can interact with.

                  Related guide: [Assistants](/docs/assistants/overview)
                sections:
                  - type: endpoint
                    key: createThread
                    path: createThread
                  - type: endpoint
                    key: getThread
                    path: getThread
                  - type: endpoint
                    key: modifyThread
                    path: modifyThread
                  - type: endpoint
                    key: deleteThread
                    path: deleteThread
                  - type: object
                    key: ThreadObject
                    path: object
              - id: messages
                title: Messages
                beta: true
                description: |
                  Create messages within threads

                  Related guide: [Assistants](/docs/assistants/overview)
                sections:
                  - type: endpoint
                    key: createMessage
                    path: createMessage
                  - type: endpoint
                    key: listMessages
                    path: listMessages
                  - type: endpoint
                    key: listMessageFiles
                    path: listMessageFiles
                  - type: endpoint
                    key: getMessage
                    path: getMessage
                  - type: endpoint
                    key: getMessageFile
                    path: getMessageFile
                  - type: endpoint
                    key: modifyMessage
                    path: modifyMessage
                  - type: object
                    key: MessageObject
                    path: object
                  - type: object
                    key: MessageFileObject
                    path: file-object
              - id: runs
                title: Runs
                beta: true
                description: |
                  Represents an execution run on a thread.

                  Related guide: [Assistants](/docs/assistants/overview)
                sections:
                  - type: endpoint
                    key: createRun
                    path: createRun
                  - type: endpoint
                    key: createThreadAndRun
                    path: createThreadAndRun
                  - type: endpoint
                    key: listRuns
                    path: listRuns
                  - type: endpoint
                    key: listRunSteps
                    path: listRunSteps
                  - type: endpoint
                    key: getRun
                    path: getRun
                  - type: endpoint
                    key: getRunStep
                    path: getRunStep
                  - type: endpoint
                    key: modifyRun
                    path: modifyRun
                  - type: endpoint
                    key: submitToolOuputsToRun
                    path: submitToolOutputs
                  - type: endpoint
                    key: cancelRun
                    path: cancelRun
                  - type: object
                    key: RunObject
                    path: object
                  - type: object
                    key: RunStepObject
                    path: step-object
              - id: completions
                title: Completions
                legacy: true
                description: >
                  Given a prompt, the model will return one or more predicted
                  completions along with the probabilities of alternative tokens
                  at each position. Most developer should use our [Chat
                  Completions
                  API](/docs/guides/text-generation/text-generation-models) to
                  leverage our best and newest models. Most models that support
                  the legacy Completions endpoint [will be shut off on January
                  4th, 2024](/docs/deprecations/2023-07-06-gpt-and-embeddings).
                sections:
                  - type: endpoint
                    key: createCompletion
                    path: create
                  - type: object
                    key: CreateCompletionResponse
                    path: null
    overlays:
      - type: APIs.io Search
        url: >-
          overlays/https://github.com/apis-json/artisanal/tree/main/apis/openai/chat-openapi-search.yml
      - type: APIs.io Search
        url: overlays/chat-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/chat-openapi-api-evangelist-ratings.yml
    aid: openai:openai-chat-api
  - name: OpenAI Chat Completions API
    description: >-
      Chat models take a list of messages as input and return a model-generated
      message as output. Although the chat format is designed to make multi-turn
      conversations easy, it’s just as useful for single-turn tasks without any
      conversation.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: >-
      https://platform.openai.com/docs/guides/text-generation/chat-completions-api
    baseURL: https://platform.openai.com/
    tags: []
    properties:
      - type: Documentation
        url: https://platform.openai.com/docs/api-reference
      - type: OpenAPI
        data:
          openapi: 3.0.0
          info:
            title: OpenAI Completions
            license:
              name: MIT
              url: https://github.com/openai/openai-openapi/blob/master/LICENSE
          tags:
            - name: Assistants
              description: Build Assistants that can call models and use tools.
            - name: Audio
              description: Learn how to turn audio into text or text into audio.
            - name: Chat
              description: >-
                Given a list of messages comprising a conversation, the model
                will return a response.
            - name: Completions
              description: >-
                Given a prompt, the model will return one or more predicted
                completions, and can also return the probabilities of
                alternative tokens at each position.
            - name: Embeddings
              description: >-
                Get a vector representation of a given input that can be easily
                consumed by machine learning models and algorithms.
            - name: Fine-tuning
              description: >-
                Manage fine-tuning jobs to tailor a model to your specific
                training data.
            - name: Files
              description: >-
                Files are used to upload documents that can be used with
                features like Assistants and Fine-tuning.
            - name: Images
              description: >-
                Given a prompt and/or an input image, the model will generate a
                new image.
            - name: Models
              description: List and describe the various models available in the API.
            - name: Moderations
              description: >-
                Given a input text, outputs if the model classifies it as
                violating OpenAI's content policy.
          paths:
            /chat/completions:
              post:
                tags:
                  - Creates
                  - Model
                  - Response
                  - For
                  - The
                  - Given
                  - Chat
                  - Conversation.
                  - Chat
                  - Completions
                summary: Creates a model response for the given chat conversation.
            /completions:
              post:
                tags:
                  - Creates
                  - Completion
                  - For
                  - The
                  - Provided
                  - Prompt
                  - And
                  - Parameters.
                  - Chat
                  - Completions
                summary: Creates a completion for the provided prompt and parameters.
          x-oaiMeta:
            groups:
              - id: audio
                title: Audio
                description: |
                  Learn how to turn audio into text or text into audio.

                  Related guide: [Speech to text](/docs/guides/speech-to-text)
                sections:
                  - type: endpoint
                    key: createSpeech
                    path: createSpeech
                  - type: endpoint
                    key: createTranscription
                    path: createTranscription
                  - type: endpoint
                    key: createTranslation
                    path: createTranslation
              - id: chat
                title: Chat
                description: >
                  Given a list of messages comprising a conversation, the model
                  will return a response.


                  Related guide: [Chat
                  Completions](/docs/guides/text-generation)
                sections:
                  - type: endpoint
                    key: createChatCompletion
                    path: create
                  - type: object
                    key: CreateChatCompletionResponse
                    path: object
                  - type: object
                    key: CreateChatCompletionStreamResponse
                    path: streaming
              - id: embeddings
                title: Embeddings
                description: >
                  Get a vector representation of a given input that can be
                  easily consumed by machine learning models and algorithms.


                  Related guide: [Embeddings](/docs/guides/embeddings)
                sections:
                  - type: endpoint
                    key: createEmbedding
                    path: create
                  - type: object
                    key: Embedding
                    path: object
              - id: fine-tuning
                title: Fine-tuning
                description: >
                  Manage fine-tuning jobs to tailor a model to your specific
                  training data.


                  Related guide: [Fine-tune models](/docs/guides/fine-tuning)
                sections:
                  - type: endpoint
                    key: createFineTuningJob
                    path: create
                  - type: endpoint
                    key: listPaginatedFineTuningJobs
                    path: list
                  - type: endpoint
                    key: listFineTuningEvents
                    path: list-events
                  - type: endpoint
                    key: retrieveFineTuningJob
                    path: retrieve
                  - type: endpoint
                    key: cancelFineTuningJob
                    path: cancel
                  - type: object
                    key: FineTuningJob
                    path: object
                  - type: object
                    key: FineTuningJobEvent
                    path: event-object
              - id: files
                title: Files
                description: >
                  Files are used to upload documents that can be used with
                  features like [Assistants](/docs/api-reference/assistants) and
                  [Fine-tuning](/docs/api-reference/fine-tuning).
                sections:
                  - type: endpoint
                    key: createFile
                    path: create
                  - type: endpoint
                    key: listFiles
                    path: list
                  - type: endpoint
                    key: retrieveFile
                    path: retrieve
                  - type: endpoint
                    key: deleteFile
                    path: delete
                  - type: endpoint
                    key: downloadFile
                    path: retrieve-contents
                  - type: object
                    key: OpenAIFile
                    path: object
              - id: images
                title: Images
                description: >
                  Given a prompt and/or an input image, the model will generate
                  a new image.


                  Related guide: [Image generation](/docs/guides/images)
                sections:
                  - type: endpoint
                    key: createImage
                    path: create
                  - type: endpoint
                    key: createImageEdit
                    path: createEdit
                  - type: endpoint
                    key: createImageVariation
                    path: createVariation
                  - type: object
                    key: Image
                    path: object
              - id: models
                title: Models
                description: >
                  List and describe the various models available in the API. You
                  can refer to the [Models](/docs/models) documentation to
                  understand what models are available and the differences
                  between them.
                sections:
                  - type: endpoint
                    key: listModels
                    path: list
                  - type: endpoint
                    key: retrieveModel
                    path: retrieve
                  - type: endpoint
                    key: deleteModel
                    path: delete
                  - type: object
                    key: Model
                    path: object
              - id: moderations
                title: Moderations
                description: >
                  Given a input text, outputs if the model classifies it as
                  violating OpenAI's content policy.


                  Related guide: [Moderations](/docs/guides/moderation)
                sections:
                  - type: endpoint
                    key: createModeration
                    path: create
                  - type: object
                    key: CreateModerationResponse
                    path: object
              - id: assistants
                title: Assistants
                beta: true
                description: >
                  Build assistants that can call models and use tools to perform
                  tasks.


                  [Get started with the Assistants API](/docs/assistants)
                sections:
                  - type: endpoint
                    key: createAssistant
                    path: createAssistant
                  - type: endpoint
                    key: createAssistantFile
                    path: createAssistantFile
                  - type: endpoint
                    key: listAssistants
                    path: listAssistants
                  - type: endpoint
                    key: listAssistantFiles
                    path: listAssistantFiles
                  - type: endpoint
                    key: getAssistant
                    path: getAssistant
                  - type: endpoint
                    key: getAssistantFile
                    path: getAssistantFile
                  - type: endpoint
                    key: modifyAssistant
                    path: modifyAssistant
                  - type: endpoint
                    key: deleteAssistant
                    path: deleteAssistant
                  - type: endpoint
                    key: deleteAssistantFile
                    path: deleteAssistantFile
                  - type: object
                    key: AssistantObject
                    path: object
                  - type: object
                    key: AssistantFileObject
                    path: file-object
              - id: threads
                title: Threads
                beta: true
                description: |
                  Create threads that assistants can interact with.

                  Related guide: [Assistants](/docs/assistants/overview)
                sections:
                  - type: endpoint
                    key: createThread
                    path: createThread
                  - type: endpoint
                    key: getThread
                    path: getThread
                  - type: endpoint
                    key: modifyThread
                    path: modifyThread
                  - type: endpoint
                    key: deleteThread
                    path: deleteThread
                  - type: object
                    key: ThreadObject
                    path: object
              - id: messages
                title: Messages
                beta: true
                description: |
                  Create messages within threads

                  Related guide: [Assistants](/docs/assistants/overview)
                sections:
                  - type: endpoint
                    key: createMessage
                    path: createMessage
                  - type: endpoint
                    key: listMessages
                    path: listMessages
                  - type: endpoint
                    key: listMessageFiles
                    path: listMessageFiles
                  - type: endpoint
                    key: getMessage
                    path: getMessage
                  - type: endpoint
                    key: getMessageFile
                    path: getMessageFile
                  - type: endpoint
                    key: modifyMessage
                    path: modifyMessage
                  - type: object
                    key: MessageObject
                    path: object
                  - type: object
                    key: MessageFileObject
                    path: file-object
              - id: runs
                title: Runs
                beta: true
                description: |
                  Represents an execution run on a thread.

                  Related guide: [Assistants](/docs/assistants/overview)
                sections:
                  - type: endpoint
                    key: createRun
                    path: createRun
                  - type: endpoint
                    key: createThreadAndRun
                    path: createThreadAndRun
                  - type: endpoint
                    key: listRuns
                    path: listRuns
                  - type: endpoint
                    key: listRunSteps
                    path: listRunSteps
                  - type: endpoint
                    key: getRun
                    path: getRun
                  - type: endpoint
                    key: getRunStep
                    path: getRunStep
                  - type: endpoint
                    key: modifyRun
                    path: modifyRun
                  - type: endpoint
                    key: submitToolOuputsToRun
                    path: submitToolOutputs
                  - type: endpoint
                    key: cancelRun
                    path: cancelRun
                  - type: object
                    key: RunObject
                    path: object
                  - type: object
                    key: RunStepObject
                    path: step-object
              - id: completions
                title: Completions
                legacy: true
                description: >
                  Given a prompt, the model will return one or more predicted
                  completions along with the probabilities of alternative tokens
                  at each position. Most developer should use our [Chat
                  Completions
                  API](/docs/guides/text-generation/text-generation-models) to
                  leverage our best and newest models. Most models that support
                  the legacy Completions endpoint [will be shut off on January
                  4th, 2024](/docs/deprecations/2023-07-06-gpt-and-embeddings).
                sections:
                  - type: endpoint
                    key: createCompletion
                    path: create
                  - type: object
                    key: CreateCompletionResponse
                    path: null
    overlays:
      - type: APIs.io Search
        url: >-
          overlays/https://github.com/apis-json/artisanal/tree/main/apis/openai/completions-openapi-search.yml
      - type: APIs.io Search
        url: overlays/completions-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/completions-openapi-api-evangelist-ratings.yml
    aid: openai:openai-chat-completions-api
  - name: OpenAI Embeddings API
    description: >-
      Learn how to turn text into numbers, unlocking use cases like search.
      OpenAI’s text embeddings measure the relatedness of text strings.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://platform.openai.com/docs/guides/embeddings
    baseURL: https://platform.openai.com/
    tags: []
    properties:
      - type: Documentation
        url: https://platform.openai.com/docs/api-reference
      - type: OpenAPI
        data:
          openapi: 3.0.0
          info:
            title: ' embeddings'
            license:
              name: MIT
              url: https://github.com/openai/openai-openapi/blob/master/LICENSE
          tags:
            - name: Assistants
              description: Build Assistants that can call models and use tools.
            - name: Audio
              description: Learn how to turn audio into text or text into audio.
            - name: Chat
              description: >-
                Given a list of messages comprising a conversation, the model
                will return a response.
            - name: Completions
              description: >-
                Given a prompt, the model will return one or more predicted
                completions, and can also return the probabilities of
                alternative tokens at each position.
            - name: Embeddings
              description: >-
                Get a vector representation of a given input that can be easily
                consumed by machine learning models and algorithms.
            - name: Fine-tuning
              description: >-
                Manage fine-tuning jobs to tailor a model to your specific
                training data.
            - name: Files
              description: >-
                Files are used to upload documents that can be used with
                features like Assistants and Fine-tuning.
            - name: Images
              description: >-
                Given a prompt and/or an input image, the model will generate a
                new image.
            - name: Models
              description: List and describe the various models available in the API.
            - name: Moderations
              description: >-
                Given a input text, outputs if the model classifies it as
                violating OpenAI's content policy.
          paths:
            /embeddings:
              post:
                tags:
                  - Creates
                  - An
                  - Embedding
                  - Vector
                  - Representing
                  - The
                  - Input
                  - Text.
                  - Embeddings
                summary: Creates an embedding vector representing the input text.
          x-oaiMeta:
            groups:
              - id: audio
                title: Audio
                description: |
                  Learn how to turn audio into text or text into audio.

                  Related guide: [Speech to text](/docs/guides/speech-to-text)
                sections:
                  - type: endpoint
                    key: createSpeech
                    path: createSpeech
                  - type: endpoint
                    key: createTranscription
                    path: createTranscription
                  - type: endpoint
                    key: createTranslation
                    path: createTranslation
              - id: chat
                title: Chat
                description: >
                  Given a list of messages comprising a conversation, the model
                  will return a response.


                  Related guide: [Chat
                  Completions](/docs/guides/text-generation)
                sections:
                  - type: endpoint
                    key: createChatCompletion
                    path: create
                  - type: object
                    key: CreateChatCompletionResponse
                    path: object
                  - type: object
                    key: CreateChatCompletionStreamResponse
                    path: streaming
              - id: embeddings
                title: Embeddings
                description: >
                  Get a vector representation of a given input that can be
                  easily consumed by machine learning models and algorithms.


                  Related guide: [Embeddings](/docs/guides/embeddings)
                sections:
                  - type: endpoint
                    key: createEmbedding
                    path: create
                  - type: object
                    key: Embedding
                    path: object
              - id: fine-tuning
                title: Fine-tuning
                description: >
                  Manage fine-tuning jobs to tailor a model to your specific
                  training data.


                  Related guide: [Fine-tune models](/docs/guides/fine-tuning)
                sections:
                  - type: endpoint
                    key: createFineTuningJob
                    path: create
                  - type: endpoint
                    key: listPaginatedFineTuningJobs
                    path: list
                  - type: endpoint
                    key: listFineTuningEvents
                    path: list-events
                  - type: endpoint
                    key: retrieveFineTuningJob
                    path: retrieve
                  - type: endpoint
                    key: cancelFineTuningJob
                    path: cancel
                  - type: object
                    key: FineTuningJob
                    path: object
                  - type: object
                    key: FineTuningJobEvent
                    path: event-object
              - id: files
                title: Files
                description: >
                  Files are used to upload documents that can be used with
                  features like [Assistants](/docs/api-reference/assistants) and
                  [Fine-tuning](/docs/api-reference/fine-tuning).
                sections:
                  - type: endpoint
                    key: createFile
                    path: create
                  - type: endpoint
                    key: listFiles
                    path: list
                  - type: endpoint
                    key: retrieveFile
                    path: retrieve
                  - type: endpoint
                    key: deleteFile
                    path: delete
                  - type: endpoint
                    key: downloadFile
                    path: retrieve-contents
                  - type: object
                    key: OpenAIFile
                    path: object
              - id: images
                title: Images
                description: >
                  Given a prompt and/or an input image, the model will generate
                  a new image.


                  Related guide: [Image generation](/docs/guides/images)
                sections:
                  - type: endpoint
                    key: createImage
                    path: create
                  - type: endpoint
                    key: createImageEdit
                    path: createEdit
                  - type: endpoint
                    key: createImageVariation
                    path: createVariation
                  - type: object
                    key: Image
                    path: object
              - id: models
                title: Models
                description: >
                  List and describe the various models available in the API. You
                  can refer to the [Models](/docs/models) documentation to
                  understand what models are available and the differences
                  between them.
                sections:
                  - type: endpoint
                    key: listModels
                    path: list
                  - type: endpoint
                    key: retrieveModel
                    path: retrieve
                  - type: endpoint
                    key: deleteModel
                    path: delete
                  - type: object
                    key: Model
                    path: object
              - id: moderations
                title: Moderations
                description: >
                  Given a input text, outputs if the model classifies it as
                  violating OpenAI's content policy.


                  Related guide: [Moderations](/docs/guides/moderation)
                sections:
                  - type: endpoint
                    key: createModeration
                    path: create
                  - type: object
                    key: CreateModerationResponse
                    path: object
              - id: assistants
                title: Assistants
                beta: true
                description: >
                  Build assistants that can call models and use tools to perform
                  tasks.


                  [Get started with the Assistants API](/docs/assistants)
                sections:
                  - type: endpoint
                    key: createAssistant
                    path: createAssistant
                  - type: endpoint
                    key: createAssistantFile
                    path: createAssistantFile
                  - type: endpoint
                    key: listAssistants
                    path: listAssistants
                  - type: endpoint
                    key: listAssistantFiles
                    path: listAssistantFiles
                  - type: endpoint
                    key: getAssistant
                    path: getAssistant
                  - type: endpoint
                    key: getAssistantFile
                    path: getAssistantFile
                  - type: endpoint
                    key: modifyAssistant
                    path: modifyAssistant
                  - type: endpoint
                    key: deleteAssistant
                    path: deleteAssistant
                  - type: endpoint
                    key: deleteAssistantFile
                    path: deleteAssistantFile
                  - type: object
                    key: AssistantObject
                    path: object
                  - type: object
                    key: AssistantFileObject
                    path: file-object
              - id: threads
                title: Threads
                beta: true
                description: |
                  Create threads that assistants can interact with.

                  Related guide: [Assistants](/docs/assistants/overview)
                sections:
                  - type: endpoint
                    key: createThread
                    path: createThread
                  - type: endpoint
                    key: getThread
                    path: getThread
                  - type: endpoint
                    key: modifyThread
                    path: modifyThread
                  - type: endpoint
                    key: deleteThread
                    path: deleteThread
                  - type: object
                    key: ThreadObject
                    path: object
              - id: messages
                title: Messages
                beta: true
                description: |
                  Create messages within threads

                  Related guide: [Assistants](/docs/assistants/overview)
                sections:
                  - type: endpoint
                    key: createMessage
                    path: createMessage
                  - type: endpoint
                    key: listMessages
                    path: listMessages
                  - type: endpoint
                    key: listMessageFiles
                    path: listMessageFiles
                  - type: endpoint
                    key: getMessage
                    path: getMessage
                  - type: endpoint
                    key: getMessageFile
                    path: getMessageFile
                  - type: endpoint
                    key: modifyMessage
                    path: modifyMessage
                  - type: object
                    key: MessageObject
                    path: object
                  - type: object
                    key: MessageFileObject
                    path: file-object
              - id: runs
                title: Runs
                beta: true
                description: |
                  Represents an execution run on a thread.

                  Related guide: [Assistants](/docs/assistants/overview)
                sections:
                  - type: endpoint
                    key: createRun
                    path: createRun
                  - type: endpoint
                    key: createThreadAndRun
                    path: createThreadAndRun
                  - type: endpoint
                    key: listRuns
                    path: listRuns
                  - type: endpoint
                    key: listRunSteps
                    path: listRunSteps
                  - type: endpoint
                    key: getRun
                    path: getRun
                  - type: endpoint
                    key: getRunStep
                    path: getRunStep
                  - type: endpoint
                    key: modifyRun
                    path: modifyRun
                  - type: endpoint
                    key: submitToolOuputsToRun
                    path: submitToolOutputs
                  - type: endpoint
                    key: cancelRun
                    path: cancelRun
                  - type: object
                    key: RunObject
                    path: object
                  - type: object
                    key: RunStepObject
                    path: step-object
              - id: completions
                title: Completions
                legacy: true
                description: >
                  Given a prompt, the model will return one or more predicted
                  completions along with the probabilities of alternative tokens
                  at each position. Most developer should use our [Chat
                  Completions
                  API](/docs/guides/text-generation/text-generation-models) to
                  leverage our best and newest models. Most models that support
                  the legacy Completions endpoint [will be shut off on January
                  4th, 2024](/docs/deprecations/2023-07-06-gpt-and-embeddings).
                sections:
                  - type: endpoint
                    key: createCompletion
                    path: create
                  - type: object
                    key: CreateCompletionResponse
                    path: null
    overlays:
      - type: APIs.io Search
        url: >-
          overlays/https://github.com/apis-json/artisanal/tree/main/apis/openai/embeddings-openapi-search.yml
      - type: APIs.io Search
        url: overlays/embeddings-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/embeddings-openapi-api-evangelist-ratings.yml
    aid: openai:openai-embeddings-api
  - name: OpenAI Files API
    description: >-
      Files are used to upload documents that can be used with features like
      Assistants and Fine-tuning. Upload a file that can be used across various
      endpoints. The size of all the files uploaded by one organization can be
      up to 100 GB.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://platform.openai.com/docs/api-reference/files
    baseURL: https://platform.openai.com/
    tags: []
    properties:
      - type: Documentation
        url: https://platform.openai.com/docs/api-reference
      - type: OpenAPI
        data:
          openapi: 3.0.0
          info:
            title: ' files'
            license:
              name: MIT
              url: https://github.com/openai/openai-openapi/blob/master/LICENSE
          tags:
            - name: Assistants
              description: Build Assistants that can call models and use tools.
            - name: Audio
              description: Learn how to turn audio into text or text into audio.
            - name: Chat
              description: >-
                Given a list of messages comprising a conversation, the model
                will return a response.
            - name: Completions
              description: >-
                Given a prompt, the model will return one or more predicted
                completions, and can also return the probabilities of
                alternative tokens at each position.
            - name: Embeddings
              description: >-
                Get a vector representation of a given input that can be easily
                consumed by machine learning models and algorithms.
            - name: Fine-tuning
              description: >-
                Manage fine-tuning jobs to tailor a model to your specific
                training data.
            - name: Files
              description: >-
                Files are used to upload documents that can be used with
                features like Assistants and Fine-tuning.
            - name: Images
              description: >-
                Given a prompt and/or an input image, the model will generate a
                new image.
            - name: Models
              description: List and describe the various models available in the API.
            - name: Moderations
              description: >-
                Given a input text, outputs if the model classifies it as
                violating OpenAI's content policy.
          paths:
            /files:
              get:
                tags:
                  - Returns
                  - List
                  - Of
                  - Files
                  - That
                  - Belong
                  - To
                  - The
                  - User's
                  - Organization.
                  - Files
                summary: >-
                  Returns a list of files that belong to the user's
                  organization.
              post:
                tags:
                  - Upload
                  - File
                  - That
                  - Can
                  - Be
                  - Used
                  - Across
                  - Various
                  - Endpoints.
                  - The
                  - Size
                  - Of
                  - All
                  - Files
                  - Uploaded
                  - By
                  - One
                  - Organization
                  - Up
                  - To
                  - '100'
                  - |+
                    B.

                  - Individual
                  - Maximum
                  - '512'
                  - Or
                  - Million
                  - Tokens
                  - For
                  - Assistants.
                  - See
                  - Assistants
                  - Tools
                  - Guide](/docs/assistants/tools)
                  - Learn
                  - More
                  - About
                  - Types
                  - Supported.
                  - Fine-tuning
                  - Only
                  - Supports
                  - '`.jsonl`'
                  - |+
                    Files.

                  - Please
                  - '[contact'
                  - Us](https://help.openai.com/)
                  - If
                  - You
                  - Need
                  - Increase
                  - These
                  - Storage
                  - |
                    Limits.
                  - Files
                summary: >
                  Upload a file that can be used across various endpoints. The
                  size of all the files uploaded by one organization can be up
                  to 100 GB.


                  The size of individual files can be a maximum of 512 MB or 2
                  million tokens for Assistants. See the [Assistants Tools
                  guide](/docs/assistants/tools) to learn more about the types
                  of files supported. The Fine-tuning API only supports `.jsonl`
                  files.


                  Please [contact us](https://help.openai.com/) if you need to
                  increase these storage limits.
            /files/{file_id}:
              delete:
                tags:
                  - Delete
                  - File.
                  - Files
                  - File_id
                summary: Delete a file.
              get:
                tags:
                  - Returns
                  - Information
                  - About
                  - Specific
                  - File.
                  - Files
                  - File_id
                summary: Returns information about a specific file.
            /files/{file_id}/content:
              get:
                tags:
                  - Returns
                  - The
                  - Contents
                  - Of
                  - Specified
                  - File.
                  - Files
                  - File_id
                  - Content
                summary: Returns the contents of the specified file.
            /assistants/{assistant_id}/files:
              get:
                tags:
                  - Returns
                  - List
                  - Of
                  - Assistant
                  - Files.
                  - Files
                  - File_id
                  - Content
                  - Assistants
                  - Assistant_id
                summary: Returns a list of assistant files.
              post:
                tags:
                  - Create
                  - An
                  - Assistant
                  - File
                  - By
                  - Attaching
                  - File](/docs/api-reference/files)
                  - To
                  - '[assistant](/docs/api-reference/assistants).'
                  - Files
                  - File_id
                  - Content
                  - Assistants
                  - Assistant_id
                summary: >-
                  Create an assistant file by attaching a
                  [File](/docs/api-reference/files) to an
                  [assistant](/docs/api-reference/assistants).
            /assistants/{assistant_id}/files/{file_id}:
              get:
                tags:
                  - Retrieves
                  - An
                  - Assistant
                  - File.
                  - Files
                  - File_id
                  - Content
                  - Assistants
                  - Assistant_id
                summary: Retrieves an AssistantFile.
              delete:
                tags:
                  - Delete
                  - An
                  - Assistant
                  - File.
                  - Files
                  - File_id
                  - Content
                  - Assistants
                  - Assistant_id
                summary: Delete an assistant file.
            /threads/{thread_id}/messages/{message_id}/files:
              get:
                tags:
                  - Returns
                  - List
                  - Of
                  - Message
                  - Files.
                  - Files
                  - File_id
                  - Content
                  - Assistants
                  - Assistant_id
                  - Threads
                  - Thread_id
                  - Messages
                  - Message_id
                summary: Returns a list of message files.
            /threads/{thread_id}/messages/{message_id}/files/{file_id}:
              get:
                tags:
                  - Retrieves
                  - Message
                  - File.
                  - Files
                  - File_id
                  - Content
                  - Assistants
                  - Assistant_id
                  - Threads
                  - Thread_id
                  - Messages
                  - Message_id
                summary: Retrieves a message file.
          x-oaiMeta:
            groups:
              - id: audio
                title: Audio
                description: |
                  Learn how to turn audio into text or text into audio.

                  Related guide: [Speech to text](/docs/guides/speech-to-text)
                sections:
                  - type: endpoint
                    key: createSpeech
                    path: createSpeech
                  - type: endpoint
                    key: createTranscription
                    path: createTranscription
                  - type: endpoint
                    key: createTranslation
                    path: createTranslation
              - id: chat
                title: Chat
                description: >
                  Given a list of messages comprising a conversation, the model
                  will return a response.


                  Related guide: [Chat
                  Completions](/docs/guides/text-generation)
                sections:
                  - type: endpoint
                    key: createChatCompletion
                    path: create
                  - type: object
                    key: CreateChatCompletionResponse
                    path: object
                  - type: object
                    key: CreateChatCompletionStreamResponse
                    path: streaming
              - id: embeddings
                title: Embeddings
                description: >
                  Get a vector representation of a given input that can be
                  easily consumed by machine learning models and algorithms.


                  Related guide: [Embeddings](/docs/guides/embeddings)
                sections:
                  - type: endpoint
                    key: createEmbedding
                    path: create
                  - type: object
                    key: Embedding
                    path: object
              - id: fine-tuning
                title: Fine-tuning
                description: >
                  Manage fine-tuning jobs to tailor a model to your specific
                  training data.


                  Related guide: [Fine-tune models](/docs/guides/fine-tuning)
                sections:
                  - type: endpoint
                    key: createFineTuningJob
                    path: create
                  - type: endpoint
                    key: listPaginatedFineTuningJobs
                    path: list
                  - type: endpoint
                    key: listFineTuningEvents
                    path: list-events
                  - type: endpoint
                    key: retrieveFineTuningJob
                    path: retrieve
                  - type: endpoint
                    key: cancelFineTuningJob
                    path: cancel
                  - type: object
                    key: FineTuningJob
                    path: object
                  - type: object
                    key: FineTuningJobEvent
                    path: event-object
              - id: files
                title: Files
                description: >
                  Files are used to upload documents that can be used with
                  features like [Assistants](/docs/api-reference/assistants) and
                  [Fine-tuning](/docs/api-reference/fine-tuning).
                sections:
                  - type: endpoint
                    key: createFile
                    path: create
                  - type: endpoint
                    key: listFiles
                    path: list
                  - type: endpoint
                    key: retrieveFile
                    path: retrieve
                  - type: endpoint
                    key: deleteFile
                    path: delete
                  - type: endpoint
                    key: downloadFile
                    path: retrieve-contents
                  - type: object
                    key: OpenAIFile
                    path: object
              - id: images
                title: Images
                description: >
                  Given a prompt and/or an input image, the model will generate
                  a new image.


                  Related guide: [Image generation](/docs/guides/images)
                sections:
                  - type: endpoint
                    key: createImage
                    path: create
                  - type: endpoint
                    key: createImageEdit
                    path: createEdit
                  - type: endpoint
                    key: createImageVariation
                    path: createVariation
                  - type: object
                    key: Image
                    path: object
              - id: models
                title: Models
                description: >
                  List and describe the various models available in the API. You
                  can refer to the [Models](/docs/models) documentation to
                  understand what models are available and the differences
                  between them.
                sections:
                  - type: endpoint
                    key: listModels
                    path: list
                  - type: endpoint
                    key: retrieveModel
                    path: retrieve
                  - type: endpoint
                    key: deleteModel
                    path: delete
                  - type: object
                    key: Model
                    path: object
              - id: moderations
                title: Moderations
                description: >
                  Given a input text, outputs if the model classifies it as
                  violating OpenAI's content policy.


                  Related guide: [Moderations](/docs/guides/moderation)
                sections:
                  - type: endpoint
                    key: createModeration
                    path: create
                  - type: object
                    key: CreateModerationResponse
                    path: object
              - id: assistants
                title: Assistants
                beta: true
                description: >
                  Build assistants that can call models and use tools to perform
                  tasks.


                  [Get started with the Assistants API](/docs/assistants)
                sections:
                  - type: endpoint
                    key: createAssistant
                    path: createAssistant
                  - type: endpoint
                    key: createAssistantFile
                    path: createAssistantFile
                  - type: endpoint
                    key: listAssistants
                    path: listAssistants
                  - type: endpoint
                    key: listAssistantFiles
                    path: listAssistantFiles
                  - type: endpoint
                    key: getAssistant
                    path: getAssistant
                  - type: endpoint
                    key: getAssistantFile
                    path: getAssistantFile
                  - type: endpoint
                    key: modifyAssistant
                    path: modifyAssistant
                  - type: endpoint
                    key: deleteAssistant
                    path: deleteAssistant
                  - type: endpoint
                    key: deleteAssistantFile
                    path: deleteAssistantFile
                  - type: object
                    key: AssistantObject
                    path: object
                  - type: object
                    key: AssistantFileObject
                    path: file-object
              - id: threads
                title: Threads
                beta: true
                description: |
                  Create threads that assistants can interact with.

                  Related guide: [Assistants](/docs/assistants/overview)
                sections:
                  - type: endpoint
                    key: createThread
                    path: createThread
                  - type: endpoint
                    key: getThread
                    path: getThread
                  - type: endpoint
                    key: modifyThread
                    path: modifyThread
                  - type: endpoint
                    key: deleteThread
                    path: deleteThread
                  - type: object
                    key: ThreadObject
                    path: object
              - id: messages
                title: Messages
                beta: true
                description: |
                  Create messages within threads

                  Related guide: [Assistants](/docs/assistants/overview)
                sections:
                  - type: endpoint
                    key: createMessage
                    path: createMessage
                  - type: endpoint
                    key: listMessages
                    path: listMessages
                  - type: endpoint
                    key: listMessageFiles
                    path: listMessageFiles
                  - type: endpoint
                    key: getMessage
                    path: getMessage
                  - type: endpoint
                    key: getMessageFile
                    path: getMessageFile
                  - type: endpoint
                    key: modifyMessage
                    path: modifyMessage
                  - type: object
                    key: MessageObject
                    path: object
                  - type: object
                    key: MessageFileObject
                    path: file-object
              - id: runs
                title: Runs
                beta: true
                description: |
                  Represents an execution run on a thread.

                  Related guide: [Assistants](/docs/assistants/overview)
                sections:
                  - type: endpoint
                    key: createRun
                    path: createRun
                  - type: endpoint
                    key: createThreadAndRun
                    path: createThreadAndRun
                  - type: endpoint
                    key: listRuns
                    path: listRuns
                  - type: endpoint
                    key: listRunSteps
                    path: listRunSteps
                  - type: endpoint
                    key: getRun
                    path: getRun
                  - type: endpoint
                    key: getRunStep
                    path: getRunStep
                  - type: endpoint
                    key: modifyRun
                    path: modifyRun
                  - type: endpoint
                    key: submitToolOuputsToRun
                    path: submitToolOutputs
                  - type: endpoint
                    key: cancelRun
                    path: cancelRun
                  - type: object
                    key: RunObject
                    path: object
                  - type: object
                    key: RunStepObject
                    path: step-object
              - id: completions
                title: Completions
                legacy: true
                description: >
                  Given a prompt, the model will return one or more predicted
                  completions along with the probabilities of alternative tokens
                  at each position. Most developer should use our [Chat
                  Completions
                  API](/docs/guides/text-generation/text-generation-models) to
                  leverage our best and newest models. Most models that support
                  the legacy Completions endpoint [will be shut off on January
                  4th, 2024](/docs/deprecations/2023-07-06-gpt-and-embeddings).
                sections:
                  - type: endpoint
                    key: createCompletion
                    path: create
                  - type: object
                    key: CreateCompletionResponse
                    path: null
    overlays:
      - type: APIs.io Search
        url: >-
          overlays/https://github.com/apis-json/artisanal/tree/main/apis/openai/files-openapi-search.yml
      - type: APIs.io Search
        url: overlays/files-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/files-openapi-api-evangelist-ratings.yml
    aid: openai:openai-files-api
  - name: OpenAI Fine Tuning API
    description: >-
      Manage fine-tuning jobs to tailor a model to your specific training data.
      Creates a fine-tuning job which begins the process of creating a new model
      from a given dataset.Response includes details of the enqueued job
      including job status and the name of the fine-tuned models once complete.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://platform.openai.com/docs/api-reference/fine-tuning
    baseURL: https://platform.openai.com/
    tags: []
    properties:
      - type: Documentation
        url: https://platform.openai.com/docs/api-reference
      - type: OpenAPI
        data:
          openapi: 3.0.0
          info:
            title: ' fine tuning'
            license:
              name: MIT
              url: https://github.com/openai/openai-openapi/blob/master/LICENSE
          tags:
            - name: Assistants
              description: Build Assistants that can call models and use tools.
            - name: Audio
              description: Learn how to turn audio into text or text into audio.
            - name: Chat
              description: >-
                Given a list of messages comprising a conversation, the model
                will return a response.
            - name: Completions
              description: >-
                Given a prompt, the model will return one or more predicted
                completions, and can also return the probabilities of
                alternative tokens at each position.
            - name: Embeddings
              description: >-
                Get a vector representation of a given input that can be easily
                consumed by machine learning models and algorithms.
            - name: Fine-tuning
              description: >-
                Manage fine-tuning jobs to tailor a model to your specific
                training data.
            - name: Files
              description: >-
                Files are used to upload documents that can be used with
                features like Assistants and Fine-tuning.
            - name: Images
              description: >-
                Given a prompt and/or an input image, the model will generate a
                new image.
            - name: Models
              description: List and describe the various models available in the API.
            - name: Moderations
              description: >-
                Given a input text, outputs if the model classifies it as
                violating OpenAI's content policy.
          paths:
            /fine_tuning/jobs:
              post:
                tags:
                  - Creates
                  - Fine-tuning
                  - Job
                  - Which
                  - Begins
                  - The
                  - Process
                  - Of
                  - Creating
                  - New
                  - Model
                  - From
                  - Given
                  - |+
                    Dataset.

                  - Response
                  - Includes
                  - Details
                  - Enqueued
                  - Including
                  - Status
                  - And
                  - Name
                  - Fine-tuned
                  - Models
                  - Once
                  - |-
                    Complete.

                    [
                  - Learn
                  - More
                  - About
                  - |
                    Fine-tuning](/docs/guides/fine-tuning)
                  - Fine_tuning
                  - Jobs
                summary: >
                  Creates a fine-tuning job which begins the process of creating
                  a new model from a given dataset.


                  Response includes details of the enqueued job including job
                  status and the name of the fine-tuned models once complete.


                  [Learn more about fine-tuning](/docs/guides/fine-tuning)
              get:
                tags:
                  - List
                  - Your
                  - Organization's
                  - Fine-tuning
                  - |
                    Jobs
                  - Fine_tuning
                  - Jobs
                summary: |
                  List your organization's fine-tuning jobs
            /fine_tuning/jobs/{fine_tuning_job_id}:
              get:
                tags:
                  - Get
                  - Info
                  - About
                  - Fine-tuning
                  - |-
                    Job.

                    [
                  - Learn
                  - More
                  - |
                    Fine-tuning](/docs/guides/fine-tuning)
                  - Fine_tuning
                  - Jobs
                  - Fine_tuning_job_id
                summary: |
                  Get info about a fine-tuning job.

                  [Learn more about fine-tuning](/docs/guides/fine-tuning)
            /fine_tuning/jobs/{fine_tuning_job_id}/events:
              get:
                tags:
                  - Get
                  - Status
                  - Updates
                  - For
                  - Fine-tuning
                  - |
                    Job.
                  - Fine_tuning
                  - Jobs
                  - Fine_tuning_job_id
                  - Events
                summary: |
                  Get status updates for a fine-tuning job.
            /fine_tuning/jobs/{fine_tuning_job_id}/cancel:
              post:
                tags:
                  - Immediately
                  - Cancel
                  - Fine-tune
                  - |
                    Job.
                  - Fine_tuning
                  - Jobs
                  - Fine_tuning_job_id
                  - Events
                  - Cancel
                summary: |
                  Immediately cancel a fine-tune job.
          x-oaiMeta:
            groups:
              - id: audio
                title: Audio
                description: |
                  Learn how to turn audio into text or text into audio.

                  Related guide: [Speech to text](/docs/guides/speech-to-text)
                sections:
                  - type: endpoint
                    key: createSpeech
                    path: createSpeech
                  - type: endpoint
                    key: createTranscription
                    path: createTranscription
                  - type: endpoint
                    key: createTranslation
                    path: createTranslation
              - id: chat
                title: Chat
                description: >
                  Given a list of messages comprising a conversation, the model
                  will return a response.


                  Related guide: [Chat
                  Completions](/docs/guides/text-generation)
                sections:
                  - type: endpoint
                    key: createChatCompletion
                    path: create
                  - type: object
                    key: CreateChatCompletionResponse
                    path: object
                  - type: object
                    key: CreateChatCompletionStreamResponse
                    path: streaming
              - id: embeddings
                title: Embeddings
                description: >
                  Get a vector representation of a given input that can be
                  easily consumed by machine learning models and algorithms.


                  Related guide: [Embeddings](/docs/guides/embeddings)
                sections:
                  - type: endpoint
                    key: createEmbedding
                    path: create
                  - type: object
                    key: Embedding
                    path: object
              - id: fine-tuning
                title: Fine-tuning
                description: >
                  Manage fine-tuning jobs to tailor a model to your specific
                  training data.


                  Related guide: [Fine-tune models](/docs/guides/fine-tuning)
                sections:
                  - type: endpoint
                    key: createFineTuningJob
                    path: create
                  - type: endpoint
                    key: listPaginatedFineTuningJobs
                    path: list
                  - type: endpoint
                    key: listFineTuningEvents
                    path: list-events
                  - type: endpoint
                    key: retrieveFineTuningJob
                    path: retrieve
                  - type: endpoint
                    key: cancelFineTuningJob
                    path: cancel
                  - type: object
                    key: FineTuningJob
                    path: object
                  - type: object
                    key: FineTuningJobEvent
                    path: event-object
              - id: files
                title: Files
                description: >
                  Files are used to upload documents that can be used with
                  features like [Assistants](/docs/api-reference/assistants) and
                  [Fine-tuning](/docs/api-reference/fine-tuning).
                sections:
                  - type: endpoint
                    key: createFile
                    path: create
                  - type: endpoint
                    key: listFiles
                    path: list
                  - type: endpoint
                    key: retrieveFile
                    path: retrieve
                  - type: endpoint
                    key: deleteFile
                    path: delete
                  - type: endpoint
                    key: downloadFile
                    path: retrieve-contents
                  - type: object
                    key: OpenAIFile
                    path: object
              - id: images
                title: Images
                description: >
                  Given a prompt and/or an input image, the model will generate
                  a new image.


                  Related guide: [Image generation](/docs/guides/images)
                sections:
                  - type: endpoint
                    key: createImage
                    path: create
                  - type: endpoint
                    key: createImageEdit
                    path: createEdit
                  - type: endpoint
                    key: createImageVariation
                    path: createVariation
                  - type: object
                    key: Image
                    path: object
              - id: models
                title: Models
                description: >
                  List and describe the various models available in the API. You
                  can refer to the [Models](/docs/models) documentation to
                  understand what models are available and the differences
                  between them.
                sections:
                  - type: endpoint
                    key: listModels
                    path: list
                  - type: endpoint
                    key: retrieveModel
                    path: retrieve
                  - type: endpoint
                    key: deleteModel
                    path: delete
                  - type: object
                    key: Model
                    path: object
              - id: moderations
                title: Moderations
                description: >
                  Given a input text, outputs if the model classifies it as
                  violating OpenAI's content policy.


                  Related guide: [Moderations](/docs/guides/moderation)
                sections:
                  - type: endpoint
                    key: createModeration
                    path: create
                  - type: object
                    key: CreateModerationResponse
                    path: object
              - id: assistants
                title: Assistants
                beta: true
                description: >
                  Build assistants that can call models and use tools to perform
                  tasks.


                  [Get started with the Assistants API](/docs/assistants)
                sections:
                  - type: endpoint
                    key: createAssistant
                    path: createAssistant
                  - type: endpoint
                    key: createAssistantFile
                    path: createAssistantFile
                  - type: endpoint
                    key: listAssistants
                    path: listAssistants
                  - type: endpoint
                    key: listAssistantFiles
                    path: listAssistantFiles
                  - type: endpoint
                    key: getAssistant
                    path: getAssistant
                  - type: endpoint
                    key: getAssistantFile
                    path: getAssistantFile
                  - type: endpoint
                    key: modifyAssistant
                    path: modifyAssistant
                  - type: endpoint
                    key: deleteAssistant
                    path: deleteAssistant
                  - type: endpoint
                    key: deleteAssistantFile
                    path: deleteAssistantFile
                  - type: object
                    key: AssistantObject
                    path: object
                  - type: object
                    key: AssistantFileObject
                    path: file-object
              - id: threads
                title: Threads
                beta: true
                description: |
                  Create threads that assistants can interact with.

                  Related guide: [Assistants](/docs/assistants/overview)
                sections:
                  - type: endpoint
                    key: createThread
                    path: createThread
                  - type: endpoint
                    key: getThread
                    path: getThread
                  - type: endpoint
                    key: modifyThread
                    path: modifyThread
                  - type: endpoint
                    key: deleteThread
                    path: deleteThread
                  - type: object
                    key: ThreadObject
                    path: object
              - id: messages
                title: Messages
                beta: true
                description: |
                  Create messages within threads

                  Related guide: [Assistants](/docs/assistants/overview)
                sections:
                  - type: endpoint
                    key: createMessage
                    path: createMessage
                  - type: endpoint
                    key: listMessages
                    path: listMessages
                  - type: endpoint
                    key: listMessageFiles
                    path: listMessageFiles
                  - type: endpoint
                    key: getMessage
                    path: getMessage
                  - type: endpoint
                    key: getMessageFile
                    path: getMessageFile
                  - type: endpoint
                    key: modifyMessage
                    path: modifyMessage
                  - type: object
                    key: MessageObject
                    path: object
                  - type: object
                    key: MessageFileObject
                    path: file-object
              - id: runs
                title: Runs
                beta: true
                description: |
                  Represents an execution run on a thread.

                  Related guide: [Assistants](/docs/assistants/overview)
                sections:
                  - type: endpoint
                    key: createRun
                    path: createRun
                  - type: endpoint
                    key: createThreadAndRun
                    path: createThreadAndRun
                  - type: endpoint
                    key: listRuns
                    path: listRuns
                  - type: endpoint
                    key: listRunSteps
                    path: listRunSteps
                  - type: endpoint
                    key: getRun
                    path: getRun
                  - type: endpoint
                    key: getRunStep
                    path: getRunStep
                  - type: endpoint
                    key: modifyRun
                    path: modifyRun
                  - type: endpoint
                    key: submitToolOuputsToRun
                    path: submitToolOutputs
                  - type: endpoint
                    key: cancelRun
                    path: cancelRun
                  - type: object
                    key: RunObject
                    path: object
                  - type: object
                    key: RunStepObject
                    path: step-object
              - id: completions
                title: Completions
                legacy: true
                description: >
                  Given a prompt, the model will return one or more predicted
                  completions along with the probabilities of alternative tokens
                  at each position. Most developer should use our [Chat
                  Completions
                  API](/docs/guides/text-generation/text-generation-models) to
                  leverage our best and newest models. Most models that support
                  the legacy Completions endpoint [will be shut off on January
                  4th, 2024](/docs/deprecations/2023-07-06-gpt-and-embeddings).
                sections:
                  - type: endpoint
                    key: createCompletion
                    path: create
                  - type: object
                    key: CreateCompletionResponse
                    path: null
    overlays:
      - type: APIs.io Search
        url: >-
          overlays/https://github.com/apis-json/artisanal/tree/main/apis/openai/fint-tuning-openapi-search.yml
      - type: APIs.io Search
        url: overlays/fint-tuning-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/fine-tuning-openapi-api-evangelist-ratings.yml
      - type: APIs.io Search
        url: overlays/fine-tuning-openapi-search.yml
    aid: openai:openai-fine-tuning-api
  - name: OpenAI Images API
    description: >-
      Learn how to generate or manipulate images with DALL·E in the API. The
      Images API provides three methods for interacting with images - creating
      images from scratch based on a text prompt, creating edited versions of
      images by having the model replace some areas of a pre-existing image,
      based on a new text prompt, Creating variations of an existing image.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://platform.openai.com/docs/guides/images/image-generation
    baseURL: https://platform.openai.com/
    tags: []
    properties:
      - type: Documentation
        url: https://platform.openai.com/docs/api-reference
      - type: OpenAPI
        data:
          openapi: 3.0.0
          info:
            title: ' images'
            license:
              name: MIT
              url: https://github.com/openai/openai-openapi/blob/master/LICENSE
          tags:
            - name: Assistants
              description: Build Assistants that can call models and use tools.
            - name: Audio
              description: Learn how to turn audio into text or text into audio.
            - name: Chat
              description: >-
                Given a list of messages comprising a conversation, the model
                will return a response.
            - name: Completions
              description: >-
                Given a prompt, the model will return one or more predicted
                completions, and can also return the probabilities of
                alternative tokens at each position.
            - name: Embeddings
              description: >-
                Get a vector representation of a given input that can be easily
                consumed by machine learning models and algorithms.
            - name: Fine-tuning
              description: >-
                Manage fine-tuning jobs to tailor a model to your specific
                training data.
            - name: Files
              description: >-
                Files are used to upload documents that can be used with
                features like Assistants and Fine-tuning.
            - name: Images
              description: >-
                Given a prompt and/or an input image, the model will generate a
                new image.
            - name: Models
              description: List and describe the various models available in the API.
            - name: Moderations
              description: >-
                Given a input text, outputs if the model classifies it as
                violating OpenAI's content policy.
          paths:
            /images/generations:
              post:
                tags:
                  - Creates
                  - An
                  - Image
                  - Given
                  - Prompt.
                  - Images
                  - Generations
                summary: Creates an image given a prompt.
            /images/edits:
              post:
                tags:
                  - Creates
                  - An
                  - Edited
                  - Or
                  - Extended
                  - Image
                  - Given
                  - Original
                  - And
                  - Prompt.
                  - Images
                  - Generations
                  - Edits
                summary: >-
                  Creates an edited or extended image given an original image
                  and a prompt.
            /images/variations:
              post:
                tags:
                  - Creates
                  - Variation
                  - Of
                  - Given
                  - Image.
                  - Images
                  - Generations
                  - Edits
                  - Variations
                summary: Creates a variation of a given image.
          x-oaiMeta:
            groups:
              - id: audio
                title: Audio
                description: |
                  Learn how to turn audio into text or text into audio.

                  Related guide: [Speech to text](/docs/guides/speech-to-text)
                sections:
                  - type: endpoint
                    key: createSpeech
                    path: createSpeech
                  - type: endpoint
                    key: createTranscription
                    path: createTranscription
                  - type: endpoint
                    key: createTranslation
                    path: createTranslation
              - id: chat
                title: Chat
                description: >
                  Given a list of messages comprising a conversation, the model
                  will return a response.


                  Related guide: [Chat
                  Completions](/docs/guides/text-generation)
                sections:
                  - type: endpoint
                    key: createChatCompletion
                    path: create
                  - type: object
                    key: CreateChatCompletionResponse
                    path: object
                  - type: object
                    key: CreateChatCompletionStreamResponse
                    path: streaming
              - id: embeddings
                title: Embeddings
                description: >
                  Get a vector representation of a given input that can be
                  easily consumed by machine learning models and algorithms.


                  Related guide: [Embeddings](/docs/guides/embeddings)
                sections:
                  - type: endpoint
                    key: createEmbedding
                    path: create
                  - type: object
                    key: Embedding
                    path: object
              - id: fine-tuning
                title: Fine-tuning
                description: >
                  Manage fine-tuning jobs to tailor a model to your specific
                  training data.


                  Related guide: [Fine-tune models](/docs/guides/fine-tuning)
                sections:
                  - type: endpoint
                    key: createFineTuningJob
                    path: create
                  - type: endpoint
                    key: listPaginatedFineTuningJobs
                    path: list
                  - type: endpoint
                    key: listFineTuningEvents
                    path: list-events
                  - type: endpoint
                    key: retrieveFineTuningJob
                    path: retrieve
                  - type: endpoint
                    key: cancelFineTuningJob
                    path: cancel
                  - type: object
                    key: FineTuningJob
                    path: object
                  - type: object
                    key: FineTuningJobEvent
                    path: event-object
              - id: files
                title: Files
                description: >
                  Files are used to upload documents that can be used with
                  features like [Assistants](/docs/api-reference/assistants) and
                  [Fine-tuning](/docs/api-reference/fine-tuning).
                sections:
                  - type: endpoint
                    key: createFile
                    path: create
                  - type: endpoint
                    key: listFiles
                    path: list
                  - type: endpoint
                    key: retrieveFile
                    path: retrieve
                  - type: endpoint
                    key: deleteFile
                    path: delete
                  - type: endpoint
                    key: downloadFile
                    path: retrieve-contents
                  - type: object
                    key: OpenAIFile
                    path: object
              - id: images
                title: Images
                description: >
                  Given a prompt and/or an input image, the model will generate
                  a new image.


                  Related guide: [Image generation](/docs/guides/images)
                sections:
                  - type: endpoint
                    key: createImage
                    path: create
                  - type: endpoint
                    key: createImageEdit
                    path: createEdit
                  - type: endpoint
                    key: createImageVariation
                    path: createVariation
                  - type: object
                    key: Image
                    path: object
              - id: models
                title: Models
                description: >
                  List and describe the various models available in the API. You
                  can refer to the [Models](/docs/models) documentation to
                  understand what models are available and the differences
                  between them.
                sections:
                  - type: endpoint
                    key: listModels
                    path: list
                  - type: endpoint
                    key: retrieveModel
                    path: retrieve
                  - type: endpoint
                    key: deleteModel
                    path: delete
                  - type: object
                    key: Model
                    path: object
              - id: moderations
                title: Moderations
                description: >
                  Given a input text, outputs if the model classifies it as
                  violating OpenAI's content policy.


                  Related guide: [Moderations](/docs/guides/moderation)
                sections:
                  - type: endpoint
                    key: createModeration
                    path: create
                  - type: object
                    key: CreateModerationResponse
                    path: object
              - id: assistants
                title: Assistants
                beta: true
                description: >
                  Build assistants that can call models and use tools to perform
                  tasks.


                  [Get started with the Assistants API](/docs/assistants)
                sections:
                  - type: endpoint
                    key: createAssistant
                    path: createAssistant
                  - type: endpoint
                    key: createAssistantFile
                    path: createAssistantFile
                  - type: endpoint
                    key: listAssistants
                    path: listAssistants
                  - type: endpoint
                    key: listAssistantFiles
                    path: listAssistantFiles
                  - type: endpoint
                    key: getAssistant
                    path: getAssistant
                  - type: endpoint
                    key: getAssistantFile
                    path: getAssistantFile
                  - type: endpoint
                    key: modifyAssistant
                    path: modifyAssistant
                  - type: endpoint
                    key: deleteAssistant
                    path: deleteAssistant
                  - type: endpoint
                    key: deleteAssistantFile
                    path: deleteAssistantFile
                  - type: object
                    key: AssistantObject
                    path: object
                  - type: object
                    key: AssistantFileObject
                    path: file-object
              - id: threads
                title: Threads
                beta: true
                description: |
                  Create threads that assistants can interact with.

                  Related guide: [Assistants](/docs/assistants/overview)
                sections:
                  - type: endpoint
                    key: createThread
                    path: createThread
                  - type: endpoint
                    key: getThread
                    path: getThread
                  - type: endpoint
                    key: modifyThread
                    path: modifyThread
                  - type: endpoint
                    key: deleteThread
                    path: deleteThread
                  - type: object
                    key: ThreadObject
                    path: object
              - id: messages
                title: Messages
                beta: true
                description: |
                  Create messages within threads

                  Related guide: [Assistants](/docs/assistants/overview)
                sections:
                  - type: endpoint
                    key: createMessage
                    path: createMessage
                  - type: endpoint
                    key: listMessages
                    path: listMessages
                  - type: endpoint
                    key: listMessageFiles
                    path: listMessageFiles
                  - type: endpoint
                    key: getMessage
                    path: getMessage
                  - type: endpoint
                    key: getMessageFile
                    path: getMessageFile
                  - type: endpoint
                    key: modifyMessage
                    path: modifyMessage
                  - type: object
                    key: MessageObject
                    path: object
                  - type: object
                    key: MessageFileObject
                    path: file-object
              - id: runs
                title: Runs
                beta: true
                description: |
                  Represents an execution run on a thread.

                  Related guide: [Assistants](/docs/assistants/overview)
                sections:
                  - type: endpoint
                    key: createRun
                    path: createRun
                  - type: endpoint
                    key: createThreadAndRun
                    path: createThreadAndRun
                  - type: endpoint
                    key: listRuns
                    path: listRuns
                  - type: endpoint
                    key: listRunSteps
                    path: listRunSteps
                  - type: endpoint
                    key: getRun
                    path: getRun
                  - type: endpoint
                    key: getRunStep
                    path: getRunStep
                  - type: endpoint
                    key: modifyRun
                    path: modifyRun
                  - type: endpoint
                    key: submitToolOuputsToRun
                    path: submitToolOutputs
                  - type: endpoint
                    key: cancelRun
                    path: cancelRun
                  - type: object
                    key: RunObject
                    path: object
                  - type: object
                    key: RunStepObject
                    path: step-object
              - id: completions
                title: Completions
                legacy: true
                description: >
                  Given a prompt, the model will return one or more predicted
                  completions along with the probabilities of alternative tokens
                  at each position. Most developer should use our [Chat
                  Completions
                  API](/docs/guides/text-generation/text-generation-models) to
                  leverage our best and newest models. Most models that support
                  the legacy Completions endpoint [will be shut off on January
                  4th, 2024](/docs/deprecations/2023-07-06-gpt-and-embeddings).
                sections:
                  - type: endpoint
                    key: createCompletion
                    path: create
                  - type: object
                    key: CreateCompletionResponse
                    path: null
    overlays:
      - type: APIs.io Search
        url: >-
          overlays/https://github.com/apis-json/artisanal/tree/main/apis/openai/images-openapi-search.yml
      - type: APIs.io Search
        url: overlays/images-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/images-openapi-api-evangelist-ratings.yml
    aid: openai:openai-images-api
  - name: OpenAI Threads API
    description: Create threads that assistants can interact with.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://platform.openai.com/docs/api-reference/threads
    baseURL: https://platform.openai.com/
    tags: []
    properties:
      - type: Documentation
        url: https://platform.openai.com/docs/api-reference
      - type: OpenAPI
        data:
          openapi: 3.0.0
          info:
            title: ' threads'
            license:
              name: MIT
              url: https://github.com/openai/openai-openapi/blob/master/LICENSE
          tags:
            - name: Assistants
              description: Build Assistants that can call models and use tools.
            - name: Audio
              description: Learn how to turn audio into text or text into audio.
            - name: Chat
              description: >-
                Given a list of messages comprising a conversation, the model
                will return a response.
            - name: Completions
              description: >-
                Given a prompt, the model will return one or more predicted
                completions, and can also return the probabilities of
                alternative tokens at each position.
            - name: Embeddings
              description: >-
                Get a vector representation of a given input that can be easily
                consumed by machine learning models and algorithms.
            - name: Fine-tuning
              description: >-
                Manage fine-tuning jobs to tailor a model to your specific
                training data.
            - name: Files
              description: >-
                Files are used to upload documents that can be used with
                features like Assistants and Fine-tuning.
            - name: Images
              description: >-
                Given a prompt and/or an input image, the model will generate a
                new image.
            - name: Models
              description: List and describe the various models available in the API.
            - name: Moderations
              description: >-
                Given a input text, outputs if the model classifies it as
                violating OpenAI's content policy.
          paths:
            /threads:
              post:
                tags:
                  - Create
                  - Thread.
                  - Threads
                summary: Create a thread.
            /threads/{thread_id}:
              get:
                tags:
                  - Retrieves
                  - Thread.
                  - Threads
                  - Thread_id
                summary: Retrieves a thread.
              post:
                tags:
                  - Modifies
                  - Thread.
                  - Threads
                  - Thread_id
                summary: Modifies a thread.
              delete:
                tags:
                  - Delete
                  - Thread.
                  - Threads
                  - Thread_id
                summary: Delete a thread.
            /threads/{thread_id}/messages:
              get:
                tags:
                  - Returns
                  - List
                  - Of
                  - Messages
                  - For
                  - Given
                  - Thread.
                  - Threads
                  - Thread_id
                  - Messages
                summary: Returns a list of messages for a given thread.
              post:
                tags:
                  - Create
                  - Message.
                  - Threads
                  - Thread_id
                  - Messages
                summary: Create a message.
            /threads/{thread_id}/messages/{message_id}:
              get:
                tags:
                  - Retrieve
                  - Message.
                  - Threads
                  - Thread_id
                  - Messages
                  - Message_id
                summary: Retrieve a message.
              post:
                tags:
                  - Modifies
                  - Message.
                  - Threads
                  - Thread_id
                  - Messages
                  - Message_id
                summary: Modifies a message.
            /threads/runs:
              post:
                tags:
                  - Create
                  - Thread
                  - And
                  - Run
                  - It
                  - In
                  - One
                  - Request.
                  - Threads
                  - Thread_id
                  - Messages
                  - Message_id
                  - Runs
                summary: Create a thread and run it in one request.
            /threads/{thread_id}/runs:
              get:
                tags:
                  - Returns
                  - List
                  - Of
                  - Runs
                  - Belonging
                  - To
                  - Thread.
                  - Threads
                  - Thread_id
                  - Messages
                  - Message_id
                  - Runs
                summary: Returns a list of runs belonging to a thread.
              post:
                tags:
                  - Create
                  - Run.
                  - Threads
                  - Thread_id
                  - Messages
                  - Message_id
                  - Runs
                summary: Create a run.
            /threads/{thread_id}/runs/{run_id}:
              get:
                tags:
                  - Retrieves
                  - Run.
                  - Threads
                  - Thread_id
                  - Messages
                  - Message_id
                  - Runs
                  - Run_id
                summary: Retrieves a run.
              post:
                tags:
                  - Modifies
                  - Run.
                  - Threads
                  - Thread_id
                  - Messages
                  - Message_id
                  - Runs
                  - Run_id
                summary: Modifies a run.
            /threads/{thread_id}/runs/{run_id}/submit_tool_outputs:
              post:
                tags:
                  - When
                  - Run
                  - Has
                  - The
                  - '`status:'
                  - '"requires_action"`'
                  - And
                  - '`required_action.type`'
                  - Is
                  - '`submit_tool_outputs`,'
                  - This
                  - Endpoint
                  - Can
                  - Be
                  - Used
                  - To
                  - Submit
                  - Outputs
                  - From
                  - Tool
                  - Calls
                  - Once
                  - They're
                  - All
                  - Completed.
                  - Must
                  - Submitted
                  - In
                  - Single
                  - |
                    Request.
                  - Threads
                  - Thread_id
                  - Messages
                  - Message_id
                  - Runs
                  - Run_id
                  - Submit_tool_outputs
                summary: >
                  When a run has the `status: "requires_action"` and
                  `required_action.type` is `submit_tool_outputs`, this endpoint
                  can be used to submit the outputs from the tool calls once
                  they're all completed. All outputs must be submitted in a
                  single request.
            /threads/{thread_id}/runs/{run_id}/cancel:
              post:
                tags:
                  - Cancels
                  - Run
                  - That
                  - Is
                  - '`in_progress`.'
                  - Threads
                  - Thread_id
                  - Messages
                  - Message_id
                  - Runs
                  - Run_id
                  - Submit_tool_outputs
                  - Cancel
                summary: Cancels a run that is `in_progress`.
            /threads/{thread_id}/runs/{run_id}/steps:
              get:
                tags:
                  - Returns
                  - List
                  - Of
                  - Run
                  - Steps
                  - Belonging
                  - To
                  - Run.
                  - Threads
                  - Thread_id
                  - Messages
                  - Message_id
                  - Runs
                  - Run_id
                  - Submit_tool_outputs
                  - Cancel
                  - Steps
                summary: Returns a list of run steps belonging to a run.
            /threads/{thread_id}/runs/{run_id}/steps/{step_id}:
              get:
                tags:
                  - Retrieves
                  - Run
                  - Step.
                  - Threads
                  - Thread_id
                  - Messages
                  - Message_id
                  - Runs
                  - Run_id
                  - Submit_tool_outputs
                  - Cancel
                  - Steps
                  - Step_id
                summary: Retrieves a run step.
            /threads/{thread_id}/messages/{message_id}/files:
              get:
                tags:
                  - Returns
                  - List
                  - Of
                  - Message
                  - Files.
                  - Threads
                  - Thread_id
                  - Messages
                  - Message_id
                  - Runs
                  - Run_id
                  - Submit_tool_outputs
                  - Cancel
                  - Steps
                  - Step_id
                  - Files
                summary: Returns a list of message files.
            /threads/{thread_id}/messages/{message_id}/files/{file_id}:
              get:
                tags:
                  - Retrieves
                  - Message
                  - File.
                  - Threads
                  - Thread_id
                  - Messages
                  - Message_id
                  - Runs
                  - Run_id
                  - Submit_tool_outputs
                  - Cancel
                  - Steps
                  - Step_id
                  - Files
                  - File_id
                summary: Retrieves a message file.
          x-oaiMeta:
            groups:
              - id: audio
                title: Audio
                description: |
                  Learn how to turn audio into text or text into audio.

                  Related guide: [Speech to text](/docs/guides/speech-to-text)
                sections:
                  - type: endpoint
                    key: createSpeech
                    path: createSpeech
                  - type: endpoint
                    key: createTranscription
                    path: createTranscription
                  - type: endpoint
                    key: createTranslation
                    path: createTranslation
              - id: chat
                title: Chat
                description: >
                  Given a list of messages comprising a conversation, the model
                  will return a response.


                  Related guide: [Chat
                  Completions](/docs/guides/text-generation)
                sections:
                  - type: endpoint
                    key: createChatCompletion
                    path: create
                  - type: object
                    key: CreateChatCompletionResponse
                    path: object
                  - type: object
                    key: CreateChatCompletionStreamResponse
                    path: streaming
              - id: embeddings
                title: Embeddings
                description: >
                  Get a vector representation of a given input that can be
                  easily consumed by machine learning models and algorithms.


                  Related guide: [Embeddings](/docs/guides/embeddings)
                sections:
                  - type: endpoint
                    key: createEmbedding
                    path: create
                  - type: object
                    key: Embedding
                    path: object
              - id: fine-tuning
                title: Fine-tuning
                description: >
                  Manage fine-tuning jobs to tailor a model to your specific
                  training data.


                  Related guide: [Fine-tune models](/docs/guides/fine-tuning)
                sections:
                  - type: endpoint
                    key: createFineTuningJob
                    path: create
                  - type: endpoint
                    key: listPaginatedFineTuningJobs
                    path: list
                  - type: endpoint
                    key: listFineTuningEvents
                    path: list-events
                  - type: endpoint
                    key: retrieveFineTuningJob
                    path: retrieve
                  - type: endpoint
                    key: cancelFineTuningJob
                    path: cancel
                  - type: object
                    key: FineTuningJob
                    path: object
                  - type: object
                    key: FineTuningJobEvent
                    path: event-object
              - id: files
                title: Files
                description: >
                  Files are used to upload documents that can be used with
                  features like [Assistants](/docs/api-reference/assistants) and
                  [Fine-tuning](/docs/api-reference/fine-tuning).
                sections:
                  - type: endpoint
                    key: createFile
                    path: create
                  - type: endpoint
                    key: listFiles
                    path: list
                  - type: endpoint
                    key: retrieveFile
                    path: retrieve
                  - type: endpoint
                    key: deleteFile
                    path: delete
                  - type: endpoint
                    key: downloadFile
                    path: retrieve-contents
                  - type: object
                    key: OpenAIFile
                    path: object
              - id: images
                title: Images
                description: >
                  Given a prompt and/or an input image, the model will generate
                  a new image.


                  Related guide: [Image generation](/docs/guides/images)
                sections:
                  - type: endpoint
                    key: createImage
                    path: create
                  - type: endpoint
                    key: createImageEdit
                    path: createEdit
                  - type: endpoint
                    key: createImageVariation
                    path: createVariation
                  - type: object
                    key: Image
                    path: object
              - id: models
                title: Models
                description: >
                  List and describe the various models available in the API. You
                  can refer to the [Models](/docs/models) documentation to
                  understand what models are available and the differences
                  between them.
                sections:
                  - type: endpoint
                    key: listModels
                    path: list
                  - type: endpoint
                    key: retrieveModel
                    path: retrieve
                  - type: endpoint
                    key: deleteModel
                    path: delete
                  - type: object
                    key: Model
                    path: object
              - id: moderations
                title: Moderations
                description: >
                  Given a input text, outputs if the model classifies it as
                  violating OpenAI's content policy.


                  Related guide: [Moderations](/docs/guides/moderation)
                sections:
                  - type: endpoint
                    key: createModeration
                    path: create
                  - type: object
                    key: CreateModerationResponse
                    path: object
              - id: assistants
                title: Assistants
                beta: true
                description: >
                  Build assistants that can call models and use tools to perform
                  tasks.


                  [Get started with the Assistants API](/docs/assistants)
                sections:
                  - type: endpoint
                    key: createAssistant
                    path: createAssistant
                  - type: endpoint
                    key: createAssistantFile
                    path: createAssistantFile
                  - type: endpoint
                    key: listAssistants
                    path: listAssistants
                  - type: endpoint
                    key: listAssistantFiles
                    path: listAssistantFiles
                  - type: endpoint
                    key: getAssistant
                    path: getAssistant
                  - type: endpoint
                    key: getAssistantFile
                    path: getAssistantFile
                  - type: endpoint
                    key: modifyAssistant
                    path: modifyAssistant
                  - type: endpoint
                    key: deleteAssistant
                    path: deleteAssistant
                  - type: endpoint
                    key: deleteAssistantFile
                    path: deleteAssistantFile
                  - type: object
                    key: AssistantObject
                    path: object
                  - type: object
                    key: AssistantFileObject
                    path: file-object
              - id: threads
                title: Threads
                beta: true
                description: |
                  Create threads that assistants can interact with.

                  Related guide: [Assistants](/docs/assistants/overview)
                sections:
                  - type: endpoint
                    key: createThread
                    path: createThread
                  - type: endpoint
                    key: getThread
                    path: getThread
                  - type: endpoint
                    key: modifyThread
                    path: modifyThread
                  - type: endpoint
                    key: deleteThread
                    path: deleteThread
                  - type: object
                    key: ThreadObject
                    path: object
              - id: messages
                title: Messages
                beta: true
                description: |
                  Create messages within threads

                  Related guide: [Assistants](/docs/assistants/overview)
                sections:
                  - type: endpoint
                    key: createMessage
                    path: createMessage
                  - type: endpoint
                    key: listMessages
                    path: listMessages
                  - type: endpoint
                    key: listMessageFiles
                    path: listMessageFiles
                  - type: endpoint
                    key: getMessage
                    path: getMessage
                  - type: endpoint
                    key: getMessageFile
                    path: getMessageFile
                  - type: endpoint
                    key: modifyMessage
                    path: modifyMessage
                  - type: object
                    key: MessageObject
                    path: object
                  - type: object
                    key: MessageFileObject
                    path: file-object
              - id: runs
                title: Runs
                beta: true
                description: |
                  Represents an execution run on a thread.

                  Related guide: [Assistants](/docs/assistants/overview)
                sections:
                  - type: endpoint
                    key: createRun
                    path: createRun
                  - type: endpoint
                    key: createThreadAndRun
                    path: createThreadAndRun
                  - type: endpoint
                    key: listRuns
                    path: listRuns
                  - type: endpoint
                    key: listRunSteps
                    path: listRunSteps
                  - type: endpoint
                    key: getRun
                    path: getRun
                  - type: endpoint
                    key: getRunStep
                    path: getRunStep
                  - type: endpoint
                    key: modifyRun
                    path: modifyRun
                  - type: endpoint
                    key: submitToolOuputsToRun
                    path: submitToolOutputs
                  - type: endpoint
                    key: cancelRun
                    path: cancelRun
                  - type: object
                    key: RunObject
                    path: object
                  - type: object
                    key: RunStepObject
                    path: step-object
              - id: completions
                title: Completions
                legacy: true
                description: >
                  Given a prompt, the model will return one or more predicted
                  completions along with the probabilities of alternative tokens
                  at each position. Most developer should use our [Chat
                  Completions
                  API](/docs/guides/text-generation/text-generation-models) to
                  leverage our best and newest models. Most models that support
                  the legacy Completions endpoint [will be shut off on January
                  4th, 2024](/docs/deprecations/2023-07-06-gpt-and-embeddings).
                sections:
                  - type: endpoint
                    key: createCompletion
                    path: create
                  - type: object
                    key: CreateCompletionResponse
                    path: null
    overlays:
      - type: APIs.io Search
        url: >-
          overlays/https://github.com/apis-json/artisanal/tree/main/apis/openai/threads-openapi-search.yml
      - type: APIs.io Search
        url: overlays/threads-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/threads-openapi-api-evangelist-ratings.yml
    aid: openai:openai-threads-api
  - aid: twilio:twilio-assistant-api
    name: Twilio Assistant API
    description: >-
      Intelligent virtual assistants (IVA) are incredibly sophisticated
      applications with the potential to revolutionize the way modern businesses
      service customers.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://www.twilio.com/blog/what-is-intelligent-virtual-assistant
    baseURL: https:/api.twilio.com
    tags: []
    properties:
      - type: Documentation
        url: https://www.twilio.com/blog/what-is-intelligent-virtual-assistant
      - type: OpenAPI
        data:
          info:
            title: Assistants
            license:
              name: Apache 2.0
              url: https://www.apache.org/licenses/LICENSE-2.0.html
          openapi: 3.0.1
          paths:
            /understand/Assistants/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Assistants
                  - Sid
              post:
                description: ''
                tags:
                  - Assistants
                  - Sid
              delete:
                description: ''
                tags:
                  - Assistants
                  - Sid
            /understand/Assistants/{AssistantSid}/FallbackActions:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Assistants
                  - Sid
                  - Assistant
                  - Fallback
                  - Actions
              post:
                description: ''
                tags:
                  - Assistants
                  - Sid
                  - Assistant
                  - Fallback
                  - Actions
            /understand/Assistants/{AssistantSid}/InitiationActions:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Assistants
                  - Sid
                  - Assistant
                  - Fallback
                  - Actions
                  - Initiation
              post:
                description: ''
                tags:
                  - Assistants
                  - Sid
                  - Assistant
                  - Fallback
                  - Actions
                  - Initiation
            /understand/Assistants/{AssistantSid}/Dialogues/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Assistants
                  - Sid
                  - Assistant
                  - Fallback
                  - Actions
                  - Initiation
                  - Dialogues
            /understand/Assistants/{AssistantSid}/Tasks/{TaskSid}/Fields/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Assistants
                  - Sid
                  - Assistant
                  - Fallback
                  - Actions
                  - Initiation
                  - Dialogues
                  - Tasks
                  - Task
                  - Fields
              delete:
                description: ''
                tags:
                  - Assistants
                  - Sid
                  - Assistant
                  - Fallback
                  - Actions
                  - Initiation
                  - Dialogues
                  - Tasks
                  - Task
                  - Fields
            /understand/Assistants/{AssistantSid}/Tasks/{TaskSid}/Fields:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Assistants
                  - Sid
                  - Assistant
                  - Fallback
                  - Actions
                  - Initiation
                  - Dialogues
                  - Tasks
                  - Task
                  - Fields
              post:
                description: ''
                tags:
                  - Assistants
                  - Sid
                  - Assistant
                  - Fallback
                  - Actions
                  - Initiation
                  - Dialogues
                  - Tasks
                  - Task
                  - Fields
            /understand/Assistants/{AssistantSid}/FieldTypes/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Assistants
                  - Sid
                  - Assistant
                  - Fallback
                  - Actions
                  - Initiation
                  - Dialogues
                  - Tasks
                  - Task
                  - Fields
                  - Field
                  - Types
              post:
                description: ''
                tags:
                  - Assistants
                  - Sid
                  - Assistant
                  - Fallback
                  - Actions
                  - Initiation
                  - Dialogues
                  - Tasks
                  - Task
                  - Fields
                  - Field
                  - Types
              delete:
                description: ''
                tags:
                  - Assistants
                  - Sid
                  - Assistant
                  - Fallback
                  - Actions
                  - Initiation
                  - Dialogues
                  - Tasks
                  - Task
                  - Fields
                  - Field
                  - Types
            /understand/Assistants/{AssistantSid}/FieldTypes:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Assistants
                  - Sid
                  - Assistant
                  - Fallback
                  - Actions
                  - Initiation
                  - Dialogues
                  - Tasks
                  - Task
                  - Fields
                  - Field
                  - Types
              post:
                description: ''
                tags:
                  - Assistants
                  - Sid
                  - Assistant
                  - Fallback
                  - Actions
                  - Initiation
                  - Dialogues
                  - Tasks
                  - Task
                  - Fields
                  - Field
                  - Types
            /understand/Assistants/{AssistantSid}/FieldTypes/{FieldTypeSid}/FieldValues/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Assistants
                  - Sid
                  - Assistant
                  - Fallback
                  - Actions
                  - Initiation
                  - Dialogues
                  - Tasks
                  - Task
                  - Fields
                  - Field
                  - Types
                  - Type
                  - Values
              delete:
                description: ''
                tags:
                  - Assistants
                  - Sid
                  - Assistant
                  - Fallback
                  - Actions
                  - Initiation
                  - Dialogues
                  - Tasks
                  - Task
                  - Fields
                  - Field
                  - Types
                  - Type
                  - Values
            /understand/Assistants/{AssistantSid}/FieldTypes/{FieldTypeSid}/FieldValues:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Assistants
                  - Sid
                  - Assistant
                  - Fallback
                  - Actions
                  - Initiation
                  - Dialogues
                  - Tasks
                  - Task
                  - Fields
                  - Field
                  - Types
                  - Type
                  - Values
              post:
                description: ''
                tags:
                  - Assistants
                  - Sid
                  - Assistant
                  - Fallback
                  - Actions
                  - Initiation
                  - Dialogues
                  - Tasks
                  - Task
                  - Fields
                  - Field
                  - Types
                  - Type
                  - Values
            /understand/Assistants/{AssistantSid}/ModelBuilds/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Assistants
                  - Sid
                  - Assistant
                  - Fallback
                  - Actions
                  - Initiation
                  - Dialogues
                  - Tasks
                  - Task
                  - Fields
                  - Field
                  - Types
                  - Type
                  - Values
                  - Model
                  - Builds
              post:
                description: ''
                tags:
                  - Assistants
                  - Sid
                  - Assistant
                  - Fallback
                  - Actions
                  - Initiation
                  - Dialogues
                  - Tasks
                  - Task
                  - Fields
                  - Field
                  - Types
                  - Type
                  - Values
                  - Model
                  - Builds
              delete:
                description: ''
                tags:
                  - Assistants
                  - Sid
                  - Assistant
                  - Fallback
                  - Actions
                  - Initiation
                  - Dialogues
                  - Tasks
                  - Task
                  - Fields
                  - Field
                  - Types
                  - Type
                  - Values
                  - Model
                  - Builds
            /understand/Assistants/{AssistantSid}/ModelBuilds:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Assistants
                  - Sid
                  - Assistant
                  - Fallback
                  - Actions
                  - Initiation
                  - Dialogues
                  - Tasks
                  - Task
                  - Fields
                  - Field
                  - Types
                  - Type
                  - Values
                  - Model
                  - Builds
              post:
                description: ''
                tags:
                  - Assistants
                  - Sid
                  - Assistant
                  - Fallback
                  - Actions
                  - Initiation
                  - Dialogues
                  - Tasks
                  - Task
                  - Fields
                  - Field
                  - Types
                  - Type
                  - Values
                  - Model
                  - Builds
            /understand/Assistants/{AssistantSid}/Queries/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Assistants
                  - Sid
                  - Assistant
                  - Fallback
                  - Actions
                  - Initiation
                  - Dialogues
                  - Tasks
                  - Task
                  - Fields
                  - Field
                  - Types
                  - Type
                  - Values
                  - Model
                  - Builds
                  - Queries
              post:
                description: ''
                tags:
                  - Assistants
                  - Sid
                  - Assistant
                  - Fallback
                  - Actions
                  - Initiation
                  - Dialogues
                  - Tasks
                  - Task
                  - Fields
                  - Field
                  - Types
                  - Type
                  - Values
                  - Model
                  - Builds
                  - Queries
              delete:
                description: ''
                tags:
                  - Assistants
                  - Sid
                  - Assistant
                  - Fallback
                  - Actions
                  - Initiation
                  - Dialogues
                  - Tasks
                  - Task
                  - Fields
                  - Field
                  - Types
                  - Type
                  - Values
                  - Model
                  - Builds
                  - Queries
            /understand/Assistants/{AssistantSid}/Queries:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Assistants
                  - Sid
                  - Assistant
                  - Fallback
                  - Actions
                  - Initiation
                  - Dialogues
                  - Tasks
                  - Task
                  - Fields
                  - Field
                  - Types
                  - Type
                  - Values
                  - Model
                  - Builds
                  - Queries
              post:
                description: ''
                tags:
                  - Assistants
                  - Sid
                  - Assistant
                  - Fallback
                  - Actions
                  - Initiation
                  - Dialogues
                  - Tasks
                  - Task
                  - Fields
                  - Field
                  - Types
                  - Type
                  - Values
                  - Model
                  - Builds
                  - Queries
            /understand/Assistants/{AssistantSid}/Tasks/{TaskSid}/Samples/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Assistants
                  - Sid
                  - Assistant
                  - Fallback
                  - Actions
                  - Initiation
                  - Dialogues
                  - Tasks
                  - Task
                  - Fields
                  - Field
                  - Types
                  - Type
                  - Values
                  - Model
                  - Builds
                  - Queries
                  - Samples
              post:
                description: ''
                tags:
                  - Assistants
                  - Sid
                  - Assistant
                  - Fallback
                  - Actions
                  - Initiation
                  - Dialogues
                  - Tasks
                  - Task
                  - Fields
                  - Field
                  - Types
                  - Type
                  - Values
                  - Model
                  - Builds
                  - Queries
                  - Samples
              delete:
                description: ''
                tags:
                  - Assistants
                  - Sid
                  - Assistant
                  - Fallback
                  - Actions
                  - Initiation
                  - Dialogues
                  - Tasks
                  - Task
                  - Fields
                  - Field
                  - Types
                  - Type
                  - Values
                  - Model
                  - Builds
                  - Queries
                  - Samples
            /understand/Assistants/{AssistantSid}/Tasks/{TaskSid}/Samples:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Assistants
                  - Sid
                  - Assistant
                  - Fallback
                  - Actions
                  - Initiation
                  - Dialogues
                  - Tasks
                  - Task
                  - Fields
                  - Field
                  - Types
                  - Type
                  - Values
                  - Model
                  - Builds
                  - Queries
                  - Samples
              post:
                description: ''
                tags:
                  - Assistants
                  - Sid
                  - Assistant
                  - Fallback
                  - Actions
                  - Initiation
                  - Dialogues
                  - Tasks
                  - Task
                  - Fields
                  - Field
                  - Types
                  - Type
                  - Values
                  - Model
                  - Builds
                  - Queries
                  - Samples
            /understand/Assistants/{AssistantSid}/StyleSheet:
              description: 'TODO: Resource-level docs'
              get:
                description: Returns Style sheet JSON object for this Assistant
                tags:
                  - Assistants
                  - Sid
                  - Assistant
                  - Fallback
                  - Actions
                  - Initiation
                  - Dialogues
                  - Tasks
                  - Task
                  - Fields
                  - Field
                  - Types
                  - Type
                  - Values
                  - Model
                  - Builds
                  - Queries
                  - Samples
                  - Style
                  - Sheet
              post:
                description: >-
                  Updates the style sheet for an assistant identified by
                  {AssistantSid} or {AssistantUniqueName}.
                tags:
                  - Assistants
                  - Sid
                  - Assistant
                  - Fallback
                  - Actions
                  - Initiation
                  - Dialogues
                  - Tasks
                  - Task
                  - Fields
                  - Field
                  - Types
                  - Type
                  - Values
                  - Model
                  - Builds
                  - Queries
                  - Samples
                  - Style
                  - Sheet
            /understand/Assistants/{AssistantSid}/Tasks/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Assistants
                  - Sid
                  - Assistant
                  - Fallback
                  - Actions
                  - Initiation
                  - Dialogues
                  - Tasks
                  - Task
                  - Fields
                  - Field
                  - Types
                  - Type
                  - Values
                  - Model
                  - Builds
                  - Queries
                  - Samples
                  - Style
                  - Sheet
              post:
                description: ''
                tags:
                  - Assistants
                  - Sid
                  - Assistant
                  - Fallback
                  - Actions
                  - Initiation
                  - Dialogues
                  - Tasks
                  - Task
                  - Fields
                  - Field
                  - Types
                  - Type
                  - Values
                  - Model
                  - Builds
                  - Queries
                  - Samples
                  - Style
                  - Sheet
              delete:
                description: ''
                tags:
                  - Assistants
                  - Sid
                  - Assistant
                  - Fallback
                  - Actions
                  - Initiation
                  - Dialogues
                  - Tasks
                  - Task
                  - Fields
                  - Field
                  - Types
                  - Type
                  - Values
                  - Model
                  - Builds
                  - Queries
                  - Samples
                  - Style
                  - Sheet
            /understand/Assistants/{AssistantSid}/Tasks:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Assistants
                  - Sid
                  - Assistant
                  - Fallback
                  - Actions
                  - Initiation
                  - Dialogues
                  - Tasks
                  - Task
                  - Fields
                  - Field
                  - Types
                  - Type
                  - Values
                  - Model
                  - Builds
                  - Queries
                  - Samples
                  - Style
                  - Sheet
              post:
                description: ''
                tags:
                  - Assistants
                  - Sid
                  - Assistant
                  - Fallback
                  - Actions
                  - Initiation
                  - Dialogues
                  - Tasks
                  - Task
                  - Fields
                  - Field
                  - Types
                  - Type
                  - Values
                  - Model
                  - Builds
                  - Queries
                  - Samples
                  - Style
                  - Sheet
            /understand/Assistants/{AssistantSid}/Tasks/{TaskSid}/Actions:
              description: 'TODO: Resource-level docs'
              get:
                description: Returns JSON actions for this Task.
                tags:
                  - Assistants
                  - Sid
                  - Assistant
                  - Fallback
                  - Actions
                  - Initiation
                  - Dialogues
                  - Tasks
                  - Task
                  - Fields
                  - Field
                  - Types
                  - Type
                  - Values
                  - Model
                  - Builds
                  - Queries
                  - Samples
                  - Style
                  - Sheet
              post:
                description: >-
                  Updates the actions of an Task identified by {TaskSid} or
                  {TaskUniqueName}.
                tags:
                  - Assistants
                  - Sid
                  - Assistant
                  - Fallback
                  - Actions
                  - Initiation
                  - Dialogues
                  - Tasks
                  - Task
                  - Fields
                  - Field
                  - Types
                  - Type
                  - Values
                  - Model
                  - Builds
                  - Queries
                  - Samples
                  - Style
                  - Sheet
            /understand/Assistants/{AssistantSid}/Tasks/{TaskSid}/Statistics:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Assistants
                  - Sid
                  - Assistant
                  - Fallback
                  - Actions
                  - Initiation
                  - Dialogues
                  - Tasks
                  - Task
                  - Fields
                  - Field
                  - Types
                  - Type
                  - Values
                  - Model
                  - Builds
                  - Queries
                  - Samples
                  - Style
                  - Sheet
                  - Statistics
          tags:
            - name: PreviewDeployedDevicesCertificate
            - name: PreviewDeployedDevicesDeployment
            - name: PreviewDeployedDevicesDevice
            - name: PreviewDeployedDevicesFleet
            - name: PreviewDeployedDevicesKey
            - name: PreviewHostedNumbersAuthorizationDocument
            - name: PreviewHostedNumbersDependentHostedNumberOrder
            - name: PreviewHostedNumbersHostedNumberOrder
            - null
            - null
            - null
            - null
            - name: PreviewSyncDocument
            - name: PreviewSyncDocumentPermission
            - name: PreviewSyncService
            - name: PreviewSyncSyncList
            - name: PreviewSyncSyncListItem
            - name: PreviewSyncSyncListPermission
            - name: PreviewSyncSyncMap
            - name: PreviewSyncSyncMapItem
            - name: PreviewSyncSyncMapPermission
            - name: Assistants
            - name: Actions
            - name: Actions
            - name: PreviewUnderstandDialogue
            - name: PreviewUnderstandField
            - name: PreviewUnderstandFieldType
            - name: PreviewUnderstandFieldValue
            - name: PreviewUnderstandModelBuild
            - name: PreviewUnderstandQuery
            - name: PreviewUnderstandSample
            - name: PreviewUnderstandStyleSheet
            - name: PreviewUnderstandTask
            - name: PreviewUnderstandTaskActions
            - name: PreviewUnderstandTaskStatistics
            - name: PreviewWirelessCommand
            - name: PreviewWirelessRatePlan
            - name: PreviewWirelessSim
            - name: PreviewWirelessUsage
          x-maturity:
            - name: Preview
              description: >-
                PLEASE NOTE that this is a Preview product that is subject to
                change. Use it with caution. If you currently do not have
                developer preview access, please contact https://www.twilio
    overlays:
      - type: APIs.io Search
        url: overlays/assistant-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/assistant-openapi-api-evangelist-ratings.yml
  - aid: twilio:twilio-autopilot-api
    name: Twilio Autopilot API
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
            title: Twilio - Autopilot
            license:
              name: Apache 2.0
              url: https://www.apache.org/licenses/LICENSE-2.0.html
          openapi: 3.0.1
          paths:
            /v1/Assistants/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Assistants
                  - Sid
              post:
                description: ''
                tags:
                  - Assistants
                  - Sid
              delete:
                description: ''
                tags:
                  - Assistants
                  - Sid
            /v1/Assistants:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Assistants
                  - Sid
              post:
                description: ''
                tags:
                  - Assistants
                  - Sid
            /v1/Assistants/{AssistantSid}/Defaults:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Assistants
                  - Sid
                  - Assistant
                  - Defaults
              post:
                description: ''
                tags:
                  - Assistants
                  - Sid
                  - Assistant
                  - Defaults
            /v1/Assistants/{AssistantSid}/Dialogues/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Assistants
                  - Sid
                  - Assistant
                  - Defaults
                  - Dialogues
            /v1/Assistants/{AssistantSid}/Dialogues:
              description: 'TODO: Resource-level docs'
            /v1/Assistants/{AssistantSid}/Tasks/{TaskSid}/Fields/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Assistants
                  - Sid
                  - Assistant
                  - Defaults
                  - Dialogues
                  - Tasks
                  - Task
                  - Fields
              delete:
                description: ''
                tags:
                  - Assistants
                  - Sid
                  - Assistant
                  - Defaults
                  - Dialogues
                  - Tasks
                  - Task
                  - Fields
            /v1/Assistants/{AssistantSid}/Tasks/{TaskSid}/Fields:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Assistants
                  - Sid
                  - Assistant
                  - Defaults
                  - Dialogues
                  - Tasks
                  - Task
                  - Fields
              post:
                description: ''
                tags:
                  - Assistants
                  - Sid
                  - Assistant
                  - Defaults
                  - Dialogues
                  - Tasks
                  - Task
                  - Fields
            /v1/Assistants/{AssistantSid}/FieldTypes/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Assistants
                  - Sid
                  - Assistant
                  - Defaults
                  - Dialogues
                  - Tasks
                  - Task
                  - Fields
                  - Field
                  - Types
              post:
                description: ''
                tags:
                  - Assistants
                  - Sid
                  - Assistant
                  - Defaults
                  - Dialogues
                  - Tasks
                  - Task
                  - Fields
                  - Field
                  - Types
              delete:
                description: ''
                tags:
                  - Assistants
                  - Sid
                  - Assistant
                  - Defaults
                  - Dialogues
                  - Tasks
                  - Task
                  - Fields
                  - Field
                  - Types
            /v1/Assistants/{AssistantSid}/FieldTypes:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Assistants
                  - Sid
                  - Assistant
                  - Defaults
                  - Dialogues
                  - Tasks
                  - Task
                  - Fields
                  - Field
                  - Types
              post:
                description: ''
                tags:
                  - Assistants
                  - Sid
                  - Assistant
                  - Defaults
                  - Dialogues
                  - Tasks
                  - Task
                  - Fields
                  - Field
                  - Types
            /v1/Assistants/{AssistantSid}/FieldTypes/{FieldTypeSid}/FieldValues/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Assistants
                  - Sid
                  - Assistant
                  - Defaults
                  - Dialogues
                  - Tasks
                  - Task
                  - Fields
                  - Field
                  - Types
                  - Type
                  - Values
              delete:
                description: ''
                tags:
                  - Assistants
                  - Sid
                  - Assistant
                  - Defaults
                  - Dialogues
                  - Tasks
                  - Task
                  - Fields
                  - Field
                  - Types
                  - Type
                  - Values
            /v1/Assistants/{AssistantSid}/FieldTypes/{FieldTypeSid}/FieldValues:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Assistants
                  - Sid
                  - Assistant
                  - Defaults
                  - Dialogues
                  - Tasks
                  - Task
                  - Fields
                  - Field
                  - Types
                  - Type
                  - Values
              post:
                description: ''
                tags:
                  - Assistants
                  - Sid
                  - Assistant
                  - Defaults
                  - Dialogues
                  - Tasks
                  - Task
                  - Fields
                  - Field
                  - Types
                  - Type
                  - Values
            /v1/Assistants/{AssistantSid}/ModelBuilds/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Assistants
                  - Sid
                  - Assistant
                  - Defaults
                  - Dialogues
                  - Tasks
                  - Task
                  - Fields
                  - Field
                  - Types
                  - Type
                  - Values
                  - Model
                  - Builds
              post:
                description: ''
                tags:
                  - Assistants
                  - Sid
                  - Assistant
                  - Defaults
                  - Dialogues
                  - Tasks
                  - Task
                  - Fields
                  - Field
                  - Types
                  - Type
                  - Values
                  - Model
                  - Builds
              delete:
                description: ''
                tags:
                  - Assistants
                  - Sid
                  - Assistant
                  - Defaults
                  - Dialogues
                  - Tasks
                  - Task
                  - Fields
                  - Field
                  - Types
                  - Type
                  - Values
                  - Model
                  - Builds
            /v1/Assistants/{AssistantSid}/ModelBuilds:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Assistants
                  - Sid
                  - Assistant
                  - Defaults
                  - Dialogues
                  - Tasks
                  - Task
                  - Fields
                  - Field
                  - Types
                  - Type
                  - Values
                  - Model
                  - Builds
              post:
                description: ''
                tags:
                  - Assistants
                  - Sid
                  - Assistant
                  - Defaults
                  - Dialogues
                  - Tasks
                  - Task
                  - Fields
                  - Field
                  - Types
                  - Type
                  - Values
                  - Model
                  - Builds
            /v1/Assistants/{AssistantSid}/Queries/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Assistants
                  - Sid
                  - Assistant
                  - Defaults
                  - Dialogues
                  - Tasks
                  - Task
                  - Fields
                  - Field
                  - Types
                  - Type
                  - Values
                  - Model
                  - Builds
                  - Queries
              post:
                description: ''
                tags:
                  - Assistants
                  - Sid
                  - Assistant
                  - Defaults
                  - Dialogues
                  - Tasks
                  - Task
                  - Fields
                  - Field
                  - Types
                  - Type
                  - Values
                  - Model
                  - Builds
                  - Queries
              delete:
                description: ''
                tags:
                  - Assistants
                  - Sid
                  - Assistant
                  - Defaults
                  - Dialogues
                  - Tasks
                  - Task
                  - Fields
                  - Field
                  - Types
                  - Type
                  - Values
                  - Model
                  - Builds
                  - Queries
            /v1/Assistants/{AssistantSid}/Queries:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Assistants
                  - Sid
                  - Assistant
                  - Defaults
                  - Dialogues
                  - Tasks
                  - Task
                  - Fields
                  - Field
                  - Types
                  - Type
                  - Values
                  - Model
                  - Builds
                  - Queries
              post:
                description: ''
                tags:
                  - Assistants
                  - Sid
                  - Assistant
                  - Defaults
                  - Dialogues
                  - Tasks
                  - Task
                  - Fields
                  - Field
                  - Types
                  - Type
                  - Values
                  - Model
                  - Builds
                  - Queries
            /v1/Assistants/Restore:
              description: 'TODO: Resource-level docs'
              post:
                description: ''
                tags:
                  - Assistants
                  - Sid
                  - Assistant
                  - Defaults
                  - Dialogues
                  - Tasks
                  - Task
                  - Fields
                  - Field
                  - Types
                  - Type
                  - Values
                  - Model
                  - Builds
                  - Queries
                  - Restore
            /v1/Assistants/{AssistantSid}/Tasks/{TaskSid}/Samples/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Assistants
                  - Sid
                  - Assistant
                  - Defaults
                  - Dialogues
                  - Tasks
                  - Task
                  - Fields
                  - Field
                  - Types
                  - Type
                  - Values
                  - Model
                  - Builds
                  - Queries
                  - Restore
                  - Samples
              post:
                description: ''
                tags:
                  - Assistants
                  - Sid
                  - Assistant
                  - Defaults
                  - Dialogues
                  - Tasks
                  - Task
                  - Fields
                  - Field
                  - Types
                  - Type
                  - Values
                  - Model
                  - Builds
                  - Queries
                  - Restore
                  - Samples
              delete:
                description: ''
                tags:
                  - Assistants
                  - Sid
                  - Assistant
                  - Defaults
                  - Dialogues
                  - Tasks
                  - Task
                  - Fields
                  - Field
                  - Types
                  - Type
                  - Values
                  - Model
                  - Builds
                  - Queries
                  - Restore
                  - Samples
            /v1/Assistants/{AssistantSid}/Tasks/{TaskSid}/Samples:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Assistants
                  - Sid
                  - Assistant
                  - Defaults
                  - Dialogues
                  - Tasks
                  - Task
                  - Fields
                  - Field
                  - Types
                  - Type
                  - Values
                  - Model
                  - Builds
                  - Queries
                  - Restore
                  - Samples
              post:
                description: ''
                tags:
                  - Assistants
                  - Sid
                  - Assistant
                  - Defaults
                  - Dialogues
                  - Tasks
                  - Task
                  - Fields
                  - Field
                  - Types
                  - Type
                  - Values
                  - Model
                  - Builds
                  - Queries
                  - Restore
                  - Samples
            /v1/Assistants/{AssistantSid}/StyleSheet:
              description: 'TODO: Resource-level docs'
              get:
                description: Returns Style sheet JSON object for the Assistant
                tags:
                  - Assistants
                  - Sid
                  - Assistant
                  - Defaults
                  - Dialogues
                  - Tasks
                  - Task
                  - Fields
                  - Field
                  - Types
                  - Type
                  - Values
                  - Model
                  - Builds
                  - Queries
                  - Restore
                  - Samples
                  - Style
                  - Sheet
              post:
                description: >-
                  Updates the style sheet for an Assistant identified by
                  `assistant_sid`.
                tags:
                  - Assistants
                  - Sid
                  - Assistant
                  - Defaults
                  - Dialogues
                  - Tasks
                  - Task
                  - Fields
                  - Field
                  - Types
                  - Type
                  - Values
                  - Model
                  - Builds
                  - Queries
                  - Restore
                  - Samples
                  - Style
                  - Sheet
            /v1/Assistants/{AssistantSid}/Tasks/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Assistants
                  - Sid
                  - Assistant
                  - Defaults
                  - Dialogues
                  - Tasks
                  - Task
                  - Fields
                  - Field
                  - Types
                  - Type
                  - Values
                  - Model
                  - Builds
                  - Queries
                  - Restore
                  - Samples
                  - Style
                  - Sheet
              post:
                description: ''
                tags:
                  - Assistants
                  - Sid
                  - Assistant
                  - Defaults
                  - Dialogues
                  - Tasks
                  - Task
                  - Fields
                  - Field
                  - Types
                  - Type
                  - Values
                  - Model
                  - Builds
                  - Queries
                  - Restore
                  - Samples
                  - Style
                  - Sheet
              delete:
                description: ''
                tags:
                  - Assistants
                  - Sid
                  - Assistant
                  - Defaults
                  - Dialogues
                  - Tasks
                  - Task
                  - Fields
                  - Field
                  - Types
                  - Type
                  - Values
                  - Model
                  - Builds
                  - Queries
                  - Restore
                  - Samples
                  - Style
                  - Sheet
            /v1/Assistants/{AssistantSid}/Tasks:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Assistants
                  - Sid
                  - Assistant
                  - Defaults
                  - Dialogues
                  - Tasks
                  - Task
                  - Fields
                  - Field
                  - Types
                  - Type
                  - Values
                  - Model
                  - Builds
                  - Queries
                  - Restore
                  - Samples
                  - Style
                  - Sheet
              post:
                description: ''
                tags:
                  - Assistants
                  - Sid
                  - Assistant
                  - Defaults
                  - Dialogues
                  - Tasks
                  - Task
                  - Fields
                  - Field
                  - Types
                  - Type
                  - Values
                  - Model
                  - Builds
                  - Queries
                  - Restore
                  - Samples
                  - Style
                  - Sheet
            /v1/Assistants/{AssistantSid}/Tasks/{TaskSid}/Actions:
              description: 'TODO: Resource-level docs'
              get:
                description: Returns JSON actions for the Task.
                tags:
                  - Assistants
                  - Sid
                  - Assistant
                  - Defaults
                  - Dialogues
                  - Tasks
                  - Task
                  - Fields
                  - Field
                  - Types
                  - Type
                  - Values
                  - Model
                  - Builds
                  - Queries
                  - Restore
                  - Samples
                  - Style
                  - Sheet
                  - Actions
              post:
                description: >-
                  Updates the actions of an Task identified by {TaskSid} or
                  {TaskUniqueName}.
                tags:
                  - Assistants
                  - Sid
                  - Assistant
                  - Defaults
                  - Dialogues
                  - Tasks
                  - Task
                  - Fields
                  - Field
                  - Types
                  - Type
                  - Values
                  - Model
                  - Builds
                  - Queries
                  - Restore
                  - Samples
                  - Style
                  - Sheet
                  - Actions
            /v1/Assistants/{AssistantSid}/Tasks/{TaskSid}/Statistics:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Assistants
                  - Sid
                  - Assistant
                  - Defaults
                  - Dialogues
                  - Tasks
                  - Task
                  - Fields
                  - Field
                  - Types
                  - Type
                  - Values
                  - Model
                  - Builds
                  - Queries
                  - Restore
                  - Samples
                  - Style
                  - Sheet
                  - Actions
                  - Statistics
            /v1/Assistants/{AssistantSid}/Webhooks/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Assistants
                  - Sid
                  - Assistant
                  - Defaults
                  - Dialogues
                  - Tasks
                  - Task
                  - Fields
                  - Field
                  - Types
                  - Type
                  - Values
                  - Model
                  - Builds
                  - Queries
                  - Restore
                  - Samples
                  - Style
                  - Sheet
                  - Actions
                  - Statistics
                  - Webhooks
              post:
                description: ''
                tags:
                  - Assistants
                  - Sid
                  - Assistant
                  - Defaults
                  - Dialogues
                  - Tasks
                  - Task
                  - Fields
                  - Field
                  - Types
                  - Type
                  - Values
                  - Model
                  - Builds
                  - Queries
                  - Restore
                  - Samples
                  - Style
                  - Sheet
                  - Actions
                  - Statistics
                  - Webhooks
              delete:
                description: ''
                tags:
                  - Assistants
                  - Sid
                  - Assistant
                  - Defaults
                  - Dialogues
                  - Tasks
                  - Task
                  - Fields
                  - Field
                  - Types
                  - Type
                  - Values
                  - Model
                  - Builds
                  - Queries
                  - Restore
                  - Samples
                  - Style
                  - Sheet
                  - Actions
                  - Statistics
                  - Webhooks
            /v1/Assistants/{AssistantSid}/Webhooks:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Assistants
                  - Sid
                  - Assistant
                  - Defaults
                  - Dialogues
                  - Tasks
                  - Task
                  - Fields
                  - Field
                  - Types
                  - Type
                  - Values
                  - Model
                  - Builds
                  - Queries
                  - Restore
                  - Samples
                  - Style
                  - Sheet
                  - Actions
                  - Statistics
                  - Webhooks
              post:
                description: ''
                tags:
                  - Assistants
                  - Sid
                  - Assistant
                  - Defaults
                  - Dialogues
                  - Tasks
                  - Task
                  - Fields
                  - Field
                  - Types
                  - Type
                  - Values
                  - Model
                  - Builds
                  - Queries
                  - Restore
                  - Samples
                  - Style
                  - Sheet
                  - Actions
                  - Statistics
                  - Webhooks
          tags:
            - name: AutopilotV1Assistant
            - name: AutopilotV1Defaults
            - name: AutopilotV1Dialogue
            - name: AutopilotV1Field
            - name: AutopilotV1FieldType
            - name: AutopilotV1FieldValue
            - name: AutopilotV1ModelBuild
            - name: AutopilotV1Query
            - name: AutopilotV1RestoreAssistant
            - name: AutopilotV1Sample
            - name: AutopilotV1StyleSheet
            - name: AutopilotV1Task
            - name: AutopilotV1TaskActions
            - name: AutopilotV1TaskStatistics
            - name: AutopilotV1Webhook
          x-maturity:
            - name: Preview
              description: >-
                PLEASE NOTE that this is a Preview product that is subject to
                change. Use it with caution. If you currently do not have
                developer preview access, please contact https://www.twilio
    overlays:
      - type: APIs.io Search
        url: overlays/autopilot-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/autopilot-openapi-api-evangelist-ratings.yml
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---