---
name: Ali
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/ali.png
url: https://example.com/apis/ali.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Ali
apis:
  - name: amp
    description: >-
      <p>Amazon Managed Service for Prometheus is a serverless,
      Prometheus-compatible monitoring service for container metrics that makes
      it easier to securely monitor container environments at scale. With Amazon
      Managed Service for Prometheus, you can use the same open-source
      Prometheus data model and query language that you use today to monitor the
      performance of your containerized workloads, and also enjoy improved
      scalability, availability, and security without having to manage the
      underlying infrastructure.</p> <p>For more information about Amazon
      Managed Service for Prometheus, see the <a
      href="https://docs.aws.amazon.com/prometheus/latest/userguide/what-is-Amazon-Managed-Service-Prometheus.html">Amazon
      Managed Service for Prometheus</a> User Guide.</p> <p>Amazon Managed
      Service for Prometheus includes two APIs.</p> <ul> <li> <p>Use the Amazon
      Web Services API described in this guide to manage Amazon Managed Service
      for Prometheus resources, such as workspaces, rule groups, and alert
      managers.</p> </li> <li> <p>Use the <a
      href="https://docs.aws.amazon.com/prometheus/latest/userguide/AMP-APIReference.html#AMP-APIReference-Prometheus-Compatible-Apis">Prometheus-compatible
      API</a> to work within your Prometheus workspace.</p> </li> </ul>
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
            title: amp
          paths:
            /workspaces/{workspaceId}/alertmanager/definition:
              PUT:
                summary: PutAlertManagerDefinition
                description: >-
                  <p>Updates an existing alert manager definition in a
                  workspace. If the workspace does not already have an alert
                  manager definition, don't use this operation to create it.
                  Instead, use <code>CreateAlertManagerDefinition</code>.</p>
                tags:
                  - Put
                  - Alerts
                  - Managers
                  - Definitions
                  - Identifiers
                  - Alert Management
                  - Definitions
            /workspaces/{workspaceId}/logging:
              PUT:
                summary: UpdateLoggingConfiguration
                description: >-
                  <p>Updates the log group ARN or the workspace ID of the
                  current logging configuration.</p>
                tags:
                  - Update
                  - Logging
                  - Configurations
                  - Identifiers
                  - Alert Management
                  - Definitions
                  - Logging
            /workspaces/{workspaceId}/rulegroupsnamespaces:
              GET:
                summary: ListRuleGroupsNamespaces
                description: >-
                  <p>Returns a list of rule groups namespaces in a
                  workspace.</p>
                tags:
                  - Lists
                  - Rules
                  - Groups
                  - Namespaces
                  - Identifiers
                  - Alert Management
                  - Definitions
                  - Logging
                  - Rule Groups Namespaces
            /scrapers:
              GET:
                summary: ListScrapers
                description: >-
                  <p>The <code>ListScrapers</code> operation lists all of the
                  scrapers in your account. This includes scrapers being created
                  or deleted. You can optionally filter the returned list.</p>
                tags:
                  - Lists
                  - Scrapers
                  - Identifiers
                  - Alert Management
                  - Definitions
                  - Logging
                  - Rule Groups Namespaces
                  - Scrapers
            /workspaces:
              GET:
                summary: ListWorkspaces
                description: >-
                  <p>Lists all of the Amazon Managed Service for Prometheus
                  workspaces in your account. This includes workspaces being
                  created or deleted. </p>
                tags:
                  - Lists
                  - Workspaces
                  - Identifiers
                  - Alert Management
                  - Definitions
                  - Logging
                  - Rule Groups Namespaces
                  - Scrapers
                  - Workspaces
            /workspaces/{workspaceId}/rulegroupsnamespaces/{name}:
              PUT:
                summary: PutRuleGroupsNamespace
                description: >-
                  <p>Updates an existing rule groups namespace within a
                  workspace. A rule groups namespace is associated with exactly
                  one rules file. A workspace can have multiple rule groups
                  namespaces.</p> <p>Use this operation only to update existing
                  rule groups namespaces. To create a new rule groups namespace,
                  use <code>CreateRuleGroupsNamespace</code>.</p> <p>You can't
                  use this operation to add tags to an existing rule groups
                  namespace. Instead, use <code>TagResource</code>.</p>
                tags:
                  - Put
                  - Rules
                  - Groups
                  - Namespaces
                  - Identifiers
                  - Alert Management
                  - Definitions
                  - Logging
                  - Rule Groups Namespaces
                  - Scrapers
                  - Workspaces
                  - Names
            /scrapers/{scraperId}:
              GET:
                summary: DescribeScraper
                description: >-
                  <p>The <code>DescribeScraper</code> operation displays
                  information about an existing scraper.</p>
                tags:
                  - Describe
                  - Scrapers
                  - Identifiers
                  - Alert Management
                  - Definitions
                  - Logging
                  - Rule Groups Namespaces
                  - Scrapers
                  - Workspaces
                  - Names
            /workspaces/{workspaceId}:
              GET:
                summary: DescribeWorkspace
                description: <p>Returns information about an existing workspace. </p>
                tags:
                  - Describe
                  - Workspaces
                  - Identifiers
                  - Alert Management
                  - Definitions
                  - Logging
                  - Rule Groups Namespaces
                  - Scrapers
                  - Workspaces
                  - Names
            /scraperconfiguration:
              GET:
                summary: GetDefaultScraperConfiguration
                description: >-
                  <p>The <code>GetDefaultScraperConfiguration</code> operation
                  returns the default scraper configuration used when Amazon EKS
                  creates a scraper for you.</p>
                tags:
                  - Get
                  - Default
                  - Scrapers
                  - Configurations
                  - Identifiers
                  - Alert Management
                  - Definitions
                  - Logging
                  - Rule Groups Namespaces
                  - Scrapers
                  - Workspaces
                  - Names
                  - Scraper Configurations
            /tags/{resourceArn}:
              DELETE:
                summary: UntagResource
                description: >-
                  <p>Removes the specified tags from an Amazon Managed Service
                  for Prometheus resource. The only resources that can be tagged
                  are workspaces and rule groups namespaces. </p>
                tags:
                  - Untag
                  - Resources
                  - Identifiers
                  - Alert Management
                  - Definitions
                  - Logging
                  - Rule Groups Namespaces
                  - Scrapers
                  - Workspaces
                  - Names
                  - Scraper Configurations
                  - ARN
            /workspaces/{workspaceId}/alias:
              POST:
                summary: UpdateWorkspaceAlias
                description: <p>Updates the alias of an existing work
                tags:
                  - Update
                  - Workspaces
                  - Alias
                  - Identifiers
                  - Alert Management
                  - Definitions
                  - Logging
                  - Rule Groups Namespaces
                  - Scrapers
                  - Workspaces
                  - Names
                  - Scraper Configurations
                  - ARN
                  - Ali
    overlays:
      - type: APIs.io Search
        url: overlays/amp-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/amp-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:amp
  - name: payment-cryptography
    description: >-
      <p>Amazon Web Services Payment Cryptography Control Plane APIs manage
      encryption keys for use during payment-related cryptographic operations.
      You can create, import, export, share, manage, and delete keys. You can
      also manage Identity and Access Management (IAM) policies for keys. For
      more information, see <a
      href="https://docs.aws.amazon.com/payment-cryptography/latest/userguide/security-iam.html">Identity
      and access management</a> in the <i>Amazon Web Services Payment
      Cryptography User Guide.</i> </p> <p>To use encryption keys for
      payment-related transaction processing and associated cryptographic
      operations, you use the <a
      href="https://docs.aws.amazon.com/payment-cryptography/latest/DataAPIReference/Welcome.html">Amazon
      Web Services Payment Cryptography Data Plane</a>. You can perform actions
      like encrypt, decrypt, generate, and verify payment-related data.</p>
      <p>All Amazon Web Services Payment Cryptography API calls must be signed
      and transmitted using Transport Layer Security (TLS). We recommend you
      always use the latest supported TLS version for logging API requests. </p>
      <p>Amazon Web Services Payment Cryptography supports CloudTrail for
      control plane operations, a service that logs Amazon Web Services API
      calls and related events for your Amazon Web Services account and delivers
      them to an Amazon S3 bucket you specify. By using the information
      collected by CloudTrail, you can determine what requests were made to
      Amazon Web Services Payment Cryptography, who made the request, when it
      was made, and so on. If you don't conﬁgure a trail, you can still view the
      most recent events in the CloudTrail console. For more information, see
      the <a
      href="https://docs.aws.amazon.com/awscloudtrail/latest/userguide/">CloudTrail
      User Guide</a>.</p>
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
            title: payment-cryptography
          paths:
            /:
              POST:
                summary: UpdateAlias
                description: >-
                  <p>Associates an existing Amazon Web Services Payment
                  Cryptography alias with a different key. Each alias is
                  associated with only one Amazon Web Services Payment
                  Cryptography key at a time, although a key can have multiple
                  aliases. The alias and the Amazon Web Services Payment
                  Cryptography key must be in the same Amazon Web Services
                  account and Amazon Web Services Region</p> <p>
                  <b>Cross-account use:</b> This operation can't be used across
                  different Amazon Web Services accounts.</p> <p> <b>Related
                  operations:</b> </p> <ul> <li> <p> <a>CreateAlias</a> </p>
                  </li> <li> <p> <a>DeleteAlias</a> </p> </li> <li> <p>
                  <a>GetAlias</a> </p> </li> <li> <p> <a>ListAliases</a> </p> <
                tags:
                  - Update
                  - Ali
    overlays:
      - type: APIs.io Search
        url: overlays/payment-cryptography-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/payment-cryptography-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:payment-cryptography
  - name: states
    description: >-
      <fullname>Step Functions</fullname> <p>Step Functions is a service that
      lets you coordinate the components of distributed applications and
      microservices using visual workflows.</p> <p>You can use Step Functions to
      build applications from individual components, each of which performs a
      discrete function, or <i>task</i>, allowing you to scale and change
      applications quickly. Step Functions provides a console that helps
      visualize the components of your application as a series of steps. Step
      Functions automatically triggers and tracks each step, and retries steps
      when there are errors, so your application executes predictably and in the
      right order every time. Step Functions logs the state of each step, so you
      can quickly diagnose and debug any issues.</p> <p>Step Functions manages
      operations and underlying infrastructure to ensure your application is
      available at any scale. You can run tasks on Amazon Web Services, your own
      servers, or any system that has access to Amazon Web Services. You can
      access and use Step Functions using the console, the Amazon Web Services
      SDKs, or an HTTP API. For more information about Step Functions, see the
      <i> <a
      href="https://docs.aws.amazon.com/step-functions/latest/dg/welcome.html">Step
      Functions Developer Guide</a> </i>.</p> <important> <p>If you use the Step
      Functions API actions using Amazon Web Services SDK integrations, make
      sure the API actions are in camel case and parameter names are in Pascal
      case. For example, you could use Step Functions API action
      <code>startSyncExecution</code> and specify its parameter as
      <code>StateMachineArn</code>.</p> </important>
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
            title: states
          paths:
            /:
              POST:
                summary: UpdateStateMachineAlias
                description: >-
                  <p>Updates the configuration of an existing state machine <a
                  href="https://docs.aws.amazon.com/step-functions/latest/dg/concepts-state-machine-alias.html">alias</a>
                  by modifying its <code>description</code> or
                  <code>routingConfiguration</code>.</p> <p>You must specify at
                  least one of the <code>description</code> or
                  <code>routingConfiguration</code> parameters to update a state
                  machine alias.</p> <note> <p>
                  <code>UpdateStateMachineAlias</code> is an idempotent API.
                  Step Functions bases the idempotency check on the
                  <code>stateMachineAliasArn</code>, <code>description</code>,
                  and <code>routingConfiguration</code> parameters. Requests
                  with the same parameters return an idempotent response.</p>
                  </note> <note> <p>This operation is eventually consistent. All
                  <a>StartExecution</a> requests made within a few seconds use
                  the latest alias configuration. Executions started immediately
                  after calling <code>UpdateStateMachineAlias</code> may use the
                  previous routing configuration.</p> </note> <p> <b>Related
                  operations:</b> </p> <ul> <li> <p>
                  <a>CreateStateMachineAlias</a> </p> </li> <li> <p>
                  <a>DescribeStateMachineAlias</a> </p> </li> <li> <p>
                  <a>ListStateMachineAliases</a> </p> </li> <li> <p>
                  <a>DeleteStateMachineAlias</a> </p> <
                tags:
                  - Update
                  - States
                  - Machines
                  - Ali
    overlays:
      - type: APIs.io Search
        url: overlays/states-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/states-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:states
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---