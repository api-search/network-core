---
name: Begins
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/begins.png
url: https://example.com/apis/begins.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Begins
apis:
  - name: rds-data
    description: >-
      <p><fullname>RDS Data API</fullname> <p>Amazon RDS provides an HTTP
      endpoint to run SQL statements on an Amazon Aurora DB cluster. To run
      these statements, you use the RDS Data API (Data API).</p> <p>Data API is
      available with the following types of Aurora databases:</p> <ul> <li>
      <p>Aurora PostgreSQL - Serverless v2, Serverless v1, and provisioned</p>
      </li> <li> <p>Aurora MySQL - Serverless v1 only</p> </li> </ul> <p>For
      more information about the Data API, see <a
      href="https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/data-api.html">Using
      RDS Data API</a> in the <i>Amazon Aurora User Guide</i>.</p></p>
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
            title: rds-data
          paths:
            /BatchExecute:
              POST:
                summary: BatchExecuteStatement
                description: >-
                  <p>Runs a batch SQL statement over an array of data.</p>
                  <p>You can run bulk update and insert operations for multiple
                  records using a DML statement with different parameter sets.
                  Bulk operations can provide a significant performance
                  improvement over individual insert and update operations.</p>
                  <note> <p>If a call isn't part of a transaction because it
                  doesn't include the <code>transactionID</code> parameter,
                  changes that result from the call are committed
                  automatically.</p> <p>There isn't a fixed upper limit on the
                  number of parameter sets. However, the maximum size of the
                  HTTP request submitted through the Data API is 4 MiB. If the
                  request exceeds this limit, the Data API returns an error and
                  doesn't process the request. This 4-MiB limit includes the
                  size of the HTTP headers and the JSON notation in the request.
                  Thus, the number of parameter sets that you can include
                  depends on a combination of factors, such as the size of the
                  SQL statement and the size of each parameter set.</p> <p>The
                  response size limit is 1 MiB. If the call returns more than 1
                  MiB of response data, the call is terminated.</p> </note>
                tags:
                  - Batches
                  - Execute
                  - Statements
                  - Batches
                  - Execute
            /BeginTransaction:
              POST:
                summary: BeginTransaction
                description: >-
                  <p>Starts a SQL transaction.</p> <note> <p>A transaction can
                  run for a maximum of 24 hours. A transaction is terminated and
                  rolled back automatically after 24 hours.</p> <p>A transaction
                  times out if no calls use its transaction ID in three minutes.
                  If a transaction times out before it's committed, it's rolled
                  back automatically.</p> <p>DDL statements inside a transaction
                  cause an implicit commit. We recommend that you run each DDL
                  statement in a separate <code>ExecuteStatement</code> call
                  with <code>continueAfterTimeout</code> enabled.</p> </note>
                tags:
                  - Begins
                  - Transactions
                  - Batches
                  - Execute
                  - Begins
                  - Transactions
            /CommitTransaction:
              POST:
                summary: CommitTransaction
                description: >-
                  <p>Ends a SQL transaction started with the
                  <code>BeginTransaction</code> operation and commits the
                  changes.</p>
                tags:
                  - Commit
                  - Transactions
                  - Batches
                  - Execute
                  - Begins
                  - Transactions
                  - Commit
            /ExecuteSql:
              POST:
                summary: ExecuteSql
                description: >-
                  <p>Runs one or more SQL statements.</p> <note> <p>This
                  operation isn't supported for Aurora PostgreSQL Serverless v2
                  and provisioned DB clusters, and for Aurora Serverless v1 DB
                  clusters, the operation is deprecated. Use the
                  <code>BatchExecuteStatement</code> or
                  <code>ExecuteStatement</code> operation.</p> </note>
                tags:
                  - Execute
                  - SQL
                  - Batches
                  - Execute
                  - Begins
                  - Transactions
                  - Commit
                  - SQL
            /Execute:
              POST:
                summary: ExecuteStatement
                description: >-
                  <p>Runs a SQL statement against a database.</p> <note> <p>If a
                  call isn't part of a transaction because it doesn't include
                  the <code>transactionID</code> parameter, changes that result
                  from the call are committed automatically.</p> <p>If the
                  binary response data from the database is more than 1 MB, the
                  call is terminated.</p> </note>
                tags:
                  - Execute
                  - Statements
                  - Batches
                  - Execute
                  - Begins
                  - Transactions
                  - Commit
                  - SQL
            /RollbackTransaction:
              POST:
                summary: RollbackTransaction
                description: >-
                  <p>Performs a rollback of a transaction. Rolling back a
                  transaction cancels its ch
                tags:
                  - Rollback
                  - Transactions
                  - Batches
                  - Execute
                  - Begins
                  - Transactions
                  - Commit
                  - SQL
                  - Rollback
    overlays:
      - type: APIs.io Search
        url: overlays/rds-data-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/rds-data-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:rds-data
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
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---