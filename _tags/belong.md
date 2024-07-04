---
name: Belong
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/belong.png
url: https://example.com/apis/belong.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Belong
apis:
  - name: FactSet IRN Meetings API
    description: >-
      Meetings API allows users to extract, create, update and delete their
      meetings and appointments in Internal Research Notes application.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.factset.com/api-catalog/irn-meetings-api
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: https://developer.factset.com/api-catalog/irn-meetings-api#overview
      - type: SDKs
        url: https://developer.factset.com/api-catalog/irn-meetings-api#sdkLibrary
      - type: Jupyter Notebooks
        url: https://developer.factset.com/api-catalog/irn-meetings-api#notebooks
      - type: Code Snippets
        url: https://developer.factset.com/api-catalog/irn-meetings-api#codeSnippet
      - type: Change Log
        url: https://developer.factset.com/api-catalog/irn-meetings-api#changelog
      - type: OpenAPI
        data:
          openapi: 3.0.1
          info:
            title: IRN API v1
          paths:
            /v1/meetings:
              get:
                tags:
                  - Get
                  - All
                  - The
                  - Meetings
                  - In
                  - Specified
                  - Date
                  - Range
                  - Filtered
                  - 'On'
                  - Given
                  - Identifiers
                  - V1
                  - Meetings
                summary: >-
                  Get all the meetings in the specified date range filtered on
                  the given identifiers
              post:
                tags:
                  - Create
                  - Meeting
                  - V1
                  - Meetings
                summary: Create a meeting
            /v1/meetings/{meetingId}:
              get:
                tags:
                  - Get
                  - Details
                  - Of
                  - Meeting
                  - V1
                  - Meetings
                  - Id
                summary: Get details of a meeting
              put:
                tags:
                  - Update
                  - Meeting
                  - V1
                  - Meetings
                  - Id
                summary: Update meeting
              delete:
                tags:
                  - Delete
                  - Meeting
                  - V1
                  - Meetings
                  - Id
                summary: Delete a Meeting
            /v1/meetings/{meetingId}/attachments:
              get:
                tags:
                  - Get
                  - All
                  - The
                  - Attachments
                  - Belonging
                  - To
                  - Meeting
                  - V1
                  - Meetings
                  - Id
                  - Attachments
                summary: Get all the attachments belonging to a meeting
              post:
                tags:
                  - Create
                  - An
                  - Attachment
                  - For
                  - Existing
                  - Meeting
                  - V1
                  - Meetings
                  - Id
                  - Attachments
                summary: Create an attachment for a existing meeting
            /v1/meetings/{meetingId}/attachments/{attachmentId}/download:
              get:
                tags:
                  - Download
                  - An
                  - Attachment
                  - From
                  - Meeting
                  - V1
                  - Meetings
                  - Id
                  - Attachments
                  - Attachment
                  - Download
                summary: Download an attachment from a Meeting
            /v1/meetings/{meetingId}/comments:
              get:
                tags:
                  - Get
                  - All
                  - Comments
                  - For
                  - Meeting
                  - V1
                  - Meetings
                  - Id
                  - Attachments
                  - Attachment
                  - Download
                  - Comments
                summary: Get all comments for a meeting
              post:
                tags:
                  - Create
                  - Comment
                  - To
                  - Meeting
                  - V1
                  - Meetings
                  - Id
                  - Attachments
                  - Attachment
                  - Download
                  - Comments
                summary: Create a comment to a Meeting
            /v1/meetings/{meetingId}/comments/{commentId}:
              get:
                tags:
                  - Get
                  - Details
                  - Of
                  - Comment
                  - Belonging
                  - To
                  - Meeting
                  - V1
                  - Meetings
                  - Id
                  - Attachments
                  - Attachment
                  - Download
                  - Comments
                  - Comment
                summary: Get details of a comment belonging to a meeting
              patch:
                tags:
                  - Edit
                  - Comment
                  - For
                  - Meeting
                  - V1
                  - Meetings
                  - Id
                  - Attachments
                  - Attachment
                  - Download
                  - Comments
                  - Comment
                summary: Edit a comment for a meeting
              delete:
                tags:
                  - Delete
                  - Comment
                  - From
                  - Meeting
                  - V1
                  - Meetings
                  - Id
                  - Attachments
                  - Attachment
                  - Download
                  - Comments
                  - Comment
                summary: Delete a Comment from a Meeting
            /v1/meetings/{meetingId}/comments/{commentId}/attachments:
              get:
                tags:
                  - Get
                  - Attachments
                  - Summary
                  - Of
                  - Comment
                  - Belonging
                  - To
                  - Meeting
                  - V1
                  - Meetings
                  - Id
                  - Attachments
                  - Attachment
                  - Download
                  - Comments
                  - Comment
                summary: Get attachments summary of a comment belonging to a meeting
              post:
                tags:
                  - Create
                  - Comment
                  - Attachment
                  - To
                  - Meeting
                  - V1
                  - Meetings
                  - Id
                  - Attachments
                  - Attachment
                  - Download
                  - Comments
                  - Comment
                summary: Create a comment attachment to a Meeting
            /v1/meetings/{meetingId}/comments/{commentId}/attachments/{attachmentId}/download:
              get:
                tags:
                  - Download
                  - Single
                  - Attachment
                  - Detail
                  - Of
                  - Comment
                  - Belonging
                  - To
                  - Meeting
                  - V1
                  - Meetings
                  - Id
                  - Attachments
                  - Attachment
                  - Download
                  - Comments
                  - Comment
                summary: >-
                  Download single attachment detail of a comment belonging to a
                  meeting
            /v1/meetings/{meetingId}/events:
              get:
                tags:
                  - Get
                  - All
                  - The
                  - Record
                  - Events
                  - That
                  - Belong
                  - To
                  - Meeting
                  - V1
                  - Meetings
                  - Id
                  - Attachments
                  - Attachment
                  - Download
                  - Comments
                  - Comment
                  - Events
                summary: Get all the record events that belong to a meeting
            /v1/meetings/{meetingId}/events/{recordEventId}:
              get:
                tags:
                  - Get
                  - Details
                  - Of
                  - Record
                  - Event
                  - Meeting
                  - V1
                  - Meetings
                  - Id
                  - Attachments
                  - Attachment
                  - Download
                  - Comments
                  - Comment
                  - Events
                  - Record
                  - Event
                summary: Get details of a record event of a meeting
            /v1/meetings/{meetingId}/attachments/{attachmentId}:
              delete:
                tags:
                  - Delete
                  - Attachment
                  - From
                  - Meeting
                  - V1
                  - Meetings
                  - Id
                  - Attachments
                  - Attachment
                  - Download
                  - Comments
                  - Comment
                  - Events
                  - Record
                  - Event
                summary: Delete attachment from meeting
          tags:
            - name: Attachments
            - name: Comments
            - name: Events
            - name: null
    overlays:
      - type: APIs.io Search
        url: overlays/irn-meetings-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/irn-meetings-openapi-api-evangelist-ratings.yml
    aid: factset:factset-irn-meetings-api
  - name: FactSet Content Feeds Data Dictionary
    description: >-
      Browse data items and definitions available through FactSet's off platform
      product offerings.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.factset.com/api-catalog/content-feeds-data-dictionary
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: >-
          https://developer.factset.com/api-catalog/content-feeds-data-dictionary#overview
      - type: SDKs
        url: >-
          https://developer.factset.com/api-catalog/content-feeds-data-dictionary#sdkLibrary
      - type: Jupyter Notebooks
        url: >-
          https://developer.factset.com/api-catalog/content-feeds-data-dictionary#notebooks
      - type: Code Snippets
        url: >-
          https://developer.factset.com/api-catalog/content-feeds-data-dictionary#codeSnippet
      - type: Change Log
        url: >-
          https://developer.factset.com/api-catalog/content-feeds-data-dictionary#changelog
      - type: OpenAPI
        data:
          openapi: 3.0.0
          info:
            title: CTS Data Dictionary API
          paths:
            /navigator/products:
              get:
                tags:
                  - Get
                  - The
                  - List
                  - Of
                  - Products
                  - For
                  - Navigator.
                  - Navigator
                  - Products
                summary: Get the list of products for Navigator.
            /navigator/data_items/{Product_id}:
              get:
                tags:
                  - Get
                  - The
                  - List
                  - Of
                  - Data
                  - Items
                  - Associated
                  - With
                  - Product
                  - For
                  - Navigator.
                  - Navigator
                  - Products
                  - Product_id
                summary: >-
                  Get the list of data items associated with a product for
                  Navigator.
            /navigator/sources/{DataItem_id}:
              get:
                tags:
                  - Get
                  - List
                  - Of
                  - Sources
                  - Where
                  - The
                  - Specified
                  - Data
                  - Item
                  - Can
                  - Be
                  - Found,
                  - For
                  - Each
                  - Delivery
                  - Method,
                  - Filtered
                  - To
                  - Appearances
                  - Given
                  - Within
                  - Product.
                  - Navigator
                  - Products
                  - Product_id
                  - Data
                  - Item_id
                summary: >-
                  Get a list of sources where the specified data item can be
                  found, for each delivery method, filtered to the appearances
                  of the given data item within the specified product.
            /navigator/sources:
              get:
                tags:
                  - Get
                  - List
                  - Of
                  - Sources
                  - By
                  - Delivery
                  - Method
                  - For
                  - The
                  - Given
                  - Product_id
                  - Navigator
                  - Products
                  - Product_id
                  - Data
                  - Item_id
                  - Sources
                summary: >-
                  Get a list of sources by delivery method for the given
                  product_id
            /navigator/table_fields/{Table_id}:
              get:
                tags:
                  - Get
                  - The
                  - List
                  - Of
                  - Fields
                  - Associated
                  - With
                  - Table
                  - For
                  - Navigator,
                  - And
                  - Code
                  - Information
                  - Specified
                  - Data
                  - Item,
                  - If
                  - Applicable.
                  - Navigator
                  - Products
                  - Product_id
                  - Data
                  - Item_id
                  - Sources
                  - Table_id
                summary: >-
                  Get the list of fields associated with a table for Navigator,
                  and the code information for the specified data item, if
                  applicable.
            /navigator/basic_search:
              post:
                tags:
                  - Returns
                  - The
                  - Data
                  - Items
                  - (along
                  - With
                  - Products
                  - They
                  - Belong
                  - To)
                  - That
                  - Contain
                  - At
                  - Least
                  - One
                  - Of
                  - Search
                  - Terms
                  - As
                  - Substring
                  - Either
                  - Their
                  - Na
                  - Navigator
                  - Products
                  - Product_id
                  - Data
                  - Item_id
                  - Sources
                  - Table_id
                  - Basic_search
                summary: >-
                  Returns the data items (along with the products they belong
                  to) that contain at least one of the search terms as a
                  substring of either their
    overlays:
      - type: APIs.io Search
        url: overlays/content-feeds-data-dictionary-openapi-search.yml
      - type: API Evangelist Ratings
        url: >-
          overlays/content-feeds-data-dictionary-openapi-api-evangelist-ratings.yml
    aid: factset:factset-content-feeds-data-dictionary
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
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---