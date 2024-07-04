---
name: Async
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/async.png
url: https://example.com/apis/async.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Async
apis:
  - name: lambda
    description: >-
      <fullname>AWS Lambda</fullname> <p><b>Overview</b></p> <p>This is the AWS
      Lambda API Reference. The AWS Lambda Developer Guide provides additional
      information. For the service overview, go to <a
      href="http://docs.aws.amazon.com/lambda/latest/dg/welcome.html">What is
      AWS Lambda</a>, and for information about how the service works, go to <a
      href="http://docs.aws.amazon.com/lambda/latest/dg/lambda-introduction.html">AWS
      LambdaL How it Works</a> in the AWS Lambda Developer Guide.</p>
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
            title: lambda
          paths:
            /2018-10-31/layers/{LayerName}/versions/{VersionNumber}/policy:
              GET:
                summary: GetLayerVersionPolicy
                description: >-
                  <p>Returns the permission policy for a version of an <a
                  href="https://docs.aws.amazon.com/lambda/latest/dg/configuration-layers.html">Lambda
                  layer</a>. For more information, see
                  <a>AddLayerVersionPermission</a>.</p>
                tags:
                  - Get
                  - Layers
                  - Versions
                  - Policies
                  - Layers
                  - Names
                  - Versions
                  - Versions
                  - Numbers
                  - Policies
            /2015-03-31/functions/{FunctionName}/policy:
              GET:
                summary: GetPolicy
                description: >-
                  <p>Returns the <a
                  href="https://docs.aws.amazon.com/lambda/latest/dg/access-control-resource-based.html">resource-based
                  IAM policy</a> for a function, version, or alias.</p>
                tags:
                  - Get
                  - Policies
                  - Layers
                  - Names
                  - Versions
                  - Versions
                  - Numbers
                  - Policies
                  - Functions
            /2015-03-31/functions/{FunctionName}/aliases:
              GET:
                summary: ListAliases
                description: >-
                  <p>Returns a list of <a
                  href="https://docs.aws.amazon.com/lambda/latest/dg/configuration-aliases.html">aliases</a>
                  for a Lambda function.</p>
                tags:
                  - Lists
                  - Aliases
                  - Layers
                  - Names
                  - Versions
                  - Versions
                  - Numbers
                  - Policies
                  - Functions
                  - Aliases
            /2020-04-22/code-signing-configs/:
              GET:
                summary: ListCodeSigningConfigs
                description: >-
                  <p>Returns a list of <a
                  href="https://docs.aws.amazon.com/lambda/latest/dg/configuring-codesigning.html">code
                  signing configurations</a>. A request returns up to 10,000
                  configurations per call. You can use the <code>MaxItems</code>
                  parameter to return fewer configurations per call. </p>
                tags:
                  - Lists
                  - Code
                  - Signing
                  - Configurations
                  - Layers
                  - Names
                  - Versions
                  - Versions
                  - Numbers
                  - Policies
                  - Functions
                  - Aliases
                  - '2020'
                  - '04'
                  - '22'
                  - Code
                  - Signing
                  - Configurations
            /2015-03-31/event-source-mappings/:
              GET:
                summary: ListEventSourceMappings
                description: >-
                  <p>Lists event source mappings. Specify an
                  <code>EventSourceArn</code> to show only event source mappings
                  for a single event source.</p>
                tags:
                  - Lists
                  - Events
                  - Source
                  - Mapping
                  - Layers
                  - Names
                  - Versions
                  - Versions
                  - Numbers
                  - Policies
                  - Functions
                  - Aliases
                  - '2020'
                  - '04'
                  - '22'
                  - Code
                  - Signing
                  - Configurations
                  - '2015'
                  - '03'
                  - '31'
                  - Events
                  - Source
                  - Mapping
            /2015-03-31/functions:
              POST:
                summary: CreateFunction
                description: >-
                  <p>Creates a Lambda function. To create a function, you need a
                  <a
                  href="https://docs.aws.amazon.com/lambda/latest/dg/gettingstarted-package.html">deployment
                  package</a> and an <a
                  href="https://docs.aws.amazon.com/lambda/latest/dg/intro-permission-model.html#lambda-intro-execution-role">execution
                  role</a>. The deployment package is a .zip file archive or
                  container image that contains your function code. The
                  execution role grants the function permission to use Amazon
                  Web Services, such as Amazon CloudWatch Logs for log streaming
                  and X-Ray for request tracing.</p> <p>If the deployment
                  package is a <a
                  href="https://docs.aws.amazon.com/lambda/latest/dg/lambda-images.html">container
                  image</a>, then you set the package type to
                  <code>Image</code>. For a container image, the code property
                  must include the URI of a container image in the Amazon ECR
                  registry. You do not need to specify the handler and runtime
                  properties.</p> <p>If the deployment package is a <a
                  href="https://docs.aws.amazon.com/lambda/latest/dg/gettingstarted-package.html#gettingstarted-package-zip">.zip
                  file archive</a>, then you set the package type to
                  <code>Zip</code>. For a .zip file archive, the code property
                  specifies the location of the .zip file. You must also specify
                  the handler and runtime properties. The code in the deployment
                  package must be compatible with the target instruction set
                  architecture of the function (<code>x86-64</code> or
                  <code>arm64</code>). If you do not specify the architecture,
                  then the default value is <code>x86-64</code>.</p> <p>When you
                  create a function, Lambda provisions an instance of the
                  function and its supporting resources. If your function
                  connects to a VPC, this process can take a minute or so.
                  During this time, you can't invoke or modify the function. The
                  <code>State</code>, <code>StateReason</code>, and
                  <code>StateReasonCode</code> fields in the response from
                  <a>GetFunctionConfiguration</a> indicate when the function is
                  ready to invoke. For more information, see <a
                  href="https://docs.aws.amazon.com/lambda/latest/dg/functions-states.html">Lambda
                  function states</a>.</p> <p>A function has an unpublished
                  version, and can have published versions and aliases. The
                  unpublished version changes when you update your function's
                  code and configuration. A published version is a snapshot of
                  your function code and configuration that can't be changed. An
                  alias is a named resource that maps to a version, and can be
                  changed to map to a different version. Use the
                  <code>Publish</code> parameter to create version
                  <code>1</code> of your function from its initial
                  configuration.</p> <p>The other parameters let you configure
                  version-specific and function-level settings. You can modify
                  version-specific settings later with
                  <a>UpdateFunctionConfiguration</a>. Function-level settings
                  apply to both the unpublished and published versions of the
                  function, and include tags (<a>TagResource</a>) and
                  per-function concurrency limits
                  (<a>PutFunctionConcurrency</a>).</p> <p>You can use code
                  signing if your deployment package is a .zip file archive. To
                  enable code signing for this function, specify the ARN of a
                  code-signing configuration. When a user attempts to deploy a
                  code package with <a>UpdateFunctionCode</a>, Lambda checks
                  that the code package has a valid signature from a trusted
                  publisher. The code-signing configuration includes set of
                  signing profiles, which define the trusted publishers for this
                  function.</p> <p>If another Amazon Web Services account or an
                  Amazon Web Service invokes your function, use
                  <a>AddPermission</a> to grant permission by creating a
                  resource-based Identity and Access Management (IAM) policy.
                  You can grant permissions at the function level, on a version,
                  or on an alias.</p> <p>To invoke your function directly, use
                  <a>Invoke</a>. To invoke your function in response to events
                  in other Amazon Web Services, create an event source mapping
                  (<a>CreateEventSourceMapping</a>), or configure a function
                  trigger in the other service. For more information, see <a
                  href="https://docs.aws.amazon.com/lambda/latest/dg/lambda-invocation.html">Invoking
                  Lambda functions</a>.</p>
                tags:
                  - Create
                  - Functions
                  - Layers
                  - Names
                  - Versions
                  - Versions
                  - Numbers
                  - Policies
                  - Functions
                  - Aliases
                  - '2020'
                  - '04'
                  - '22'
                  - Code
                  - Signing
                  - Configurations
                  - '2015'
                  - '03'
                  - '31'
                  - Events
                  - Source
                  - Mapping
                  - Functions
            /2021-10-31/functions/{FunctionName}/url:
              PUT:
                summary: UpdateFunctionUrlConfig
                description: <p>Updates the configuration for a Lambda function URL.</p>
                tags:
                  - Update
                  - Functions
                  - URL
                  - Configurations
                  - Layers
                  - Names
                  - Versions
                  - Versions
                  - Numbers
                  - Policies
                  - Functions
                  - Aliases
                  - '2020'
                  - '04'
                  - '22'
                  - Code
                  - Signing
                  - Configurations
                  - '2015'
                  - '03'
                  - '31'
                  - Events
                  - Source
                  - Mapping
                  - Functions
                  - URL
            /2015-03-31/functions/{FunctionName}/aliases/{Name}:
              PUT:
                summary: UpdateAlias
                description: >-
                  <p>Updates the configuration of a Lambda function <a
                  href="https://docs.aws.amazon.com/lambda/latest/dg/configuration-aliases.html">alias</a>.</p>
                tags:
                  - Update
                  - Alias
                  - Layers
                  - Names
                  - Versions
                  - Versions
                  - Numbers
                  - Policies
                  - Functions
                  - Aliases
                  - '2020'
                  - '04'
                  - '22'
                  - Code
                  - Signing
                  - Configurations
                  - '2015'
                  - '03'
                  - '31'
                  - Events
                  - Source
                  - Mapping
                  - Functions
                  - URL
            /2020-04-22/code-signing-configs/{CodeSigningConfigArn}:
              PUT:
                summary: UpdateCodeSigningConfig
                description: >-
                  <p>Update the code signing configuration. Changes to the code
                  signing configuration take effect the next time a user tries
                  to deploy a code package to the function. </p>
                tags:
                  - Update
                  - Code
                  - Signing
                  - Configurations
                  - Layers
                  - Names
                  - Versions
                  - Versions
                  - Numbers
                  - Policies
                  - Functions
                  - Aliases
                  - '2020'
                  - '04'
                  - '22'
                  - Code
                  - Signing
                  - Configurations
                  - '2015'
                  - '03'
                  - '31'
                  - Events
                  - Source
                  - Mapping
                  - Functions
                  - URL
                  - Configurations
                  - ARN
            /2015-03-31/event-source-mappings/{UUID}:
              PUT:
                summary: UpdateEventSourceMapping
                description: >-
                  <p>Updates an event source mapping. You can change the
                  function that Lambda invokes, or pause invocation and resume
                  later from the same location.</p> <p>For details about how to
                  configure different event sources, see the following topics.
                  </p> <ul> <li> <p> <a
                  href="https://docs.aws.amazon.com/lambda/latest/dg/with-ddb.html#services-dynamodb-eventsourcemapping">
                  Amazon DynamoDB Streams</a> </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/lambda/latest/dg/with-kinesis.html#services-kinesis-eventsourcemapping">
                  Amazon Kinesis</a> </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/lambda/latest/dg/with-sqs.html#events-sqs-eventsource">
                  Amazon SQS</a> </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/lambda/latest/dg/with-mq.html#services-mq-eventsourcemapping">
                  Amazon MQ and RabbitMQ</a> </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/lambda/latest/dg/with-msk.html">
                  Amazon MSK</a> </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/lambda/latest/dg/kafka-smaa.html">
                  Apache Kafka</a> </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/lambda/latest/dg/with-documentdb.html">
                  Amazon DocumentDB</a> </p> </li> </ul> <p>The following error
                  handling options are available only for stream sources
                  (DynamoDB and Kinesis):</p> <ul> <li> <p>
                  <code>BisectBatchOnFunctionError</code> – If the function
                  returns an error, split the batch in two and retry.</p> </li>
                  <li> <p> <code>DestinationConfig</code> – Send discarded
                  records to an Amazon SQS queue or Amazon SNS topic.</p> </li>
                  <li> <p> <code>MaximumRecordAgeInSeconds</code> – Discard
                  records older than the specified age. The default value is
                  infinite (-1). When set to infinite (-1), failed records are
                  retried until the record expires</p> </li> <li> <p>
                  <code>MaximumRetryAttempts</code> – Discard records after the
                  specified number of retries. The default value is infinite
                  (-1). When set to infinite (-1), failed records are retried
                  until the record expires.</p> </li> <li> <p>
                  <code>ParallelizationFactor</code> – Process multiple batches
                  from each shard concurrently.</p> </li> </ul> <p>For
                  information about which configuration parameters apply to each
                  event source, see the following topics.</p> <ul> <li> <p> <a
                  href="https://docs.aws.amazon.com/lambda/latest/dg/with-ddb.html#services-ddb-params">
                  Amazon DynamoDB Streams</a> </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/lambda/latest/dg/with-kinesis.html#services-kinesis-params">
                  Amazon Kinesis</a> </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/lambda/latest/dg/with-sqs.html#services-sqs-params">
                  Amazon SQS</a> </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/lambda/latest/dg/with-mq.html#services-mq-params">
                  Amazon MQ and RabbitMQ</a> </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/lambda/latest/dg/with-msk.html#services-msk-parms">
                  Amazon MSK</a> </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/lambda/latest/dg/with-kafka.html#services-kafka-parms">
                  Apache Kafka</a> </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/lambda/latest/dg/with-documentdb.html#docdb-configuration">
                  Amazon DocumentDB</a> </p> </li> </ul>
                tags:
                  - Update
                  - Events
                  - Source
                  - Mapping
                  - Layers
                  - Names
                  - Versions
                  - Versions
                  - Numbers
                  - Policies
                  - Functions
                  - Aliases
                  - '2020'
                  - '04'
                  - '22'
                  - Code
                  - Signing
                  - Configurations
                  - '2015'
                  - '03'
                  - '31'
                  - Events
                  - Source
                  - Mapping
                  - Functions
                  - URL
                  - Configurations
                  - ARN
                  - UUID
            /2015-03-31/functions/{FunctionName}:
              GET:
                summary: GetFunction
                description: >-
                  <p>Returns information about the function or function version,
                  with a link to download the deployment package that's valid
                  for 10 minutes. If you specify a function version, only
                  details that are specific to that version are returned.</p>
                tags:
                  - Get
                  - Functions
                  - Layers
                  - Names
                  - Versions
                  - Versions
                  - Numbers
                  - Policies
                  - Functions
                  - Aliases
                  - '2020'
                  - '04'
                  - '22'
                  - Code
                  - Signing
                  - Configurations
                  - '2015'
                  - '03'
                  - '31'
                  - Events
                  - Source
                  - Mapping
                  - Functions
                  - URL
                  - Configurations
                  - ARN
                  - UUID
            /2020-06-30/functions/{FunctionName}/code-signing-config:
              PUT:
                summary: PutFunctionCodeSigningConfig
                description: >-
                  <p>Update the code signing configuration for the function.
                  Changes to the code signing configuration take effect the next
                  time a user tries to deploy a code package to the function.
                  </p>
                tags:
                  - Put
                  - Functions
                  - Code
                  - Signing
                  - Configurations
                  - Layers
                  - Names
                  - Versions
                  - Versions
                  - Numbers
                  - Policies
                  - Functions
                  - Aliases
                  - '2020'
                  - '04'
                  - '22'
                  - Code
                  - Signing
                  - Configurations
                  - '2015'
                  - '03'
                  - '31'
                  - Events
                  - Source
                  - Mapping
                  - Functions
                  - URL
                  - Configurations
                  - ARN
                  - UUID
            /2017-10-31/functions/{FunctionName}/concurrency:
              PUT:
                summary: PutFunctionConcurrency
                description: >-
                  <p>Sets the maximum number of simultaneous executions for a
                  function, and reserves capacity for that concurrency
                  level.</p> <p>Concurrency settings apply to the function as a
                  whole, including all published versions and the unpublished
                  version. Reserving concurrency both ensures that your function
                  has capacity to process the specified number of events
                  simultaneously, and prevents it from scaling beyond that
                  level. Use <a>GetFunction</a> to see the current setting for a
                  function.</p> <p>Use <a>GetAccountSettings</a> to see your
                  Regional concurrency limit. You can reserve concurrency for as
                  many functions as you like, as long as you leave at least 100
                  simultaneous executions unreserved for functions that aren't
                  configured with a per-function limit. For more information,
                  see <a
                  href="https://docs.aws.amazon.com/lambda/latest/dg/invocation-scaling.html">Lambda
                  function scaling</a>.</p>
                tags:
                  - Put
                  - Functions
                  - Concurrency
                  - Layers
                  - Names
                  - Versions
                  - Versions
                  - Numbers
                  - Policies
                  - Functions
                  - Aliases
                  - '2020'
                  - '04'
                  - '22'
                  - Code
                  - Signing
                  - Configurations
                  - '2015'
                  - '03'
                  - '31'
                  - Events
                  - Source
                  - Mapping
                  - Functions
                  - URL
                  - Configurations
                  - ARN
                  - UUID
                  - Concurrency
            /2019-09-25/functions/{FunctionName}/event-invoke-config:
              POST:
                summary: UpdateFunctionEventInvokeConfig
                description: >-
                  <p>Updates the configuration for asynchronous invocation for a
                  function, version, or alias.</p> <p>To configure options for
                  asynchronous invocation, use
                  <a>PutFunctionEventInvokeConfig</a>.</p>
                tags:
                  - Update
                  - Functions
                  - Events
                  - Invoke
                  - Configurations
                  - Layers
                  - Names
                  - Versions
                  - Versions
                  - Numbers
                  - Policies
                  - Functions
                  - Aliases
                  - '2020'
                  - '04'
                  - '22'
                  - Code
                  - Signing
                  - Configurations
                  - '2015'
                  - '03'
                  - '31'
                  - Events
                  - Source
                  - Mapping
                  - Functions
                  - URL
                  - Configurations
                  - ARN
                  - UUID
                  - Concurrency
                  - Invoke
            /2018-10-31/layers/{LayerName}/versions/{VersionNumber}:
              GET:
                summary: GetLayerVersion
                description: >-
                  <p>Returns information about a version of an <a
                  href="https://docs.aws.amazon.com/lambda/latest/dg/configuration-layers.html">Lambda
                  layer</a>, with a link to download the layer archive that's
                  valid for 10 minutes.</p>
                tags:
                  - Get
                  - Layers
                  - Versions
                  - Layers
                  - Names
                  - Versions
                  - Versions
                  - Numbers
                  - Policies
                  - Functions
                  - Aliases
                  - '2020'
                  - '04'
                  - '22'
                  - Code
                  - Signing
                  - Configurations
                  - '2015'
                  - '03'
                  - '31'
                  - Events
                  - Source
                  - Mapping
                  - Functions
                  - URL
                  - Configurations
                  - ARN
                  - UUID
                  - Concurrency
                  - Invoke
            /2019-09-30/functions/{FunctionName}/provisioned-concurrency:
              PUT:
                summary: PutProvisionedConcurrencyConfig
                description: >-
                  <p>Adds a provisioned concurrency configuration to a
                  function's alias or version.</p>
                tags:
                  - Put
                  - Provisioned
                  - Concurrency
                  - Configurations
                  - Layers
                  - Names
                  - Versions
                  - Versions
                  - Numbers
                  - Policies
                  - Functions
                  - Aliases
                  - '2020'
                  - '04'
                  - '22'
                  - Code
                  - Signing
                  - Configurations
                  - '2015'
                  - '03'
                  - '31'
                  - Events
                  - Source
                  - Mapping
                  - Functions
                  - URL
                  - Configurations
                  - ARN
                  - UUID
                  - Concurrency
                  - Invoke
                  - Provisioned
            /2016-08-19/account-settings/:
              GET:
                summary: GetAccountSettings
                description: >-
                  <p>Retrieves details about your account's <a
                  href="https://docs.aws.amazon.com/lambda/latest/dg/limits.html">limits</a>
                  and usage in an Amazon Web Services Region.</p>
                tags:
                  - Get
                  - Account
                  - Settings
                  - Layers
                  - Names
                  - Versions
                  - Versions
                  - Numbers
                  - Policies
                  - Functions
                  - Aliases
                  - '2020'
                  - '04'
                  - '22'
                  - Code
                  - Signing
                  - Configurations
                  - '2015'
                  - '03'
                  - '31'
                  - Events
                  - Source
                  - Mapping
                  - Functions
                  - URL
                  - Configurations
                  - ARN
                  - UUID
                  - Concurrency
                  - Invoke
                  - Provisioned
                  - '2016'
                  - '08'
                  - '19'
                  - Account
                  - Settings
            /2019-09-30/functions/{FunctionName}/concurrency:
              GET:
                summary: GetFunctionConcurrency
                description: >-
                  <p>Returns details about the reserved concurrency
                  configuration for a function. To set a concurrency limit for a
                  function, use <a>PutFunctionConcurrency</a>.</p>
                tags:
                  - Get
                  - Functions
                  - Concurrency
                  - Layers
                  - Names
                  - Versions
                  - Versions
                  - Numbers
                  - Policies
                  - Functions
                  - Aliases
                  - '2020'
                  - '04'
                  - '22'
                  - Code
                  - Signing
                  - Configurations
                  - '2015'
                  - '03'
                  - '31'
                  - Events
                  - Source
                  - Mapping
                  - Functions
                  - URL
                  - Configurations
                  - ARN
                  - UUID
                  - Concurrency
                  - Invoke
                  - Provisioned
                  - '2016'
                  - '08'
                  - '19'
                  - Account
                  - Settings
            /2015-03-31/functions/{FunctionName}/configuration:
              PUT:
                summary: UpdateFunctionConfiguration
                description: >-
                  <p>Modify the version-specific settings of a Lambda
                  function.</p> <p>When you update a function, Lambda provisions
                  an instance of the function and its supporting resources. If
                  your function connects to a VPC, this process can take a
                  minute. During this time, you can't modify the function, but
                  you can still invoke it. The <code>LastUpdateStatus</code>,
                  <code>LastUpdateStatusReason</code>, and
                  <code>LastUpdateStatusReasonCode</code> fields in the response
                  from <a>GetFunctionConfiguration</a> indicate when the update
                  is complete and the function is processing events with the new
                  configuration. For more information, see <a
                  href="https://docs.aws.amazon.com/lambda/latest/dg/functions-states.html">Lambda
                  function states</a>.</p> <p>These settings can vary between
                  versions of a function and are locked when you publish a
                  version. You can't modify the configuration of a published
                  version, only the unpublished version.</p> <p>To configure
                  function concurrency, use <a>PutFunctionConcurrency</a>. To
                  grant invoke permissions to an Amazon Web Services account or
                  Amazon Web Service, use <a>AddPermission</a>.</p>
                tags:
                  - Update
                  - Functions
                  - Configurations
                  - Layers
                  - Names
                  - Versions
                  - Versions
                  - Numbers
                  - Policies
                  - Functions
                  - Aliases
                  - '2020'
                  - '04'
                  - '22'
                  - Code
                  - Signing
                  - Configurations
                  - '2015'
                  - '03'
                  - '31'
                  - Events
                  - Source
                  - Mapping
                  - Functions
                  - URL
                  - Configurations
                  - ARN
                  - UUID
                  - Concurrency
                  - Invoke
                  - Provisioned
                  - '2016'
                  - '08'
                  - '19'
                  - Account
                  - Settings
                  - Configurations
            /2018-10-31/layers?find=LayerVersion:
              GET:
                summary: GetLayerVersionByArn
                description: >-
                  <p>Returns information about a version of an <a
                  href="https://docs.aws.amazon.com/lambda/latest/dg/configuration-layers.html">Lambda
                  layer</a>, with a link to download the layer archive that's
                  valid for 10 minutes.</p>
                tags:
                  - Get
                  - Layers
                  - Versions
                  - By
                  - ARN
                  - Layers
                  - Names
                  - Versions
                  - Versions
                  - Numbers
                  - Policies
                  - Functions
                  - Aliases
                  - '2020'
                  - '04'
                  - '22'
                  - Code
                  - Signing
                  - Configurations
                  - '2015'
                  - '03'
                  - '31'
                  - Events
                  - Source
                  - Mapping
                  - Functions
                  - URL
                  - Configurations
                  - ARN
                  - UUID
                  - Concurrency
                  - Invoke
                  - Provisioned
                  - '2016'
                  - '08'
                  - '19'
                  - Account
                  - Settings
                  - Configurations
            /2021-07-20/functions/{FunctionName}/runtime-management-config:
              PUT:
                summary: PutRuntimeManagementConfig
                description: >-
                  <p>Sets the runtime management configuration for a function's
                  version. For more information, see <a
                  href="https://docs.aws.amazon.com/lambda/latest/dg/runtimes-update.html">Runtime
                  updates</a>.</p>
                tags:
                  - Put
                  - Runtime
                  - Management
                  - Configurations
                  - Layers
                  - Names
                  - Versions
                  - Versions
                  - Numbers
                  - Policies
                  - Functions
                  - Aliases
                  - '2020'
                  - '04'
                  - '22'
                  - Code
                  - Signing
                  - Configurations
                  - '2015'
                  - '03'
                  - '31'
                  - Events
                  - Source
                  - Mapping
                  - Functions
                  - URL
                  - Configurations
                  - ARN
                  - UUID
                  - Concurrency
                  - Invoke
                  - Provisioned
                  - '2016'
                  - '08'
                  - '19'
                  - Account
                  - Settings
                  - Configurations
                  - Runtime
                  - Management
            /2015-03-31/functions/{FunctionName}/invocations:
              POST:
                summary: Invoke
                description: >-
                  <p>Invokes a Lambda function. You can invoke a function
                  synchronously (and wait for the response), or asynchronously.
                  By default, Lambda invokes your function synchronously (i.e.
                  the<code>InvocationType</code> is
                  <code>RequestResponse</code>). To invoke a function
                  asynchronously, set <code>InvocationType</code> to
                  <code>Event</code>. Lambda passes the
                  <code>ClientContext</code> object to your function for
                  synchronous invocations only.</p> <p>For <a
                  href="https://docs.aws.amazon.com/lambda/latest/dg/invocation-sync.html">synchronous
                  invocation</a>, details about the function response, including
                  errors, are included in the response body and headers. For
                  either invocation type, you can find more information in the
                  <a
                  href="https://docs.aws.amazon.com/lambda/latest/dg/monitoring-functions.html">execution
                  log</a> and <a
                  href="https://docs.aws.amazon.com/lambda/latest/dg/lambda-x-ray.html">trace</a>.</p>
                  <p>When an error occurs, your function may be invoked multiple
                  times. Retry behavior varies by error type, client, event
                  source, and invocation type. For example, if you invoke a
                  function asynchronously and it returns an error, Lambda
                  executes the function up to two more times. For more
                  information, see <a
                  href="https://docs.aws.amazon.com/lambda/latest/dg/invocation-retries.html">Error
                  handling and automatic retries in Lambda</a>.</p> <p>For <a
                  href="https://docs.aws.amazon.com/lambda/latest/dg/invocation-async.html">asynchronous
                  invocation</a>, Lambda adds events to a queue before sending
                  them to your function. If your function does not have enough
                  capacity to keep up with the queue, events may be lost.
                  Occasionally, your function may receive the same event
                  multiple times, even if no error occurs. To retain events that
                  were not processed, configure your function with a <a
                  href="https://docs.aws.amazon.com/lambda/latest/dg/invocation-async.html#invocation-dlq">dead-letter
                  queue</a>.</p> <p>The status code in the API response doesn't
                  reflect function errors. Error codes are reserved for errors
                  that prevent your function from executing, such as permissions
                  errors, <a
                  href="https://docs.aws.amazon.com/lambda/latest/dg/gettingstarted-limits.html">quota</a>
                  errors, or issues with your function's code and configuration.
                  For example, Lambda returns
                  <code>TooManyRequestsException</code> if running the function
                  would cause you to exceed a concurrency limit at either the
                  account level (<code>ConcurrentInvocationLimitExceeded</code>)
                  or function level
                  (<code>ReservedFunctionConcurrentInvocationLimitExceeded</code>).</p>
                  <p>For functions with a long timeout, your client might
                  disconnect during synchronous invocation while it waits for a
                  response. Configure your HTTP client, SDK, firewall, proxy, or
                  operating system to allow for long connections with timeout or
                  keep-alive settings.</p> <p>This operation requires permission
                  for the <a
                  href="https://docs.aws.amazon.com/IAM/latest/UserGuide/list_awslambda.html">lambda:InvokeFunction</a>
                  action. For details on how to set up permissions for
                  cross-account invocations, see <a
                  href="https://docs.aws.amazon.com/lambda/latest/dg/access-control-resource-based.html#permissions-resource-xaccountinvoke">Granting
                  function access to other accounts</a>.</p>
                tags:
                  - Invoke
                  - Layers
                  - Names
                  - Versions
                  - Versions
                  - Numbers
                  - Policies
                  - Functions
                  - Aliases
                  - '2020'
                  - '04'
                  - '22'
                  - Code
                  - Signing
                  - Configurations
                  - '2015'
                  - '03'
                  - '31'
                  - Events
                  - Source
                  - Mapping
                  - Functions
                  - URL
                  - Configurations
                  - ARN
                  - UUID
                  - Concurrency
                  - Invoke
                  - Provisioned
                  - '2016'
                  - '08'
                  - '19'
                  - Account
                  - Settings
                  - Configurations
                  - Runtime
                  - Management
                  - Invocations
            /2014-11-13/functions/{FunctionName}/invoke-async/:
              POST:
                summary: InvokeAsync
                description: >-
                  <important> <p>For asynchronous function invocation, use
                  <a>Invoke</a>.</p> </important> <p>Invokes a function
                  asynchronously.</p>
                tags:
                  - Invoke
                  - Async
                  - Layers
                  - Names
                  - Versions
                  - Versions
                  - Numbers
                  - Policies
                  - Functions
                  - Aliases
                  - '2020'
                  - '04'
                  - '22'
                  - Code
                  - Signing
                  - Configurations
                  - '2015'
                  - '03'
                  - '31'
                  - Events
                  - Source
                  - Mapping
                  - Functions
                  - URL
                  - Configurations
                  - ARN
                  - UUID
                  - Concurrency
                  - Invoke
                  - Provisioned
                  - '2016'
                  - '08'
                  - '19'
                  - Account
                  - Settings
                  - Configurations
                  - Runtime
                  - Management
                  - Invocations
                  - Async
            /2021-11-15/functions/{FunctionName}/response-streaming-invocations:
              POST:
                summary: InvokeWithResponseStream
                description: >-
                  <p>Configure your Lambda functions to stream response payloads
                  back to clients. For more information, see <a
                  href="https://docs.aws.amazon.com/lambda/latest/dg/configuration-response-streaming.html">Configuring
                  a Lambda function to stream responses</a>.</p> <p>This
                  operation requires permission for the <a
                  href="https://docs.aws.amazon.com/IAM/latest/UserGuide/list_awslambda.html">lambda:InvokeFunction</a>
                  action. For details on how to set up permissions for
                  cross-account invocations, see <a
                  href="https://docs.aws.amazon.com/lambda/latest/dg/access-control-resource-based.html#permissions-resource-xaccountinvoke">Granting
                  function access to other accounts</a>.</p>
                tags:
                  - Invoke
                  - With
                  - Responses
                  - Stream
                  - Layers
                  - Names
                  - Versions
                  - Versions
                  - Numbers
                  - Policies
                  - Functions
                  - Aliases
                  - '2020'
                  - '04'
                  - '22'
                  - Code
                  - Signing
                  - Configurations
                  - '2015'
                  - '03'
                  - '31'
                  - Events
                  - Source
                  - Mapping
                  - Functions
                  - URL
                  - Configurations
                  - ARN
                  - UUID
                  - Concurrency
                  - Invoke
                  - Provisioned
                  - '2016'
                  - '08'
                  - '19'
                  - Account
                  - Settings
                  - Configurations
                  - Runtime
                  - Management
                  - Invocations
                  - Async
                  - Responses
                  - Streaming
            /2019-09-25/functions/{FunctionName}/event-invoke-config/list:
              GET:
                summary: ListFunctionEventInvokeConfigs
                description: >-
                  <p>Retrieves a list of configurations for asynchronous
                  invocation for a function.</p> <p>To configure options for
                  asynchronous invocation, use
                  <a>PutFunctionEventInvokeConfig</a>.</p>
                tags:
                  - Lists
                  - Functions
                  - Events
                  - Invoke
                  - Configurations
                  - Layers
                  - Names
                  - Versions
                  - Versions
                  - Numbers
                  - Policies
                  - Functions
                  - Aliases
                  - '2020'
                  - '04'
                  - '22'
                  - Code
                  - Signing
                  - Configurations
                  - '2015'
                  - '03'
                  - '31'
                  - Events
                  - Source
                  - Mapping
                  - Functions
                  - URL
                  - Configurations
                  - ARN
                  - UUID
                  - Concurrency
                  - Invoke
                  - Provisioned
                  - '2016'
                  - '08'
                  - '19'
                  - Account
                  - Settings
                  - Configurations
                  - Runtime
                  - Management
                  - Invocations
                  - Async
                  - Responses
                  - Streaming
                  - Lists
            /2021-10-31/functions/{FunctionName}/urls:
              GET:
                summary: ListFunctionUrlConfigs
                description: >-
                  <p>Returns a list of Lambda function URLs for the specified
                  function.</p>
                tags:
                  - Lists
                  - Functions
                  - URL
                  - Configurations
                  - Layers
                  - Names
                  - Versions
                  - Versions
                  - Numbers
                  - Policies
                  - Functions
                  - Aliases
                  - '2020'
                  - '04'
                  - '22'
                  - Code
                  - Signing
                  - Configurations
                  - '2015'
                  - '03'
                  - '31'
                  - Events
                  - Source
                  - Mapping
                  - Functions
                  - URL
                  - Configurations
                  - ARN
                  - UUID
                  - Concurrency
                  - Invoke
                  - Provisioned
                  - '2016'
                  - '08'
                  - '19'
                  - Account
                  - Settings
                  - Configurations
                  - Runtime
                  - Management
                  - Invocations
                  - Async
                  - Responses
                  - Streaming
                  - Lists
                  - URL
            /2015-03-31/functions/:
              GET:
                summary: ListFunctions
                description: >-
                  <p>Returns a list of Lambda functions, with the
                  version-specific configuration of each. Lambda returns up to
                  50 functions per call.</p> <p>Set <code>FunctionVersion</code>
                  to <code>ALL</code> to include all published versions of each
                  function in addition to the unpublished version.</p> <note>
                  <p>The <code>ListFunctions</code> operation returns a subset
                  of the <a>FunctionConfiguration</a> fields. To get the
                  additional fields (State, StateReasonCode, StateReason,
                  LastUpdateStatus, LastUpdateStatusReason,
                  LastUpdateStatusReasonCode, RuntimeVersionConfig) for a
                  function or version, use <a>GetFunction</a>.</p> </note>
                tags:
                  - Lists
                  - Functions
                  - Layers
                  - Names
                  - Versions
                  - Versions
                  - Numbers
                  - Policies
                  - Functions
                  - Aliases
                  - '2020'
                  - '04'
                  - '22'
                  - Code
                  - Signing
                  - Configurations
                  - '2015'
                  - '03'
                  - '31'
                  - Events
                  - Source
                  - Mapping
                  - Functions
                  - URL
                  - Configurations
                  - ARN
                  - UUID
                  - Concurrency
                  - Invoke
                  - Provisioned
                  - '2016'
                  - '08'
                  - '19'
                  - Account
                  - Settings
                  - Configurations
                  - Runtime
                  - Management
                  - Invocations
                  - Async
                  - Responses
                  - Streaming
                  - Lists
                  - URL
            /2020-04-22/code-signing-configs/{CodeSigningConfigArn}/functions:
              GET:
                summary: ListFunctionsByCodeSigningConfig
                description: >-
                  <p>List the functions that use the specified code signing
                  configuration. You can use this method prior to deleting a
                  code signing configuration, to verify that no functions are
                  using it.</p>
                tags:
                  - Lists
                  - Functions
                  - By
                  - Code
                  - Signing
                  - Configurations
                  - Layers
                  - Names
                  - Versions
                  - Versions
                  - Numbers
                  - Policies
                  - Functions
                  - Aliases
                  - '2020'
                  - '04'
                  - '22'
                  - Code
                  - Signing
                  - Configurations
                  - '2015'
                  - '03'
                  - '31'
                  - Events
                  - Source
                  - Mapping
                  - Functions
                  - URL
                  - Configurations
                  - ARN
                  - UUID
                  - Concurrency
                  - Invoke
                  - Provisioned
                  - '2016'
                  - '08'
                  - '19'
                  - Account
                  - Settings
                  - Configurations
                  - Runtime
                  - Management
                  - Invocations
                  - Async
                  - Responses
                  - Streaming
                  - Lists
                  - URL
            /2018-10-31/layers/{LayerName}/versions:
              POST:
                summary: PublishLayerVersion
                description: >-
                  <p>Creates an <a
                  href="https://docs.aws.amazon.com/lambda/latest/dg/configuration-layers.html">Lambda
                  layer</a> from a ZIP archive. Each time you call
                  <code>PublishLayerVersion</code> with the same layer name, a
                  new version is created.</p> <p>Add layers to your function
                  with <a>CreateFunction</a> or
                  <a>UpdateFunctionConfiguration</a>.</p>
                tags:
                  - Publish
                  - Layers
                  - Versions
                  - Layers
                  - Names
                  - Versions
                  - Versions
                  - Numbers
                  - Policies
                  - Functions
                  - Aliases
                  - '2020'
                  - '04'
                  - '22'
                  - Code
                  - Signing
                  - Configurations
                  - '2015'
                  - '03'
                  - '31'
                  - Events
                  - Source
                  - Mapping
                  - Functions
                  - URL
                  - Configurations
                  - ARN
                  - UUID
                  - Concurrency
                  - Invoke
                  - Provisioned
                  - '2016'
                  - '08'
                  - '19'
                  - Account
                  - Settings
                  - Configurations
                  - Runtime
                  - Management
                  - Invocations
                  - Async
                  - Responses
                  - Streaming
                  - Lists
                  - URL
            /2018-10-31/layers:
              GET:
                summary: ListLayers
                description: >-
                  <p>Lists <a
                  href="https://docs.aws.amazon.com/lambda/latest/dg/invocation-layers.html">Lambda
                  layers</a> and shows information about the latest version of
                  each. Specify a <a
                  href="https://docs.aws.amazon.com/lambda/latest/dg/lambda-runtimes.html">runtime
                  identifier</a> to list only layers that indicate that they're
                  compatible with that runtime. Specify a compatible
                  architecture to include only layers that are compatible with
                  that <a
                  href="https://docs.aws.amazon.com/lambda/latest/dg/foundation-arch.html">instruction
                  set architecture</a>.</p>
                tags:
                  - Lists
                  - Layers
                  - Layers
                  - Names
                  - Versions
                  - Versions
                  - Numbers
                  - Policies
                  - Functions
                  - Aliases
                  - '2020'
                  - '04'
                  - '22'
                  - Code
                  - Signing
                  - Configurations
                  - '2015'
                  - '03'
                  - '31'
                  - Events
                  - Source
                  - Mapping
                  - Functions
                  - URL
                  - Configurations
                  - ARN
                  - UUID
                  - Concurrency
                  - Invoke
                  - Provisioned
                  - '2016'
                  - '08'
                  - '19'
                  - Account
                  - Settings
                  - Configurations
                  - Runtime
                  - Management
                  - Invocations
                  - Async
                  - Responses
                  - Streaming
                  - Lists
                  - URL
                  - '2018'
                  - '10'
                  - Layers
            /2019-09-30/functions/{FunctionName}/provisioned-concurrency?List=ALL:
              GET:
                summary: ListProvisionedConcurrencyConfigs
                description: >-
                  <p>Retrieves a list of provisioned concurrency configurations
                  for a function.</p>
                tags:
                  - Lists
                  - Provisioned
                  - Concurrency
                  - Configurations
                  - Layers
                  - Names
                  - Versions
                  - Versions
                  - Numbers
                  - Policies
                  - Functions
                  - Aliases
                  - '2020'
                  - '04'
                  - '22'
                  - Code
                  - Signing
                  - Configurations
                  - '2015'
                  - '03'
                  - '31'
                  - Events
                  - Source
                  - Mapping
                  - Functions
                  - URL
                  - Configurations
                  - ARN
                  - UUID
                  - Concurrency
                  - Invoke
                  - Provisioned
                  - '2016'
                  - '08'
                  - '19'
                  - Account
                  - Settings
                  - Configurations
                  - Runtime
                  - Management
                  - Invocations
                  - Async
                  - Responses
                  - Streaming
                  - Lists
                  - URL
                  - '2018'
                  - '10'
                  - Layers
                  - Concurrency
                  - Lists
            /2017-03-31/tags/{ARN}:
              DELETE:
                summary: UntagResource
                description: >-
                  <p>Removes <a
                  href="https://docs.aws.amazon.com/lambda/latest/dg/tagging.html">tags</a>
                  from a function.</p>
                tags:
                  - Untag
                  - Resources
                  - Layers
                  - Names
                  - Versions
                  - Versions
                  - Numbers
                  - Policies
                  - Functions
                  - Aliases
                  - '2020'
                  - '04'
                  - '22'
                  - Code
                  - Signing
                  - Configurations
                  - '2015'
                  - '03'
                  - '31'
                  - Events
                  - Source
                  - Mapping
                  - Functions
                  - URL
                  - Configurations
                  - ARN
                  - UUID
                  - Concurrency
                  - Invoke
                  - Provisioned
                  - '2016'
                  - '08'
                  - '19'
                  - Account
                  - Settings
                  - Configurations
                  - Runtime
                  - Management
                  - Invocations
                  - Async
                  - Responses
                  - Streaming
                  - Lists
                  - URL
                  - '2018'
                  - '10'
                  - Layers
                  - Concurrency
                  - Lists
                  - '2017'
                  - Tags
            /2015-03-31/functions/{FunctionName}/versions:
              POST:
                summary: PublishVersion
                description: >-
                  <p>Creates a <a
                  href="https://docs.aws.amazon.com/lambda/latest/dg/versioning-aliases.html">version</a>
                  from the current code and configuration of a function. Use
                  versions to create a snapshot of your function code and
                  configuration that doesn't change.</p> <p>Lambda doesn't
                  publish a version if the function's configuration and code
                  haven't changed since the last version. Use
                  <a>UpdateFunctionCode</a> or
                  <a>UpdateFunctionConfiguration</a> to update the function
                  before publishing a version.</p> <p>Clients can invoke
                  versions directly or with an alias. To create an alias, use
                  <a>CreateAlias</a>.</p>
                tags:
                  - Publish
                  - Versions
                  - Layers
                  - Names
                  - Versions
                  - Versions
                  - Numbers
                  - Policies
                  - Functions
                  - Aliases
                  - '2020'
                  - '04'
                  - '22'
                  - Code
                  - Signing
                  - Configurations
                  - '2015'
                  - '03'
                  - '31'
                  - Events
                  - Source
                  - Mapping
                  - Functions
                  - URL
                  - Configurations
                  - ARN
                  - UUID
                  - Concurrency
                  - Invoke
                  - Provisioned
                  - '2016'
                  - '08'
                  - '19'
                  - Account
                  - Settings
                  - Configurations
                  - Runtime
                  - Management
                  - Invocations
                  - Async
                  - Responses
                  - Streaming
                  - Lists
                  - URL
                  - '2018'
                  - '10'
                  - Layers
                  - Concurrency
                  - Lists
                  - '2017'
                  - Tags
            /2018-10-31/layers/{LayerName}/versions/{VersionNumber}/policy/{StatementId}:
              DELETE:
                summary: RemoveLayerVersionPermission
                description: >-
                  <p>Removes a statement from the permissions policy for a
                  version of an <a
                  href="https://docs.aws.amazon.com/lambda/latest/dg/configuration-layers.html">Lambda
                  layer</a>. For more information, see
                  <a>AddLayerVersionPermission</a>.</p>
                tags:
                  - Removes
                  - Layers
                  - Versions
                  - Permission
                  - Layers
                  - Names
                  - Versions
                  - Versions
                  - Numbers
                  - Policies
                  - Functions
                  - Aliases
                  - '2020'
                  - '04'
                  - '22'
                  - Code
                  - Signing
                  - Configurations
                  - '2015'
                  - '03'
                  - '31'
                  - Events
                  - Source
                  - Mapping
                  - Functions
                  - URL
                  - Configurations
                  - ARN
                  - UUID
                  - Concurrency
                  - Invoke
                  - Provisioned
                  - '2016'
                  - '08'
                  - '19'
                  - Account
                  - Settings
                  - Configurations
                  - Runtime
                  - Management
                  - Invocations
                  - Async
                  - Responses
                  - Streaming
                  - Lists
                  - URL
                  - '2018'
                  - '10'
                  - Layers
                  - Concurrency
                  - Lists
                  - '2017'
                  - Tags
                  - Statements
                  - Identifiers
            /2015-03-31/functions/{FunctionName}/policy/{StatementId}:
              DELETE:
                summary: RemovePermission
                description: >-
                  <p>Revokes function-use permission from an Amazon Web Service
                  or another Amazon Web Services account. You can get the ID of
                  the statement from the output of <a>GetPolicy</a>.</p>
                tags:
                  - Removes
                  - Permission
                  - Layers
                  - Names
                  - Versions
                  - Versions
                  - Numbers
                  - Policies
                  - Functions
                  - Aliases
                  - '2020'
                  - '04'
                  - '22'
                  - Code
                  - Signing
                  - Configurations
                  - '2015'
                  - '03'
                  - '31'
                  - Events
                  - Source
                  - Mapping
                  - Functions
                  - URL
                  - Configurations
                  - ARN
                  - UUID
                  - Concurrency
                  - Invoke
                  - Provisioned
                  - '2016'
                  - '08'
                  - '19'
                  - Account
                  - Settings
                  - Configurations
                  - Runtime
                  - Management
                  - Invocations
                  - Async
                  - Responses
                  - Streaming
                  - Lists
                  - URL
                  - '2018'
                  - '10'
                  - Layers
                  - Concurrency
                  - Lists
                  - '2017'
                  - Tags
                  - Statements
                  - Identifiers
            /2015-03-31/functions/{FunctionName}/code:
              PUT:
                summary: UpdateFunctionCode
                description: >-
                  <p>Updates a Lambda function's code. If code signing is
                  enabled for the function, the code package must be signed by a
                  trusted publisher. For more information, see <a
                  href="https://docs.aws.amazon.com/lambda/latest/dg/configuration-codesigning.html">Configuring
                  code signing for Lambda</a>.</p> <p>If the function's package
                  type is <code>Image</code>, then you must specify the code
                  package in <code>ImageUri</code> as the URI of a <a
                  href="https://docs.aws.amazon.com/lambda/latest/dg/lambda-images.html">container
                  image</a> in the Amazon ECR registry.</p> <p>If the function's
                  package type is <code>Zip</code>, then you must specify the
                  deployment package as a <a
                  href="https://docs.aws.amazon.com/lambda/latest/dg/gettingstarted-package.html#gettingstarted-package-zip">.zip
                  file archive</a>. Enter the Amazon S3 bucket and key of the
                  code .zip file location. You can also provide the function
                  code inline using the <code>ZipFile</code> field.</p> <p>The
                  code in the deployment package must be compatible with the
                  target instruction set architecture of the function
                  (<code>x86-64</code> or <code>arm64</code>).</p> <p>The
                  function's code is locked when you publish a version. You
                  can't modify the code of a published version, only the
                  unpublished version.</p> <note> <p>For a function defined as a
                  container image, Lambda resolves the image tag to an image
                  digest. In Amazon ECR, if you update the image tag to a new
                  image, Lambda does not automatically update the function.</
                tags:
                  - Update
                  - Functions
                  - Code
                  - Layers
                  - Names
                  - Versions
                  - Versions
                  - Numbers
                  - Policies
                  - Functions
                  - Aliases
                  - '2020'
                  - '04'
                  - '22'
                  - Code
                  - Signing
                  - Configurations
                  - '2015'
                  - '03'
                  - '31'
                  - Events
                  - Source
                  - Mapping
                  - Functions
                  - URL
                  - Configurations
                  - ARN
                  - UUID
                  - Concurrency
                  - Invoke
                  - Provisioned
                  - '2016'
                  - '08'
                  - '19'
                  - Account
                  - Settings
                  - Configurations
                  - Runtime
                  - Management
                  - Invocations
                  - Async
                  - Responses
                  - Streaming
                  - Lists
                  - URL
                  - '2018'
                  - '10'
                  - Layers
                  - Concurrency
                  - Lists
                  - '2017'
                  - Tags
                  - Statements
                  - null
    overlays:
      - type: APIs.io Search
        url: overlays/lambda-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/lambda-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:lambda
  - name: s3control
    description: >-
      <p> Amazon Web Services S3 Control provides access to Amazon S3 control
      plane actions. </p>
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
            title: s3control
          paths:
            /v20180820/accessgrantsinstance/identitycenter:
              DELETE:
                summary: DissociateAccessGrantsIdentityCenter
                description: >-
                  <p>Dissociates the Amazon Web Services IAM Identity Center
                  instance from the S3 Access Grants instance. </p> <dl>
                  <dt>Permissions</dt> <dd> <p>You must have the
                  <code>s3:DissociateAccessGrantsIdentityCenter</code>
                  permission to use this operation. </p> </dd> <dt>Additional
                  Permissions</dt> <dd> <p>You must have the
                  <code>sso:DeleteApplication</code> permission to use this
                  operation. </p> </dd> </dl>
                tags:
                  - Dissociate
                  - Access
                  - Grants
                  - Identity
                  - Center
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
            /v20180820/accessgrantsinstance/grant:
              POST:
                summary: CreateAccessGrant
                description: >-
                  <p>Creates an access grant that gives a grantee access to your
                  S3 data. The grantee can be an IAM user or role or a directory
                  user, or group. Before you can create a grant, you must have
                  an S3 Access Grants instance in the same Region as the S3
                  data. You can create an S3 Access Grants instance using the <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_CreateAccessGrantsInstance.html">CreateAccessGrantsInstance</a>.
                  You must also have registered at least one S3 data location in
                  your S3 Access Grants instance using <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_CreateAccessGrantsLocation.html">CreateAccessGrantsLocation</a>.
                  </p> <dl> <dt>Permissions</dt> <dd> <p>You must have the
                  <code>s3:CreateAccessGrant</code> permission to use this
                  operation. </p> </dd> <dt>Additional Permissions</dt> <dd>
                  <p>For any directory identity -
                  <code>sso:DescribeInstance</code> and
                  <code>sso:DescribeApplication</code> </p> <p>For directory
                  users - <code>identitystore:DescribeUser</code> </p> <p>For
                  directory groups - <code>identitystore:DescribeGroup</code>
                  </p> </dd> </dl>
                tags:
                  - Create
                  - Access
                  - Grant
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
            /v20180820/accessgrantsinstance:
              GET:
                summary: GetAccessGrantsInstance
                description: >-
                  <p>Retrieves the S3 Access Grants instance for a Region in
                  your account. </p> <dl> <dt>Permissions</dt> <dd> <p>You must
                  have the <code>s3:GetAccessGrantsInstance</code> permission to
                  use this operation. </p> </dd> </dl>
                tags:
                  - Get
                  - Access
                  - Grants
                  - Instances
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
            /v20180820/accessgrantsinstance/location:
              POST:
                summary: CreateAccessGrantsLocation
                description: >-
                  <p>The S3 data location that you would like to register in
                  your S3 Access Grants instance. Your S3 data must be in the
                  same Region as your S3 Access Grants instance. The location
                  can be one of the following: </p> <ul> <li> <p>The default S3
                  location <code>s3://</code> </p> </li> <li> <p>A bucket -
                  <code>S3://&lt;bucket-name&gt;</code> </p> </li> <li> <p>A
                  bucket and prefix -
                  <code>S3://&lt;bucket-name&gt;/&lt;prefix&gt;</code> </p>
                  </li> </ul> <p>When you register a location, you must include
                  the IAM role that has permission to manage the S3 location
                  that you are registering. Give S3 Access Grants permission to
                  assume this role <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/access-grants-location.html">using
                  a policy</a>. S3 Access Grants assumes this role to manage
                  access to the location and to vend temporary credentials to
                  grantees or client applications. </p> <dl>
                  <dt>Permissions</dt> <dd> <p>You must have the
                  <code>s3:CreateAccessGrantsLocation</code> permission to use
                  this operation. </p> </dd> <dt>Additional Permissions</dt>
                  <dd> <p>You must also have the following permission for the
                  specified IAM role: <code>iam:PassRole</code> </p> </dd> </dl>
                tags:
                  - Create
                  - Access
                  - Grants
                  - Locations
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
            /v20180820/accesspoint/{name}:
              GET:
                summary: GetAccessPoint
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Returns configuration information
                  about the specified access point.</p> <p/> <p>All Amazon S3 on
                  Outposts REST API requests for this action require an
                  additional parameter of <code>x-amz-outpost-id</code> to be
                  passed with the request. In addition, you must use an S3 on
                  Outposts endpoint hostname prefix instead of
                  <code>s3-control</code>. For an example of the request syntax
                  for Amazon S3 on Outposts that uses the S3 on Outposts
                  endpoint hostname prefix and the <code>x-amz-outpost-id</code>
                  derived by using the access point ARN, see the <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_GetAccessPoint.html#API_control_GetAccessPoint_Examples">Examples</a>
                  section.</p> <p>The following actions are related to
                  <code>GetAccessPoint</code>:</p> <ul> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_CreateAccessPoint.html">CreateAccessPoint</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_DeleteAccessPoint.html">DeleteAccessPoint</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_ListAccessPoints.html">ListAccessPoints</a>
                  </p> </li> </ul>
                tags:
                  - Get
                  - Access
                  - Points
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
                  - Access Point
                  - Names
            /v20180820/accesspointforobjectlambda/{name}:
              GET:
                summary: GetAccessPointForObjectLambda
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Returns configuration information
                  about the specified Object Lambda Access Point</p> <p>The
                  following actions are related to
                  <code>GetAccessPointForObjectLambda</code>:</p> <ul> <li> <p>
                  <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_CreateAccessPointForObjectLambda.html">CreateAccessPointForObjectLambda</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_DeleteAccessPointForObjectLambda.html">DeleteAccessPointForObjectLambda</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_ListAccessPointsForObjectLambda.html">ListAccessPointsForObjectLambda</a>
                  </p> </li> </ul>
                tags:
                  - Get
                  - Access
                  - Points
                  - For
                  - Objects
                  - Lambda
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
                  - Access Point
                  - Names
                  - Access Point
            /v20180820/bucket/{name}:
              GET:
                summary: GetBucket
                description: >-
                  <note> <p>Gets an Amazon S3 on Outposts bucket. For more
                  information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/S3onOutposts.html">
                  Using Amazon S3 on Outposts</a> in the <i>Amazon S3 User
                  Guide</i>.</p> </note> <p>If you are using an identity other
                  than the root user of the Amazon Web Services account that
                  owns the Outposts bucket, the calling identity must have the
                  <code>s3-outposts:GetBucket</code> permissions on the
                  specified Outposts bucket and belong to the Outposts bucket
                  owner's account in order to use this action. Only users from
                  Outposts bucket owner account with the right permissions can
                  perform actions on an Outposts bucket. </p> <p> If you don't
                  have <code>s3-outposts:GetBucket</code> permissions or you're
                  not using an identity that belongs to the bucket owner's
                  account, Amazon S3 returns a <code>403 Access Denied</code>
                  error.</p> <p>The following actions are related to
                  <code>GetBucket</code> for Amazon S3 on Outposts:</p> <p>All
                  Amazon S3 on Outposts REST API requests for this action
                  require an additional parameter of
                  <code>x-amz-outpost-id</code> to be passed with the request.
                  In addition, you must use an S3 on Outposts endpoint hostname
                  prefix instead of <code>s3-control</code>. For an example of
                  the request syntax for Amazon S3 on Outposts that uses the S3
                  on Outposts endpoint hostname prefix and the
                  <code>x-amz-outpost-id</code> derived by using the access
                  point ARN, see the <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_GetBucket.html#API_control_GetBucket_Examples">Examples</a>
                  section.</p> <ul> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_PutObject.html">PutObject</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_CreateBucket.html">CreateBucket</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_DeleteBucket.html">DeleteBucket</a>
                  </p> </li> </ul>
                tags:
                  - Get
                  - Bucket
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
                  - Access Point
                  - Names
                  - Access Point
                  - Bucket
            /v20180820/jobs:
              GET:
                summary: ListJobs
                description: >-
                  <p>Lists current S3 Batch Operations jobs as well as the jobs
                  that have ended within the last 30 days for the Amazon Web
                  Services account making the request. For more information, see
                  <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/batch-ops.html">S3
                  Batch Operations</a> in the <i>Amazon S3 User Guide</i>.</p>
                  <dl> <dt>Permissions</dt> <dd> <p>To use the
                  <code>ListJobs</code> operation, you must have permission to
                  perform the <code>s3:ListJobs</code> action.</p> </dd> </dl>
                  <p>Related actions include:</p> <p/> <ul> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_CreateJob.html">CreateJob</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_DescribeJob.html">DescribeJob</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_UpdateJobPriority.html">UpdateJobPriority</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_UpdateJobStatus.html">UpdateJobStatus</a>
                  </p> </li> </ul>
                tags:
                  - Lists
                  - Jobs
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
                  - Access Point
                  - Names
                  - Access Point
                  - Bucket
                  - Jobs
            /v20180820/async-requests/mrap/create:
              POST:
                summary: CreateMultiRegionAccessPoint
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Creates a Multi-Region Access Point
                  and associates it with the specified buckets. For more
                  information about creating Multi-Region Access Points, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/CreatingMultiRegionAccessPoints.html">Creating
                  Multi-Region Access Points</a> in the <i>Amazon S3 User
                  Guide</i>.</p> <p>This action will always be routed to the US
                  West (Oregon) Region. For more information about the
                  restrictions around managing Multi-Region Access Points, see
                  <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/ManagingMultiRegionAccessPoints.html">Managing
                  Multi-Region Access Points</a> in the <i>Amazon S3 User
                  Guide</i>.</p> <p>This request is asynchronous, meaning that
                  you might receive a response before the command has completed.
                  When this request provides a response, it provides a token
                  that you can use to monitor the status of the request with
                  <code>DescribeMultiRegionAccessPointOperation</code>.</p>
                  <p>The following actions are related to
                  <code>CreateMultiRegionAccessPoint</code>:</p> <ul> <li> <p>
                  <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_DeleteMultiRegionAccessPoint.html">DeleteMultiRegionAccessPoint</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_DescribeMultiRegionAccessPointOperation.html">DescribeMultiRegionAccessPointOperation</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_GetMultiRegionAccessPoint.html">GetMultiRegionAccessPoint</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_ListMultiRegionAccessPoints.html">ListMultiRegionAccessPoints</a>
                  </p> </li> </ul>
                tags:
                  - Create
                  - Multi
                  - Regions
                  - Access
                  - Points
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
                  - Access Point
                  - Names
                  - Access Point
                  - Bucket
                  - Jobs
                  - Async
                  - Requests
                  - Mrap
                  - Create
            /v20180820/storagelensgroup:
              GET:
                summary: ListStorageLensGroups
                description: >-
                  <p> Lists all the Storage Lens groups in the specified home
                  Region. </p> <p>To use this operation, you must have the
                  permission to perform the
                  <code>s3:ListStorageLensGroups</code> action. For more
                  information about the required Storage Lens Groups
                  permissions, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/storage_lens_iam_permissions.html#storage_lens_groups_permissions">Setting
                  account permissions to use S3 Storage Lens groups</a>.</p>
                  <p>For information about Storage Lens groups errors, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/ErrorResponses.html#S3LensErrorCodeList">List
                  of Amazon S3 Storage Lens error codes</a>.</p>
                tags:
                  - Lists
                  - Storage
                  - Lens
                  - Groups
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
                  - Access Point
                  - Names
                  - Access Point
                  - Bucket
                  - Jobs
                  - Async
                  - Requests
                  - Mrap
                  - Create
                  - Storage Lens Groups
            /v20180820/accessgrantsinstance/grant/{id}:
              GET:
                summary: GetAccessGrant
                description: >-
                  <p>Get the details of an access grant from your S3 Access
                  Grants instance.</p> <dl> <dt>Permissions</dt> <dd> <p>You
                  must have the <code>s3:GetAccessGrant</code> permission to use
                  this operation. </p> </dd> </dl>
                tags:
                  - Get
                  - Access
                  - Grant
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
                  - Access Point
                  - Names
                  - Access Point
                  - Bucket
                  - Jobs
                  - Async
                  - Requests
                  - Mrap
                  - Create
                  - Storage Lens Groups
                  - Identifiers
            /v20180820/accessgrantsinstance/resourcepolicy:
              PUT:
                summary: PutAccessGrantsInstanceResourcePolicy
                description: >-
                  <p>Updates the resource policy of the S3 Access Grants
                  instance. </p> <dl> <dt>Permissions</dt> <dd> <p>You must have
                  the <code>s3:PutAccessGrantsInstanceResourcePolicy</code>
                  permission to use this operation. </p> </dd> </dl>
                tags:
                  - Put
                  - Access
                  - Grants
                  - Instances
                  - Resources
                  - Policies
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
                  - Access Point
                  - Names
                  - Access Point
                  - Bucket
                  - Jobs
                  - Async
                  - Requests
                  - Mrap
                  - Create
                  - Storage Lens Groups
                  - Identifiers
                  - Resource Policies
            /v20180820/accessgrantsinstance/location/{id}:
              PUT:
                summary: UpdateAccessGrantsLocation
                description: >-
                  <p>Updates the IAM role of a registered location in your S3
                  Access Grants instance.</p> <dl> <dt>Permissions</dt> <dd>
                  <p>You must have the
                  <code>s3:UpdateAccessGrantsLocation</code> permission to use
                  this operation. </p> </dd> <dt>Additional Permissions</dt>
                  <dd> <p>You must also have the following permission:
                  <code>iam:PassRole</code> </p> </dd> </dl>
                tags:
                  - Update
                  - Access
                  - Grants
                  - Locations
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
                  - Access Point
                  - Names
                  - Access Point
                  - Bucket
                  - Jobs
                  - Async
                  - Requests
                  - Mrap
                  - Create
                  - Storage Lens Groups
                  - Identifiers
                  - Resource Policies
            /v20180820/accesspoint/{name}/policy:
              PUT:
                summary: PutAccessPointPolicy
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Associates an access policy with the
                  specified access point. Each access point can have only one
                  policy, so a request made to this API replaces any existing
                  policy associated with the specified access point.</p> <p/>
                  <p>All Amazon S3 on Outposts REST API requests for this action
                  require an additional parameter of
                  <code>x-amz-outpost-id</code> to be passed with the request.
                  In addition, you must use an S3 on Outposts endpoint hostname
                  prefix instead of <code>s3-control</code>. For an example of
                  the request syntax for Amazon S3 on Outposts that uses the S3
                  on Outposts endpoint hostname prefix and the
                  <code>x-amz-outpost-id</code> derived by using the access
                  point ARN, see the <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_PutAccessPointPolicy.html#API_control_PutAccessPointPolicy_Examples">Examples</a>
                  section.</p> <p>The following actions are related to
                  <code>PutAccessPointPolicy</code>:</p> <ul> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_GetAccessPointPolicy.html">GetAccessPointPolicy</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_DeleteAccessPointPolicy.html">DeleteAccessPointPolicy</a>
                  </p> </li> </ul>
                tags:
                  - Put
                  - Access
                  - Points
                  - Policies
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
                  - Access Point
                  - Names
                  - Access Point
                  - Bucket
                  - Jobs
                  - Async
                  - Requests
                  - Mrap
                  - Create
                  - Storage Lens Groups
                  - Identifiers
                  - Resource Policies
                  - Policies
            /v20180820/accesspointforobjectlambda/{name}/policy:
              PUT:
                summary: PutAccessPointPolicyForObjectLambda
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Creates or replaces resource policy
                  for an Object Lambda Access Point. For an example policy, see
                  <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/olap-create.html#olap-create-cli">Creating
                  Object Lambda Access Points</a> in the <i>Amazon S3 User
                  Guide</i>.</p> <p>The following actions are related to
                  <code>PutAccessPointPolicyForObjectLambda</code>:</p> <ul>
                  <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_DeleteAccessPointPolicyForObjectLambda.html">DeleteAccessPointPolicyForObjectLambda</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_GetAccessPointPolicyForObjectLambda.html">GetAccessPointPolicyForObjectLambda</a>
                  </p> </li> </ul>
                tags:
                  - Put
                  - Access
                  - Points
                  - Policies
                  - For
                  - Objects
                  - Lambda
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
                  - Access Point
                  - Names
                  - Access Point
                  - Bucket
                  - Jobs
                  - Async
                  - Requests
                  - Mrap
                  - Create
                  - Storage Lens Groups
                  - Identifiers
                  - Resource Policies
                  - Policies
            /v20180820/bucket/{name}/lifecycleconfiguration:
              PUT:
                summary: PutBucketLifecycleConfiguration
                description: >-
                  <note> <p>This action puts a lifecycle configuration to an
                  Amazon S3 on Outposts bucket. To put a lifecycle configuration
                  to an S3 bucket, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_PutBucketLifecycleConfiguration.html">PutBucketLifecycleConfiguration</a>
                  in the <i>Amazon S3 API Reference</i>. </p> </note> <p>Creates
                  a new lifecycle configuration for the S3 on Outposts bucket or
                  replaces an existing lifecycle configuration. Outposts buckets
                  only support lifecycle configurations that delete/expire
                  objects after a certain period of time and abort incomplete
                  multipart uploads.</p> <p/> <p>All Amazon S3 on Outposts REST
                  API requests for this action require an additional parameter
                  of <code>x-amz-outpost-id</code> to be passed with the
                  request. In addition, you must use an S3 on Outposts endpoint
                  hostname prefix instead of <code>s3-control</code>. For an
                  example of the request syntax for Amazon S3 on Outposts that
                  uses the S3 on Outposts endpoint hostname prefix and the
                  <code>x-amz-outpost-id</code> derived by using the access
                  point ARN, see the <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_PutBucketLifecycleConfiguration.html#API_control_PutBucketLifecycleConfiguration_Examples">Examples</a>
                  section.</p> <p>The following actions are related to
                  <code>PutBucketLifecycleConfiguration</code>:</p> <ul> <li>
                  <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_GetBucketLifecycleConfiguration.html">GetBucketLifecycleConfiguration</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_DeleteBucketLifecycleConfiguration.html">DeleteBucketLifecycleConfiguration</a>
                  </p> </li> </ul>
                tags:
                  - Put
                  - Bucket
                  - Lifecycle
                  - Configurations
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
                  - Access Point
                  - Names
                  - Access Point
                  - Bucket
                  - Jobs
                  - Async
                  - Requests
                  - Mrap
                  - Create
                  - Storage Lens Groups
                  - Identifiers
                  - Resource Policies
                  - Policies
                  - Lifecycle Configuration
            /v20180820/bucket/{name}/policy:
              PUT:
                summary: PutBucketPolicy
                description: >-
                  <note> <p>This action puts a bucket policy to an Amazon S3 on
                  Outposts bucket. To put a policy on an S3 bucket, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_PutBucketPolicy.html">PutBucketPolicy</a>
                  in the <i>Amazon S3 API Reference</i>. </p> </note> <p>Applies
                  an Amazon S3 bucket policy to an Outposts bucket. For more
                  information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/S3onOutposts.html">Using
                  Amazon S3 on Outposts</a> in the <i>Amazon S3 User
                  Guide</i>.</p> <p>If you are using an identity other than the
                  root user of the Amazon Web Services account that owns the
                  Outposts bucket, the calling identity must have the
                  <code>PutBucketPolicy</code> permissions on the specified
                  Outposts bucket and belong to the bucket owner's account in
                  order to use this action.</p> <p>If you don't have
                  <code>PutBucketPolicy</code> permissions, Amazon S3 returns a
                  <code>403 Access Denied</code> error. If you have the correct
                  permissions, but you're not using an identity that belongs to
                  the bucket owner's account, Amazon S3 returns a <code>405
                  Method Not Allowed</code> error.</p> <important> <p> As a
                  security precaution, the root user of the Amazon Web Services
                  account that owns a bucket can always use this action, even if
                  the policy explicitly denies the root user the ability to
                  perform this action. </p> </important> <p>For more information
                  about bucket policies, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/using-iam-policies.html">Using
                  Bucket Policies and User Policies</a>.</p> <p>All Amazon S3 on
                  Outposts REST API requests for this action require an
                  additional parameter of <code>x-amz-outpost-id</code> to be
                  passed with the request. In addition, you must use an S3 on
                  Outposts endpoint hostname prefix instead of
                  <code>s3-control</code>. For an example of the request syntax
                  for Amazon S3 on Outposts that uses the S3 on Outposts
                  endpoint hostname prefix and the <code>x-amz-outpost-id</code>
                  derived by using the access point ARN, see the <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_PutBucketPolicy.html#API_control_PutBucketPolicy_Examples">Examples</a>
                  section.</p> <p>The following actions are related to
                  <code>PutBucketPolicy</code>:</p> <ul> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_GetBucketPolicy.html">GetBucketPolicy</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_DeleteBucketPolicy.html">DeleteBucketPolicy</a>
                  </p> </li> </ul>
                tags:
                  - Put
                  - Bucket
                  - Policies
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
                  - Access Point
                  - Names
                  - Access Point
                  - Bucket
                  - Jobs
                  - Async
                  - Requests
                  - Mrap
                  - Create
                  - Storage Lens Groups
                  - Identifiers
                  - Resource Policies
                  - Policies
                  - Lifecycle Configuration
            /v20180820/bucket/{name}/replication:
              PUT:
                summary: PutBucketReplication
                description: >-
                  <note> <p>This action creates an Amazon S3 on Outposts
                  bucket's replication configuration. To create an S3 bucket's
                  replication configuration, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_PutBucketReplication.html">PutBucketReplication</a>
                  in the <i>Amazon S3 API Reference</i>. </p> </note> <p>Creates
                  a replication configuration or replaces an existing one. For
                  information about S3 replication on Outposts configuration,
                  see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/S3OutpostsReplication.html">Replicating
                  objects for S3 on Outposts</a> in the <i>Amazon S3 User
                  Guide</i>.</p> <note> <p>It can take a while to propagate
                  <code>PUT</code> or <code>DELETE</code> requests for a
                  replication configuration to all S3 on Outposts systems.
                  Therefore, the replication configuration that's returned by a
                  <code>GET</code> request soon after a <code>PUT</code> or
                  <code>DELETE</code> request might return a more recent result
                  than what's on the Outpost. If an Outpost is offline, the
                  delay in updating the replication configuration on that
                  Outpost can be significant.</p> </note> <p>Specify the
                  replication configuration in the request body. In the
                  replication configuration, you provide the following
                  information:</p> <ul> <li> <p>The name of the destination
                  bucket or buckets where you want S3 on Outposts to replicate
                  objects</p> </li> <li> <p>The Identity and Access Management
                  (IAM) role that S3 on Outposts can assume to replicate objects
                  on your behalf</p> </li> <li> <p>Other relevant information,
                  such as replication rules</p> </li> </ul> <p>A replication
                  configuration must include at least one rule and can contain a
                  maximum of 100. Each rule identifies a subset of objects to
                  replicate by filtering the objects in the source Outposts
                  bucket. To choose additional subsets of objects to replicate,
                  add a rule for each subset.</p> <p>To specify a subset of the
                  objects in the source Outposts bucket to apply a replication
                  rule to, add the <code>Filter</code> element as a child of the
                  <code>Rule</code> element. You can filter objects based on an
                  object key prefix, one or more object tags, or both. When you
                  add the <code>Filter</code> element in the configuration, you
                  must also add the following elements:
                  <code>DeleteMarkerReplication</code>, <code>Status</code>, and
                  <code>Priority</code>.</p> <p>Using
                  <code>PutBucketReplication</code> on Outposts requires that
                  both the source and destination buckets must have versioning
                  enabled. For information about enabling versioning on a
                  bucket, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/S3OutpostsManagingVersioning.html">Managing
                  S3 Versioning for your S3 on Outposts bucket</a>.</p> <p>For
                  information about S3 on Outposts replication failure reasons,
                  see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/outposts-replication-eventbridge.html#outposts-replication-failure-codes">Replication
                  failure reasons</a> in the <i>Amazon S3 User Guide</i>.</p>
                  <p> <b>Handling Replication of Encrypted Objects</b> </p>
                  <p>Outposts buckets are encrypted at all times. All the
                  objects in the source Outposts bucket are encrypted and can be
                  replicated. Also, all the replicas in the destination Outposts
                  bucket are encrypted with the same encryption key as the
                  objects in the source Outposts bucket.</p> <p>
                  <b>Permissions</b> </p> <p>To create a
                  <code>PutBucketReplication</code> request, you must have
                  <code>s3-outposts:PutReplicationConfiguration</code>
                  permissions for the bucket. The Outposts bucket owner has this
                  permission by default and can grant it to others. For more
                  information about permissions, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/S3OutpostsIAM.html">Setting
                  up IAM with S3 on Outposts</a> and <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/S3OutpostsBucketPolicy.html">Managing
                  access to S3 on Outposts buckets</a>. </p> <note> <p>To
                  perform this operation, the user or role must also have the
                  <code>iam:CreateRole</code> and <code>iam:PassRole</code>
                  permissions. For more information, see <a
                  href="https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_use_passrole.html">Granting
                  a user permissions to pass a role to an Amazon Web Services
                  service</a>.</p> </note> <p>All Amazon S3 on Outposts REST API
                  requests for this action require an additional parameter of
                  <code>x-amz-outpost-id</code> to be passed with the request.
                  In addition, you must use an S3 on Outposts endpoint hostname
                  prefix instead of <code>s3-control</code>. For an example of
                  the request syntax for Amazon S3 on Outposts that uses the S3
                  on Outposts endpoint hostname prefix and the
                  <code>x-amz-outpost-id</code> derived by using the access
                  point ARN, see the <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_PutBucketReplication.html#API_control_PutBucketReplication_Examples">Examples</a>
                  section.</p> <p>The following operations are related to
                  <code>PutBucketReplication</code>:</p> <ul> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_GetBucketReplication.html">GetBucketReplication</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_DeleteBucketReplication.html">DeleteBucketReplication</a>
                  </p> </li> </ul>
                tags:
                  - Put
                  - Bucket
                  - Replication
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
                  - Access Point
                  - Names
                  - Access Point
                  - Bucket
                  - Jobs
                  - Async
                  - Requests
                  - Mrap
                  - Create
                  - Storage Lens Groups
                  - Identifiers
                  - Resource Policies
                  - Policies
                  - Lifecycle Configuration
                  - Replication
            /v20180820/bucket/{name}/tagging:
              PUT:
                summary: PutBucketTagging
                description: >-
                  <note> <p>This action puts tags on an Amazon S3 on Outposts
                  bucket. To put tags on an S3 bucket, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_PutBucketTagging.html">PutBucketTagging</a>
                  in the <i>Amazon S3 API Reference</i>. </p> </note> <p>Sets
                  the tags for an S3 on Outposts bucket. For more information,
                  see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/S3onOutposts.html">Using
                  Amazon S3 on Outposts</a> in the <i>Amazon S3 User
                  Guide</i>.</p> <p>Use tags to organize your Amazon Web
                  Services bill to reflect your own cost structure. To do this,
                  sign up to get your Amazon Web Services account bill with tag
                  key values included. Then, to see the cost of combined
                  resources, organize your billing information according to
                  resources with the same tag key values. For example, you can
                  tag several resources with a specific application name, and
                  then organize your billing information to see the total cost
                  of that application across several services. For more
                  information, see <a
                  href="https://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/cost-alloc-tags.html">Cost
                  allocation and tagging</a>.</p> <note> <p>Within a bucket, if
                  you add a tag that has the same key as an existing tag, the
                  new value overwrites the old value. For more information, see
                  <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/CostAllocTagging.html">
                  Using cost allocation in Amazon S3 bucket tags</a>.</p>
                  </note> <p>To use this action, you must have permissions to
                  perform the <code>s3-outposts:PutBucketTagging</code> action.
                  The Outposts bucket owner has this permission by default and
                  can grant this permission to others. For more information
                  about permissions, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/using-with-s3-actions.html#using-with-s3-actions-related-to-bucket-subresources">
                  Permissions Related to Bucket Subresource Operations</a> and
                  <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/s3-access-control.html">Managing
                  access permissions to your Amazon S3 resources</a>.</p> <p>
                  <code>PutBucketTagging</code> has the following special
                  errors:</p> <ul> <li> <p>Error code:
                  <code>InvalidTagError</code> </p> <ul> <li> <p>Description:
                  The tag provided was not a valid tag. This error can occur if
                  the tag did not pass input validation. For information about
                  tag restrictions, see <a
                  href="https://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/allocation-tag-restrictions.html">
                  User-Defined Tag Restrictions</a> and <a
                  href="https://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/aws-tag-restrictions.html">
                  Amazon Web Services-Generated Cost Allocation Tag
                  Restrictions</a>.</p> </li> </ul> </li> <li> <p>Error code:
                  <code>MalformedXMLError</code> </p> <ul> <li> <p>Description:
                  The XML provided does not match the schema.</p> </li> </ul>
                  </li> <li> <p>Error code: <code>OperationAbortedError </code>
                  </p> <ul> <li> <p>Description: A conflicting conditional
                  action is currently in progress against this resource. Try
                  again.</p> </li> </ul> </li> <li> <p>Error code:
                  <code>InternalError</code> </p> <ul> <li> <p>Description: The
                  service was unable to apply the provided tag to the
                  bucket.</p> </li> </ul> </li> </ul> <p>All Amazon S3 on
                  Outposts REST API requests for this action require an
                  additional parameter of <code>x-amz-outpost-id</code> to be
                  passed with the request. In addition, you must use an S3 on
                  Outposts endpoint hostname prefix instead of
                  <code>s3-control</code>. For an example of the request syntax
                  for Amazon S3 on Outposts that uses the S3 on Outposts
                  endpoint hostname prefix and the <code>x-amz-outpost-id</code>
                  derived by using the access point ARN, see the <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_PutBucketTagging.html#API_control_PutBucketTagging_Examples">Examples</a>
                  section.</p> <p>The following actions are related to
                  <code>PutBucketTagging</code>:</p> <ul> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_GetBucketTagging.html">GetBucketTagging</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_DeleteBucketTagging.html">DeleteBucketTagging</a>
                  </p> </li> </ul>
                tags:
                  - Put
                  - Bucket
                  - Tagging
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
                  - Access Point
                  - Names
                  - Access Point
                  - Bucket
                  - Jobs
                  - Async
                  - Requests
                  - Mrap
                  - Create
                  - Storage Lens Groups
                  - Identifiers
                  - Resource Policies
                  - Policies
                  - Lifecycle Configuration
                  - Replication
                  - Tagging
            /v20180820/jobs/{id}/tagging:
              PUT:
                summary: PutJobTagging
                description: >-
                  <p>Sets the supplied tag-set on an S3 Batch Operations
                  job.</p> <p>A tag is a key-value pair. You can associate S3
                  Batch Operations tags with any job by sending a PUT request
                  against the tagging subresource that is associated with the
                  job. To modify the existing tag set, you can either replace
                  the existing tag set entirely, or make changes within the
                  existing tag set by retrieving the existing tag set using <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_GetJobTagging.html">GetJobTagging</a>,
                  modify that tag set, and use this operation to replace the tag
                  set with the one you modified. For more information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/batch-ops-managing-jobs.html#batch-ops-job-tags">Controlling
                  access and labeling jobs using tags</a> in the <i>Amazon S3
                  User Guide</i>. </p> <note> <ul> <li> <p>If you send this
                  request with an empty tag set, Amazon S3 deletes the existing
                  tag set on the Batch Operations job. If you use this method,
                  you are charged for a Tier 1 Request (PUT). For more
                  information, see <a
                  href="http://aws.amazon.com/s3/pricing/">Amazon S3
                  pricing</a>.</p> </li> <li> <p>For deleting existing tags for
                  your Batch Operations job, a <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_DeleteJobTagging.html">DeleteJobTagging</a>
                  request is preferred because it achieves the same result
                  without incurring charges.</p> </li> <li> <p>A few things to
                  consider about using tags:</p> <ul> <li> <p>Amazon S3 limits
                  the maximum number of tags to 50 tags per job.</p> </li> <li>
                  <p>You can associate up to 50 tags with a job as long as they
                  have unique tag keys.</p> </li> <li> <p>A tag key can be up to
                  128 Unicode characters in length, and tag values can be up to
                  256 Unicode characters in length.</p> </li> <li> <p>The key
                  and values are case sensitive.</p> </li> <li> <p>For
                  tagging-related restrictions related to characters and
                  encodings, see <a
                  href="https://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/allocation-tag-restrictions.html">User-Defined
                  Tag Restrictions</a> in the <i>Billing and Cost Management
                  User Guide</i>.</p> </li> </ul> </li> </ul> </note> <dl>
                  <dt>Permissions</dt> <dd> <p>To use the
                  <code>PutJobTagging</code> operation, you must have permission
                  to perform the <code>s3:PutJobTagging</code> action.</p> </dd>
                  </dl> <p>Related actions include:</p> <ul> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_CreateJob.html">CreateJob</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_GetJobTagging.html">GetJobTagging</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_DeleteJobTagging.html">DeleteJobTagging</a>
                  </p> </li> </ul>
                tags:
                  - Put
                  - Jobs
                  - Tagging
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
                  - Access Point
                  - Names
                  - Access Point
                  - Bucket
                  - Jobs
                  - Async
                  - Requests
                  - Mrap
                  - Create
                  - Storage Lens Groups
                  - Identifiers
                  - Resource Policies
                  - Policies
                  - Lifecycle Configuration
                  - Replication
                  - Tagging
            /v20180820/async-requests/mrap/delete:
              POST:
                summary: DeleteMultiRegionAccessPoint
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Deletes a Multi-Region Access Point.
                  This action does not delete the buckets associated with the
                  Multi-Region Access Point, only the Multi-Region Access Point
                  itself.</p> <p>This action will always be routed to the US
                  West (Oregon) Region. For more information about the
                  restrictions around managing Multi-Region Access Points, see
                  <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/ManagingMultiRegionAccessPoints.html">Managing
                  Multi-Region Access Points</a> in the <i>Amazon S3 User
                  Guide</i>.</p> <p>This request is asynchronous, meaning that
                  you might receive a response before the command has completed.
                  When this request provides a response, it provides a token
                  that you can use to monitor the status of the request with
                  <code>DescribeMultiRegionAccessPointOperation</code>.</p>
                  <p>The following actions are related to
                  <code>DeleteMultiRegionAccessPoint</code>:</p> <ul> <li> <p>
                  <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_CreateMultiRegionAccessPoint.html">CreateMultiRegionAccessPoint</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_DescribeMultiRegionAccessPointOperation.html">DescribeMultiRegionAccessPointOperation</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_GetMultiRegionAccessPoint.html">GetMultiRegionAccessPoint</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_ListMultiRegionAccessPoints.html">ListMultiRegionAccessPoints</a>
                  </p> </li> </ul>
                tags:
                  - Delete
                  - Multi
                  - Regions
                  - Access
                  - Points
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
                  - Access Point
                  - Names
                  - Access Point
                  - Bucket
                  - Jobs
                  - Async
                  - Requests
                  - Mrap
                  - Create
                  - Storage Lens Groups
                  - Identifiers
                  - Resource Policies
                  - Policies
                  - Lifecycle Configuration
                  - Replication
                  - Tagging
                  - Delete
            /v20180820/configuration/publicAccessBlock:
              PUT:
                summary: PutPublicAccessBlock
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Creates or modifies the
                  <code>PublicAccessBlock</code> configuration for an Amazon Web
                  Services account. For this operation, users must have the
                  <code>s3:PutAccountPublicAccessBlock</code> permission. For
                  more information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/access-control-block-public-access.html">
                  Using Amazon S3 block public access</a>.</p> <p>Related
                  actions include:</p> <ul> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_GetPublicAccessBlock.html">GetPublicAccessBlock</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_DeletePublicAccessBlock.html">DeletePublicAccessBlock</a>
                  </p> </li> </ul>
                tags:
                  - Put
                  - Public
                  - Access
                  - Blocks
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
                  - Access Point
                  - Names
                  - Access Point
                  - Bucket
                  - Jobs
                  - Async
                  - Requests
                  - Mrap
                  - Create
                  - Storage Lens Groups
                  - Identifiers
                  - Resource Policies
                  - Policies
                  - Lifecycle Configuration
                  - Replication
                  - Tagging
                  - Delete
                  - Access
                  - Blocks
            /v20180820/storagelens/{storagelensid}:
              PUT:
                summary: PutStorageLensConfiguration
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Puts an Amazon S3 Storage Lens
                  configuration. For more information about S3 Storage Lens, see
                  <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/storage_lens.html">Working
                  with Amazon S3 Storage Lens</a> in the <i>Amazon S3 User
                  Guide</i>. For a complete list of S3 Storage Lens metrics, see
                  <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/storage_lens_metrics_glossary.html">S3
                  Storage Lens metrics glossary</a> in the <i>Amazon S3 User
                  Guide</i>.</p> <note> <p>To use this action, you must have
                  permission to perform the
                  <code>s3:PutStorageLensConfiguration</code> action. For more
                  information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/storage_lens_iam_permissions.html">Setting
                  permissions to use Amazon S3 Storage Lens</a> in the <i>Amazon
                  S3 User Guide</i>.</p> </note>
                tags:
                  - Put
                  - Storage
                  - Lens
                  - Configurations
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
                  - Access Point
                  - Names
                  - Access Point
                  - Bucket
                  - Jobs
                  - Async
                  - Requests
                  - Mrap
                  - Create
                  - Storage Lens Groups
                  - Identifiers
                  - Resource Policies
                  - Policies
                  - Lifecycle Configuration
                  - Replication
                  - Tagging
                  - Delete
                  - Access
                  - Blocks
                  - Storage Lens
                  - Storage Lens
            /v20180820/storagelens/{storagelensid}/tagging:
              PUT:
                summary: PutStorageLensConfigurationTagging
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Put or replace tags on an existing
                  Amazon S3 Storage Lens configuration. For more information
                  about S3 Storage Lens, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/storage_lens.html">Assessing
                  your storage activity and usage with Amazon S3 Storage Lens
                  </a> in the <i>Amazon S3 User Guide</i>.</p> <note> <p>To use
                  this action, you must have permission to perform the
                  <code>s3:PutStorageLensConfigurationTagging</code> action. For
                  more information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/storage_lens_iam_permissions.html">Setting
                  permissions to use Amazon S3 Storage Lens</a> in the <i>Amazon
                  S3 User Guide</i>.</p> </note>
                tags:
                  - Put
                  - Storage
                  - Lens
                  - Configurations
                  - Tagging
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
                  - Access Point
                  - Names
                  - Access Point
                  - Bucket
                  - Jobs
                  - Async
                  - Requests
                  - Mrap
                  - Create
                  - Storage Lens Groups
                  - Identifiers
                  - Resource Policies
                  - Policies
                  - Lifecycle Configuration
                  - Replication
                  - Tagging
                  - Delete
                  - Access
                  - Blocks
                  - Storage Lens
                  - Storage Lens
            /v20180820/storagelensgroup/{name}:
              PUT:
                summary: UpdateStorageLensGroup
                description: >-
                  <p> Updates the existing Storage Lens group.</p> <p>To use
                  this operation, you must have the permission to perform the
                  <code>s3:UpdateStorageLensGroup</code> action. For more
                  information about the required Storage Lens Groups
                  permissions, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/storage_lens_iam_permissions.html#storage_lens_groups_permissions">Setting
                  account permissions to use S3 Storage Lens groups</a>.</p>
                  <p>For information about Storage Lens groups errors, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/ErrorResponses.html#S3LensErrorCodeList">List
                  of Amazon S3 Storage Lens error codes</a>.</p>
                tags:
                  - Update
                  - Storage
                  - Lens
                  - Group
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
                  - Access Point
                  - Names
                  - Access Point
                  - Bucket
                  - Jobs
                  - Async
                  - Requests
                  - Mrap
                  - Create
                  - Storage Lens Groups
                  - Identifiers
                  - Resource Policies
                  - Policies
                  - Lifecycle Configuration
                  - Replication
                  - Tagging
                  - Delete
                  - Access
                  - Blocks
                  - Storage Lens
                  - Storage Lens
            /v20180820/jobs/{id}:
              GET:
                summary: DescribeJob
                description: >-
                  <p>Retrieves the configuration parameters and status for a
                  Batch Operations job. For more information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/batch-ops.html">S3
                  Batch Operations</a> in the <i>Amazon S3 User Guide</i>.</p>
                  <dl> <dt>Permissions</dt> <dd> <p>To use the
                  <code>DescribeJob</code> operation, you must have permission
                  to perform the <code>s3:DescribeJob</code> action.</p> </dd>
                  </dl> <p>Related actions include:</p> <ul> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_CreateJob.html">CreateJob</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_ListJobs.html">ListJobs</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_UpdateJobPriority.html">UpdateJobPriority</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_UpdateJobStatus.html">UpdateJobStatus</a>
                  </p> </li> </ul>
                tags:
                  - Describe
                  - Jobs
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
                  - Access Point
                  - Names
                  - Access Point
                  - Bucket
                  - Jobs
                  - Async
                  - Requests
                  - Mrap
                  - Create
                  - Storage Lens Groups
                  - Identifiers
                  - Resource Policies
                  - Policies
                  - Lifecycle Configuration
                  - Replication
                  - Tagging
                  - Delete
                  - Access
                  - Blocks
                  - Storage Lens
                  - Storage Lens
            /v20180820/async-requests/mrap/{request_token+}:
              GET:
                summary: DescribeMultiRegionAccessPointOperation
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Retrieves the status of an
                  asynchronous request to manage a Multi-Region Access Point.
                  For more information about managing Multi-Region Access Points
                  and how asynchronous requests work, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/ManagingMultiRegionAccessPoints.html">Managing
                  Multi-Region Access Points</a> in the <i>Amazon S3 User
                  Guide</i>.</p> <p>The following actions are related to
                  <code>GetMultiRegionAccessPoint</code>:</p> <ul> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_CreateMultiRegionAccessPoint.html">CreateMultiRegionAccessPoint</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_DeleteMultiRegionAccessPoint.html">DeleteMultiRegionAccessPoint</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_GetMultiRegionAccessPoint.html">GetMultiRegionAccessPoint</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_ListMultiRegionAccessPoints.html">ListMultiRegionAccessPoints</a>
                  </p> </li> </ul>
                tags:
                  - Describe
                  - Multi
                  - Regions
                  - Access
                  - Points
                  - Operation
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
                  - Access Point
                  - Names
                  - Access Point
                  - Bucket
                  - Jobs
                  - Async
                  - Requests
                  - Mrap
                  - Create
                  - Storage Lens Groups
                  - Identifiers
                  - Resource Policies
                  - Policies
                  - Lifecycle Configuration
                  - Replication
                  - Tagging
                  - Delete
                  - Access
                  - Blocks
                  - Storage Lens
                  - Storage Lens
                  - Request_token+
            /v20180820/accessgrantsinstance/prefix:
              GET:
                summary: GetAccessGrantsInstanceForPrefix
                description: >-
                  <p>Retrieve the S3 Access Grants instance that contains a
                  particular prefix. </p> <dl> <dt>Permissions</dt> <dd> <p>You
                  must have the <code>s3:GetAccessGrantsInstanceForPrefix</code>
                  permission for the caller account to use this operation. </p>
                  </dd> <dt>Additional Permissions</dt> <dd> <p>The prefix owner
                  account must grant you the following permissions to their S3
                  Access Grants instance:
                  <code>s3:GetAccessGrantsInstanceForPrefix</code>. </p> </dd>
                  </dl>
                tags:
                  - Get
                  - Access
                  - Grants
                  - Instances
                  - For
                  - Prefix
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
                  - Access Point
                  - Names
                  - Access Point
                  - Bucket
                  - Jobs
                  - Async
                  - Requests
                  - Mrap
                  - Create
                  - Storage Lens Groups
                  - Identifiers
                  - Resource Policies
                  - Policies
                  - Lifecycle Configuration
                  - Replication
                  - Tagging
                  - Delete
                  - Access
                  - Blocks
                  - Storage Lens
                  - Storage Lens
                  - Request_token+
                  - Prefix
            /v20180820/accesspointforobjectlambda/{name}/configuration:
              PUT:
                summary: PutAccessPointConfigurationForObjectLambda
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Replaces configuration for an Object
                  Lambda Access Point.</p> <p>The following actions are related
                  to
                  <code>PutAccessPointConfigurationForObjectLambda</code>:</p>
                  <ul> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_GetAccessPointConfigurationForObjectLambda.html">GetAccessPointConfigurationForObjectLambda</a>
                  </p> </li> </ul>
                tags:
                  - Put
                  - Access
                  - Points
                  - Configurations
                  - For
                  - Objects
                  - Lambda
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
                  - Access Point
                  - Names
                  - Access Point
                  - Bucket
                  - Jobs
                  - Async
                  - Requests
                  - Mrap
                  - Create
                  - Storage Lens Groups
                  - Identifiers
                  - Resource Policies
                  - Policies
                  - Lifecycle Configuration
                  - Replication
                  - Tagging
                  - Delete
                  - Access
                  - Blocks
                  - Storage Lens
                  - Storage Lens
                  - Request_token+
                  - Prefix
                  - Configurations
            /v20180820/accesspoint/{name}/policyStatus:
              GET:
                summary: GetAccessPointPolicyStatus
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Indicates whether the specified access
                  point currently has a policy that allows public access. For
                  more information about public access through access points,
                  see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/access-points.html">Managing
                  Data Access with Amazon S3 access points</a> in the <i>Amazon
                  S3 User Guide</i>.</p>
                tags:
                  - Get
                  - Access
                  - Points
                  - Policies
                  - Status
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
                  - Access Point
                  - Names
                  - Access Point
                  - Bucket
                  - Jobs
                  - Async
                  - Requests
                  - Mrap
                  - Create
                  - Storage Lens Groups
                  - Identifiers
                  - Resource Policies
                  - Policies
                  - Lifecycle Configuration
                  - Replication
                  - Tagging
                  - Delete
                  - Access
                  - Blocks
                  - Storage Lens
                  - Storage Lens
                  - Request_token+
                  - Prefix
                  - Configurations
                  - Status
            /v20180820/accesspointforobjectlambda/{name}/policyStatus:
              GET:
                summary: GetAccessPointPolicyStatusForObjectLambda
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Returns the status of the resource
                  policy associated with an Object Lambda Access Point.</p>
                tags:
                  - Get
                  - Access
                  - Points
                  - Policies
                  - Status
                  - For
                  - Objects
                  - Lambda
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
                  - Access Point
                  - Names
                  - Access Point
                  - Bucket
                  - Jobs
                  - Async
                  - Requests
                  - Mrap
                  - Create
                  - Storage Lens Groups
                  - Identifiers
                  - Resource Policies
                  - Policies
                  - Lifecycle Configuration
                  - Replication
                  - Tagging
                  - Delete
                  - Access
                  - Blocks
                  - Storage Lens
                  - Storage Lens
                  - Request_token+
                  - Prefix
                  - Configurations
                  - Status
            /v20180820/bucket/{name}/versioning:
              PUT:
                summary: PutBucketVersioning
                description: >-
                  <note> <p>This operation sets the versioning state for S3 on
                  Outposts buckets only. To set the versioning state for an S3
                  bucket, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_PutBucketVersioning.html">PutBucketVersioning</a>
                  in the <i>Amazon S3 API Reference</i>. </p> </note> <p>Sets
                  the versioning state for an S3 on Outposts bucket. With S3
                  Versioning, you can save multiple distinct copies of your
                  objects and recover from unintended user actions and
                  application failures.</p> <p>You can set the versioning state
                  to one of the following:</p> <ul> <li> <p> <b>Enabled</b> -
                  Enables versioning for the objects in the bucket. All objects
                  added to the bucket receive a unique version ID.</p> </li>
                  <li> <p> <b>Suspended</b> - Suspends versioning for the
                  objects in the bucket. All objects added to the bucket receive
                  the version ID <code>null</code>.</p> </li> </ul> <p>If you've
                  never set versioning on your bucket, it has no versioning
                  state. In that case, a <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_GetBucketVersioning.html">
                  GetBucketVersioning</a> request does not return a versioning
                  state value.</p> <p>When you enable S3 Versioning, for each
                  object in your bucket, you have a current version and zero or
                  more noncurrent versions. You can configure your bucket S3
                  Lifecycle rules to expire noncurrent versions after a
                  specified time period. For more information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/S3OutpostsLifecycleManaging.html">
                  Creating and managing a lifecycle configuration for your S3 on
                  Outposts bucket</a> in the <i>Amazon S3 User Guide</i>.</p>
                  <p>If you have an object expiration lifecycle configuration in
                  your non-versioned bucket and you want to maintain the same
                  permanent delete behavior when you enable versioning, you must
                  add a noncurrent expiration policy. The noncurrent expiration
                  lifecycle configuration will manage the deletes of the
                  noncurrent object versions in the version-enabled bucket. For
                  more information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/Versioning.html">Versioning</a>
                  in the <i>Amazon S3 User Guide</i>.</p> <p>All Amazon S3 on
                  Outposts REST API requests for this action require an
                  additional parameter of <code>x-amz-outpost-id</code> to be
                  passed with the request. In addition, you must use an S3 on
                  Outposts endpoint hostname prefix instead of
                  <code>s3-control</code>. For an example of the request syntax
                  for Amazon S3 on Outposts that uses the S3 on Outposts
                  endpoint hostname prefix and the <code>x-amz-outpost-id</code>
                  derived by using the access point ARN, see the <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_PutBucketVersioning.html#API_control_PutBucketVersioning_Examples">Examples</a>
                  section.</p> <p>The following operations are related to
                  <code>PutBucketVersioning</code> for S3 on Outposts.</p> <ul>
                  <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_GetBucketVersioning.html">GetBucketVersioning</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_PutBucketLifecycleConfiguration.html">PutBucketLifecycleConfiguration</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_GetBucketLifecycleConfiguration.html">GetBucketLifecycleConfiguration</a>
                  </p> </li> </ul>
                tags:
                  - Put
                  - Bucket
                  - Versioning
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
                  - Access Point
                  - Names
                  - Access Point
                  - Bucket
                  - Jobs
                  - Async
                  - Requests
                  - Mrap
                  - Create
                  - Storage Lens Groups
                  - Identifiers
                  - Resource Policies
                  - Policies
                  - Lifecycle Configuration
                  - Replication
                  - Tagging
                  - Delete
                  - Access
                  - Blocks
                  - Storage Lens
                  - Storage Lens
                  - Request_token+
                  - Prefix
                  - Configurations
                  - Status
                  - Versioning
            /v20180820/accessgrantsinstance/dataaccess:
              GET:
                summary: GetDataAccess
                description: >-
                  <p>Returns a temporary access credential from S3 Access Grants
                  to the grantee or client application. The <a
                  href="https://docs.aws.amazon.com/STS/latest/APIReference/API_Credentials.html">temporary
                  credential</a> is an Amazon Web Services STS token that grants
                  them access to the S3 data. </p> <dl> <dt>Permissions</dt>
                  <dd> <p>You must have the <code>s3:GetDataAccess</code>
                  permission to use this operation. </p> </dd> <dt>Additional
                  Permissions</dt> <dd> <p>The IAM role that S3 Access Grants
                  assumes must have the following permissions specified in the
                  trust policy when registering the location:
                  <code>sts:AssumeRole</code>, for directory users or groups
                  <code>sts:SetContext</code>, and for IAM users or roles
                  <code>sts:SourceIdentity</code>. </p> </dd> </dl>
                tags:
                  - Get
                  - Data
                  - Access
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
                  - Access Point
                  - Names
                  - Access Point
                  - Bucket
                  - Jobs
                  - Async
                  - Requests
                  - Mrap
                  - Create
                  - Storage Lens Groups
                  - Identifiers
                  - Resource Policies
                  - Policies
                  - Lifecycle Configuration
                  - Replication
                  - Tagging
                  - Delete
                  - Access
                  - Blocks
                  - Storage Lens
                  - Storage Lens
                  - Request_token+
                  - Prefix
                  - Configurations
                  - Status
                  - Versioning
                  - Data Access
            /v20180820/mrap/instances/{name+}:
              GET:
                summary: GetMultiRegionAccessPoint
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Returns configuration information
                  about the specified Multi-Region Access Point.</p> <p>This
                  action will always be routed to the US West (Oregon) Region.
                  For more information about the restrictions around managing
                  Multi-Region Access Points, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/ManagingMultiRegionAccessPoints.html">Managing
                  Multi-Region Access Points</a> in the <i>Amazon S3 User
                  Guide</i>.</p> <p>The following actions are related to
                  <code>GetMultiRegionAccessPoint</code>:</p> <ul> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_CreateMultiRegionAccessPoint.html">CreateMultiRegionAccessPoint</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_DeleteMultiRegionAccessPoint.html">DeleteMultiRegionAccessPoint</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_DescribeMultiRegionAccessPointOperation.html">DescribeMultiRegionAccessPointOperation</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_ListMultiRegionAccessPoints.html">ListMultiRegionAccessPoints</a>
                  </p> </li> </ul>
                tags:
                  - Get
                  - Multi
                  - Regions
                  - Access
                  - Points
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
                  - Access Point
                  - Names
                  - Access Point
                  - Bucket
                  - Jobs
                  - Async
                  - Requests
                  - Mrap
                  - Create
                  - Storage Lens Groups
                  - Identifiers
                  - Resource Policies
                  - Policies
                  - Lifecycle Configuration
                  - Replication
                  - Tagging
                  - Delete
                  - Access
                  - Blocks
                  - Storage Lens
                  - Storage Lens
                  - Request_token+
                  - Prefix
                  - Configurations
                  - Status
                  - Versioning
                  - Data Access
                  - Instances
                  - Names
            /v20180820/mrap/instances/{name+}/policy:
              GET:
                summary: GetMultiRegionAccessPointPolicy
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Returns the access control policy of
                  the specified Multi-Region Access Point.</p> <p>This action
                  will always be routed to the US West (Oregon) Region. For more
                  information about the restrictions around managing
                  Multi-Region Access Points, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/ManagingMultiRegionAccessPoints.html">Managing
                  Multi-Region Access Points</a> in the <i>Amazon S3 User
                  Guide</i>.</p> <p>The following actions are related to
                  <code>GetMultiRegionAccessPointPolicy</code>:</p> <ul> <li>
                  <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_GetMultiRegionAccessPointPolicyStatus.html">GetMultiRegionAccessPointPolicyStatus</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_PutMultiRegionAccessPointPolicy.html">PutMultiRegionAccessPointPolicy</a>
                  </p> </li> </ul>
                tags:
                  - Get
                  - Multi
                  - Regions
                  - Access
                  - Points
                  - Policies
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
                  - Access Point
                  - Names
                  - Access Point
                  - Bucket
                  - Jobs
                  - Async
                  - Requests
                  - Mrap
                  - Create
                  - Storage Lens Groups
                  - Identifiers
                  - Resource Policies
                  - Policies
                  - Lifecycle Configuration
                  - Replication
                  - Tagging
                  - Delete
                  - Access
                  - Blocks
                  - Storage Lens
                  - Storage Lens
                  - Request_token+
                  - Prefix
                  - Configurations
                  - Status
                  - Versioning
                  - Data Access
                  - Instances
                  - Names
            /v20180820/mrap/instances/{name+}/policystatus:
              GET:
                summary: GetMultiRegionAccessPointPolicyStatus
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Indicates whether the specified
                  Multi-Region Access Point has an access control policy that
                  allows public access.</p> <p>This action will always be routed
                  to the US West (Oregon) Region. For more information about the
                  restrictions around managing Multi-Region Access Points, see
                  <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/ManagingMultiRegionAccessPoints.html">Managing
                  Multi-Region Access Points</a> in the <i>Amazon S3 User
                  Guide</i>.</p> <p>The following actions are related to
                  <code>GetMultiRegionAccessPointPolicyStatus</code>:</p> <ul>
                  <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_GetMultiRegionAccessPointPolicy.html">GetMultiRegionAccessPointPolicy</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_PutMultiRegionAccessPointPolicy.html">PutMultiRegionAccessPointPolicy</a>
                  </p> </li> </ul>
                tags:
                  - Get
                  - Multi
                  - Regions
                  - Access
                  - Points
                  - Policies
                  - Status
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
                  - Access Point
                  - Names
                  - Access Point
                  - Bucket
                  - Jobs
                  - Async
                  - Requests
                  - Mrap
                  - Create
                  - Storage Lens Groups
                  - Identifiers
                  - Resource Policies
                  - Policies
                  - Lifecycle Configuration
                  - Replication
                  - Tagging
                  - Delete
                  - Access
                  - Blocks
                  - Storage Lens
                  - Storage Lens
                  - Request_token+
                  - Prefix
                  - Configurations
                  - Status
                  - Versioning
                  - Data Access
                  - Instances
                  - Names
                  - Policy Status
            /v20180820/mrap/instances/{mrap+}/routes:
              PATCH:
                summary: SubmitMultiRegionAccessPointRoutes
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Submits an updated route configuration
                  for a Multi-Region Access Point. This API operation updates
                  the routing status for the specified Regions from active to
                  passive, or from passive to active. A value of <code>0</code>
                  indicates a passive status, which means that traffic won't be
                  routed to the specified Region. A value of <code>100</code>
                  indicates an active status, which means that traffic will be
                  routed to the specified Region. At least one Region must be
                  active at all times.</p> <p>When the routing configuration is
                  changed, any in-progress operations (uploads, copies, deletes,
                  and so on) to formerly active Regions will continue to run to
                  their final completion state (success or failure). The routing
                  configurations of any Regions that aren’t specified remain
                  unchanged.</p> <note> <p>Updated routing configurations might
                  not be immediately applied. It can take up to 2 minutes for
                  your changes to take effect.</p> </note> <p>To submit routing
                  control changes and failover requests, use the Amazon S3
                  failover control infrastructure endpoints in these five Amazon
                  Web Services Regions:</p> <ul> <li> <p> <code>us-east-1</code>
                  </p> </li> <li> <p> <code>us-west-2</code> </p> </li> <li> <p>
                  <code>ap-southeast-2</code> </p> </li> <li> <p>
                  <code>ap-northeast-1</code> </p> </li> <li> <p>
                  <code>eu-west-1</code> </p> </li> </ul> <note> <p>Your Amazon
                  S3 bucket does not need to be in these five Regions.</p>
                  </note>
                tags:
                  - Submit
                  - Multi
                  - Regions
                  - Access
                  - Points
                  - Routes
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
                  - Access Point
                  - Names
                  - Access Point
                  - Bucket
                  - Jobs
                  - Async
                  - Requests
                  - Mrap
                  - Create
                  - Storage Lens Groups
                  - Identifiers
                  - Resource Policies
                  - Policies
                  - Lifecycle Configuration
                  - Replication
                  - Tagging
                  - Delete
                  - Access
                  - Blocks
                  - Storage Lens
                  - Storage Lens
                  - Request_token+
                  - Prefix
                  - Configurations
                  - Status
                  - Versioning
                  - Data Access
                  - Instances
                  - Names
                  - Policy Status
                  - Mrap+
                  - Routes
            /v20180820/accessgrantsinstance/grants:
              GET:
                summary: ListAccessGrants
                description: >-
                  <p>Returns the list of access grants in your S3 Access Grants
                  instance.</p> <dl> <dt>Permissions</dt> <dd> <p>You must have
                  the <code>s3:ListAccessGrants</code> permission to use this
                  operation. </p> </dd> </dl>
                tags:
                  - Lists
                  - Access
                  - Grants
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
                  - Access Point
                  - Names
                  - Access Point
                  - Bucket
                  - Jobs
                  - Async
                  - Requests
                  - Mrap
                  - Create
                  - Storage Lens Groups
                  - Identifiers
                  - Resource Policies
                  - Policies
                  - Lifecycle Configuration
                  - Replication
                  - Tagging
                  - Delete
                  - Access
                  - Blocks
                  - Storage Lens
                  - Storage Lens
                  - Request_token+
                  - Prefix
                  - Configurations
                  - Status
                  - Versioning
                  - Data Access
                  - Instances
                  - Names
                  - Policy Status
                  - Mrap+
                  - Routes
                  - Grants
            /v20180820/accessgrantsinstances:
              GET:
                summary: ListAccessGrantsInstances
                description: >-
                  <p>Returns a list of S3 Access Grants instances. An S3 Access
                  Grants instance serves as a logical grouping for your
                  individual access grants. You can only have one S3 Access
                  Grants instance per Region per account.</p> <dl>
                  <dt>Permissions</dt> <dd> <p>You must have the
                  <code>s3:ListAccessGrantsInstances</code> permission to use
                  this operation. </p> </dd> </dl>
                tags:
                  - Lists
                  - Access
                  - Grants
                  - Instances
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
                  - Access Point
                  - Names
                  - Access Point
                  - Bucket
                  - Jobs
                  - Async
                  - Requests
                  - Mrap
                  - Create
                  - Storage Lens Groups
                  - Identifiers
                  - Resource Policies
                  - Policies
                  - Lifecycle Configuration
                  - Replication
                  - Tagging
                  - Delete
                  - Access
                  - Blocks
                  - Storage Lens
                  - Storage Lens
                  - Request_token+
                  - Prefix
                  - Configurations
                  - Status
                  - Versioning
                  - Data Access
                  - Instances
                  - Names
                  - Policy Status
                  - Mrap+
                  - Routes
                  - Grants
                  - Access Grants Instances
            /v20180820/accessgrantsinstance/locations:
              GET:
                summary: ListAccessGrantsLocations
                description: >-
                  <p>Returns a list of the locations registered in your S3
                  Access Grants instance.</p> <dl> <dt>Permissions</dt> <dd>
                  <p>You must have the <code>s3:ListAccessGrantsLocations</code>
                  permission to use this operation. </p> </dd> </dl>
                tags:
                  - Lists
                  - Access
                  - Grants
                  - Locations
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
                  - Access Point
                  - Names
                  - Access Point
                  - Bucket
                  - Jobs
                  - Async
                  - Requests
                  - Mrap
                  - Create
                  - Storage Lens Groups
                  - Identifiers
                  - Resource Policies
                  - Policies
                  - Lifecycle Configuration
                  - Replication
                  - Tagging
                  - Delete
                  - Access
                  - Blocks
                  - Storage Lens
                  - Storage Lens
                  - Request_token+
                  - Prefix
                  - Configurations
                  - Status
                  - Versioning
                  - Data Access
                  - Instances
                  - Names
                  - Policy Status
                  - Mrap+
                  - Routes
                  - Grants
                  - Access Grants Instances
                  - Locations
            /v20180820/accesspoint:
              GET:
                summary: ListAccessPoints
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Returns a list of the access points
                  that are owned by the current account that's associated with
                  the specified bucket. You can retrieve up to 1000 access
                  points per call. If the specified bucket has more than 1,000
                  access points (or the number specified in
                  <code>maxResults</code>, whichever is less), the response will
                  include a continuation token that you can use to list the
                  additional access points.</p> <p/> <p>All Amazon S3 on
                  Outposts REST API requests for this action require an
                  additional parameter of <code>x-amz-outpost-id</code> to be
                  passed with the request. In addition, you must use an S3 on
                  Outposts endpoint hostname prefix instead of
                  <code>s3-control</code>. For an example of the request syntax
                  for Amazon S3 on Outposts that uses the S3 on Outposts
                  endpoint hostname prefix and the <code>x-amz-outpost-id</code>
                  derived by using the access point ARN, see the <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_GetAccessPoint.html#API_control_GetAccessPoint_Examples">Examples</a>
                  section.</p> <p>The following actions are related to
                  <code>ListAccessPoints</code>:</p> <ul> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_CreateAccessPoint.html">CreateAccessPoint</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_DeleteAccessPoint.html">DeleteAccessPoint</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_GetAccessPoint.html">GetAccessPoint</a>
                  </p> </li> </ul>
                tags:
                  - Lists
                  - Access
                  - Points
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
                  - Access Point
                  - Names
                  - Access Point
                  - Bucket
                  - Jobs
                  - Async
                  - Requests
                  - Mrap
                  - Create
                  - Storage Lens Groups
                  - Identifiers
                  - Resource Policies
                  - Policies
                  - Lifecycle Configuration
                  - Replication
                  - Tagging
                  - Delete
                  - Access
                  - Blocks
                  - Storage Lens
                  - Storage Lens
                  - Request_token+
                  - Prefix
                  - Configurations
                  - Status
                  - Versioning
                  - Data Access
                  - Instances
                  - Names
                  - Policy Status
                  - Mrap+
                  - Routes
                  - Grants
                  - Access Grants Instances
                  - Locations
            /v20180820/accesspointforobjectlambda:
              GET:
                summary: ListAccessPointsForObjectLambda
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Returns some or all (up to 1,000)
                  access points associated with the Object Lambda Access Point
                  per call. If there are more access points than what can be
                  returned in one call, the response will include a continuation
                  token that you can use to list the additional access
                  points.</p> <p>The following actions are related to
                  <code>ListAccessPointsForObjectLambda</code>:</p> <ul> <li>
                  <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_CreateAccessPointForObjectLambda.html">CreateAccessPointForObjectLambda</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_DeleteAccessPointForObjectLambda.html">DeleteAccessPointForObjectLambda</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_GetAccessPointForObjectLambda.html">GetAccessPointForObjectLambda</a>
                  </p> </li> </ul>
                tags:
                  - Lists
                  - Access
                  - Points
                  - For
                  - Objects
                  - Lambda
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
                  - Access Point
                  - Names
                  - Access Point
                  - Bucket
                  - Jobs
                  - Async
                  - Requests
                  - Mrap
                  - Create
                  - Storage Lens Groups
                  - Identifiers
                  - Resource Policies
                  - Policies
                  - Lifecycle Configuration
                  - Replication
                  - Tagging
                  - Delete
                  - Access
                  - Blocks
                  - Storage Lens
                  - Storage Lens
                  - Request_token+
                  - Prefix
                  - Configurations
                  - Status
                  - Versioning
                  - Data Access
                  - Instances
                  - Names
                  - Policy Status
                  - Mrap+
                  - Routes
                  - Grants
                  - Access Grants Instances
                  - Locations
            /v20180820/mrap/instances:
              GET:
                summary: ListMultiRegionAccessPoints
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Returns a list of the Multi-Region
                  Access Points currently associated with the specified Amazon
                  Web Services account. Each call can return up to 100
                  Multi-Region Access Points, the maximum number of Multi-Region
                  Access Points that can be associated with a single
                  account.</p> <p>This action will always be routed to the US
                  West (Oregon) Region. For more information about the
                  restrictions around managing Multi-Region Access Points, see
                  <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/ManagingMultiRegionAccessPoints.html">Managing
                  Multi-Region Access Points</a> in the <i>Amazon S3 User
                  Guide</i>.</p> <p>The following actions are related to
                  <code>ListMultiRegionAccessPoint</code>:</p> <ul> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_CreateMultiRegionAccessPoint.html">CreateMultiRegionAccessPoint</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_DeleteMultiRegionAccessPoint.html">DeleteMultiRegionAccessPoint</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_DescribeMultiRegionAccessPointOperation.html">DescribeMultiRegionAccessPointOperation</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_GetMultiRegionAccessPoint.html">GetMultiRegionAccessPoint</a>
                  </p> </li> </ul>
                tags:
                  - Lists
                  - Multi
                  - Regions
                  - Access
                  - Points
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
                  - Access Point
                  - Names
                  - Access Point
                  - Bucket
                  - Jobs
                  - Async
                  - Requests
                  - Mrap
                  - Create
                  - Storage Lens Groups
                  - Identifiers
                  - Resource Policies
                  - Policies
                  - Lifecycle Configuration
                  - Replication
                  - Tagging
                  - Delete
                  - Access
                  - Blocks
                  - Storage Lens
                  - Storage Lens
                  - Request_token+
                  - Prefix
                  - Configurations
                  - Status
                  - Versioning
                  - Data Access
                  - Instances
                  - Names
                  - Policy Status
                  - Mrap+
                  - Routes
                  - Grants
                  - Access Grants Instances
                  - Locations
            /v20180820/bucket:
              GET:
                summary: ListRegionalBuckets
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Returns a list of all Outposts buckets
                  in an Outpost that are owned by the authenticated sender of
                  the request. For more information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/S3onOutposts.html">Using
                  Amazon S3 on Outposts</a> in the <i>Amazon S3 User
                  Guide</i>.</p> <p>For an example of the request syntax for
                  Amazon S3 on Outposts that uses the S3 on Outposts endpoint
                  hostname prefix and <code>x-amz-outpost-id</code> in your
                  request, see the <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_ListRegionalBuckets.html#API_control_ListRegionalBuckets_Examples">Examples</a>
                  section.</p>
                tags:
                  - Lists
                  - Regional
                  - Buckets
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
                  - Access Point
                  - Names
                  - Access Point
                  - Bucket
                  - Jobs
                  - Async
                  - Requests
                  - Mrap
                  - Create
                  - Storage Lens Groups
                  - Identifiers
                  - Resource Policies
                  - Policies
                  - Lifecycle Configuration
                  - Replication
                  - Tagging
                  - Delete
                  - Access
                  - Blocks
                  - Storage Lens
                  - Storage Lens
                  - Request_token+
                  - Prefix
                  - Configurations
                  - Status
                  - Versioning
                  - Data Access
                  - Instances
                  - Names
                  - Policy Status
                  - Mrap+
                  - Routes
                  - Grants
                  - Access Grants Instances
                  - Locations
            /v20180820/storagelens:
              GET:
                summary: ListStorageLensConfigurations
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Gets a list of Amazon S3 Storage Lens
                  configurations. For more information about S3 Storage Lens,
                  see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/storage_lens.html">Assessing
                  your storage activity and usage with Amazon S3 Storage Lens
                  </a> in the <i>Amazon S3 User Guide</i>.</p> <note> <p>To use
                  this action, you must have permission to perform the
                  <code>s3:ListStorageLensConfigurations</code> action. For more
                  information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/dev/storage_lens_iam_permissions.html">Setting
                  permissions to use Amazon S3 Storage Lens</a> in the <i>Amazon
                  S3 User Guide</i>.</p> </note>
                tags:
                  - Lists
                  - Storage
                  - Lens
                  - Configurations
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
                  - Access Point
                  - Names
                  - Access Point
                  - Bucket
                  - Jobs
                  - Async
                  - Requests
                  - Mrap
                  - Create
                  - Storage Lens Groups
                  - Identifiers
                  - Resource Policies
                  - Policies
                  - Lifecycle Configuration
                  - Replication
                  - Tagging
                  - Delete
                  - Access
                  - Blocks
                  - Storage Lens
                  - Storage Lens
                  - Request_token+
                  - Prefix
                  - Configurations
                  - Status
                  - Versioning
                  - Data Access
                  - Instances
                  - Names
                  - Policy Status
                  - Mrap+
                  - Routes
                  - Grants
                  - Access Grants Instances
                  - Locations
            /v20180820/tags/{resourceArn+}:
              DELETE:
                summary: UntagResource
                description: >-
                  <p> This operation removes the specified Amazon Web Services
                  resource tags from an S3 resource. Each tag is a label
                  consisting of a user-defined key and value. Tags can help you
                  manage, identify, organize, search for, and filter resources.
                  </p> <note> <p>This operation is only supported for <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/storage-lens-groups.html">S3
                  Storage Lens groups</a> and for <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/access-grants-tagging.html">S3
                  Access Grants</a>. The tagged resource can be an S3 Storage
                  Lens group or S3 Access Grants instance, registered location,
                  or grant. </p> </note> <dl> <dt>Permissions</dt> <dd> <p>You
                  must have the <code>s3:UntagResource</code> permission to use
                  this operation. </p> </dd> </dl> <p>For more information about
                  the required Storage Lens Groups permissions, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/storage_lens_iam_permissions.html#storage_lens_groups_permissions">Setting
                  account permissions to use S3 Storage Lens groups</a>.</p>
                  <p>For information about S3 Tagging errors, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/ErrorResponses.html#S3TaggingErrorCodeList">List
                  of Amazon S3 Tagging error codes</a>.</p>
                tags:
                  - Untag
                  - Resources
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
                  - Access Point
                  - Names
                  - Access Point
                  - Bucket
                  - Jobs
                  - Async
                  - Requests
                  - Mrap
                  - Create
                  - Storage Lens Groups
                  - Identifiers
                  - Resource Policies
                  - Policies
                  - Lifecycle Configuration
                  - Replication
                  - Tagging
                  - Delete
                  - Access
                  - Blocks
                  - Storage Lens
                  - Storage Lens
                  - Request_token+
                  - Prefix
                  - Configurations
                  - Status
                  - Versioning
                  - Data Access
                  - Instances
                  - Names
                  - Policy Status
                  - Mrap+
                  - Routes
                  - Grants
                  - Access Grants Instances
                  - Locations
                  - ARN
            /v20180820/async-requests/mrap/put-policy:
              POST:
                summary: PutMultiRegionAccessPointPolicy
                description: >-
                  <note> <p>This operation is not supported by directory
                  buckets.</p> </note> <p>Associates an access control policy
                  with the specified Multi-Region Access Point. Each
                  Multi-Region Access Point can have only one policy, so a
                  request made to this action replaces any existing policy that
                  is associated with the specified Multi-Region Access
                  Point.</p> <p>This action will always be routed to the US West
                  (Oregon) Region. For more information about the restrictions
                  around managing Multi-Region Access Points, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/ManagingMultiRegionAccessPoints.html">Managing
                  Multi-Region Access Points</a> in the <i>Amazon S3 User
                  Guide</i>.</p> <p>The following actions are related to
                  <code>PutMultiRegionAccessPointPolicy</code>:</p> <ul> <li>
                  <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_GetMultiRegionAccessPointPolicy.html">GetMultiRegionAccessPointPolicy</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_GetMultiRegionAccessPointPolicyStatus.html">GetMultiRegionAccessPointPolicyStatus</a>
                  </p> </li> </ul>
                tags:
                  - Put
                  - Multi
                  - Regions
                  - Access
                  - Points
                  - Policies
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
                  - Access Point
                  - Names
                  - Access Point
                  - Bucket
                  - Jobs
                  - Async
                  - Requests
                  - Mrap
                  - Create
                  - Storage Lens Groups
                  - Identifiers
                  - Resource Policies
                  - Policies
                  - Lifecycle Configuration
                  - Replication
                  - Tagging
                  - Delete
                  - Access
                  - Blocks
                  - Storage Lens
                  - Storage Lens
                  - Request_token+
                  - Prefix
                  - Configurations
                  - Status
                  - Versioning
                  - Data Access
                  - Instances
                  - Names
                  - Policy Status
                  - Mrap+
                  - Routes
                  - Grants
                  - Access Grants Instances
                  - Locations
                  - ARN
                  - Put
            /v20180820/jobs/{id}/priority:
              POST:
                summary: UpdateJobPriority
                description: >-
                  <p>Updates an existing S3 Batch Operations job's priority. For
                  more information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/batch-ops.html">S3
                  Batch Operations</a> in the <i>Amazon S3 User Guide</i>.</p>
                  <dl> <dt>Permissions</dt> <dd> <p>To use the
                  <code>UpdateJobPriority</code> operation, you must have
                  permission to perform the <code>s3:UpdateJobPriority</code>
                  action.</p> </dd> </dl> <p>Related actions include:</p> <ul>
                  <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_CreateJob.html">CreateJob</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_ListJobs.html">ListJobs</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_DescribeJob.html">DescribeJob</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_UpdateJobStatus.html">UpdateJobStatus</a>
                  </p> </li> </ul>
                tags:
                  - Update
                  - Jobs
                  - Priorities
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
                  - Access Point
                  - Names
                  - Access Point
                  - Bucket
                  - Jobs
                  - Async
                  - Requests
                  - Mrap
                  - Create
                  - Storage Lens Groups
                  - Identifiers
                  - Resource Policies
                  - Policies
                  - Lifecycle Configuration
                  - Replication
                  - Tagging
                  - Delete
                  - Access
                  - Blocks
                  - Storage Lens
                  - Storage Lens
                  - Request_token+
                  - Prefix
                  - Configurations
                  - Status
                  - Versioning
                  - Data Access
                  - Instances
                  - Names
                  - Policy Status
                  - Mrap+
                  - Routes
                  - Grants
                  - Access Grants Instances
                  - Locations
                  - ARN
                  - Put
                  - Priorities
            /v20180820/jobs/{id}/status:
              POST:
                summary: UpdateJobStatus
                description: >-
                  <p>Updates the status for the specified job. Use this
                  operation to confirm that you want to run a job or to cancel
                  an existing job. For more information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/batch-ops.html">S3
                  Batch Operations</a> in the <i>Amazon S3 User Guide</i>.</p>
                  <dl> <dt>Permissions</dt> <dd> <p>To use the
                  <code>UpdateJobStatus</code> operation, you must have
                  permission to perform the <code>s3:UpdateJobStatus</code>
                  action.</p> </dd> </dl> <p>Related actions include:</p> <ul>
                  <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_CreateJob.html">CreateJob</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_ListJobs.html">ListJobs</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_DescribeJob.html">DescribeJob</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_control_UpdateJobStatus.html">UpdateJobStatus</a>
                  </p> <
                tags:
                  - Update
                  - Jobs
                  - Status
                  - V20180820
                  - Access Grants Instances
                  - Identity Center
                  - Grant
                  - Locations
                  - Access Point
                  - Names
                  - Access Point
                  - Bucket
                  - Jobs
                  - Async
                  - Requests
                  - Mrap
                  - Create
                  - Storage Lens Groups
                  - Identifiers
                  - Resource Policies
                  - Policies
                  - Lifecycle Configuration
                  - Replication
                  - Tagging
                  - Delete
                  - Access
                  - Blocks
                  - Storage Lens
                  - Storage Lens
                  - Request_token+
                  - Prefix
                  - Configurations
                  - Status
                  - Versioning
                  - Data Access
                  - Instances
                  - Names
                  - Policy Status
                  - Mrap+
                  - Routes
                  - Grants
                  - Access Grants Instances
                  - Locations
                  - ARN
                  - Put
                  - Priorities
    overlays:
      - type: APIs.io Search
        url: overlays/s3control-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/s3control-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:s3control
  - name: runtime.sagemaker
    description: <p> The Amazon SageMaker runtime API. </p>
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
            title: runtime.sagemaker
          paths:
            /endpoints/{EndpointName}/invocations:
              POST:
                summary: InvokeEndpoint
                description: >-
                  <p>After you deploy a model into production using Amazon
                  SageMaker hosting services, your client applications use this
                  API to get inferences from the model hosted at the specified
                  endpoint. </p> <p>For an overview of Amazon SageMaker, see <a
                  href="https://docs.aws.amazon.com/sagemaker/latest/dg/how-it-works.html">How
                  It Works</a>. </p> <p>Amazon SageMaker strips all POST headers
                  except those supported by the API. Amazon SageMaker might add
                  additional headers. You should not rely on the behavior of
                  headers outside those enumerated in the request syntax. </p>
                  <p>Calls to <code>InvokeEndpoint</code> are authenticated by
                  using Amazon Web Services Signature Version 4. For
                  information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/sig-v4-authenticating-requests.html">Authenticating
                  Requests (Amazon Web Services Signature Version 4)</a> in the
                  <i>Amazon S3 API Reference</i>.</p> <p>A customer's model
                  containers must respond to requests within 60 seconds. The
                  model itself can have a maximum processing time of 60 seconds
                  before responding to invocations. If your model is going to
                  take 50-60 seconds of processing time, the SDK socket timeout
                  should be set to be 70 seconds.</p> <note> <p>Endpoints are
                  scoped to an individual account, and are not public. The URL
                  does not contain the account ID, but Amazon SageMaker
                  determines the account ID from the authentication token that
                  is supplied by the caller.</p> </note>
                tags:
                  - Invoke
                  - Endpoints
                  - Endpoints
                  - Names
                  - Invocations
            /endpoints/{EndpointName}/async-invocations:
              POST:
                summary: InvokeEndpointAsync
                description: >-
                  <p>After you deploy a model into production using Amazon
                  SageMaker hosting services, your client applications use this
                  API to get inferences from the model hosted at the specified
                  endpoint in an asynchronous manner.</p> <p>Inference requests
                  sent to this API are enqueued for asynchronous processing. The
                  processing of the inference request may or may not complete
                  before you receive a response from this API. The response from
                  this API will not contain the result of the inference request
                  but contain information about where you can locate it.</p>
                  <p>Amazon SageMaker strips all POST headers except those
                  supported by the API. Amazon SageMaker might add additional
                  headers. You should not rely on the behavior of headers
                  outside those enumerated in the request syntax. </p> <p>Calls
                  to <code>InvokeEndpointAsync</code> are authenticated by using
                  Amazon Web Services Signature Version 4. For information, see
                  <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/sig-v4-authenticating-requests.html">Authenticating
                  Requests (Amazon Web Services Signature Version 4)</a> in the
                  <i>Amazon S3 API Reference</i>.</p>
                tags:
                  - Invoke
                  - Endpoints
                  - Async
                  - Endpoints
                  - Names
                  - Invocations
                  - Async
            /endpoints/{EndpointName}/invocations-response-stream:
              POST:
                summary: InvokeEndpointWithResponseStream
                description: >-
                  <p>Invokes a model at the specified endpoint to return the
                  inference response as a stream. The inference stream provides
                  the response payload incrementally as a series of parts.
                  Before you can get an inference stream, you must have access
                  to a model that's deployed using Amazon SageMaker hosting
                  services, and the container for that model must support
                  inference streaming.</p> <p>For more information that can help
                  you use this API, see the following sections in the <i>Amazon
                  SageMaker Developer Guide</i>:</p> <ul> <li> <p>For
                  information about how to add streaming support to a model, see
                  <a
                  href="https://docs.aws.amazon.com/sagemaker/latest/dg/your-algorithms-inference-code.html#your-algorithms-inference-code-how-containe-serves-requests">How
                  Containers Serve Requests</a>.</p> </li> <li> <p>For
                  information about how to process the streaming response, see
                  <a
                  href="https://docs.aws.amazon.com/sagemaker/latest/dg/realtime-endpoints-test-endpoints.html">Invoke
                  real-time endpoints</a>.</p> </li> </ul> <p>Before you can use
                  this operation, your IAM permissions must allow the
                  <code>sagemaker:InvokeEndpoint</code> action. For more
                  information about Amazon SageMaker actions for IAM policies,
                  see <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_amazonsagemaker.html">Actions,
                  resources, and condition keys for Amazon SageMaker</a> in the
                  <i>IAM Service Authorization Reference</i>.</p> <p>Amazon
                  SageMaker strips all POST headers except those supported by
                  the API. Amazon SageMaker might add additional headers. You
                  should not rely on the behavior of headers outside those
                  enumerated in the request syntax. </p> <p>Calls to
                  <code>InvokeEndpointWithResponseStream</code> are
                  authenticated by using Amazon Web Services Signature Version
                  4. For information, see <a
                  href="https://docs.aws.amazon.com/AmazonS3/latest/API/sig-v4-authenticating-requests.html">Authenticating
                  Requests (Amazon Web Services Signature Version 4)</a> in the
                  <i>Amazon S3 API Referenc
                tags:
                  - Invoke
                  - Endpoints
                  - With
                  - Responses
                  - Stream
                  - Endpoints
                  - Names
                  - Invocations
                  - Async
                  - Responses
                  - Stre
    overlays:
      - type: APIs.io Search
        url: overlays/runtimesagemaker-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/runtimesagemaker-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:runtimesagemaker
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