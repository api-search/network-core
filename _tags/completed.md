---
name: Completed
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/completed.png
url: https://example.com/apis/completed.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Completed
apis:
  - name: FactSet Conversational API Powered by FactSet Mercury
    description: >-
      The FactSet Conversational API allows clients to white-label core FactSet
      Mercury capabilities in a client’s chatbot experience.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: >-
      https://developer.factset.com/api-catalog/conversational-api-powered-factset-mercury
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: >-
          https://developer.factset.com/api-catalog/conversational-api-powered-factset-mercury#overview
      - type: SDKs
        url: >-
          https://developer.factset.com/api-catalog/conversational-api-powered-factset-mercury#sdkLibrary
      - type: Jupyter Notebooks
        url: >-
          https://developer.factset.com/api-catalog/conversational-api-powered-factset-mercury#notebooks
      - type: Code Snippets
        url: >-
          https://developer.factset.com/api-catalog/conversational-api-powered-factset-mercury#codeSnippet
      - type: Change Log
        url: >-
          https://developer.factset.com/api-catalog/conversational-api-powered-factset-mercury#changelog
      - type: OpenAPI
        data:
          openapi: 3.0.3
          info:
            title: Conversational API Powered by FactSet Mercury
            license:
              name: Apache License, Version 2.0
              url: https://www.apache.org/licenses/LICENSE-2.0
          paths:
            /create:
              post:
                summary: Create a chat request for a given natural language query.
                description: >
                  Returns a chat ID for polling the response to a natural
                  language query for financial data.

                    This endpoint is an interface for initializing a request for an answer from FactSet Mercury, our large language model for surfacing FactSet datasets through conversational natural language queries. Use the `/create` endpoint to start generating responses for one-off questions. Responses contain a chat ID and status for the chat process.
                tags:
                  - Create
                  - Chat
                  - Request
                  - For
                  - Given
                  - Natural
                  - Language
                  - Query.
                  - Create
            /status:
              post:
                summary: Retrieve the status of a chat response process.
                description: >
                  Returns the status of a chat response for a given chat
                  conversation ID (recevied from the `/create` endpoint). Poll
                  the `/status` endpoint with your conversation ID to confirm
                  when your data is ready.

                  Answers may take minutes to generate, depending on the
                  complexity of the query.
                tags:
                  - Retrieve
                  - The
                  - Status
                  - Of
                  - Chat
                  - Response
                  - Process.
                  - Create
                  - Status
            /result:
              post:
                summary: Retrieve the completed response for your query.
                description: >
                  Returns FactSet content and data in response to the query
                  provided to the `/create` endpoint. This endpoint is the final
                  step in the single-question request process.

                  Responses contain a combination of Microsoft Adaptive Cards
                  for data/tables and markdown for text.
                tags:
                  - Retrieve
                  - The
                  - Completed
                  - Response
                  - For
                  - Your
                  - Query.
                  - Create
                  - Status
                  - Result
          tags:
            - name: Single Question Chat
          externalDocs:
            description: API Documentation
            url: https://developer.factset.com/api-catalog/conversational-api-pow
    overlays:
      - type: APIs.io Search
        url: overlays/conversational-api-powered-by-mercury-openapi-search.yml
      - type: API Evangelist Ratings
        url: >-
          overlays/conversational-api-powered-by-mercury-openapi-api-evangelist-ratings.yml
    aid: factset:factset-conversational-api-powered-by-factset-mercury
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
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---