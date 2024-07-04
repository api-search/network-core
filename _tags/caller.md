---
name: Caller
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/caller.png
url: https://example.com/apis/caller.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Caller
apis:
  - name: connect
    description: >-
      <p>Amazon Connect is a cloud-based contact center solution that you use to
      set up and manage a customer contact center and provide reliable customer
      engagement at any scale.</p> <p>Amazon Connect provides metrics and
      real-time reporting that enable you to optimize contact routing. You can
      also resolve customer issues more efficiently by getting customers in
      touch with the appropriate agents.</p> <p>There are limits to the number
      of Amazon Connect resources that you can create. There are also limits to
      the number of requests that you can make per second. For more information,
      see <a
      href="https://docs.aws.amazon.com/connect/latest/adminguide/amazon-connect-service-limits.html">Amazon
      Connect Service Quotas</a> in the <i>Amazon Connect Administrator
      Guide</i>.</p> <p>You can connect programmatically to an Amazon Web
      Services service by using an endpoint. For a list of Amazon Connect
      endpoints, see <a
      href="https://docs.aws.amazon.com/general/latest/gr/connect_region.html">Amazon
      Connect Endpoints</a>.</p>
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
            title: connect
          paths:
            /evaluation-forms/{InstanceId}/{EvaluationFormId}/activate:
              POST:
                summary: ActivateEvaluationForm
                description: >-
                  <p>Activates an evaluation form in the specified Amazon
                  Connect instance. After the evaluation form is activated, it
                  is available to start new evaluations based on the form. </p>
                tags:
                  - Activate
                  - Evaluations
                  - Forms
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
            /analytics-data/instance/{InstanceId}/association:
              GET:
                summary: ListAnalyticsDataAssociations
                description: >-
                  <p>This API is in preview release for Amazon Connect and is
                  subject to change.</p> <p>Lists the association status of
                  requested dataset ID for a given Amazon Connect instance.</p>
                tags:
                  - Lists
                  - Analytics
                  - Data
                  - Associations
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
            /instance/{InstanceId}/approved-origin:
              DELETE:
                summary: DisassociateApprovedOrigin
                description: >-
                  <p>This API is in preview release for Amazon Connect and is
                  subject to change.</p> <p>Revokes access to integrated
                  applications from Amazon Connect.</p>
                tags:
                  - Disassociate
                  - Approved
                  - Origin
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
            /instance/{InstanceId}/bot:
              POST:
                summary: DisassociateBot
                description: >-
                  <p>This API is in preview release for Amazon Connect and is
                  subject to change.</p> <p>Revokes authorization from the
                  specified instance to access the specified Amazon Lex or
                  Amazon Lex V2 bot. </p>
                tags:
                  - Disassociate
                  - Bot
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
            /default-vocabulary/{InstanceId}/{LanguageCode}:
              PUT:
                summary: AssociateDefaultVocabulary
                description: >-
                  <p>Associates an existing vocabulary as the default. Contact
                  Lens for Amazon Connect uses the vocabulary in post-call and
                  real-time analysis sessions for the given language.</p>
                tags:
                  - Associate
                  - Default
                  - Vocabularies
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
            /flow-associations/{InstanceId}:
              PUT:
                summary: AssociateFlow
                description: <p>Associates a connect resource to a flow.</p>
                tags:
                  - Associate
                  - Flow
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
            /instance/{InstanceId}/storage-config:
              PUT:
                summary: AssociateInstanceStorageConfig
                description: >-
                  <p>This API is in preview release for Amazon Connect and is
                  subject to change.</p> <p>Associates a storage resource type
                  for the first time. You can only associate one type of storage
                  configuration in a single call. This means, for example, that
                  you can't define an instance with multiple S3 buckets for
                  storing chat transcripts.</p> <p>This API does not create a
                  resource that doesn't exist. It only associates it to the
                  instance. Ensure that the resource being specified in the
                  storage configuration, like an S3 bucket, exists when being
                  used for association.</p>
                tags:
                  - Associate
                  - Instances
                  - Storage
                  - Configurations
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
            /instance/{InstanceId}/lambda-function:
              DELETE:
                summary: DisassociateLambdaFunction
                description: >-
                  <p>This API is in preview release for Amazon Connect and is
                  subject to change.</p> <p>Remove the Lambda function from the
                  dropdown options available in the relevant flow blocks.</p>
                tags:
                  - Disassociate
                  - Lambda
                  - Functions
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
            /instance/{InstanceId}/lex-bot:
              DELETE:
                summary: DisassociateLexBot
                description: >-
                  <p>This API is in preview release for Amazon Connect and is
                  subject to change.</p> <p>Revokes authorization from the
                  specified instance to access the specified Amazon Lex bot.</p>
                tags:
                  - Disassociate
                  - Lex
                  - Bot
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
            /phone-number/{PhoneNumberId}/contact-flow:
              DELETE:
                summary: DisassociatePhoneNumberContactFlow
                description: >-
                  <p>Removes the flow association from a phone number claimed to
                  your Amazon Connect instance.</p> <important> <p>If the number
                  is claimed to a traffic distribution group, and you are
                  calling this API using an instance in the Amazon Web Services
                  Region where the traffic distribution group was created, you
                  can use either a full phone number ARN or UUID value for the
                  <code>PhoneNumberId</code> URI request parameter. However, if
                  the number is claimed to a traffic distribution group and you
                  are calling this API using an instance in the alternate Amazon
                  Web Services Region associated with the traffic distribution
                  group, you must provide a full phone number ARN. If a UUID is
                  provided in this scenario, you will receive a
                  <code>ResourceNotFoundException</code>.</p> </important>
                tags:
                  - Disassociate
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
            /queues/{InstanceId}/{QueueId}/associate-quick-connects:
              POST:
                summary: AssociateQueueQuickConnects
                description: >-
                  <p>This API is in preview release for Amazon Connect and is
                  subject to change.</p> <p>Associates a set of quick connects
                  with a queue.</p>
                tags:
                  - Associate
                  - Queues
                  - Quick
                  - Connects
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
            /routing-profiles/{InstanceId}/{RoutingProfileId}/associate-queues:
              POST:
                summary: AssociateRoutingProfileQueues
                description: <p>Associates a set of queues with a routing profile.</p>
                tags:
                  - Associate
                  - Routing
                  - Profiles
                  - Queues
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
            /instance/{InstanceId}/security-key:
              PUT:
                summary: AssociateSecurityKey
                description: >-
                  <p>This API is in preview release for Amazon Connect and is
                  subject to change.</p> <p>Associates a security key to the
                  instance.</p>
                tags:
                  - Associate
                  - Security
                  - Keys
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
            /traffic-distribution-group/{TrafficDistributionGroupId}/user:
              GET:
                summary: ListTrafficDistributionGroupUsers
                description: <p>Lists traffic distribution group users.</p>
                tags:
                  - Lists
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
            /users/{InstanceId}/{UserId}/associate-proficiencies:
              POST:
                summary: AssociateUserProficiencies
                description: <p>&gt;Associates a set of proficiencies with a user.</p>
                tags:
                  - Associate
                  - Users
                  - Proficiencies
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
            /analytics-data/instance/{InstanceId}/associations:
              POST:
                summary: BatchDisassociateAnalyticsDataSet
                description: >-
                  <p>This API is in preview release for Amazon Connect and is
                  subject to change.</p> <p>Removes a list of analytics datasets
                  associated with a given Amazon Connect instance. You can
                  disassociate multiple datasets in a single call.</p>
                tags:
                  - Batches
                  - Disassociate
                  - Analytics
                  - Data
                  - Sets
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
            /flow-associations-batch/{InstanceId}:
              POST:
                summary: BatchGetFlowAssociation
                description: <p>Retrieve the flow associations for the given resources.</p>
                tags:
                  - Batches
                  - Get
                  - Flow
                  - Association
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
            /contact/batch/{InstanceId}:
              PUT:
                summary: BatchPutContact
                description: >-
                  <note> <p>Only the Amazon Connect outbound campaigns service
                  principal is allowed to assume a role in your account and call
                  this API.</p> </note> <p>Allows you to create a batch of
                  contacts in Amazon Connect. The outbound campaigns capability
                  ingests dial requests via the <a
                  href="https://docs.aws.amazon.com/connect-outbound/latest/APIReference/API_PutDialRequestBatch.html">PutDialRequestBatch</a>
                  API. It then uses BatchPutContact to create contacts
                  corresponding to those dial requests. If agents are available,
                  the dial requests are dialed out, which results in a voice
                  call. The resulting voice call uses the same contactId that
                  was created by BatchPutContact. </p>
                tags:
                  - Batches
                  - Put
                  - Contacts
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
            /phone-number/claim:
              POST:
                summary: ClaimPhoneNumber
                description: >-
                  <p>Claims an available phone number to your Amazon Connect
                  instance or traffic distribution group. You can call this API
                  only in the same Amazon Web Services Region where the Amazon
                  Connect instance or traffic distribution group was
                  created.</p> <p>For more information about how to use this
                  operation, see <a
                  href="https://docs.aws.amazon.com/connect/latest/adminguide/claim-phone-number.html">Claim
                  a phone number in your country</a> and <a
                  href="https://docs.aws.amazon.com/connect/latest/adminguide/claim-phone-numbers-traffic-distribution-groups.html">Claim
                  phone numbers to traffic distribution groups</a> in the
                  <i>Amazon Connect Administrator Guide</i>. </p> <important>
                  <p>You can call the <a
                  href="https://docs.aws.amazon.com/connect/latest/APIReference/API_SearchAvailablePhoneNumbers.html">SearchAvailablePhoneNumbers</a>
                  API for available phone numbers that you can claim. Call the
                  <a
                  href="https://docs.aws.amazon.com/connect/latest/APIReference/API_DescribePhoneNumber.html">DescribePhoneNumber</a>
                  API to verify the status of a previous <a
                  href="https://docs.aws.amazon.com/connect/latest/APIReference/API_ClaimPhoneNumber.html">ClaimPhoneNumber</a>
                  operation.</p> </important> <p>If you plan to claim and
                  release numbers frequently during a 30 day period, contact us
                  for a service quota exception. Otherwise, it is possible you
                  will be blocked from claiming and releasing any more numbers
                  until 30 days past the oldest number released has expired.</p>
                  <p>By default you can claim and release up to 200% of your
                  maximum number of active phone numbers during any 30 day
                  period. If you claim and release phone numbers using the UI or
                  API during a rolling 30 day cycle that exceeds 200% of your
                  phone number service level quota, you will be blocked from
                  claiming any more numbers until 30 days past the oldest number
                  released has expired. </p> <p>For example, if you already have
                  99 claimed numbers and a service level quota of 99 phone
                  numbers, and in any 30 day period you release 99, claim 99,
                  and then release 99, you will have exceeded the 200% limit. At
                  that point you are blocked from claiming any more numbers
                  until you open an Amazon Web Services support ticket.</p>
                tags:
                  - Claim
                  - Phone
                  - Numbers
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
            /agent-status/{InstanceId}:
              GET:
                summary: ListAgentStatuses
                description: >-
                  <p>This API is in preview release for Amazon Connect and is
                  subject to change.</p> <p>Lists agent statuses.</p>
                tags:
                  - Lists
                  - Agent
                  - Statuses
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
            /contact-flows/{InstanceId}:
              PUT:
                summary: CreateContactFlow
                description: >-
                  <p>Creates a flow for the specified Amazon Connect
                  instance.</p> <p>You can also create and update flows using
                  the <a
                  href="https://docs.aws.amazon.com/connect/latest/APIReference/flow-language.html">Amazon
                  Connect Flow language</a>.</p>
                tags:
                  - Create
                  - Contacts
                  - Flow
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
            /contact-flow-modules/{InstanceId}:
              PUT:
                summary: CreateContactFlowModule
                description: >-
                  <p>Creates a flow module for the specified Amazon Connect
                  instance. </p>
                tags:
                  - Create
                  - Contacts
                  - Flow
                  - Modules
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
            /evaluation-forms/{InstanceId}:
              GET:
                summary: ListEvaluationForms
                description: >-
                  <p>Lists evaluation forms in the specified Amazon Connect
                  instance.</p>
                tags:
                  - Lists
                  - Evaluations
                  - Forms
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
            /hours-of-operations/{InstanceId}:
              PUT:
                summary: CreateHoursOfOperation
                description: >-
                  <p>This API is in preview release for Amazon Connect and is
                  subject to change.</p> <p>Creates hours of operation. </p>
                tags:
                  - Create
                  - Hours
                  - Of
                  - Operation
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
            /instance:
              GET:
                summary: ListInstances
                description: >-
                  <p>This API is in preview release for Amazon Connect and is
                  subject to change.</p> <p>Return a list of instances which are
                  in active state, creation-in-progress state, and failed state.
                  Instances that aren't successfully created (they are in a
                  failed state) are returned only for 24 hours after the
                  CreateInstance API was invoked.</p>
                tags:
                  - Lists
                  - Instances
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
            /instance/{InstanceId}/integration-associations:
              GET:
                summary: ListIntegrationAssociations
                description: >-
                  <p>Provides summary information about the Amazon Web Services
                  resource associations for the specified Amazon Connect
                  instance.</p>
                tags:
                  - Lists
                  - Integrations
                  - Associations
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
            /contact/create-participant:
              POST:
                summary: CreateParticipant
                description: >-
                  <p>Adds a new participant into an on-going chat contact. For
                  more information, see <a
                  href="https://docs.aws.amazon.com/connect/latest/adminguide/chat-customize-flow.html">Customize
                  chat flow experiences by integrating custom
                  participants</a>.</p>
                tags:
                  - Create
                  - Participants
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
            /contact/persistent-contact-association/{InstanceId}/{InitialContactId}:
              POST:
                summary: CreatePersistentContactAssociation
                description: >-
                  <p>Enables rehydration of chats for the lifespan of a contact.
                  For more information about chat rehydration, see <a
                  href="https://docs.aws.amazon.com/connect/latest/adminguide/chat-persistence.html">Enable
                  persistent chat</a> in the <i>Amazon Connect Administrator
                  Guide</i>. </p>
                tags:
                  - Create
                  - Persistent
                  - Contacts
                  - Association
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
            /predefined-attributes/{InstanceId}:
              GET:
                summary: ListPredefinedAttributes
                description: >-
                  <p>Lists predefined attributes for the specified Amazon
                  Connect instance.</p>
                tags:
                  - Lists
                  - Predefined
                  - Attributes
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
            /prompts/{InstanceId}:
              PUT:
                summary: CreatePrompt
                description: >-
                  <p>Creates a prompt. For more information about prompts, such
                  as supported file types and maximum length, see <a
                  href="https://docs.aws.amazon.com/connect/latest/adminguide/prompts.html">Create
                  prompts</a> in the <i>Amazon Connect Administrator's
                  Guide</i>.</p>
                tags:
                  - Create
                  - Prompts
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
            /queues/{InstanceId}:
              PUT:
                summary: CreateQueue
                description: >-
                  <p>This API is in preview release for Amazon Connect and is
                  subject to change.</p> <p>Creates a new queue for the
                  specified Amazon Connect instance.</p> <important> <ul> <li>
                  <p>If the phone number is claimed to a traffic distribution
                  group that was created in the same Region as the Amazon
                  Connect instance where you are calling this API, then you can
                  use a full phone number ARN or a UUID for
                  <code>OutboundCallerIdNumberId</code>. However, if the phone
                  number is claimed to a traffic distribution group that is in
                  one Region, and you are calling this API from an instance in
                  another Amazon Web Services Region that is associated with the
                  traffic distribution group, you must provide a full phone
                  number ARN. If a UUID is provided in this scenario, you will
                  receive a <code>ResourceNotFoundException</code>.</p> </li>
                  <li> <p>Only use the phone number ARN format that doesn't
                  contain <code>instance</code> in the path, for example,
                  <code>arn:aws:connect:us-east-1:1234567890:phone-number/uuid</code>.
                  This is the same ARN format that is returned when you call the
                  <a
                  href="https://docs.aws.amazon.com/connect/latest/APIReference/API_ListPhoneNumbersV2.html">ListPhoneNumbersV2</a>
                  API.</p> </li> <li> <p>If you plan to use IAM policies to
                  allow/deny access to this API for phone number resources
                  claimed to a traffic distribution group, see <a
                  href="https://docs.aws.amazon.com/connect/latest/adminguide/security_iam_resource-level-policy-examples.html#allow-deny-queue-actions-replica-region">Allow
                  or Deny queue API actions for phone numbers in a replica
                  Region</a>.</p> </li> </ul> </important>
                tags:
                  - Create
                  - Queues
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
            /quick-connects/{InstanceId}:
              GET:
                summary: ListQuickConnects
                description: >-
                  <p>Provides information about the quick connects for the
                  specified Amazon Connect instance. </p>
                tags:
                  - Lists
                  - Quick
                  - Connects
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
            /routing-profiles/{InstanceId}:
              PUT:
                summary: CreateRoutingProfile
                description: <p>Creates a new routing profile.</p>
                tags:
                  - Create
                  - Routing
                  - Profiles
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
            /rules/{InstanceId}:
              GET:
                summary: ListRules
                description: >-
                  <p>List all rules for the specified Amazon Connect
                  instance.</p>
                tags:
                  - Lists
                  - Rules
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
            /security-profiles/{InstanceId}:
              PUT:
                summary: CreateSecurityProfile
                description: <p>Creates a security profile.</p>
                tags:
                  - Create
                  - Security
                  - Profiles
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
            /instance/{InstanceId}/task/template:
              GET:
                summary: ListTaskTemplates
                description: >-
                  <p>Lists task templates for the specified Amazon Connect
                  instance.</p>
                tags:
                  - Lists
                  - Tasks
                  - Templates
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
            /traffic-distribution-group:
              PUT:
                summary: CreateTrafficDistributionGroup
                description: >-
                  <p>Creates a traffic distribution group given an Amazon
                  Connect instance that has been replicated. </p> <note> <p>The
                  <code>SignInConfig</code> distribution is available only on a
                  default <code>TrafficDistributionGroup</code> (see the
                  <code>IsDefault</code> parameter in the <a
                  href="https://docs.aws.amazon.com/connect/latest/APIReference/API_TrafficDistributionGroup.html">TrafficDistributionGroup</a>
                  data type). If you call <code>UpdateTrafficDistribution</code>
                  with a modified <code>SignInConfig</code> and a non-default
                  <code>TrafficDistributionGroup</code>, an
                  <code>InvalidRequestException</code> is returned.</p> </note>
                  <p>For more information about creating traffic distribution
                  groups, see <a
                  href="https://docs.aws.amazon.com/connect/latest/adminguide/setup-traffic-distribution-groups.html">Set
                  up traffic distribution groups</a> in the <i>Amazon Connect
                  Administrator Guide</i>. </p>
                tags:
                  - Create
                  - Traffic
                  - Distributions
                  - Group
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
            /instance/{InstanceId}/integration-associations/{IntegrationAssociationId}/use-cases:
              GET:
                summary: ListUseCases
                description: <p>Lists the use cases for the integration association. </p>
                tags:
                  - Lists
                  - Use
                  - Cases
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
            /users/{InstanceId}:
              PUT:
                summary: CreateUser
                description: >-
                  <p>Creates a user account for the specified Amazon Connect
                  instance.</p> <important> <p>Certain <a
                  href="https://docs.aws.amazon.com/connect/latest/APIReference/API_UserIdentityInfo.html">UserIdentityInfo</a>
                  parameters are required in some situations. For example,
                  <code>Email</code> is required if you are using SAML for
                  identity management. <code>FirstName</code> and
                  <code>LastName</code> are required if you are using Amazon
                  Connect or SAML for identity management.</p> </important>
                  <p>For information about how to create users using the Amazon
                  Connect admin website, see <a
                  href="https://docs.aws.amazon.com/connect/latest/adminguide/user-management.html">Add
                  Users</a> in the <i>Amazon Connect Administrator
                  Guide</i>.</p>
                tags:
                  - Create
                  - Users
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
            /user-hierarchy-groups/{InstanceId}:
              PUT:
                summary: CreateUserHierarchyGroup
                description: <p>Creates a new user hierarchy group.</p>
                tags:
                  - Create
                  - Users
                  - Hierarchy
                  - Group
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
            /views/{InstanceId}:
              GET:
                summary: ListViews
                description: >-
                  <p>Returns views in the given instance.</p> <p>Results are
                  sorted primarily by type, and secondarily by name.</p>
                tags:
                  - Lists
                  - Views
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
            /views/{InstanceId}/{ViewId}/versions:
              GET:
                summary: ListViewVersions
                description: >-
                  <p>Returns all the available versions for the specified Amazon
                  Connect instance and view identifier.</p> <p>Results will be
                  sorted from highest to lowest.</p>
                tags:
                  - Lists
                  - View
                  - Versions
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
            /vocabulary/{InstanceId}:
              POST:
                summary: CreateVocabulary
                description: >-
                  <p>Creates a custom vocabulary associated with your Amazon
                  Connect instance. You can set a custom vocabulary to be your
                  default vocabulary for a given language. Contact Lens for
                  Amazon Connect uses the default vocabulary in post-call and
                  real-time contact analysis sessions for that language.</p>
                tags:
                  - Create
                  - Vocabularies
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
            /evaluation-forms/{InstanceId}/{EvaluationFormId}/deactivate:
              POST:
                summary: DeactivateEvaluationForm
                description: >-
                  <p>Deactivates an evaluation form in the specified Amazon
                  Connect instance. After a form is deactivated, it is no longer
                  available for users to start new evaluations based on the
                  form. </p>
                tags:
                  - Deactivate
                  - Evaluations
                  - Forms
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
            /contact-evaluations/{InstanceId}/{EvaluationId}:
              POST:
                summary: UpdateContactEvaluation
                description: >-
                  <p>Updates details about a contact evaluation in the specified
                  Amazon Connect instance. A contact evaluation must be in draft
                  state. Answers included in the request are merged with
                  existing answers for the given evaluation. An answer or note
                  can be deleted by passing an empty object (<code>{}</code>) to
                  the question identifier. </p>
                tags:
                  - Update
                  - Contacts
                  - Evaluations
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
            /contact-flows/{InstanceId}/{ContactFlowId}:
              GET:
                summary: DescribeContactFlow
                description: >-
                  <p>Describes the specified flow.</p> <p>You can also create
                  and update flows using the <a
                  href="https://docs.aws.amazon.com/connect/latest/APIReference/flow-language.html">Amazon
                  Connect Flow language</a>.</p>
                tags:
                  - Describe
                  - Contacts
                  - Flow
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
            /contact-flow-modules/{InstanceId}/{ContactFlowModuleId}:
              GET:
                summary: DescribeContactFlowModule
                description: <p>Describes the specified flow module.</p>
                tags:
                  - Describe
                  - Contacts
                  - Flow
                  - Modules
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
            /evaluation-forms/{InstanceId}/{EvaluationFormId}:
              PUT:
                summary: UpdateEvaluationForm
                description: >-
                  <p>Updates details about a specific evaluation form version in
                  the specified Amazon Connect instance. Question and section
                  identifiers cannot be duplicated within the same evaluation
                  form.</p> <p>This operation does not support partial updates.
                  Instead it does a full update of evaluation form content.</p>
                tags:
                  - Update
                  - Evaluations
                  - Forms
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
            /hours-of-operations/{InstanceId}/{HoursOfOperationId}:
              POST:
                summary: UpdateHoursOfOperation
                description: >-
                  <p>This API is in preview release for Amazon Connect and is
                  subject to change.</p> <p>Updates the hours of operation.</p>
                tags:
                  - Update
                  - Hours
                  - Of
                  - Operation
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
            /instance/{InstanceId}:
              GET:
                summary: DescribeInstance
                description: >-
                  <p>This API is in preview release for Amazon Connect and is
                  subject to change.</p> <p>Returns the current state of the
                  specified instance identifier. It tracks the instance while it
                  is being created and returns an error status, if applicable.
                  </p> <p>If an instance is not created successfully, the
                  instance status reason field returns details relevant to the
                  reason. The instance in a failed state is returned only for 24
                  hours after the CreateInstance API was invoked.</p>
                tags:
                  - Describe
                  - Instances
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
            /instance/{InstanceId}/integration-associations/{IntegrationAssociationId}:
              DELETE:
                summary: DeleteIntegrationAssociation
                description: >-
                  <p>Deletes an Amazon Web Services resource association from an
                  Amazon Connect instance. The association must not have any use
                  cases associated with it.</p>
                tags:
                  - Delete
                  - Integrations
                  - Association
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
            /predefined-attributes/{InstanceId}/{Name}:
              POST:
                summary: UpdatePredefinedAttribute
                description: >-
                  <p>Updates a predefined attribute for the specified Amazon
                  Connect instance.</p>
                tags:
                  - Update
                  - Predefined
                  - Attributes
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
            /prompts/{InstanceId}/{PromptId}:
              POST:
                summary: UpdatePrompt
                description: <p>Updates a prompt.</p>
                tags:
                  - Update
                  - Prompts
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
            /queues/{InstanceId}/{QueueId}:
              GET:
                summary: DescribeQueue
                description: >-
                  <p>This API is in preview release for Amazon Connect and is
                  subject to change.</p> <p>Describes the specified queue.</p>
                tags:
                  - Describe
                  - Queues
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
            /quick-connects/{InstanceId}/{QuickConnectId}:
              GET:
                summary: DescribeQuickConnect
                description: <p>Describes the quick connect.</p>
                tags:
                  - Describe
                  - Quick
                  - Connect
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
            /routing-profiles/{InstanceId}/{RoutingProfileId}:
              GET:
                summary: DescribeRoutingProfile
                description: <p>Describes the specified routing profile.</p>
                tags:
                  - Describe
                  - Routing
                  - Profiles
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
            /rules/{InstanceId}/{RuleId}:
              PUT:
                summary: UpdateRule
                description: >-
                  <p>Updates a rule for the specified Amazon Connect
                  instance.</p> <p>Use the <a
                  href="https://docs.aws.amazon.com/connect/latest/APIReference/connect-rules-language.html">Rules
                  Function language</a> to code conditions for the rule. </p>
                tags:
                  - Update
                  - Rules
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
            /security-profiles/{InstanceId}/{SecurityProfileId}:
              POST:
                summary: UpdateSecurityProfile
                description: <p>Updates a security profile.</p>
                tags:
                  - Update
                  - Security
                  - Profiles
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
            /instance/{InstanceId}/task/template/{TaskTemplateId}:
              POST:
                summary: UpdateTaskTemplate
                description: >-
                  <p>Updates details about a specific task template in the
                  specified Amazon Connect instance. This operation does not
                  support partial updates. Instead it does a full update of
                  template content.</p>
                tags:
                  - Update
                  - Tasks
                  - Templates
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
            /traffic-distribution-group/{TrafficDistributionGroupId}:
              GET:
                summary: DescribeTrafficDistributionGroup
                description: >-
                  <p>Gets details and status of a traffic distribution
                  group.</p>
                tags:
                  - Describe
                  - Traffic
                  - Distributions
                  - Group
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
            /instance/{InstanceId}/integration-associations/{IntegrationAssociationId}/use-cases/{UseCaseId}:
              DELETE:
                summary: DeleteUseCase
                description: <p>Deletes a use case from an integration association.</p>
                tags:
                  - Delete
                  - Use
                  - Case
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
            /users/{InstanceId}/{UserId}:
              GET:
                summary: DescribeUser
                description: >-
                  <p>Describes the specified user. You can <a
                  href="https://docs.aws.amazon.com/connect/latest/adminguide/find-instance-arn.html">find
                  the instance ID in the Amazon Connect console</a> (it’s the
                  final part of the ARN). The console does not display the user
                  IDs. Instead, list the users and note the IDs provided in the
                  output.</p>
                tags:
                  - Describe
                  - Users
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
            /user-hierarchy-groups/{InstanceId}/{HierarchyGroupId}:
              GET:
                summary: DescribeUserHierarchyGroup
                description: <p>Describes the specified hierarchy group.</p>
                tags:
                  - Describe
                  - Users
                  - Hierarchy
                  - Group
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
            /views/{InstanceId}/{ViewId}:
              POST:
                summary: UpdateViewContent
                description: >-
                  <p>Updates the view content of the given view identifier in
                  the specified Amazon Connect instance.</p> <p>It performs
                  content validation if <code>Status</code> is set to
                  <code>SAVED</code> and performs full content validation if
                  <code>Status</code> is <code>PUBLISHED</code>. Note that the
                  <code>$SAVED</code> alias' content will always be updated, but
                  the <code>$LATEST</code> alias' content will only be updated
                  if <code>Status</code> is <code>PUBLISHED</code>.</p>
                tags:
                  - Update
                  - View
                  - Content
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
            /views/{InstanceId}/{ViewId}/versions/{ViewVersion}:
              DELETE:
                summary: DeleteViewVersion
                description: >-
                  <p>Deletes the particular version specified in
                  <code>ViewVersion</code> identifier.</p>
                tags:
                  - Delete
                  - View
                  - Versions
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
            /vocabulary-remove/{InstanceId}/{VocabularyId}:
              POST:
                summary: DeleteVocabulary
                description: <p>Deletes the vocabulary that has the given identifier.</p>
                tags:
                  - Delete
                  - Vocabularies
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
            /agent-status/{InstanceId}/{AgentStatusId}:
              POST:
                summary: UpdateAgentStatus
                description: >-
                  <p>This API is in preview release for Amazon Connect and is
                  subject to change.</p> <p>Updates agent status.</p>
                tags:
                  - Update
                  - Agent
                  - Status
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
            /contacts/{InstanceId}/{ContactId}:
              POST:
                summary: UpdateContact
                description: >-
                  <p>This API is in preview release for Amazon Connect and is
                  subject to change.</p> <p>Adds or updates user-defined contact
                  information associated with the specified contact. At least
                  one field to be updated must be present in the request.</p>
                  <important> <p>You can add or update user-defined contact
                  information for both ongoing and completed contacts.</p>
                  </important>
                tags:
                  - Update
                  - Contacts
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
            /instance/{InstanceId}/attribute/{AttributeType}:
              POST:
                summary: UpdateInstanceAttribute
                description: >-
                  <p>This API is in preview release for Amazon Connect and is
                  subject to change.</p> <p>Updates the value for the specified
                  attribute type.</p>
                tags:
                  - Update
                  - Instances
                  - Attributes
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
            /instance/{InstanceId}/storage-config/{AssociationId}:
              POST:
                summary: UpdateInstanceStorageConfig
                description: >-
                  <p>This API is in preview release for Amazon Connect and is
                  subject to change.</p> <p>Updates an existing configuration
                  for a resource type. This API is idempotent.</p>
                tags:
                  - Update
                  - Instances
                  - Storage
                  - Configurations
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
            /phone-number/{PhoneNumberId}:
              PUT:
                summary: UpdatePhoneNumber
                description: >-
                  <p>Updates your claimed phone number from its current Amazon
                  Connect instance or traffic distribution group to another
                  Amazon Connect instance or traffic distribution group in the
                  same Amazon Web Services Region.</p> <important> <p>After
                  using this API, you must verify that the phone number is
                  attached to the correct flow in the target instance or traffic
                  distribution group. You need to do this because the API
                  switches only the phone number to a new instance or traffic
                  distribution group. It doesn't migrate the flow configuration
                  of the phone number, too.</p> <p>You can call <a
                  href="https://docs.aws.amazon.com/connect/latest/APIReference/API_DescribePhoneNumber.html">DescribePhoneNumber</a>
                  API to verify the status of a previous <a
                  href="https://docs.aws.amazon.com/connect/latest/APIReference/API_UpdatePhoneNumber.html">UpdatePhoneNumber</a>
                  operation.</p> </important>
                tags:
                  - Update
                  - Phone
                  - Numbers
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
            /user-hierarchy-structure/{InstanceId}:
              POST:
                summary: UpdateUserHierarchyStructure
                description: >-
                  <p>Updates the user hierarchy structure: add, remove, and
                  rename user hierarchy levels.</p>
                tags:
                  - Update
                  - Users
                  - Hierarchy
                  - Structures
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
            /vocabulary/{InstanceId}/{VocabularyId}:
              GET:
                summary: DescribeVocabulary
                description: <p>Describes the specified vocabulary.</p>
                tags:
                  - Describe
                  - Vocabularies
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
            /flow-associations/{InstanceId}/{ResourceId}/{ResourceType}:
              GET:
                summary: GetFlowAssociation
                description: <p>Retrieves the flow associated for a given resource.</p>
                tags:
                  - Get
                  - Flow
                  - Association
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
            /queues/{InstanceId}/{QueueId}/disassociate-quick-connects:
              POST:
                summary: DisassociateQueueQuickConnects
                description: >-
                  <p>This API is in preview release for Amazon Connect and is
                  subject to change.</p> <p>Disassociates a set of quick
                  connects from a queue.</p>
                tags:
                  - Disassociate
                  - Queues
                  - Quick
                  - Connects
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
            /routing-profiles/{InstanceId}/{RoutingProfileId}/disassociate-queues:
              POST:
                summary: DisassociateRoutingProfileQueues
                description: <p>Disassociates a set of queues from a routing profile.</p>
                tags:
                  - Disassociate
                  - Routing
                  - Profiles
                  - Queues
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
            /instance/{InstanceId}/security-key/{AssociationId}:
              DELETE:
                summary: DisassociateSecurityKey
                description: >-
                  <p>This API is in preview release for Amazon Connect and is
                  subject to change.</p> <p>Deletes the specified security
                  key.</p>
                tags:
                  - Disassociate
                  - Security
                  - Keys
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
            /users/{InstanceId}/{UserId}/disassociate-proficiencies:
              POST:
                summary: DisassociateUserProficiencies
                description: <p>Disassociates a set of proficiencies from a user.</p>
                tags:
                  - Disassociate
                  - Users
                  - Proficiencies
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
            /users/{InstanceId}/{UserId}/contact:
              POST:
                summary: DismissUserContact
                description: >-
                  <p>Dismisses contacts from an agent’s CCP and returns the
                  agent to an available state, which allows the agent to receive
                  a new routed contact. Contacts can only be dismissed if they
                  are in a <code>MISSED</code>, <code>ERROR</code>,
                  <code>ENDED</code>, or <code>REJECTED</code> state in the <a
                  href="https://docs.aws.amazon.com/connect/latest/adminguide/about-contact-states.html">Agent
                  Event Stream</a>.</p>
                tags:
                  - Dismiss
                  - Users
                  - Contacts
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
            /contact/attributes/{InstanceId}/{InitialContactId}:
              GET:
                summary: GetContactAttributes
                description: >-
                  <p>Retrieves the contact attributes for the specified
                  contact.</p>
                tags:
                  - Get
                  - Contacts
                  - Attributes
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
            /metrics/current/{InstanceId}:
              POST:
                summary: GetCurrentMetricData
                description: >-
                  <p>Gets the real-time metric data from the specified Amazon
                  Connect instance.</p> <p>For a description of each metric, see
                  <a
                  href="https://docs.aws.amazon.com/connect/latest/adminguide/real-time-metrics-definitions.html">Real-time
                  Metrics Definitions</a> in the <i>Amazon Connect Administrator
                  Guide</i>.</p>
                tags:
                  - Get
                  - Current
                  - Metrics
                  - Data
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
            /metrics/userdata/{InstanceId}:
              POST:
                summary: GetCurrentUserData
                description: >-
                  <p>Gets the real-time active user data from the specified
                  Amazon Connect instance. </p>
                tags:
                  - Get
                  - Current
                  - Users
                  - Data
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
            /user/federate/{InstanceId}:
              GET:
                summary: GetFederationToken
                description: >-
                  <p>Supports SAML sign-in for Amazon Connect. Retrieves a token
                  for federation. The token is for the Amazon Connect user which
                  corresponds to the IAM credentials that were used to invoke
                  this action. </p> <p>For more information about how SAML
                  sign-in works in Amazon Connect, see <a
                  href="https://docs.aws.amazon.com/connect/latest/adminguide/configure-saml.html
                  ">Configure SAML with IAM for Amazon Connect in the <i>Amazon
                  Connect Administrator Guide</i>.</a> </p> <note> <p>This API
                  doesn't support root users. If you try to invoke
                  GetFederationToken with root credentials, an error message
                  similar to the following one appears: </p> <p> <code>Provided
                  identity: Principal: .... User: .... cannot be used for
                  federation with Amazon Connect</code> </p> </note>
                tags:
                  - Get
                  - Federation
                  - Tokens
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
            /metrics/historical/{InstanceId}:
              POST:
                summary: GetMetricData
                description: >-
                  <p>Gets historical metric data from the specified Amazon
                  Connect instance.</p> <p>For a description of each historical
                  metric, see <a
                  href="https://docs.aws.amazon.com/connect/latest/adminguide/historical-metrics-definitions.html">Historical
                  Metrics Definitions</a> in the <i>Amazon Connect Administrator
                  Guide</i>.</p> <note> <p>We recommend using the <a
                  href="https://docs.aws.amazon.com/connect/latest/APIReference/API_GetMetricDataV2.html">GetMetricDataV2</a>
                  API. It provides more flexibility, features, and the ability
                  to query longer time ranges than <code>GetMetricData</code>.
                  Use it to retrieve historical agent and contact metrics for
                  the last 3 months, at varying intervals. You can also use it
                  to build custom dashboards to measure historical queue and
                  agent performance. For example, you can track the number of
                  incoming contacts for the last 7 days, with data split by day,
                  to see how contact volume changed per day of the week.</p>
                  </note>
                tags:
                  - Get
                  - Metrics
                  - Data
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
            /metrics/data:
              POST:
                summary: GetMetricDataV2
                description: >-
                  <p>Gets metric data from the specified Amazon Connect
                  instance. </p> <p> <code>GetMetricDataV2</code> offers more
                  features than <a
                  href="https://docs.aws.amazon.com/connect/latest/APIReference/API_GetMetricData.html">GetMetricData</a>,
                  the previous version of this API. It has new metrics, offers
                  filtering at a metric level, and offers the ability to filter
                  and group data by channels, queues, routing profiles, agents,
                  and agent hierarchy levels. It can retrieve historical data
                  for the last 3 months, at varying intervals. </p> <p>For a
                  description of the historical metrics that are supported by
                  <code>GetMetricDataV2</code> and <code>GetMetricData</code>,
                  see <a
                  href="https://docs.aws.amazon.com/connect/latest/adminguide/historical-metrics-definitions.html">Historical
                  metrics definitions</a> in the <i>Amazon Connect
                  Administrator's Guide</i>.</p>
                tags:
                  - Get
                  - Metrics
                  - Data
                  - V2
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
            /prompts/{InstanceId}/{PromptId}/file:
              GET:
                summary: GetPromptFile
                description: <p>Gets the prompt file.</p>
                tags:
                  - Get
                  - Prompts
                  - File
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
            /traffic-distribution/{Id}:
              PUT:
                summary: UpdateTrafficDistribution
                description: >-
                  <p>Updates the traffic distribution for a given traffic
                  distribution group. </p> <note> <p>The
                  <code>SignInConfig</code> distribution is available only on a
                  default <code>TrafficDistributionGroup</code> (see the
                  <code>IsDefault</code> parameter in the <a
                  href="https://docs.aws.amazon.com/connect/latest/APIReference/API_TrafficDistributionGroup.html">TrafficDistributionGroup</a>
                  data type). If you call <code>UpdateTrafficDistribution</code>
                  with a modified <code>SignInConfig</code> and a non-default
                  <code>TrafficDistributionGroup</code>, an
                  <code>InvalidRequestException</code> is returned.</p> </note>
                  <p>For more information about updating a traffic distribution
                  group, see <a
                  href="https://docs.aws.amazon.com/connect/latest/adminguide/update-telephony-traffic-distribution.html">Update
                  telephony traffic distribution across Amazon Web Services
                  Regions </a> in the <i>Amazon Connect Administrator Guide</i>.
                  </p>
                tags:
                  - Update
                  - Traffic
                  - Distributions
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
            /phone-number/import:
              POST:
                summary: ImportPhoneNumber
                description: >-
                  <p>Imports a claimed phone number from an external service,
                  such as Amazon Pinpoint, into an Amazon Connect instance. You
                  can call this API only in the same Amazon Web Services Region
                  where the Amazon Connect instance was created.</p>
                tags:
                  - Import
                  - Phone
                  - Numbers
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
            /instance/{InstanceId}/approved-origins:
              GET:
                summary: ListApprovedOrigins
                description: >-
                  <p>This API is in preview release for Amazon Connect and is
                  subject to change.</p> <p>Returns a paginated list of all
                  approved origins associated with the instance.</p>
                tags:
                  - Lists
                  - Approved
                  - Origins
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
            /instance/{InstanceId}/bots:
              GET:
                summary: ListBots
                description: >-
                  <p>This API is in preview release for Amazon Connect and is
                  subject to change.</p> <p>For the specified version of Amazon
                  Lex, returns a paginated list of all the Amazon Lex bots
                  currently associated with the instance. Use this API to
                  returns both Amazon Lex V1 and V2 bots.</p>
                tags:
                  - Lists
                  - Bots
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
            /contact-evaluations/{InstanceId}:
              PUT:
                summary: StartContactEvaluation
                description: >-
                  <p>Starts an empty evaluation in the specified Amazon Connect
                  instance, using the given evaluation form for the particular
                  contact. The evaluation form version used for the contact
                  evaluation corresponds to the currently activated version. If
                  no version is activated for the evaluation form, the contact
                  evaluation cannot be started. </p> <note> <p>Evaluations
                  created through the public API do not contain answer values
                  suggested from automation.</p> </note>
                tags:
                  - Start
                  - Contacts
                  - Evaluations
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
            /contact-flow-modules-summary/{InstanceId}:
              GET:
                summary: ListContactFlowModules
                description: >-
                  <p>Provides information about the flow modules for the
                  specified Amazon Connect instance.</p>
                tags:
                  - Lists
                  - Contacts
                  - Flow
                  - Modules
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
            /contact-flows-summary/{InstanceId}:
              GET:
                summary: ListContactFlows
                description: >-
                  <p>Provides information about the flows for the specified
                  Amazon Connect instance.</p> <p>You can also create and update
                  flows using the <a
                  href="https://docs.aws.amazon.com/connect/latest/APIReference/flow-language.html">Amazon
                  Connect Flow language</a>.</p> <p>For more information about
                  flows, see <a
                  href="https://docs.aws.amazon.com/connect/latest/adminguide/concepts-contact-flows.html">Flows</a>
                  in the <i>Amazon Connect Administrator Guide</i>.</p>
                tags:
                  - Lists
                  - Contacts
                  - Flows
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
            /contact/references/{InstanceId}/{ContactId}:
              GET:
                summary: ListContactReferences
                description: >-
                  <p>This API is in preview release for Amazon Connect and is
                  subject to change.</p> <p>For the specified
                  <code>referenceTypes</code>, returns a list of references
                  associated with the contact. </p>
                tags:
                  - Lists
                  - Contacts
                  - References
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
            /default-vocabulary-summary/{InstanceId}:
              POST:
                summary: ListDefaultVocabularies
                description: >-
                  <p>Lists the default vocabularies for the specified Amazon
                  Connect instance.</p>
                tags:
                  - Lists
                  - Default
                  - Vocabularies
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
            /evaluation-forms/{InstanceId}/{EvaluationFormId}/versions:
              GET:
                summary: ListEvaluationFormVersions
                description: >-
                  <p>Lists versions of an evaluation form in the specified
                  Amazon Connect instance.</p>
                tags:
                  - Lists
                  - Evaluations
                  - Forms
                  - Versions
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
            /flow-associations-summary/{InstanceId}:
              GET:
                summary: ListFlowAssociations
                description: <p>List the flow association based on the filters.</p>
                tags:
                  - Lists
                  - Flow
                  - Associations
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
            /hours-of-operations-summary/{InstanceId}:
              GET:
                summary: ListHoursOfOperations
                description: >-
                  <p>Provides information about the hours of operation for the
                  specified Amazon Connect instance.</p> <p>For more information
                  about hours of operation, see <a
                  href="https://docs.aws.amazon.com/connect/latest/adminguide/set-hours-operation.html">Set
                  the Hours of Operation for a Queue</a> in the <i>Amazon
                  Connect Administrator Guide</i>.</p>
                tags:
                  - Lists
                  - Hours
                  - Of
                  - Operations
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
            /instance/{InstanceId}/attributes:
              GET:
                summary: ListInstanceAttributes
                description: >-
                  <p>This API is in preview release for Amazon Connect and is
                  subject to change.</p> <p>Returns a paginated list of all
                  attribute types for the given instance.</p>
                tags:
                  - Lists
                  - Instances
                  - Attributes
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
            /instance/{InstanceId}/storage-configs:
              GET:
                summary: ListInstanceStorageConfigs
                description: >-
                  <p>This API is in preview release for Amazon Connect and is
                  subject to change.</p> <p>Returns a paginated list of storage
                  configs for the identified instance and resource type.</p>
                tags:
                  - Lists
                  - Instances
                  - Storage
                  - Configurations
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
            /instance/{InstanceId}/lambda-functions:
              GET:
                summary: ListLambdaFunctions
                description: >-
                  <p>This API is in preview release for Amazon Connect and is
                  subject to change.</p> <p>Returns a paginated list of all
                  Lambda functions that display in the dropdown options in the
                  relevant flow blocks.</p>
                tags:
                  - Lists
                  - Lambda
                  - Functions
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
            /instance/{InstanceId}/lex-bots:
              GET:
                summary: ListLexBots
                description: >-
                  <p>This API is in preview release for Amazon Connect and is
                  subject to change.</p> <p>Returns a paginated list of all the
                  Amazon Lex V1 bots currently associated with the instance. To
                  return both Amazon Lex V1 and V2 bots, use the <a
                  href="https://docs.aws.amazon.com/connect/latest/APIReference/API_ListBots.html">ListBots</a>
                  API. </p>
                tags:
                  - Lists
                  - Lex
                  - Bots
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
            /phone-numbers-summary/{InstanceId}:
              GET:
                summary: ListPhoneNumbers
                description: >-
                  <p>Provides information about the phone numbers for the
                  specified Amazon Connect instance. </p> <p>For more
                  information about phone numbers, see <a
                  href="https://docs.aws.amazon.com/connect/latest/adminguide/contact-center-phone-number.html">Set
                  Up Phone Numbers for Your Contact Center</a> in the <i>Amazon
                  Connect Administrator Guide</i>.</p> <important> <ul> <li>
                  <p>We recommend using <a
                  href="https://docs.aws.amazon.com/connect/latest/APIReference/API_ListPhoneNumbersV2.html">ListPhoneNumbersV2</a>
                  to return phone number types. ListPhoneNumbers doesn't support
                  number types <code>UIFN</code>, <code>SHARED</code>,
                  <code>THIRD_PARTY_TF</code>, and <code>THIRD_PARTY_DID</code>.
                  While it returns numbers of those types, it incorrectly lists
                  them as <code>TOLL_FREE</code> or <code>DID</code>. </p> </li>
                  <li> <p>The phone number <code>Arn</code> value that is
                  returned from each of the items in the <a
                  href="https://docs.aws.amazon.com/connect/latest/APIReference/API_ListPhoneNumbers.html#connect-ListPhoneNumbers-response-PhoneNumberSummaryList">PhoneNumberSummaryList</a>
                  cannot be used to tag phone number resources. It will fail
                  with a <code>ResourceNotFoundException</code>. Instead, use
                  the <a
                  href="https://docs.aws.amazon.com/connect/latest/APIReference/API_ListPhoneNumbersV2.html">ListPhoneNumbersV2</a>
                  API. It returns the new phone number ARN that can be used to
                  tag phone number resources.</p> </li> </ul> </important>
                tags:
                  - Lists
                  - Phone
                  - Numbers
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
            /phone-number/list:
              POST:
                summary: ListPhoneNumbersV2
                description: >-
                  <p>Lists phone numbers claimed to your Amazon Connect instance
                  or traffic distribution group. If the provided
                  <code>TargetArn</code> is a traffic distribution group, you
                  can call this API in both Amazon Web Services Regions
                  associated with traffic distribution group.</p> <p>For more
                  information about phone numbers, see <a
                  href="https://docs.aws.amazon.com/connect/latest/adminguide/contact-center-phone-number.html">Set
                  Up Phone Numbers for Your Contact Center</a> in the <i>Amazon
                  Connect Administrator Guide</i>.</p> <note> <ul> <li> <p>When
                  given an instance ARN, <code>ListPhoneNumbersV2</code> returns
                  only the phone numbers claimed to the instance.</p> </li> <li>
                  <p>When given a traffic distribution group ARN
                  <code>ListPhoneNumbersV2</code> returns only the phone numbers
                  claimed to the traffic distribution group.</p> </li> </ul>
                  </note>
                tags:
                  - Lists
                  - Phone
                  - Numbers
                  - V2
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
            /prompts-summary/{InstanceId}:
              GET:
                summary: ListPrompts
                description: >-
                  <p>Provides information about the prompts for the specified
                  Amazon Connect instance.</p>
                tags:
                  - Lists
                  - Prompts
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
            /queues/{InstanceId}/{QueueId}/quick-connects:
              GET:
                summary: ListQueueQuickConnects
                description: >-
                  <p>This API is in preview release for Amazon Connect and is
                  subject to change.</p> <p>Lists the quick connects associated
                  with a queue.</p>
                tags:
                  - Lists
                  - Queues
                  - Quick
                  - Connects
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
            /queues-summary/{InstanceId}:
              GET:
                summary: ListQueues
                description: >-
                  <p>Provides information about the queues for the specified
                  Amazon Connect instance.</p> <p>If you do not specify a
                  <code>QueueTypes</code> parameter, both standard and agent
                  queues are returned. This might cause an unexpected truncation
                  of results if you have more than 1000 agents and you limit the
                  number of results of the API call in code.</p> <p>For more
                  information about queues, see <a
                  href="https://docs.aws.amazon.com/connect/latest/adminguide/concepts-queues-standard-and-agent.html">Queues:
                  Standard and Agent</a> in the <i>Amazon Connect Administrator
                  Guide</i>.</p>
                tags:
                  - Lists
                  - Queues
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
            /contact/list-real-time-analysis-segments-v2/{InstanceId}/{ContactId}:
              POST:
                summary: ListRealtimeContactAnalysisSegmentsV2
                description: >-
                  <p>Provides a list of analysis segments for a real-time
                  analysis session. </p>
                tags:
                  - Lists
                  - Real Time
                  - Contacts
                  - Analysis
                  - Segments
                  - V2
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
            /routing-profiles/{InstanceId}/{RoutingProfileId}/queues:
              POST:
                summary: UpdateRoutingProfileQueues
                description: >-
                  <p>Updates the properties associated with a set of queues for
                  a routing profile.</p>
                tags:
                  - Update
                  - Routing
                  - Profiles
                  - Queues
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
            /routing-profiles-summary/{InstanceId}:
              GET:
                summary: ListRoutingProfiles
                description: >-
                  <p>Provides summary information about the routing profiles for
                  the specified Amazon Connect instance.</p> <p>For more
                  information about routing profiles, see <a
                  href="https://docs.aws.amazon.com/connect/latest/adminguide/concepts-routing.html">Routing
                  Profiles</a> and <a
                  href="https://docs.aws.amazon.com/connect/latest/adminguide/routing-profiles.html">Create
                  a Routing Profile</a> in the <i>Amazon Connect Administrator
                  Guide</i>.</p>
                tags:
                  - Lists
                  - Routing
                  - Profiles
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
            /instance/{InstanceId}/security-keys:
              GET:
                summary: ListSecurityKeys
                description: >-
                  <p>This API is in preview release for Amazon Connect and is
                  subject to change.</p> <p>Returns a paginated list of all
                  security keys associated with the instance.</p>
                tags:
                  - Lists
                  - Security
                  - Keys
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
            /security-profiles-applications/{InstanceId}/{SecurityProfileId}:
              GET:
                summary: ListSecurityProfileApplications
                description: >-
                  <p>Returns a list of third-party applications in a specific
                  security profile.</p>
                tags:
                  - Lists
                  - Security
                  - Profiles
                  - Applications
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
            /security-profiles-permissions/{InstanceId}/{SecurityProfileId}:
              GET:
                summary: ListSecurityProfilePermissions
                description: <p>Lists the permissions granted to a security profile.</p>
                tags:
                  - Lists
                  - Security
                  - Profiles
                  - Permissions
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
            /security-profiles-summary/{InstanceId}:
              GET:
                summary: ListSecurityProfiles
                description: >-
                  <p>Provides summary information about the security profiles
                  for the specified Amazon Connect instance.</p> <p>For more
                  information about security profiles, see <a
                  href="https://docs.aws.amazon.com/connect/latest/adminguide/connect-security-profiles.html">Security
                  Profiles</a> in the <i>Amazon Connect Administrator
                  Guide</i>.</p>
                tags:
                  - Lists
                  - Security
                  - Profiles
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
            /tags/{resourceArn}:
              DELETE:
                summary: UntagResource
                description: <p>Removes the specified tags from the specified resource.</p>
                tags:
                  - Untag
                  - Resources
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
            /traffic-distribution-groups:
              GET:
                summary: ListTrafficDistributionGroups
                description: <p>Lists traffic distribution groups.</p>
                tags:
                  - Lists
                  - Traffic
                  - Distributions
                  - Groups
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
            /user-hierarchy-groups-summary/{InstanceId}:
              GET:
                summary: ListUserHierarchyGroups
                description: >-
                  <p>Provides summary information about the hierarchy groups for
                  the specified Amazon Connect instance.</p> <p>For more
                  information about agent hierarchies, see <a
                  href="https://docs.aws.amazon.com/connect/latest/adminguide/agent-hierarchy.html">Set
                  Up Agent Hierarchies</a> in the <i>Amazon Connect
                  Administrator Guide</i>.</p>
                tags:
                  - Lists
                  - Users
                  - Hierarchy
                  - Groups
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
            /users/{InstanceId}/{UserId}/proficiencies:
              POST:
                summary: UpdateUserProficiencies
                description: >-
                  <p>Updates the properties associated with the proficiencies of
                  a user.</p>
                tags:
                  - Update
                  - Users
                  - Proficiencies
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
            /users-summary/{InstanceId}:
              GET:
                summary: ListUsers
                description: >-
                  <p>Provides summary information about the users for the
                  specified Amazon Connect instance.</p>
                tags:
                  - Lists
                  - Users
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
            /contact/monitor:
              POST:
                summary: MonitorContact
                description: >-
                  <p>Initiates silent monitoring of a contact. The Contact
                  Control Panel (CCP) of the user specified by <i>userId</i>
                  will be set to silent monitoring mode on the contact.</p>
                tags:
                  - Monitors
                  - Contacts
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
            /contact/pause:
              POST:
                summary: PauseContact
                description: <p>Allows pausing an ongoing task contact.</p>
                tags:
                  - Pause
                  - Contacts
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
            /users/{InstanceId}/{UserId}/status:
              PUT:
                summary: PutUserStatus
                description: >-
                  <p>Changes the current status of a user or agent in Amazon
                  Connect. If the agent is currently handling a contact, this
                  sets the agent's next status.</p> <p>For more information, see
                  <a
                  href="https://docs.aws.amazon.com/connect/latest/adminguide/metrics-agent-status.html">Agent
                  status</a> and <a
                  href="https://docs.aws.amazon.com/connect/latest/adminguide/set-next-status.html">Set
                  your next status</a> in the <i>Amazon Connect Administrator
                  Guide</i>.</p>
                tags:
                  - Put
                  - Users
                  - Status
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
            /instance/{InstanceId}/replicate:
              POST:
                summary: ReplicateInstance
                description: >-
                  <p>Replicates an Amazon Connect instance in the specified
                  Amazon Web Services Region and copies configuration
                  information for Amazon Connect resources across Amazon Web
                  Services Regions. </p> <p>For more information about
                  replicating an Amazon Connect instance, see <a
                  href="https://docs.aws.amazon.com/connect/latest/adminguide/create-replica-connect-instance.html">Create
                  a replica of your existing Amazon Connect instance</a> in the
                  <i>Amazon Connect Administrator Guide</i>.</p>
                tags:
                  - Replicate
                  - Instances
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
            /contact/resume:
              POST:
                summary: ResumeContact
                description: <p>Allows resuming a task contact in a paused state.</p>
                tags:
                  - Resume
                  - Contacts
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
            /contact/resume-recording:
              POST:
                summary: ResumeContactRecording
                description: >-
                  <p>When a contact is being recorded, and the recording has
                  been suspended using SuspendContactRecording, this API resumes
                  recording whatever recording is selected in the flow
                  configuration: call, screen, or both. If only call recording
                  or only screen recording is enabled, then it would resume.</p>
                  <p>Voice and screen recordings are supported.</p>
                tags:
                  - Resume
                  - Contacts
                  - Recording
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
            /phone-number/search-available:
              POST:
                summary: SearchAvailablePhoneNumbers
                description: >-
                  <p>Searches for available phone numbers that you can claim to
                  your Amazon Connect instance or traffic distribution group. If
                  the provided <code>TargetArn</code> is a traffic distribution
                  group, you can call this API in both Amazon Web Services
                  Regions associated with the traffic distribution group.</p>
                tags:
                  - Search
                  - Available
                  - Phone
                  - Numbers
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
            /search-contacts:
              POST:
                summary: SearchContacts
                description: <p>Searches contacts in an Amazon Connect instance.</p>
                tags:
                  - Search
                  - Contacts
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
            /search-hours-of-operations:
              POST:
                summary: SearchHoursOfOperations
                description: >-
                  <p>Searches the hours of operation in an Amazon Connect
                  instance, with optional filtering.</p>
                tags:
                  - Search
                  - Hours
                  - Of
                  - Operations
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
            /search-predefined-attributes:
              POST:
                summary: SearchPredefinedAttributes
                description: <p>Predefined attributes that meet certain criteria.</p>
                tags:
                  - Search
                  - Predefined
                  - Attributes
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
            /search-prompts:
              POST:
                summary: SearchPrompts
                description: >-
                  <p>Searches prompts in an Amazon Connect instance, with
                  optional filtering.</p>
                tags:
                  - Search
                  - Prompts
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
            /search-queues:
              POST:
                summary: SearchQueues
                description: >-
                  <p>Searches queues in an Amazon Connect instance, with
                  optional filtering.</p>
                tags:
                  - Search
                  - Queues
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
            /search-quick-connects:
              POST:
                summary: SearchQuickConnects
                description: >-
                  <p>Searches quick connects in an Amazon Connect instance, with
                  optional filtering.</p>
                tags:
                  - Search
                  - Quick
                  - Connects
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
            /search-resource-tags:
              POST:
                summary: SearchResourceTags
                description: >-
                  <p>Searches tags used in an Amazon Connect instance using
                  optional search criteria.</p>
                tags:
                  - Search
                  - Resources
                  - Tags
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
            /search-routing-profiles:
              POST:
                summary: SearchRoutingProfiles
                description: >-
                  <p>Searches routing profiles in an Amazon Connect instance,
                  with optional filtering.</p>
                tags:
                  - Search
                  - Routing
                  - Profiles
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
            /search-security-profiles:
              POST:
                summary: SearchSecurityProfiles
                description: >-
                  <p>Searches security profiles in an Amazon Connect instance,
                  with optional filtering.</p>
                tags:
                  - Search
                  - Security
                  - Profiles
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
            /search-users:
              POST:
                summary: SearchUsers
                description: >-
                  <p>Searches users in an Amazon Connect instance, with optional
                  filtering. </p> <note> <p>
                  <code>AfterContactWorkTimeLimit</code> is returned in
                  milliseconds. </p> </note>
                tags:
                  - Search
                  - Users
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
                  - Users
            /vocabulary-summary/{InstanceId}:
              POST:
                summary: SearchVocabularies
                description: >-
                  <p>Searches for vocabularies within a specific Amazon Connect
                  instance using <code>State</code>,
                  <code>NameStartsWith</code>, and
                  <code>LanguageCode</code>.</p>
                tags:
                  - Search
                  - Vocabularies
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
                  - Users
            /chat-integration-event:
              POST:
                summary: SendChatIntegrationEvent
                description: >-
                  <p>Processes chat integration events from Amazon Web Services
                  or external integrations to Amazon Connect. A chat integration
                  event includes:</p> <ul> <li> <p>SourceId, DestinationId, and
                  Subtype: a set of identifiers, uniquely representing a
                  chat</p> </li> <li> <p> ChatEvent: details of the chat action
                  to perform such as sending a message, event, or disconnecting
                  from a chat</p> </li> </ul> <p>When a chat integration event
                  is sent with chat identifiers that do not map to an active
                  chat contact, a new chat contact is also created before
                  handling chat action. </p> <p>Access to this API is currently
                  restricted to Amazon Pinpoint for supporting SMS integration.
                  </p>
                tags:
                  - Send
                  - Chat
                  - Integrations
                  - Events
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
                  - Users
                  - Chat
                  - Events
            /contact/chat:
              PUT:
                summary: StartChatContact
                description: >-
                  <p>Initiates a flow to start a new chat for the customer.
                  Response of this API provides a token required to obtain
                  credentials from the <a
                  href="https://docs.aws.amazon.com/connect-participant/latest/APIReference/API_CreateParticipantConnection.html">CreateParticipantConnection</a>
                  API in the Amazon Connect Participant Service.</p> <p>When a
                  new chat contact is successfully created, clients must
                  subscribe to the participant’s connection for the created chat
                  within 5 minutes. This is achieved by invoking <a
                  href="https://docs.aws.amazon.com/connect-participant/latest/APIReference/API_CreateParticipantConnection.html">CreateParticipantConnection</a>
                  with WEBSOCKET and CONNECTION_CREDENTIALS. </p> <p>A 429 error
                  occurs in the following situations:</p> <ul> <li> <p>API rate
                  limit is exceeded. API TPS throttling returns a
                  <code>TooManyRequests</code> exception.</p> </li> <li> <p>The
                  <a
                  href="https://docs.aws.amazon.com/connect/latest/adminguide/amazon-connect-service-limits.html">quota
                  for concurrent active chats</a> is exceeded. Active chat
                  throttling returns a <code>LimitExceededException</code>.</p>
                  </li> </ul> <p>If you use the
                  <code>ChatDurationInMinutes</code> parameter and receive a 400
                  error, your account may not support the ability to configure
                  custom chat durations. For more information, contact Amazon
                  Web Services Support. </p> <p>For more information about chat,
                  see <a
                  href="https://docs.aws.amazon.com/connect/latest/adminguide/chat.html">Chat</a>
                  in the <i>Amazon Connect Administrator Guide</i>.</p>
                tags:
                  - Start
                  - Chat
                  - Contacts
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
                  - Users
                  - Chat
                  - Events
            /contact/start-recording:
              POST:
                summary: StartContactRecording
                description: >-
                  <p>Starts recording the contact: </p> <ul> <li> <p>If the API
                  is called <i>before</i> the agent joins the call, recording
                  starts when the agent joins the call.</p> </li> <li> <p>If the
                  API is called <i>after</i> the agent joins the call, recording
                  starts at the time of the API call.</p> </li> </ul>
                  <p>StartContactRecording is a one-time action. For example, if
                  you use StopContactRecording to stop recording an ongoing
                  call, you can't use StartContactRecording to restart it. For
                  scenarios where the recording has started and you want to
                  suspend and resume it, such as when collecting sensitive
                  information (for example, a credit card number), use
                  SuspendContactRecording and ResumeContactRecording.</p> <p>You
                  can use this API to override the recording behavior configured
                  in the <a
                  href="https://docs.aws.amazon.com/connect/latest/adminguide/set-recording-behavior.html">Set
                  recording behavior</a> block.</p> <p>Only voice recordings are
                  supported at this time.</p>
                tags:
                  - Start
                  - Contacts
                  - Recording
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
                  - Users
                  - Chat
                  - Events
                  - Start
            /contact/start-streaming:
              POST:
                summary: StartContactStreaming
                description: >-
                  <p> Initiates real-time message streaming for a new chat
                  contact.</p> <p> For more information about message streaming,
                  see <a
                  href="https://docs.aws.amazon.com/connect/latest/adminguide/chat-message-streaming.html">Enable
                  real-time chat message streaming</a> in the <i>Amazon Connect
                  Administrator Guide</i>.</p>
                tags:
                  - Start
                  - Contacts
                  - Streaming
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
                  - Users
                  - Chat
                  - Events
                  - Start
                  - Streaming
            /contact/outbound-voice:
              PUT:
                summary: StartOutboundVoiceContact
                description: >-
                  <p>Places an outbound call to a contact, and then initiates
                  the flow. It performs the actions in the flow that's specified
                  (in <code>ContactFlowId</code>).</p> <p>Agents do not initiate
                  the outbound API, which means that they do not dial the
                  contact. If the flow places an outbound call to a contact, and
                  then puts the contact in queue, the call is then routed to the
                  agent, like any other inbound case.</p> <p>There is a
                  60-second dialing timeout for this operation. If the call is
                  not connected after 60 seconds, it fails.</p> <note> <p>UK
                  numbers with a 447 prefix are not allowed by default. Before
                  you can dial these UK mobile numbers, you must submit a
                  service quota increase request. For more information, see <a
                  href="https://docs.aws.amazon.com/connect/latest/adminguide/amazon-connect-service-limits.html">Amazon
                  Connect Service Quotas</a> in the <i>Amazon Connect
                  Administrator Guide</i>. </p> </note> <note> <p>Campaign calls
                  are not allowed by default. Before you can make a call with
                  <code>TrafficType</code> = <code>CAMPAIGN</code>, you must
                  submit a service quota increase request to the quota <a
                  href="https://docs.aws.amazon.com/connect/latest/adminguide/amazon-connect-service-limits.html#outbound-communications-quotas">Amazon
                  Connect campaigns</a>. </p> </note>
                tags:
                  - Start
                  - Outbound
                  - Voice
                  - Contacts
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
                  - Users
                  - Chat
                  - Events
                  - Start
                  - Streaming
                  - Outbound
                  - Voice
            /contact/task:
              PUT:
                summary: StartTaskContact
                description: >-
                  <p>Initiates a flow to start a new task contact. For more
                  information about task contacts, see <a
                  href="https://docs.aws.amazon.com/connect/latest/adminguide/tasks.html">Concepts:
                  Tasks in Amazon Connect</a> in the <i>Amazon Connect
                  Administrator Guide</i>. </p> <p>When using
                  <code>PreviousContactId</code> and
                  <code>RelatedContactId</code> input parameters, note the
                  following:</p> <ul> <li> <p> <code>PreviousContactId</code>
                  </p> <ul> <li> <p>Any updates to user-defined task contact
                  attributes on any contact linked through the same
                  <code>PreviousContactId</code> will affect every contact in
                  the chain.</p> </li> <li> <p>There can be a maximum of 12
                  linked task contacts in a chain. That is, 12 task contacts can
                  be created that share the same
                  <code>PreviousContactId</code>.</p> </li> </ul> </li> <li> <p>
                  <code>RelatedContactId</code> </p> <ul> <li> <p>Copies contact
                  attributes from the related task contact to the new
                  contact.</p> </li> <li> <p>Any update on attributes in a new
                  task contact does not update attributes on previous
                  contact.</p> </li> <li> <p>There’s no limit on the number of
                  task contacts that can be created that use the same
                  <code>RelatedContactId</code>.</p> </li> </ul> </li> </ul>
                  <p>In addition, when calling StartTaskContact include only one
                  of these parameters: <code>ContactFlowID</code>,
                  <code>QuickConnectID</code>, or <code>TaskTemplateID</code>.
                  Only one parameter is required as long as the task template
                  has a flow configured to run it. If more than one parameter is
                  specified, or only the <code>TaskTemplateID</code> is
                  specified but it does not have a flow configured, the request
                  returns an error because Amazon Connect cannot identify the
                  unique flow to run when the task is created.</p> <p>A
                  <code>ServiceQuotaExceededException</code> occurs when the
                  number of open tasks exceeds the active tasks quota or there
                  are already 12 tasks referencing the same
                  <code>PreviousContactId</code>. For more information about
                  service quotas for task contacts, see <a
                  href="https://docs.aws.amazon.com/connect/latest/adminguide/amazon-connect-service-limits.html">Amazon
                  Connect service quotas</a> in the <i>Amazon Connect
                  Administrator Guide</i>. </p>
                tags:
                  - Start
                  - Tasks
                  - Contacts
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
                  - Users
                  - Chat
                  - Events
                  - Start
                  - Streaming
                  - Outbound
                  - Voice
            /contact/webrtc:
              PUT:
                summary: StartWebRTCContact
                description: >-
                  <p>Places an inbound in-app, web, or video call to a contact,
                  and then initiates the flow. It performs the actions in the
                  flow that are specified (in ContactFlowId) and present in the
                  Amazon Connect instance (specified as InstanceId).</p>
                tags:
                  - Start
                  - Web
                  - Contacts
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
                  - Users
                  - Chat
                  - Events
                  - Start
                  - Streaming
                  - Outbound
                  - Voice
                  - Web RTC
            /contact/stop:
              POST:
                summary: StopContact
                description: >-
                  <p>Ends the specified contact. This call does not work for
                  voice contacts that use the following initiation methods:</p>
                  <ul> <li> <p>DISCONNECT</p> </li> <li> <p>TRANSFER</p> </li>
                  <li> <p>QUEUE_TRANSFER</p> </li> </ul> <p>Chat and task
                  contacts, however, can be terminated in any state, regardless
                  of initiation method.</p>
                tags:
                  - Stop
                  - Contacts
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
                  - Users
                  - Chat
                  - Events
                  - Start
                  - Streaming
                  - Outbound
                  - Voice
                  - Web RTC
                  - Stop
            /contact/stop-recording:
              POST:
                summary: StopContactRecording
                description: >-
                  <p>Stops recording a call when a contact is being recorded.
                  StopContactRecording is a one-time action. If you use
                  StopContactRecording to stop recording an ongoing call, you
                  can't use StartContactRecording to restart it. For scenarios
                  where the recording has started and you want to suspend it for
                  sensitive information (for example, to collect a credit card
                  number), and then restart it, use SuspendContactRecording and
                  ResumeContactRecording.</p> <p>Only voice recordings are
                  supported at this time.</p>
                tags:
                  - Stop
                  - Contacts
                  - Recording
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
                  - Users
                  - Chat
                  - Events
                  - Start
                  - Streaming
                  - Outbound
                  - Voice
                  - Web RTC
                  - Stop
            /contact/stop-streaming:
              POST:
                summary: StopContactStreaming
                description: >-
                  <p> Ends message streaming on a specified contact. To restart
                  message streaming on that contact, call the <a
                  href="https://docs.aws.amazon.com/connect/latest/APIReference/API_StartContactStreaming.html">StartContactStreaming</a>
                  API. </p>
                tags:
                  - Stop
                  - Contacts
                  - Streaming
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
                  - Users
                  - Chat
                  - Events
                  - Start
                  - Streaming
                  - Outbound
                  - Voice
                  - Web RTC
                  - Stop
            /contact-evaluations/{InstanceId}/{EvaluationId}/submit:
              POST:
                summary: SubmitContactEvaluation
                description: >-
                  <p>Submits a contact evaluation in the specified Amazon
                  Connect instance. Answers included in the request are merged
                  with existing answers for the given evaluation. If no answers
                  or notes are passed, the evaluation is submitted with the
                  existing answers and notes. You can delete an answer or note
                  by passing an empty object (<code>{}</code>) to the question
                  identifier. </p> <p>If a contact evaluation is already in
                  submitted state, this operation will trigger a
                  resubmission.</p>
                tags:
                  - Submit
                  - Contacts
                  - Evaluations
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
                  - Users
                  - Chat
                  - Events
                  - Start
                  - Streaming
                  - Outbound
                  - Voice
                  - Web RTC
                  - Stop
                  - Submit
            /contact/suspend-recording:
              POST:
                summary: SuspendContactRecording
                description: >-
                  <p>When a contact is being recorded, this API suspends
                  recording whatever is selected in the flow configuration:
                  call, screen, or both. If only call recording or only screen
                  recording is enabled, then it would be suspended. For example,
                  you might suspend the screen recording while collecting
                  sensitive information, such as a credit card number. Then use
                  ResumeContactRecording to restart recording the screen.</p>
                  <p>The period of time that the recording is suspended is
                  filled with silence in the final recording.</p> <p>Voice and
                  screen recordings are supported.</p>
                tags:
                  - Suspend
                  - Contacts
                  - Recording
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
                  - Users
                  - Chat
                  - Events
                  - Start
                  - Streaming
                  - Outbound
                  - Voice
                  - Web RTC
                  - Stop
                  - Submit
                  - Suspend
            /contact/tags:
              POST:
                summary: TagContact
                description: >-
                  <p>Adds the specified tags to the contact resource. For more
                  information about this API is used, see <a
                  href="https://docs.aws.amazon.com/connect/latest/adminguide/granular-billing.html">Set
                  up granular billing for a detailed view of your Amazon Connect
                  usage</a>. </p>
                tags:
                  - Tags
                  - Contacts
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
                  - Users
                  - Chat
                  - Events
                  - Start
                  - Streaming
                  - Outbound
                  - Voice
                  - Web RTC
                  - Stop
                  - Submit
                  - Suspend
            /contact/transfer:
              POST:
                summary: TransferContact
                description: >-
                  <p>Transfers contacts from one agent or queue to another agent
                  or queue at any point after a contact is created. You can
                  transfer a contact to another queue by providing the flow
                  which orchestrates the contact to the destination queue. This
                  gives you more control over contact handling and helps you
                  adhere to the service level agreement (SLA) guaranteed to your
                  customers.</p> <p>Note the following requirements:</p> <ul>
                  <li> <p>Transfer is supported for only <code>TASK</code>
                  contacts.</p> </li> <li> <p>Do not use both
                  <code>QueueId</code> and <code>UserId</code> in the same
                  call.</p> </li> <li> <p>The following flow types are
                  supported: Inbound flow, Transfer to agent flow, and Transfer
                  to queue flow.</p> </li> <li> <p>The
                  <code>TransferContact</code> API can be called only on active
                  contacts.</p> </li> <li> <p>A contact cannot be transferred
                  more than 11 times.</p> </li> </ul>
                tags:
                  - Transfers
                  - Contacts
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
                  - Users
                  - Chat
                  - Events
                  - Start
                  - Streaming
                  - Outbound
                  - Voice
                  - Web RTC
                  - Stop
                  - Submit
                  - Suspend
                  - Transfers
            /contact/tags/{InstanceId}/{ContactId}:
              DELETE:
                summary: UntagContact
                description: >-
                  <p>Removes the specified tags from the contact resource. For
                  more information about this API is used, see <a
                  href="https://docs.aws.amazon.com/connect/latest/adminguide/granular-billing.html">Set
                  up granular billing for a detailed view of your Amazon Connect
                  usage</a>.</p>
                tags:
                  - Untag
                  - Contacts
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
                  - Users
                  - Chat
                  - Events
                  - Start
                  - Streaming
                  - Outbound
                  - Voice
                  - Web RTC
                  - Stop
                  - Submit
                  - Suspend
                  - Transfers
            /contact/attributes:
              POST:
                summary: UpdateContactAttributes
                description: >-
                  <p>Creates or updates user-defined contact attributes
                  associated with the specified contact.</p> <p>You can create
                  or update user-defined attributes for both ongoing and
                  completed contacts. For example, while the call is active, you
                  can update the customer's name or the reason the customer
                  called. You can add notes about steps that the agent took
                  during the call that display to the next agent that takes the
                  call. You can also update attributes for a contact using data
                  from your CRM application and save the data with the contact
                  in Amazon Connect. You could also flag calls for additional
                  analysis, such as legal review or to identify abusive
                  callers.</p> <p>Contact attributes are available in Amazon
                  Connect for 24 months, and are then deleted. For information
                  about contact record retention and the maximum size of the
                  contact record attributes section, see <a
                  href="https://docs.aws.amazon.com/connect/latest/adminguide/amazon-connect-service-limits.html#feature-limits">Feature
                  specifications</a> in the <i>Amazon Connect Administrator
                  Guide</i>. </p>
                tags:
                  - Update
                  - Contacts
                  - Attributes
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
                  - Users
                  - Chat
                  - Events
                  - Start
                  - Streaming
                  - Outbound
                  - Voice
                  - Web RTC
                  - Stop
                  - Submit
                  - Suspend
                  - Transfers
            /contact-flows/{InstanceId}/{ContactFlowId}/content:
              POST:
                summary: UpdateContactFlowContent
                description: >-
                  <p>Updates the specified flow.</p> <p>You can also create and
                  update flows using the <a
                  href="https://docs.aws.amazon.com/connect/latest/APIReference/flow-language.html">Amazon
                  Connect Flow language</a>.</p>
                tags:
                  - Update
                  - Contacts
                  - Flow
                  - Content
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
                  - Users
                  - Chat
                  - Events
                  - Start
                  - Streaming
                  - Outbound
                  - Voice
                  - Web RTC
                  - Stop
                  - Submit
                  - Suspend
                  - Transfers
                  - Content
            /contact-flows/{InstanceId}/{ContactFlowId}/metadata:
              POST:
                summary: UpdateContactFlowMetadata
                description: <p>Updates metadata about specified flow.</p>
                tags:
                  - Update
                  - Contacts
                  - Flow
                  - Metadata
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
                  - Users
                  - Chat
                  - Events
                  - Start
                  - Streaming
                  - Outbound
                  - Voice
                  - Web RTC
                  - Stop
                  - Submit
                  - Suspend
                  - Transfers
                  - Content
                  - Metadata
            /contact-flow-modules/{InstanceId}/{ContactFlowModuleId}/content:
              POST:
                summary: UpdateContactFlowModuleContent
                description: >-
                  <p>Updates specified flow module for the specified Amazon
                  Connect instance. </p>
                tags:
                  - Update
                  - Contacts
                  - Flow
                  - Modules
                  - Content
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
                  - Users
                  - Chat
                  - Events
                  - Start
                  - Streaming
                  - Outbound
                  - Voice
                  - Web RTC
                  - Stop
                  - Submit
                  - Suspend
                  - Transfers
                  - Content
                  - Metadata
            /contact-flow-modules/{InstanceId}/{ContactFlowModuleId}/metadata:
              POST:
                summary: UpdateContactFlowModuleMetadata
                description: <p>Updates metadata about specified flow module.</p>
                tags:
                  - Update
                  - Contacts
                  - Flow
                  - Modules
                  - Metadata
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
                  - Users
                  - Chat
                  - Events
                  - Start
                  - Streaming
                  - Outbound
                  - Voice
                  - Web RTC
                  - Stop
                  - Submit
                  - Suspend
                  - Transfers
                  - Content
                  - Metadata
            /contact-flows/{InstanceId}/{ContactFlowId}/name:
              POST:
                summary: UpdateContactFlowName
                description: >-
                  <p>The name of the flow.</p> <p>You can also create and update
                  flows using the <a
                  href="https://docs.aws.amazon.com/connect/latest/APIReference/flow-language.html">Amazon
                  Connect Flow language</a>.</p>
                tags:
                  - Update
                  - Contacts
                  - Flow
                  - Names
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
                  - Users
                  - Chat
                  - Events
                  - Start
                  - Streaming
                  - Outbound
                  - Voice
                  - Web RTC
                  - Stop
                  - Submit
                  - Suspend
                  - Transfers
                  - Content
                  - Metadata
            /contacts/{InstanceId}/{ContactId}/routing-data:
              POST:
                summary: UpdateContactRoutingData
                description: >-
                  <p>This API is in preview release for Amazon Connect and is
                  subject to change.</p> <p>Updates routing priority and age on
                  the contact (<b>QueuePriority</b> and
                  <b>QueueTimeAdjustmentInSeconds</b>). These properties can be
                  used to change a customer's position in the queue. For
                  example, you can move a contact to the back of the queue by
                  setting a lower routing priority relative to other contacts in
                  queue; or you can move a contact to the front of the queue by
                  increasing the routing age which will make the contact look
                  artificially older and therefore higher up in the
                  first-in-first-out routing order. Note that adjusting the
                  routing age of a contact affects only its position in queue,
                  and not its actual queue wait time as reported through
                  metrics. These properties can also be updated by using <a
                  href="https://docs.aws.amazon.com/connect/latest/adminguide/change-routing-priority.html">the
                  Set routing priority / age flow block</a>.</p>
                tags:
                  - Update
                  - Contacts
                  - Routing
                  - Data
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
                  - Users
                  - Chat
                  - Events
                  - Start
                  - Streaming
                  - Outbound
                  - Voice
                  - Web RTC
                  - Stop
                  - Submit
                  - Suspend
                  - Transfers
                  - Content
                  - Metadata
            /contact/schedule:
              POST:
                summary: UpdateContactSchedule
                description: >-
                  <p>Updates the scheduled time of a task contact that is
                  already scheduled.</p>
                tags:
                  - Update
                  - Contacts
                  - Schedules
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
                  - Users
                  - Chat
                  - Events
                  - Start
                  - Streaming
                  - Outbound
                  - Voice
                  - Web RTC
                  - Stop
                  - Submit
                  - Suspend
                  - Transfers
                  - Content
                  - Metadata
                  - Schedules
            /contact/participant-role-config/{InstanceId}/{ContactId}:
              PUT:
                summary: UpdateParticipantRoleConfig
                description: >-
                  <p>Updates timeouts for when human chat participants are to be
                  considered idle, and when agents are automatically
                  disconnected from a chat due to idleness. You can set four
                  timers:</p> <ul> <li> <p>Customer idle timeout</p> </li> <li>
                  <p>Customer auto-disconnect timeout</p> </li> <li> <p>Agent
                  idle timeout</p> </li> <li> <p>Agent auto-disconnect
                  timeout</p> </li> </ul> <p>For more information about how chat
                  timeouts work, see <a
                  href="https://docs.aws.amazon.com/connect/latest/adminguide/setup-chat-timeouts.html">Set
                  up chat timeouts for human participants</a>. </p>
                tags:
                  - Update
                  - Participants
                  - Roles
                  - Configurations
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
                  - Users
                  - Chat
                  - Events
                  - Start
                  - Streaming
                  - Outbound
                  - Voice
                  - Web RTC
                  - Stop
                  - Submit
                  - Suspend
                  - Transfers
                  - Content
                  - Metadata
                  - Schedules
            /phone-number/{PhoneNumberId}/metadata:
              PUT:
                summary: UpdatePhoneNumberMetadata
                description: >-
                  <p>Updates a phone number’s metadata.</p> <important> <p>To
                  verify the status of a previous UpdatePhoneNumberMetadata
                  operation, call the <a
                  href="https://docs.aws.amazon.com/connect/latest/APIReference/API_DescribePhoneNumber.html">DescribePhoneNumber</a>
                  API.</p> </important>
                tags:
                  - Update
                  - Phone
                  - Numbers
                  - Metadata
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
                  - Users
                  - Chat
                  - Events
                  - Start
                  - Streaming
                  - Outbound
                  - Voice
                  - Web RTC
                  - Stop
                  - Submit
                  - Suspend
                  - Transfers
                  - Content
                  - Metadata
                  - Schedules
            /queues/{InstanceId}/{QueueId}/hours-of-operation:
              POST:
                summary: UpdateQueueHoursOfOperation
                description: >-
                  <p>This API is in preview release for Amazon Connect and is
                  subject to change.</p> <p>Updates the hours of operation for
                  the specified queue.</p>
                tags:
                  - Update
                  - Queues
                  - Hours
                  - Of
                  - Operation
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
                  - Users
                  - Chat
                  - Events
                  - Start
                  - Streaming
                  - Outbound
                  - Voice
                  - Web RTC
                  - Stop
                  - Submit
                  - Suspend
                  - Transfers
                  - Content
                  - Metadata
                  - Schedules
            /queues/{InstanceId}/{QueueId}/max-contacts:
              POST:
                summary: UpdateQueueMaxContacts
                description: >-
                  <p>This API is in preview release for Amazon Connect and is
                  subject to change.</p> <p>Updates the maximum number of
                  contacts allowed in a queue before it is considered full.</p>
                tags:
                  - Update
                  - Queues
                  - Maximum
                  - Contacts
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
                  - Users
                  - Chat
                  - Events
                  - Start
                  - Streaming
                  - Outbound
                  - Voice
                  - Web RTC
                  - Stop
                  - Submit
                  - Suspend
                  - Transfers
                  - Content
                  - Metadata
                  - Schedules
                  - Maximum
            /queues/{InstanceId}/{QueueId}/name:
              POST:
                summary: UpdateQueueName
                description: >-
                  <p>This API is in preview release for Amazon Connect and is
                  subject to change.</p> <p>Updates the name and description of
                  a queue. At least <code>Name</code> or
                  <code>Description</code> must be provided.</p>
                tags:
                  - Update
                  - Queues
                  - Names
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
                  - Users
                  - Chat
                  - Events
                  - Start
                  - Streaming
                  - Outbound
                  - Voice
                  - Web RTC
                  - Stop
                  - Submit
                  - Suspend
                  - Transfers
                  - Content
                  - Metadata
                  - Schedules
                  - Maximum
            /queues/{InstanceId}/{QueueId}/outbound-caller-config:
              POST:
                summary: UpdateQueueOutboundCallerConfig
                description: >-
                  <p>This API is in preview release for Amazon Connect and is
                  subject to change.</p> <p>Updates the outbound caller ID name,
                  number, and outbound whisper flow for a specified queue.</p>
                  <important> <ul> <li> <p>If the phone number is claimed to a
                  traffic distribution group that was created in the same Region
                  as the Amazon Connect instance where you are calling this API,
                  then you can use a full phone number ARN or a UUID for
                  <code>OutboundCallerIdNumberId</code>. However, if the phone
                  number is claimed to a traffic distribution group that is in
                  one Region, and you are calling this API from an instance in
                  another Amazon Web Services Region that is associated with the
                  traffic distribution group, you must provide a full phone
                  number ARN. If a UUID is provided in this scenario, you will
                  receive a <code>ResourceNotFoundException</code>.</p> </li>
                  <li> <p>Only use the phone number ARN format that doesn't
                  contain <code>instance</code> in the path, for example,
                  <code>arn:aws:connect:us-east-1:1234567890:phone-number/uuid</code>.
                  This is the same ARN format that is returned when you call the
                  <a
                  href="https://docs.aws.amazon.com/connect/latest/APIReference/API_ListPhoneNumbersV2.html">ListPhoneNumbersV2</a>
                  API.</p> </li> <li> <p>If you plan to use IAM policies to
                  allow/deny access to this API for phone number resources
                  claimed to a traffic distribution group, see <a
                  href="https://docs.aws.amazon.com/connect/latest/adminguide/security_iam_resource-level-policy-examples.html#allow-deny-queue-actions-replica-region">Allow
                  or Deny queue API actions for phone numbers in a replica
                  Region</a>.</p> </li> </ul> </important>
                tags:
                  - Update
                  - Queues
                  - Outbound
                  - Caller
                  - Configurations
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
                  - Users
                  - Chat
                  - Events
                  - Start
                  - Streaming
                  - Outbound
                  - Voice
                  - Web RTC
                  - Stop
                  - Submit
                  - Suspend
                  - Transfers
                  - Content
                  - Metadata
                  - Schedules
                  - Maximum
                  - Caller
            /queues/{InstanceId}/{QueueId}/status:
              POST:
                summary: UpdateQueueStatus
                description: >-
                  <p>This API is in preview release for Amazon Connect and is
                  subject to change.</p> <p>Updates the status of the queue.</p>
                tags:
                  - Update
                  - Queues
                  - Status
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
                  - Users
                  - Chat
                  - Events
                  - Start
                  - Streaming
                  - Outbound
                  - Voice
                  - Web RTC
                  - Stop
                  - Submit
                  - Suspend
                  - Transfers
                  - Content
                  - Metadata
                  - Schedules
                  - Maximum
                  - Caller
            /quick-connects/{InstanceId}/{QuickConnectId}/config:
              POST:
                summary: UpdateQuickConnectConfig
                description: >-
                  <p>Updates the configuration settings for the specified quick
                  connect.</p>
                tags:
                  - Update
                  - Quick
                  - Connect
                  - Configurations
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
                  - Users
                  - Chat
                  - Events
                  - Start
                  - Streaming
                  - Outbound
                  - Voice
                  - Web RTC
                  - Stop
                  - Submit
                  - Suspend
                  - Transfers
                  - Content
                  - Metadata
                  - Schedules
                  - Maximum
                  - Caller
            /quick-connects/{InstanceId}/{QuickConnectId}/name:
              POST:
                summary: UpdateQuickConnectName
                description: >-
                  <p>Updates the name and description of a quick connect. The
                  request accepts the following data in JSON format. At least
                  <code>Name</code> or <code>Description</code> must be
                  provided.</p>
                tags:
                  - Update
                  - Quick
                  - Connect
                  - Names
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
                  - Users
                  - Chat
                  - Events
                  - Start
                  - Streaming
                  - Outbound
                  - Voice
                  - Web RTC
                  - Stop
                  - Submit
                  - Suspend
                  - Transfers
                  - Content
                  - Metadata
                  - Schedules
                  - Maximum
                  - Caller
            /routing-profiles/{InstanceId}/{RoutingProfileId}/agent-availability-timer:
              POST:
                summary: UpdateRoutingProfileAgentAvailabilityTimer
                description: >-
                  <p>Whether agents with this routing profile will have their
                  routing order calculated based on <i>time since their last
                  inbound contact</i> or <i>longest idle time</i>. </p>
                tags:
                  - Update
                  - Routing
                  - Profiles
                  - Agent
                  - Availability
                  - Timer
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
                  - Users
                  - Chat
                  - Events
                  - Start
                  - Streaming
                  - Outbound
                  - Voice
                  - Web RTC
                  - Stop
                  - Submit
                  - Suspend
                  - Transfers
                  - Content
                  - Metadata
                  - Schedules
                  - Maximum
                  - Caller
                  - Availability
                  - Timer
            /routing-profiles/{InstanceId}/{RoutingProfileId}/concurrency:
              POST:
                summary: UpdateRoutingProfileConcurrency
                description: >-
                  <p>Updates the channels that agents can handle in the Contact
                  Control Panel (CCP) for a routing profile.</p>
                tags:
                  - Update
                  - Routing
                  - Profiles
                  - Concurrency
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
                  - Users
                  - Chat
                  - Events
                  - Start
                  - Streaming
                  - Outbound
                  - Voice
                  - Web RTC
                  - Stop
                  - Submit
                  - Suspend
                  - Transfers
                  - Content
                  - Metadata
                  - Schedules
                  - Maximum
                  - Caller
                  - Availability
                  - Timer
                  - Concurrency
            /routing-profiles/{InstanceId}/{RoutingProfileId}/default-outbound-queue:
              POST:
                summary: UpdateRoutingProfileDefaultOutboundQueue
                description: >-
                  <p>Updates the default outbound queue of a routing
                  profile.</p>
                tags:
                  - Update
                  - Routing
                  - Profiles
                  - Default
                  - Outbound
                  - Queues
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
                  - Users
                  - Chat
                  - Events
                  - Start
                  - Streaming
                  - Outbound
                  - Voice
                  - Web RTC
                  - Stop
                  - Submit
                  - Suspend
                  - Transfers
                  - Content
                  - Metadata
                  - Schedules
                  - Maximum
                  - Caller
                  - Availability
                  - Timer
                  - Concurrency
                  - Default
            /routing-profiles/{InstanceId}/{RoutingProfileId}/name:
              POST:
                summary: UpdateRoutingProfileName
                description: >-
                  <p>Updates the name and description of a routing profile. The
                  request accepts the following data in JSON format. At least
                  <code>Name</code> or <code>Description</code> must be
                  provided.</p>
                tags:
                  - Update
                  - Routing
                  - Profiles
                  - Names
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
                  - Users
                  - Chat
                  - Events
                  - Start
                  - Streaming
                  - Outbound
                  - Voice
                  - Web RTC
                  - Stop
                  - Submit
                  - Suspend
                  - Transfers
                  - Content
                  - Metadata
                  - Schedules
                  - Maximum
                  - Caller
                  - Availability
                  - Timer
                  - Concurrency
                  - Default
            /users/{InstanceId}/{UserId}/hierarchy:
              POST:
                summary: UpdateUserHierarchy
                description: >-
                  <p>Assigns the specified hierarchy group to the specified
                  user.</p>
                tags:
                  - Update
                  - Users
                  - Hierarchy
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
                  - Users
                  - Chat
                  - Events
                  - Start
                  - Streaming
                  - Outbound
                  - Voice
                  - Web RTC
                  - Stop
                  - Submit
                  - Suspend
                  - Transfers
                  - Content
                  - Metadata
                  - Schedules
                  - Maximum
                  - Caller
                  - Availability
                  - Timer
                  - Concurrency
                  - Default
            /user-hierarchy-groups/{InstanceId}/{HierarchyGroupId}/name:
              POST:
                summary: UpdateUserHierarchyGroupName
                description: <p>Updates the name of the user hierarchy group. </p>
                tags:
                  - Update
                  - Users
                  - Hierarchy
                  - Group
                  - Names
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
                  - Users
                  - Chat
                  - Events
                  - Start
                  - Streaming
                  - Outbound
                  - Voice
                  - Web RTC
                  - Stop
                  - Submit
                  - Suspend
                  - Transfers
                  - Content
                  - Metadata
                  - Schedules
                  - Maximum
                  - Caller
                  - Availability
                  - Timer
                  - Concurrency
                  - Default
            /users/{InstanceId}/{UserId}/identity-info:
              POST:
                summary: UpdateUserIdentityInfo
                description: >-
                  <p>Updates the identity information for the specified
                  user.</p> <important> <p>We strongly recommend limiting who
                  has the ability to invoke <code>UpdateUserIdentityInfo</code>.
                  Someone with that ability can change the login credentials of
                  other users by changing their email address. This poses a
                  security risk to your organization. They can change the email
                  address of a user to the attacker's email address, and then
                  reset the password through email. For more information, see <a
                  href="https://docs.aws.amazon.com/connect/latest/adminguide/security-profile-best-practices.html">Best
                  Practices for Security Profiles</a> in the <i>Amazon Connect
                  Administrator Guide</i>.</p> </important>
                tags:
                  - Update
                  - Users
                  - Identity
                  - Info
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
                  - Users
                  - Chat
                  - Events
                  - Start
                  - Streaming
                  - Outbound
                  - Voice
                  - Web RTC
                  - Stop
                  - Submit
                  - Suspend
                  - Transfers
                  - Content
                  - Metadata
                  - Schedules
                  - Maximum
                  - Caller
                  - Availability
                  - Timer
                  - Concurrency
                  - Default
                  - Identity
                  - Info
            /users/{InstanceId}/{UserId}/phone-config:
              POST:
                summary: UpdateUserPhoneConfig
                description: >-
                  <p>Updates the phone configuration settings for the specified
                  user.</p>
                tags:
                  - Update
                  - Users
                  - Phone
                  - Configurations
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
                  - Users
                  - Chat
                  - Events
                  - Start
                  - Streaming
                  - Outbound
                  - Voice
                  - Web RTC
                  - Stop
                  - Submit
                  - Suspend
                  - Transfers
                  - Content
                  - Metadata
                  - Schedules
                  - Maximum
                  - Caller
                  - Availability
                  - Timer
                  - Concurrency
                  - Default
                  - Identity
                  - Info
            /users/{InstanceId}/{UserId}/routing-profile:
              POST:
                summary: UpdateUserRoutingProfile
                description: >-
                  <p>Assigns the specified routing profile to the specified
                  user.</p>
                tags:
                  - Update
                  - Users
                  - Routing
                  - Profiles
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
                  - Users
                  - Chat
                  - Events
                  - Start
                  - Streaming
                  - Outbound
                  - Voice
                  - Web RTC
                  - Stop
                  - Submit
                  - Suspend
                  - Transfers
                  - Content
                  - Metadata
                  - Schedules
                  - Maximum
                  - Caller
                  - Availability
                  - Timer
                  - Concurrency
                  - Default
                  - Identity
                  - Info
            /users/{InstanceId}/{UserId}/security-profiles:
              POST:
                summary: UpdateUserSecurityProfiles
                description: >-
                  <p>Assigns the specified security profiles to the specified
                  user.</p>
                tags:
                  - Update
                  - Users
                  - Security
                  - Profiles
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
                  - Users
                  - Chat
                  - Events
                  - Start
                  - Streaming
                  - Outbound
                  - Voice
                  - Web RTC
                  - Stop
                  - Submit
                  - Suspend
                  - Transfers
                  - Content
                  - Metadata
                  - Schedules
                  - Maximum
                  - Caller
                  - Availability
                  - Timer
                  - Concurrency
                  - Default
                  - Identity
                  - Info
            /views/{InstanceId}/{ViewId}/metadata:
              POST:
                summary: UpdateViewMetadata
                description: >-
                  <p>Updates the view metadata. Note that either
                  <code>Name</code> or <code>Description</code> must be pro
                tags:
                  - Update
                  - View
                  - Metadata
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
                  - Users
                  - Chat
                  - Events
                  - Start
                  - Streaming
                  - Outbound
                  - Voice
                  - Web RTC
                  - Stop
                  - Submit
                  - Suspend
                  - Transfers
                  - Content
                  - Metadata
                  - Schedules
                  - Maximum
                  - Caller
                  - Availability
                  - Timer
                  - Concurrency
                  - Default
                  - Identity
                  - In
    overlays:
      - type: APIs.io Search
        url: overlays/connect-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/connect-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:connect
  - name: Symphony Pod API
    description: >-
      The Symphony Pod API is used to build tools in order to manage and
      administer Symphony for your organization. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://docs.developers.symphony.com/bots/overview-of-rest-api/pod-api
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: https://docs.developers.symphony.com/bots/overview-of-rest-api/pod-api
      - type: OpenAPI
        data:
          swagger: '2.0'
          info:
            title: Pod API
          host: yourpodURL.symphony.com
          basePath: /pod
          paths:
            /v1/companycert/list:
              get:
                summary: List all trusted certs
                tags:
                  - List
                  - All
                  - Trusted
                  - Certs
                  - V1
                  - Companycert
                  - List
            /v2/companycert/create:
              post:
                summary: >-
                  Create a company trusted or untrusted certificate. Different
                  from V1 in that we reject expired certificates.
                tags:
                  - Create
                  - Company
                  - Trusted
                  - Or
                  - Untrusted
                  - Certificate.
                  - Different
                  - From
                  - V1
                  - In
                  - That
                  - We
                  - Reject
                  - Expired
                  - Certificates.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
            /v1/companycert/delete:
              post:
                summary: Delete a company certificate
                tags:
                  - Delete
                  - Company
                  - Certificate
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
            /v1/companycert/{fingerPrint}/get:
              get:
                summary: Get the details of a company certificate
                tags:
                  - Get
                  - The
                  - Details
                  - Of
                  - Company
                  - Certificate
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
            /v1/companycert/{fingerPrint}/update:
              post:
                summary: Update a company certificate
                tags:
                  - Update
                  - Company
                  - Certificate
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
            /v1/companycert/{fingerPrint}/issuedBy:
              get:
                summary: >
                  Return a list of all certificates which were verified to the
                  cert whose

                  fingerprint is passed.
                tags:
                  - Return
                  - List
                  - Of
                  - All
                  - Certificates
                  - Which
                  - Were
                  - Verified
                  - To
                  - The
                  - Cert
                  - |-
                    Whose
                    fingerprint
                  - Is
                  - |
                    Passed.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
            /v1/companycert/podmanaged/list:
              get:
                summary: List all trusted certs
                tags:
                  - List
                  - All
                  - Trusted
                  - Certs
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
            /v1/companycert/type/list:
              post:
                summary: List all certs of the given types
                tags:
                  - List
                  - All
                  - Certs
                  - Of
                  - The
                  - Given
                  - Types
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
            /v1/podcert:
              get:
                summary: >
                  Retrieve the pod certificate that can be use to validate
                  signed JWT tokens generated from the pod
                tags:
                  - Retrieve
                  - The
                  - Pod
                  - Certificate
                  - That
                  - Can
                  - Be
                  - Use
                  - To
                  - Validate
                  - Signed
                  - Tokens
                  - Generated
                  - From
                  - |
                    Pod
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
            /v1/connection/list:
              get:
                summary: List of requesting user's connection
                description: >
                  This retrieves all connections of the requesting user. (i.e.
                  both connections in which the requesting user is the sender
                  and those

                  in which the requesting user is the inivtee) By default, if
                  you haven't specified the connection status to filter on, this
                  call will only

                  return results for both "pending_incoming" and
                  "pending_outgoing". You can optionally filter by userIds to
                  further restrict the results of

                  a specific connection status. If the users are in the same
                  private pod, the users have an implicit connection status of
                  "accepted". Those

                  users will not be returned in the response if you don't
                  specify the connection status as "accepted" (default is
                  "pending")

                  and the explicit userIds in the request.
                tags:
                  - List
                  - Of
                  - Requesting
                  - User's
                  - Connection
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
            /v1/connection/create:
              post:
                summary: Sends an invitation to connect with another user
                tags:
                  - Sends
                  - An
                  - Invitation
                  - To
                  - Connect
                  - With
                  - Another
                  - User
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
            /v1/connection/accept:
              post:
                summary: Accept the connection request for the requesting user
                tags:
                  - Accept
                  - The
                  - Connection
                  - Request
                  - For
                  - Requesting
                  - User
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
            /v1/connection/reject:
              post:
                summary: Reject the connection request for the requesting user.
                description: >
                  Reject the connection between the requesting user and request
                  sender. If both users are in the same private pod,

                  an error will be returned because both users have an implicit
                  connection which cannot be rejected.
                tags:
                  - Reject
                  - The
                  - Connection
                  - Request
                  - For
                  - Requesting
                  - User.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
            /v1/connection/user/{userId}/info:
              get:
                summary: The status of the connection invitation to another user.
                tags:
                  - The
                  - Status
                  - Of
                  - Connection
                  - Invitation
                  - To
                  - Another
                  - User.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
            /v1/connection/user/{uid}/remove:
              post:
                summary: Removes a connection with a user.
                tags:
                  - Removes
                  - Connection
                  - With
                  - User.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
            /v1/im/create:
              post:
                summary: >-
                  Create a new single or multi party instant message
                  conversation between the caller and specified users.
                description: >
                  At least one user ID must be provided or

                  an error response will be sent.


                  The caller is implicitly included in the members of the

                  created chat.


                  Duplicate users will be included in the membership of the chat
                  but

                  the duplication will be silently ignored.


                  If there is an existing IM conversation with the same set of
                  participants then

                  the id of that existing stream will be returned.


                  This method was incorrectly specified to take a query
                  parameter in

                  version 1.0 of this specification but now expects a JSON array
                  of

                  user IDs in the body of the request.
                tags:
                  - Create
                  - New
                  - Single
                  - Or
                  - Multi
                  - Party
                  - Instant
                  - Message
                  - Conversation
                  - Between
                  - The
                  - Caller
                  - And
                  - Specified
                  - Users.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
            /v1/im/{id}/update:
              post:
                summary: Update the attributes of an existing IM.
                tags:
                  - Update
                  - The
                  - Attributes
                  - Of
                  - An
                  - Existing
                  - M.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
            /v1/im/{id}/info:
              get:
                summary: Get information about a partcular IM.
                tags:
                  - Get
                  - Information
                  - About
                  - Partcular
                  - M.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
            /v1/presence/feed/create:
              post:
                summary: Create Presence status feed.
                description: >
                  Create a new stream capturing presence status changes
                  ("presence feed").

                  When read from, the feed will return the current presence
                  status of company (pod) users

                  if it has changed since the last read.


                  Returns the ID of the presence feed to be used in subsequent
                  read operations.
                tags:
                  - Create
                  - Presence
                  - Status
                  - Feed.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
            /v1/presence/feed/{feedId}/read:
              get:
                summary: Read a presence status feed.
                description: >
                  Returns the current presence status of company (pod) users

                  if it has changed since the last read. Returns up to 500
                  records at a time.
                tags:
                  - Read
                  - Presence
                  - Status
                  - Feed.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
            /v1/presence/feed/{feedId}/delete:
              post:
                summary: Delete a presence status feed.
                description: |
                  Returns the ID of the deleted feed.
                tags:
                  - Delete
                  - Presence
                  - Status
                  - Feed.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
            /v3/room/create:
              post:
                summary: Create a new chatroom.
                description: >
                  Create a new chatroom.


                  If no  attributes are specified, the room is created as a
                  private chatroom.
                tags:
                  - Create
                  - New
                  - Chatroom.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
            /v3/room/search:
              post:
                summary: Search rooms according to the specified criteria.
                tags:
                  - Search
                  - Rooms
                  - According
                  - To
                  - The
                  - Specified
                  - Criteria.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
            /v3/room/{id}/info:
              get:
                summary: Get information about a partcular chatroom.
                tags:
                  - Get
                  - Information
                  - About
                  - Partcular
                  - Chatroom.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
            /v1/room/{id}/setActive:
              post:
                summary: >-
                  Deactivate or reactivate a chatroom. At creation, a new
                  chatroom is active.
                tags:
                  - Deactivate
                  - Or
                  - Reactivate
                  - Chatroom.
                  - At
                  - Creation,
                  - New
                  - Chatroom
                  - Is
                  - Active.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
            /v3/room/{id}/update:
              post:
                summary: Update the attributes of an existing chatroom.
                tags:
                  - Update
                  - The
                  - Attributes
                  - Of
                  - An
                  - Existing
                  - Chatroom.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
            /v1/room/{id}/membership/add:
              post:
                summary: Adds new member to an existing room.
                tags:
                  - Adds
                  - New
                  - Member
                  - To
                  - An
                  - Existing
                  - Room.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
            /v1/room/{id}/membership/remove:
              post:
                summary: Removes member from an existing room.
                tags:
                  - Removes
                  - Member
                  - From
                  - An
                  - Existing
                  - Room.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
            /v1/room/{id}/membership/promoteOwner:
              post:
                summary: Promotes user to owner.
                tags:
                  - Promotes
                  - User
                  - To
                  - Owner.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
            /v1/room/{id}/membership/demoteOwner:
              post:
                summary: Demotes room owner.
                tags:
                  - Demotes
                  - Room
                  - Owner.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
            /v2/room/{id}/membership/list:
              get:
                summary: Lists current members of an existing room.
                tags:
                  - Lists
                  - Current
                  - Members
                  - Of
                  - An
                  - Existing
                  - Room.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
            /v2/sessioninfo:
              get:
                summary: Get information about the current user's session.
                tags:
                  - Get
                  - Information
                  - About
                  - The
                  - Current
                  - User's
                  - Session.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
            /v2/user:
              get:
                summary: Get user information
                tags:
                  - Get
                  - User
                  - Information
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
            /v3/users:
              get:
                summary: |
                  Search users by emails or ids.
                  Only one of the search lists should be informed at a time.
                  Search lists may containt up to 100 elements.
                tags:
                  - Search
                  - Users
                  - By
                  - Emails
                  - Or
                  - |
                    Ids.
                  - Only
                  - One
                  - Of
                  - The
                  - Lists
                  - Should
                  - Be
                  - Informed
                  - At
                  - |
                    Time.
                  - May
                  - Containt
                  - Up
                  - To
                  - '100'
                  - |
                    Elements.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
            /v1/user/presence/register:
              post:
                summary: Register interest in a user's presence status
                tags:
                  - Register
                  - Interest
                  - In
                  - User's
                  - Presence
                  - Status
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
            /v2/user/presence:
              get:
                summary: Get presence information about the requesting user.
                tags:
                  - Get
                  - Presence
                  - Information
                  - About
                  - The
                  - Requesting
                  - User.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
              post:
                summary: Set the presence of the requesting user.
                tags:
                  - Set
                  - The
                  - Presence
                  - Of
                  - Requesting
                  - User.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
            /v3/user/{uid}/presence:
              get:
                summary: Get presence information about a particular user.
                tags:
                  - Get
                  - Presence
                  - Information
                  - About
                  - Particular
                  - User.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
            /v2/users/presence:
              get:
                summary: Get presence information about all company (pod) users.
                description: >
                  The returned data is taken from the in-memory cache for
                  performance

                  reasons which means inactive users may be omitted from the
                  response.


                  All non-inactive users WILL be returned and some inactive
                  users MAY

                  be included. Any omitted user IS inactive.


                  Returned records are sorted by user ID, ascending.


                  This method is expensive. It pulls ALL records from the cache,
                  sorts them and then only uses a subset.

                  For large numbers of users, this can be very inefficient both
                  due to sorting

                  and due to the cache being distributed across many nodes.


                  Addiionally, there is the potential to miss users if they
                  become active

                  after the page in which their user ID falls has already been
                  read by the client.

                  To avoid this situation, a presence feed should be created
                  (and optionally read from)

                  first to capture presence changes of users who get reactivated
                  during a paged call to this endpoint.
                tags:
                  - Get
                  - Presence
                  - Information
                  - About
                  - All
                  - Company
                  - (pod)
                  - Users.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
            /v3/user/presence:
              post:
                summary: Set presence information for a particular user.
                tags:
                  - Set
                  - Presence
                  - Information
                  - For
                  - Particular
                  - User.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
            /v1/user/search:
              post:
                summary: Search for users by name or email address
                tags:
                  - Search
                  - For
                  - Users
                  - By
                  - Name
                  - Or
                  - Email
                  - Address
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
            /v1/streams/list:
              post:
                summary: >
                  Retrieve a list of all streams of which the requesting user is
                  a member,

                  sorted by creation date (ascending).
                tags:
                  - Retrieve
                  - List
                  - Of
                  - All
                  - Streams
                  - Which
                  - The
                  - Requesting
                  - User
                  - Is
                  - |-
                    Member,
                    sorted
                  - By
                  - Creation
                  - Date
                  - |
                    (ascending).
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
            /v1/admin/user/{uid}/streams/list:
              post:
                summary: |
                  Retrieve a list of all streams of which this user is a member,
                  sorted by creation date (ascending). Since SBE 20.16.
                tags:
                  - Retrieve
                  - List
                  - Of
                  - All
                  - Streams
                  - Which
                  - This
                  - User
                  - Is
                  - |-
                    Member,
                    sorted
                  - By
                  - Creation
                  - Date
                  - (ascending).
                  - Since
                  - |
                    20.16.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
            /v2/streams/{sid}/info:
              get:
                summary: Get information about a partcular stream.
                tags:
                  - Get
                  - Information
                  - About
                  - Partcular
                  - Stream.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
            /v1/streams/{sid}/attachments:
              get:
                summary: Get attachments in a particular stream.
                tags:
                  - Get
                  - Attachments
                  - In
                  - Particular
                  - Stream.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
            /v1/admin/app/entitlement/list:
              get:
                summary: Get the list of application entitlements for the company
                tags:
                  - Get
                  - The
                  - List
                  - Of
                  - Application
                  - Entitlements
                  - For
                  - Company
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
              post:
                summary: Update the application entitlements for the company
                tags:
                  - Update
                  - The
                  - Application
                  - Entitlements
                  - For
                  - Company
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
            /v1/admin/disclaimer/{did}:
              get:
                summary: Get a disclaimer by disclaimer id
                tags:
                  - Get
                  - Disclaimer
                  - By
                  - Id
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
            /v1/admin/disclaimer/list:
              get:
                summary: List all disclaimers for the company (pod)
                tags:
                  - List
                  - All
                  - Disclaimers
                  - For
                  - The
                  - Company
                  - (pod)
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
            /v1/admin/disclaimer/{did}/users:
              get:
                summary: List all users assigned to this disclaimer
                tags:
                  - List
                  - All
                  - Users
                  - Assigned
                  - To
                  - This
                  - Disclaimer
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
            /v1/admin/group/list:
              get:
                summary: Get a list of all Information Barrier Groups
                tags:
                  - Get
                  - List
                  - Of
                  - All
                  - Information
                  - Barrier
                  - Groups
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
            /v1/admin/group/{gid}/membership/list:
              get:
                summary: Get the list of userids in this Information Barrier Group
                tags:
                  - Get
                  - The
                  - List
                  - Of
                  - Userids
                  - In
                  - This
                  - Information
                  - Barrier
                  - Group
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
            /v1/admin/group/{gid}/membership/add:
              post:
                summary: Add members to an Information Barrier group.
                tags:
                  - Add
                  - Members
                  - To
                  - An
                  - Information
                  - Barrier
                  - Group.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
            /v1/admin/group/{gid}/membership/remove:
              post:
                summary: Remove members from an Information Barrier group
                tags:
                  - Remove
                  - Members
                  - From
                  - An
                  - Information
                  - Barrier
                  - Group
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
            /v1/admin/im/create:
              post:
                summary: >-
                  Create a new single or multi party instant message
                  conversation
                description: >
                  At least two user IDs must be provided or

                  an error response will be sent.


                  The caller is not included in the members of the

                  created chat.


                  Duplicate users will be included in the membership of the chat
                  but

                  the duplication will be silently ignored.


                  If there is an existing IM conversation with the same set of
                  participants then

                  the id of that existing stream will be returned.
                tags:
                  - Create
                  - New
                  - Single
                  - Or
                  - Multi
                  - Party
                  - Instant
                  - Message
                  - Conversation
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
            /v1/admin/messagesuppression/{id}/suppress:
              post:
                summary: Suppress a message
                tags:
                  - Suppress
                  - Message
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
            /v1/admin/policy/list:
              get:
                summary: Get all Information Policies
                tags:
                  - Get
                  - All
                  - Information
                  - Policies
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
            /v1/admin/room/{id}/setActive:
              post:
                summary: Deactivate or reactivate a chatroom via AC Portal.
                tags:
                  - Deactivate
                  - Or
                  - Reactivate
                  - Chatroom
                  - Via
                  - Portal.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
            /v1/admin/room/{id}/membership/list:
              get:
                summary: Lists current and previous members of an existing room.
                tags:
                  - Lists
                  - Current
                  - And
                  - Previous
                  - Members
                  - Of
                  - An
                  - Existing
                  - Room.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
            /v1/admin/room/{id}/membership/add:
              post:
                summary: Add a member to an existing room.
                tags:
                  - Add
                  - Member
                  - To
                  - An
                  - Existing
                  - Room.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
            /v1/admin/room/{id}/membership/remove:
              post:
                summary: Remove a member from a room.
                tags:
                  - Remove
                  - Member
                  - From
                  - Room.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
            /v2/admin/user/list:
              get:
                summary: Retrieve a list of all users in the company (pod)
                tags:
                  - Retrieve
                  - List
                  - Of
                  - All
                  - Users
                  - In
                  - The
                  - Company
                  - (pod)
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
            /v1/admin/user/find:
              post:
                summary: Find a user based on attributes
                tags:
                  - Find
                  - User
                  - Based
                  - 'On'
                  - Attributes
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
            /v1/admin/user/{uid}/roles/add:
              post:
                summary: Add a role to a user
                tags:
                  - Add
                  - Role
                  - To
                  - User
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
            /v1/admin/user/{uid}/roles/remove:
              post:
                summary: Remove a role from a user
                tags:
                  - Remove
                  - Role
                  - From
                  - User
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
            /v1/admin/user/{uid}/app/entitlement/list:
              get:
                summary: Get the list of application entitlements for this user
                tags:
                  - Get
                  - The
                  - List
                  - Of
                  - Application
                  - Entitlements
                  - For
                  - This
                  - User
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
              post:
                summary: Update the application entitlements for this user
                tags:
                  - Update
                  - The
                  - Application
                  - Entitlements
                  - For
                  - This
                  - User
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
              patch:
                summary: >-
                  Update unique entitlement of an app for this user. Entitlement
                  can be installation, visibility or product
                tags:
                  - Update
                  - Unique
                  - Entitlement
                  - Of
                  - An
                  - App
                  - For
                  - This
                  - User.
                  - Can
                  - Be
                  - Installation,
                  - Visibility
                  - Or
                  - Product
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
            /v1/admin/user/{uid}/avatar:
              get:
                summary: Get the URL of the avatar of a particular user
                tags:
                  - Get
                  - The
                  - Of
                  - Avatar
                  - Particular
                  - User
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
            /v1/admin/user/{uid}/avatar/update:
              post:
                summary: Update the avatar of a particular user
                tags:
                  - Update
                  - The
                  - Avatar
                  - Of
                  - Particular
                  - User
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
            /v1/admin/user/{uid}/disclaimer:
              get:
                summary: Get the disclaimer assigned to a user
                tags:
                  - Get
                  - The
                  - Disclaimer
                  - Assigned
                  - To
                  - User
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
              delete:
                summary: Unassign a disclaimer from a user
                tags:
                  - Unassign
                  - Disclaimer
                  - From
                  - User
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
            /v1/admin/user/{uid}/disclaimer/update:
              post:
                summary: Assign a disclaimer to a user
                tags:
                  - Assign
                  - Disclaimer
                  - To
                  - User
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
            /v1/admin/user/{uid}/delegates:
              get:
                summary: Get the delegates assigned to a user
                tags:
                  - Get
                  - The
                  - Delegates
                  - Assigned
                  - To
                  - User
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
            /v1/admin/user/{uid}/delegates/update:
              post:
                summary: Update the delegates assigned to a user
                tags:
                  - Update
                  - The
                  - Delegates
                  - Assigned
                  - To
                  - User
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
            /v1/admin/user/{uid}/features:
              get:
                summary: >-
                  Get the list of Symphony feature entitlements enabled for a
                  particular user
                tags:
                  - Get
                  - The
                  - List
                  - Of
                  - Symphony
                  - Feature
                  - Entitlements
                  - Enabled
                  - For
                  - Particular
                  - User
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
            /v1/admin/user/{uid}/features/update:
              post:
                summary: >-
                  Update the list of Symphony feature entitlements for a
                  particular user
                tags:
                  - Update
                  - The
                  - List
                  - Of
                  - Symphony
                  - Feature
                  - Entitlements
                  - For
                  - Particular
                  - User
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
            /v1/user/{uid}/follow:
              post:
                summary: Make a list of users start following a specific user
                tags:
                  - Make
                  - List
                  - Of
                  - Users
                  - Start
                  - Following
                  - Specific
                  - User
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
            /v1/user/{uid}/unfollow:
              post:
                summary: Make a list of users unfollowing a specific user
                tags:
                  - Make
                  - List
                  - Of
                  - Users
                  - Unfollowing
                  - Specific
                  - User
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
            /v1/user/{uid}/followers:
              get:
                summary: Returns the list of followers for a specific user
                tags:
                  - Returns
                  - The
                  - List
                  - Of
                  - Followers
                  - For
                  - Specific
                  - User
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
            /v1/user/{uid}/following:
              get:
                summary: Returns the list of users that a specific user is following
                tags:
                  - Returns
                  - The
                  - List
                  - Of
                  - Users
                  - That
                  - Specific
                  - User
                  - Is
                  - Following
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
                  - Following
            /v1/user/manifest/own:
              post:
                summary: Update own service account manifest
                tags:
                  - Update
                  - Own
                  - Service
                  - Account
                  - Manifest
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
                  - Following
                  - Manifest
                  - Own
              get:
                summary: Get own service account manifest
                tags:
                  - Get
                  - Own
                  - Service
                  - Account
                  - Manifest
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
                  - Following
                  - Manifest
                  - Own
            /v1/admin/user/{uid}/status:
              get:
                summary: Get the status, active or inactive, for a particular user
                tags:
                  - Get
                  - The
                  - Status,
                  - Active
                  - Or
                  - Inactive,
                  - For
                  - Particular
                  - User
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
                  - Following
                  - Manifest
                  - Own
                  - Status
            /v1/admin/user/{uid}/status/update:
              post:
                summary: Update the status of a particular user
                tags:
                  - Update
                  - The
                  - Status
                  - Of
                  - Particular
                  - User
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
                  - Following
                  - Manifest
                  - Own
                  - Status
            /v2/admin/streams/list:
              post:
                summary: >
                  Retrieve all the streams across the enterprise where the
                  membership of the stream has been modified between a given
                  time range
                tags:
                  - Retrieve
                  - All
                  - The
                  - Streams
                  - Across
                  - Enterprise
                  - Where
                  - Membership
                  - Of
                  - Stream
                  - Has
                  - Been
                  - Modified
                  - Between
                  - Given
                  - Time
                  - |
                    Range
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
                  - Following
                  - Manifest
                  - Own
                  - Status
            /v1/admin/stream/{id}/membership/list:
              get:
                summary: >-
                  List the current members of an existing stream.  The stream
                  can be of type IM, MIM, or ROOM
                tags:
                  - List
                  - The
                  - Current
                  - Members
                  - Of
                  - An
                  - Existing
                  - Stream.
                  - Stream
                  - Can
                  - Be
                  - Type
                  - M,
                  - Or
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
                  - Following
                  - Manifest
                  - Own
                  - Status
                  - Stream
            /v1/admin/system/features/list:
              get:
                summary: Get the full set of Symphony features available for this pod
                tags:
                  - Get
                  - The
                  - Full
                  - Set
                  - Of
                  - Symphony
                  - Features
                  - Available
                  - For
                  - This
                  - Pod
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
                  - Following
                  - Manifest
                  - Own
                  - Status
                  - Stream
                  - System
            /v1/admin/system/protocols/list:
              get:
                summary: Get a list of all URI protocols supported by the company (pod)
                tags:
                  - Get
                  - List
                  - Of
                  - All
                  - Protocols
                  - Supported
                  - By
                  - The
                  - Company
                  - (pod)
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
                  - Following
                  - Manifest
                  - Own
                  - Status
                  - Stream
                  - System
                  - Protocols
            /v2/system/protocols:
              get:
                summary: Get a list of URI protocols supported by the company (pod)
                tags:
                  - Get
                  - List
                  - Of
                  - Protocols
                  - Supported
                  - By
                  - The
                  - Company
                  - (pod)
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
                  - Following
                  - Manifest
                  - Own
                  - Status
                  - Stream
                  - System
                  - Protocols
            /v1/admin/system/protocols:
              post:
                summary: Add an entry to URI protocols supported by the company (pod)
                tags:
                  - Add
                  - An
                  - Entry
                  - To
                  - Protocols
                  - Supported
                  - By
                  - The
                  - Company
                  - (pod)
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
                  - Following
                  - Manifest
                  - Own
                  - Status
                  - Stream
                  - System
                  - Protocols
            /v1/admin/system/protocols/{scheme}:
              delete:
                summary: >-
                  Remove an entry from URI protocols supported by the company
                  (pod)
                tags:
                  - Remove
                  - An
                  - Entry
                  - From
                  - Protocols
                  - Supported
                  - By
                  - The
                  - Company
                  - (pod)
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
                  - Following
                  - Manifest
                  - Own
                  - Status
                  - Stream
                  - System
                  - Protocols
                  - Scheme
            /v1/admin/system/roles/list:
              get:
                summary: Get a list of all roles available in the company (pod)
                tags:
                  - Get
                  - List
                  - Of
                  - All
                  - Roles
                  - Available
                  - In
                  - The
                  - Company
                  - (pod)
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
                  - Following
                  - Manifest
                  - Own
                  - Status
                  - Stream
                  - System
                  - Protocols
                  - Scheme
            /v1/message/{mid}/status:
              get:
                summary: Get the read status of a particular message.
                tags:
                  - Get
                  - The
                  - Read
                  - Status
                  - Of
                  - Particular
                  - Message.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
                  - Following
                  - Manifest
                  - Own
                  - Status
                  - Stream
                  - System
                  - Protocols
                  - Scheme
                  - Message
                  - Mid
            /v1/admin/app/create:
              post:
                summary: Creates a new app
                tags:
                  - Creates
                  - New
                  - App
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
                  - Following
                  - Manifest
                  - Own
                  - Status
                  - Stream
                  - System
                  - Protocols
                  - Scheme
                  - Message
                  - Mid
            /v1/admin/app/{id}/update:
              post:
                summary: Updates a app
                tags:
                  - Updates
                  - App
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
                  - Following
                  - Manifest
                  - Own
                  - Status
                  - Stream
                  - System
                  - Protocols
                  - Scheme
                  - Message
                  - Mid
            /v1/admin/app/{id}/delete:
              post:
                summary: Deletes a app
                tags:
                  - Deletes
                  - App
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
                  - Following
                  - Manifest
                  - Own
                  - Status
                  - Stream
                  - System
                  - Protocols
                  - Scheme
                  - Message
                  - Mid
            /v1/admin/app/{id}/get:
              get:
                summary: Gets a app
                tags:
                  - Gets
                  - App
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
                  - Following
                  - Manifest
                  - Own
                  - Status
                  - Stream
                  - System
                  - Protocols
                  - Scheme
                  - Message
                  - Mid
            /v1/admin/messages:
              post:
                summary: Fetch message details
                tags:
                  - Fetch
                  - Message
                  - Details
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
                  - Following
                  - Manifest
                  - Own
                  - Status
                  - Stream
                  - System
                  - Protocols
                  - Scheme
                  - Message
                  - Mid
                  - Messages
            /v2/admin/user/create:
              post:
                summary: Create a new V2 User
                tags:
                  - Create
                  - New
                  - V2
                  - User
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
                  - Following
                  - Manifest
                  - Own
                  - Status
                  - Stream
                  - System
                  - Protocols
                  - Scheme
                  - Message
                  - Mid
                  - Messages
            /v2/admin/user/{uid}/update:
              post:
                summary: Update an existing V2 User
                tags:
                  - Update
                  - An
                  - Existing
                  - V2
                  - User
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
                  - Following
                  - Manifest
                  - Own
                  - Status
                  - Stream
                  - System
                  - Protocols
                  - Scheme
                  - Message
                  - Mid
                  - Messages
            /v2/admin/user/{uid}:
              get:
                summary: Retrieve V2 User details for a particular user
                tags:
                  - Retrieve
                  - V2
                  - User
                  - Details
                  - For
                  - Particular
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
                  - Following
                  - Manifest
                  - Own
                  - Status
                  - Stream
                  - System
                  - Protocols
                  - Scheme
                  - Message
                  - Mid
                  - Messages
            /v1/files/allowedTypes:
              get:
                summary: Get supported attachment types for the pod
                tags:
                  - Get
                  - Supported
                  - Attachment
                  - Types
                  - For
                  - The
                  - Pod
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
                  - Following
                  - Manifest
                  - Own
                  - Status
                  - Stream
                  - System
                  - Protocols
                  - Scheme
                  - Message
                  - Mid
                  - Messages
                  - Types
            /file_ext/v1/allowed_extensions:
              get:
                summary: Allows iteration of all file extensions supported for upload
                description: >
                  Provides a RESTful API to iterate all file extensions
                  configured by the tenant admin

                  that are allowed for the upload.  Pagination of this list is
                  managed through a

                  combination of the optional request parameters and
                  service-side managed maximums.


                  Pagination of the results is provided through the before or
                  after input paramters

                  and presented through the opaque cursor values provided as
                  output from a previous

                  response.  Only one of before or after or neither may be
                  provided.


                  DO NOT store cursors. Cursors can quickly become invalid if
                  items are added or deleted.

                  Use them only during a short-period of time that you are
                  traversing the list.
                tags:
                  - Allows
                  - Iteration
                  - Of
                  - All
                  - File
                  - Extensions
                  - Supported
                  - For
                  - Upload
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
                  - Following
                  - Manifest
                  - Own
                  - Status
                  - Stream
                  - System
                  - Protocols
                  - Scheme
                  - Message
                  - Mid
                  - Messages
                  - Types
                  - File_ext
                  - Allowed_extensions
            /file_ext/v1/allowed_extensions/{extension}:
              put:
                summary: >-
                  Allows replacement or creation of a specific file extension
                  supported for upload
                description: >
                  Provides a method to create or replace a specific file
                  extension configured for upload

                  support via an admin. The API treats the file extension in the
                  path case-insensitively

                  by converting it to lowecase.
                tags:
                  - Allows
                  - Replacement
                  - Or
                  - Creation
                  - Of
                  - Specific
                  - File
                  - Extension
                  - Supported
                  - For
                  - Upload
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
                  - Following
                  - Manifest
                  - Own
                  - Status
                  - Stream
                  - System
                  - Protocols
                  - Scheme
                  - Message
                  - Mid
                  - Messages
                  - Types
                  - File_ext
                  - Allowed_extensions
                  - Extension
              delete:
                summary: >-
                  Allows deletion of a specific file extension supported for
                  upload
                description: >
                  Provides a method to delete a specific file extension
                  configured for upload

                  support via an admin. The file extension identifying the
                  resource is treated

                  case-insensitively by the API.
                tags:
                  - Allows
                  - Deletion
                  - Of
                  - Specific
                  - File
                  - Extension
                  - Supported
                  - For
                  - Upload
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
                  - Following
                  - Manifest
                  - Own
                  - Status
                  - Stream
                  - System
                  - Protocols
                  - Scheme
                  - Message
                  - Mid
                  - Messages
                  - Types
                  - File_ext
                  - Allowed_extensions
                  - Extension
            /v1/admin/messages/{messageId}/receipts:
              get:
                summary: Fetch receipts details from a specific message.
                tags:
                  - Fetch
                  - Receipts
                  - Details
                  - From
                  - Specific
                  - Message.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
                  - Following
                  - Manifest
                  - Own
                  - Status
                  - Stream
                  - System
                  - Protocols
                  - Scheme
                  - Message
                  - Mid
                  - Messages
                  - Types
                  - File_ext
                  - Allowed_extensions
                  - Extension
                  - Receipts
            /v1/languages:
              get:
                summary: Lists available languages for the pod.
                tags:
                  - Lists
                  - Available
                  - Languages
                  - For
                  - The
                  - Pod.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
                  - Following
                  - Manifest
                  - Own
                  - Status
                  - Stream
                  - System
                  - Protocols
                  - Scheme
                  - Message
                  - Mid
                  - Messages
                  - Types
                  - File_ext
                  - Allowed_extensions
                  - Extension
                  - Receipts
                  - Languages
            /v1/admin/messages/{messageId}/metadata/relationships:
              get:
                summary: Get the message metadata relationship
                tags:
                  - Get
                  - The
                  - Message
                  - Metadata
                  - Relationship
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
                  - Following
                  - Manifest
                  - Own
                  - Status
                  - Stream
                  - System
                  - Protocols
                  - Scheme
                  - Message
                  - Mid
                  - Messages
                  - Types
                  - File_ext
                  - Allowed_extensions
                  - Extension
                  - Receipts
                  - Languages
                  - Metadata
                  - Relationships
            /v1/admin/user/{userId}/suspension/update:
              put:
                summary: Update the status of suspension of a particular user
                tags:
                  - Update
                  - The
                  - Status
                  - Of
                  - Suspension
                  - Particular
                  - User
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
                  - Following
                  - Manifest
                  - Own
                  - Status
                  - Stream
                  - System
                  - Protocols
                  - Scheme
                  - Message
                  - Mid
                  - Messages
                  - Types
                  - File_ext
                  - Allowed_extensions
                  - Extension
                  - Receipts
                  - Languages
                  - Metadata
                  - Relationships
                  - Suspension
          definitions:
            Error:
              type: object
              properties:
                code:
                  type: integer
                  format: int32
                  example: 401
                message:
                  type: string
                  example: Invalid session
            CompanyCert:
              type: object
              properties:
                pem:
                  type: string
                  description: An X509 certificate in PEM format
                  example: '--BEGIN CERTIFICATE--MIIH/TC...p9DBiB/--END CERTIFICATE--'
                attributes:
                  $ref: '#/definitions/CompanyCertAttributes'
            CompanyCertDetail:
              type: object
              properties:
                companyCertAttributes:
                  $ref: '#/definitions/CompanyCertAttributes'
                companyCertInfo:
                  $ref: '#/definitions/CompanyCertInfo'
                certInfo:
                  $ref: '#/definitions/CertInfo'
            CompanyCertInfoList:
              type: array
              items:
                type: object
                properties:
                  companyCertAttributes:
                    $ref: '#/definitions/CompanyCertAttributes'
                  companyCertInfo:
                    $ref: '#/definitions/CompanyCertInfo'
                example:
                  - companyCertAttributes:
                      name: agentservice
                      type:
                        type: USER
                      status:
                        type: TRUSTED
                    companyCertInfo:
                      fingerPrint: 300a...
                      lastSeen: 0
                      updatedAt: 0
                      updatedBy: 0
                      commonName: agentservice
                      expiryDate: 1781886755000
            CompanyCertType:
              type: object
              properties:
                type:
                  type: string
                  enum:
                    - USERSIGNING
                    - USER
                    - OPERATIONSSIGNING
                    - OPERATIONSUSER
                  example: USER
            CompanyCertTypeList:
              type: array
              items:
                $ref: '#/definitions/CompanyCertType'
            CompanyCertStatus:
              type: object
              properties:
                type:
                  type: string
                  enum:
                    - TRUSTED
                    - KNOWN
                    - REVOKED
                    - DISABLED
                  example: TRUSTED
            CompanyCertAttributes:
              type: object
              properties:
                name:
                  type: string
                  description: Friendly name assigned by administrator
                  example: agentservice
                type:
                  $ref: '#/definitions/CompanyCertType'
                status:
                  $ref: '#/definitions/CompanyCertStatus'
            CompanyCertInfo:
              type: object
              properties:
                fingerPrint:
                  type: string
                  description: Unique identifier
                  example: 300a...
                issuerFingerPrint:
                  type: string
                  description: Unique identifier of issuer cert if known
                  example: 450s...
                lastSeen:
                  type: integer
                  format: int64
                  description: Date when we last saw this certificate presented
                  example: 0
                updatedAt:
                  type: integer
                  format: int64
                  description: Date when this cert was last updated by administrator
                  example: 0
                updatedBy:
                  type: integer
                  format: int64
                  description: User ID of administrator who last updated this cert
                  example: 0
                commonName:
                  type: string
                  description: >-
                    The Symphony account name which this certificate
                    authenticates
                  example: agentservice
                expiryDate:
                  type: integer
                  format: int64
                  description: Expiry date of this cert
                  example: 1781886755000
            CertInfo:
              type: array
              items:
                $ref: '#/definitions/CertInfoItem'
              example:
                - name: Validity
                  attributes:
                    - name: Not Before
                      value: Mon Jan 15 20:56:05 UTC 2018
                    - name: Not After
                      value: Thu Jan 15 20:56:05 UTC 2026
                - name: Public Key
                  attributes:
                    - name: Algorithm
                      value: RSA
                    - name: Format
                      value: X.509
            CertInfoItem:
              type: object
              properties:
                name:
                  type: string
                  example: Public Key
                attributes:
                  type: array
                  items:
                    $ref: '#/definitions/NameValuePair'
                  example:
                    - name: Algorithm
                      value: RSA
                    - name: Format
                      value: X.509
            PodCertificate:
              type: object
              properties:
                certificate:
                  description: Certificate in PEM format
                  type: string
                  example: PEM_CERTIFICATE
            NameValuePair:
              type: object
              properties:
                name:
                  type: string
                  example: Algorithm
                value:
                  type: string
                  example: RSA
            Stream:
              type: object
              properties:
                id:
                  type: string
                  example: xhGxbTcvTDK6EIMMrwdOrX___quztr2HdA
            UserError:
              description: User error information
              type: object
              properties:
                error:
                  type: string
                  description: Error code informing what is wrong
                  example: invalid.format
                email:
                  type: string
                  description: >-
                    Email with error. Only one of the following fields should be
                    present: email or id
                  example: notavalidemail
                id:
                  type: string
                  description: >-
                    Id with error. Only one of the following fields should be
                    present: email or id
                  example: notavalidid
            UserV2:
              description: User record version 2
              type: object
              properties:
                id:
                  type: integer
                  format: int64
                  example: 7696581394433
                emailAddress:
                  type: string
                  format: email
                  example: admin@symphony.com
                firstName:
                  type: string
                  example: Symphony
                lastName:
                  type: string
                  example: Admin
                displayName:
                  type: string
                  example: Symphony Admin
                title:
                  type: string
                  example: Administrator
                company:
                  type: string
                  example: Acme
                username:
                  type: string
                  example: admin@symphony.com
                location:
                  type: string
                  example: California
                accountType:
                  type: string
                  enum:
                    - NORMAL
                    - SYSTEM
                    - SDL
                  example: NORMAL
                avatars:
                  $ref: '#/definitions/AvatarList'
                workPhoneNumber:
                  type: string
                  description: >-
                    Note: only available if the application has the extended
                    user or contact permission
                  example: '+33901020304'
                mobilePhoneNumber:
                  type: string
                  description: >-
                    Note: only available if the application has the extended
                    user or contact permission
                  example: '+33601020304'
                jobFunction:
                  type: string
                  description: >-
                    Note: only available if the application has the extended
                    user or contact permission
                  example: Sales
                department:
                  type: string
                  description: >-
                    Note: only available if the application has the extended
                    user or contact permission
                  example: APIs
                division:
                  type: string
                  description: >-
                    Note: only available if the application has the extended
                    user or contact permission
                  example: Partnerships
                roles:
                  $ref: '#/definitions/StringList'
                  example:
                    - INDIVIDUAL
                    - SUPER_ADMINISTRATOR
            V2UserList:
              description: List of User record version 2
              type: object
              properties:
                users:
                  type: array
                  items:
                    $ref: '#/definitions/UserV2'
                  description: List of all users found with the search
                  example:
                    - id: 15942919536460
                      emailAddress: technicalwriter@symphony.com
                      firstName: Technical
                      lastName: Writer
                      displayName: Technical Writer
                      title: Technical Writer
                      company: Symphony
                      department: Marketing // if internal user
                      username: tw
                      accountType: NORMAL
                      location: France // if internal user
                      mobilePhoneNumber: 33601020304
                      avatars:
                        - size: original
                          url: ../avatars/static/150/default.png
                        - size: small
                          url: ../avatars/static/50/default.png
                    - id: 15942919536461
                      emailAddress: serviceaccount@symphony.com
                      firstName: null
                      lastName: null
                      displayName: Service Account
                      title: null
                      company: pod232
                      department: Marketing // if internal user
                      username: SA
                      location: France // if internal user
                      accountType: SYSTEM
                      avatars:
                        - size: original
                          url: ../avatars/static/150/default.png
                        - size: small
                          url: ../avatars/static/50/default.png
                errors:
                  type: array
                  items:
                    $ref: '#/definitions/UserError'
                  description: List of all errors found with the informed search criteria
                  example:
                    - error: invalid.format
                      email: notavalidemail
                    - error: invalid.format
                      id: 654321
            UserSearchResults:
              type: object
              properties:
                count:
                  description: The total number of users which matched the search criteria.
                  type: integer
                  format: int64
                  example: 1
                skip:
                  description: The number of skipped results.
                  type: integer
                  format: int64
                  example: 0
                limit:
                  description: The number of returned results.
                  type: integer
                  format: int64
                  example: 1
                searchQuery:
                  $ref: '#/definitions/UserSearchQuery'
                users:
                  description: A list of users which matched by the search criteria.
                  type: array
                  items:
                    $ref: '#/definitions/UserV2'
                  example:
                    - null
            UserSearchFilter:
              type: object
              properties:
                accountTypes:
                  $ref: '#/definitions/StringList'
                  description: type of user used to search
                  example: NORMAL
                title:
                  type: string
                  description: user's job title
                  example: Sales Manager
                company:
                  type: string
                  description: company name
                  example: Symphony
                location:
                  type: string
                  description: city of the user's job location
                  example: Marseille
                marketCoverage:
                  type: string
                  description: geographic area the user works with
                  example: EMEA
                responsibility:
                  type: string
                  description: user's responsibility
                  example: BAU
                function:
                  type: string
                  description: user's function
                  example: Trade Management
                instrument:
                  type: string
                  description: higher level instrument for the Asset Classes
                  example: Securities
            UserSearchQuery:
              type: object
              properties:
                query:
                  type: string
                  description: >-
                    search / query term.  This can be firstname, lastname,
                    displayname or email
                  example: jane
                filters:
                  $ref: '#/definitions/UserSearchFilter'
            UserNameList:
              type: array
              items:
                type: object
                $ref: '#/definitions/UserName'
            UserName:
              type: object
              properties:
                username:
                  type: string
                  example: dpayet
            UserIdList:
              type: array
              items:
                type: integer
                format: int64
              example:
                - 7215545058313
                - 7215545078461
            UserId:
              type: object
              properties:
                id:
                  type: integer
                  format: int64
                  example: 7215545058313
            StringId:
              type: object
              properties:
                id:
                  type: string
                  example: xhGxbTcvTDK6EIMMrwdOrX___quztr2HdA
            RoomAttributes:
              type: object
              properties:
                name:
                  type: string
                  description: Room name.
                description:
                  type: string
                  description: Room description.
                membersCanInvite:
                  type: boolean
                  description: >-
                    If true, any chatroom participant can add new participants.
                    If false, only owners can add new participants.
                discoverable:
                  type: boolean
                  description: >-
                    If true, this chatroom (name, description and messages) can
                    be searched and listed by non-participants. If false, only
                    participants can search this room.
            V3RoomAttributes:
              type: object
              properties:
                name:
                  type: string
                  description: Room name.
                  example: API room
                keywords:
                  type: array
                  description: Keywords for search to use to find this room
                  items:
                    $ref: '#/definitions/RoomTag'
                  example:
                    - key: region
                      value: EMEA
                    - key: lead
                      value: Daffy Duck
                description:
                  type: string
                  description: Room description.
                  example: Created via the API
                membersCanInvite:
                  type: boolean
                  description: >-
                    If true, any chatroom participant can add new participants.
                    If false, only owners can add new participants.
                  example: true
                discoverable:
                  type: boolean
                  description: >-
                    If true, this chatroom (name, description and messages) can
                    be searched and listed by non-participants. If false, only
                    participants can search this room.
                  example: false
                public:
                  type: boolean
                  description: >-
                    If true, this is a public chatroom. IF false, a private
                    chatroom.
                  example: false
                readOnly:
                  type: boolean
                  description: If true, only stream owners can send messages.
                  example: false
                copyProtected:
                  type: boolean
                  description: >-
                    If true, clients disable the clipboard copy for content in
                    this stream.
                  example: false
                crossPod:
                  type: boolean
                  description: If true, this room is a cross pod room
                  example: false
                viewHistory:
                  type: boolean
                  description: >-
                    If true, new members can view the room chat history of the
                    room.
                  example: false
                multiLateralRoom:
                  type: boolean
                  description: >-
                    If true, this is a multi lateral room where we can find
                    users belonging to more than 2 companies.
                  example: false
                scheduledMeeting:
                  type: boolean
                  description: If true, this room is for a scheduled meeting.
                  example: false
                subType:
                  type: string
                  description: >-
                    This field is ignored when creating a new room as it was
                    only used for email integration which is now sunset.
                pinnedMessageId:
                  type: string
                  description: >-
                    UrlSafe message id of the pinned message inside the room. To
                    perform unpin operation, send an empty string.
                  example: vd7qwNb6hLoUV0BfXXPC43___oPIvkwJbQ
                groupChat:
                  type: boolean
                  description: >-
                    If true, this room is a group chat. Note: this parameter is
                    ignored for creating rooms. Since SBE 20.16.
                  x-since: 20.16
                  example: false
            RoomSearchCriteria:
              description: >-
                Room Query Object. Used to specify the parameters for room
                search.
              properties:
                query:
                  description: The search query. Matches the room name and description.
                  type: string
                  example: automobile
                labels:
                  description: A list of room tag labels whose values will be queried.
                  type: array
                  items:
                    type: string
                  example:
                    - industry
                active:
                  description: >-
                    Restrict the search to active/inactive rooms. If
                    unspecified, search all rooms.
                  type: boolean
                  example: true
                private:
                  description: >-
                    Restrict the search to private rooms. If unspecified, search
                    all rooms.
                  type: boolean
                  example: true
                owner:
                  $ref: '#/definitions/UserId'
                creator:
                  $ref: '#/definitions/UserId'
                member:
                  $ref: '#/definitions/UserId'
                sortOrder:
                  description: >
                    Sort algorithm to be used. Supports two values: "BASIC"
                    (legacy algorithm)

                    and "RELEVANCE" (enhanced algorithm).
                  type: string
                  enum:
                    - BASIC
                    - RELEVANCE
                  example: RELEVANCE
              required:
                - query
            V2RoomSearchCriteria:
              description: >-
                Room Query Object. Used to specify the parameters for room
                search.
              allOf:
                - $ref: '#/definitions/RoomSearchCriteria'
                - type: object
                  properties:
                    subType:
                      description: >-
                        Restrict the search to the specific room subtype. Valid
                        values are: EMAIL
                      type: string
                      example: EMAIL
            V3RoomSearchResults:
              description: A list of search results and counts per search parameter.
              properties:
                count:
                  description: The total number of rooms matched by the search.
                  type: integer
                  format: int64
                  example: 2
                skip:
                  description: The number of skipped results.
                  type: integer
                  example: 0
                limit:
                  description: The number of returned results.
                  type: integer
                  example: 10
                query:
                  $ref: '#/definitions/V2RoomSearchCriteria'
                rooms:
                  description: A list of rooms matched by the query.
                  type: array
                  items:
                    $ref: '#/definitions/V3RoomDetail'
                  example:
                    - roomAttributes:
                        name: Automobile Industry Room
                        description: Room to discuss car companies
                        membersCanInvite: true
                        readOnly: false
                        copyProtected: false
                        crossPod: false
                        viewHistory: false
                        public: false
                        multiLateralRoom: false
                      roomSystemInfo:
                        id: tzwvAZIdDMG3ZPRxv+xsgH///qr+JJkWdA==
                        creationDate: 1464615003895
                        createdByUserId: 7696581411197
                        active: true
                    - roomAttributes:
                        name: Tesla Room
                        keywords:
                          - key: industry
                            value: automobile
                        description: Discussions on TSLA
                        membersCanInvite: true
                        readOnly: false
                        copyProtected: false
                        crossPod: false
                        viewHistory: false
                        public: false
                        multiLateralRoom: false
                      roomSystemInfo:
                        id: o6UkQ1TEmU0Tf/DHUlZrCH///qr+JQowdA==
                        creationDate: 1464614974947
                        createdByUserId: 7696581411197
                        active: true
                facetedMatchCount:
                  description: Detailed counts of matched rooms per search criterion.
                  type: array
                  items:
                    $ref: '#/definitions/FacetedMatchCount'
                  example:
                    - facet: industry
                      count: 1
            RoomTag:
              description: >-
                Room Tag object. A key:value pair describing additional
                properties of the room.
              properties:
                key:
                  description: A unique label of the Tag.
                  type: string
                  example: region
                value:
                  description: The value of this Tag's label.
                  type: string
                  example: EMEA
              required:
                - key
                - value
            FacetedMatchCount:
              description: An object respresenting the result count of faceted search.
              properties:
                facet:
                  description: The matched query.
                  type: string
                count:
                  description: The result count.
                  type: integer
            RoomSystemInfo:
              type: object
              properties:
                id:
                  type: string
                  example: bjHSiY4iz3ar4iIh6-VzCX___peoM7cPdA
                creationDate:
                  type: integer
                  format: int64
                  description: >-
                    The datetime when the stream was originally created.
                    Milliseconds since Jan 1 1970.
                  example: 1547661232368
                createdByUserId:
                  type: integer
                  format: int64
                  example: 14362370637825
                active:
                  type: boolean
                  description: >-
                    If false, no messages can be sent in this stream, and
                    membership is locked.
                  example: true
            ImmutableRoomAttributes:
              type: object
              description: >-
                These attributes cannot be changed once the room has been
                created
              properties:
                public:
                  type: boolean
                  description: >-
                    If true, this is a public chatroom. IF false, a private
                    chatroom.
                readOnly:
                  type: boolean
                  description: If true, only stream owners can send messages.
                copyProtected:
                  type: boolean
                  description: >-
                    If true, clients disable the clipboard copy for content in
                    this stream.
            RoomDetail:
              type: object
              properties:
                roomAttributes:
                  $ref: '#/definitions/RoomAttributes'
                roomSystemInfo:
                  $ref: '#/definitions/RoomSystemInfo'
                immutableRoomAttributes:
                  $ref: '#/definitions/ImmutableRoomAttributes'
            V3RoomDetail:
              type: object
              properties:
                roomAttributes:
                  $ref: '#/definitions/V3RoomAttributes'
                roomSystemInfo:
                  $ref: '#/definitions/RoomSystemInfo'
                groups:
                  description: List of groups (aka SDLs) that were added to the room.
                  type: array
                  items:
                    $ref: '#/definitions/GroupItem'
                  example:
                    - id: 68719476744
                      addedBy: 68719476743
            GroupItem:
              type: object
              properties:
                id:
                  description: The ID of the added group (aka SDL).
                  type: integer
                  format: int64
                  example: 68719476744
                addedBy:
                  description: The user ID who added the group to the room.
                  type: integer
                  format: int64
                  example: 68719476743
            SuccessResponse:
              type: object
              properties:
                format:
                  type: string
                  enum:
                    - TEXT
                    - XML
                  example: TEXT
                message:
                  type: string
                  example: Success
            AvatarUpdate:
              type: object
              properties:
                image:
                  description: Base64 encoded image. Original image must be less than 2MB.
                  type: string
                  example: >-
                    iVBORw0KGgoAAAANSUhEUgAAAJgAAAAoCAMAAAA11sNmAAAAGXRFWHRTb2Z0d2FyZQBBZG9iZSBJbWFnZVJlYWR5ccllPAAAAX1QTFRFAAAAVVVVZmZmc8bmd3d3jMyMmZmZ+cxA////VVVVZmZmc8bmd3d3jMyM8oCZ+cxA////VVVVZmZmc8bmd3d3jMyM////VVVVZmZmc8bmd3d3jMyMmZmZ8oCZ+cxA////ZmZmjMyM////VVVVd3d3jMyM+cxA////VVVVZmZmc8bmd3d3jMyMmZmZnMyB8oCZ+cxA////ZmZmc8bmd3d3jMyMmZmZ+cxA////d3d3jMyM8oCZ+cxA////VVVVZmZmdm1RjMyM8oCZ+cxA////ZmZmmZmZ+cxA////W1tbZmZmc8bmdpGcd3d3jMyMmZmZ8oCZ////d3d3jMyMmZmZx3iJ+cxA////VVVVZmZmc8bmd3d3jMyMuIOVyqpG////VVVVZmZmbW1td3d3jMyMmZmZ+cxA////VVVVX1xUZmZmb46ac8bmdZ+vd3d3fnNQjMyMkpeGlqaWmJyYmZmZnYlMp5FLsZhJvJ9Iz3qM0K5F78VB8oCZ+cxA////9laq9wAAAGh0Uk5TABAQEBAQEBAQICAgICAgICAwMDAwMDBAQEBAQEBAQEBQUFBgYGBgYHBwcHBwcHBwcHCAgICAgICAj4+Pj4+fn5+fn5+fr6+vr7+/v7+/v7+/v8/Pz8/Pz9/f39/f39/f7+/v7+/v7+/qia/hAAADQ0lEQVRYw+2Xa1fTQBCGV0WJCBIvxEq10YoEVNQoaLxURKNWUHRRqYgaUSC1QkWsNzT7252Z3W1TWpCjX+I5fT/ksrM782T2Tc4JYy211NL/oJ50Ot2TRLD5FdTkma6kgU2uSB1PGtiY5HqZuK0ckWAjiQNLS7CdiQPrIq6xpGHtGnr0eRXA0gnjGlqoVCoA9kTe9rfXQob1r8ntv1mUmjlGYBUJdhJv2u9FlzWVHwohAt9kBuc+Dfk8zxjnWRnn3GHM4lKuAUM5nsMIjNETOQVM4NJstQpCzKxL10TjpdJ4B5zvEtg8Wj+zGEVRtwxjVpLFckIAA8sKAVWECBGCeUJ40BI9qwCDXHBqkxDYKT8WwVWWDDFMh5QOpWtURwk0dwE8toBgV2HoeoQ6T2GL6rJsAZ7OCBAGjgUqIbAvptBgNggo/XVgMJQ3mZmHk1wVGArMCPEajrxpwwZLpJkUO4JgXax7mriiaaay1xyWRQhPjsgmAoQGk9uCVeJg1bo+TafW6enxdI26U1Ia3X6psjrJ+hcjJQpjRwLOPYf2DZ7blp2iEhxz14FxCRZ4IB/BbLlflMjDVQVsqprOKZ3HNrKY0tzg09Wzt4Ho59r3NThlKO6E0iLkDTNUe4EloLAb4FGCIUuebrg2HIB5ihgXEJgNZI4Ci6XbDKxUevvp9bcvH98Xi8WvVTAo6no5yBbgtSt0B6AEAoRGM/PXOuZUd0qDgUeFxnWFfEGaaX8q9eyH0qsP998USTczmUx7/BPkqlSByOs6NrwY8EJpMPxa+E51P5XHTL1VLj0RDlm0B6w+XVPd+kV6fHRieWrbwHMEO6FjDr5TMTCuLYElctjGOo+x9WC4r0hrh9RyGsrWwPhGDiOdk1js4tJy+Qpjh24Ui/t0LIceJ/PkG8GM0P4jGPqogFYILQ2GxtsS2F7CYoeXAKzcCwO7B2rBrPrCcqMRrOadjcHgCy/NZ8VW+VsDY9cAi+14QWDv2tZHLcfzXP2tsWxTvRK2oS9gxLBjHrZsmm3oKZbreVbdqur0arpNtGeCwMoPk/czcuDUAwArn07gf9IwgpUPJhVsqi2hYLOdiQSb7Uugx3qH+zpZSy211FJNvwFNoXAncdBvawAAAABJRU5ErkJggg==
            Avatar:
              type: object
              properties:
                size:
                  description: The Avatar Size
                  type: string
                  example: original
                url:
                  description: Url of the image
                  type: string
                  example: ../avatars/izcQTdRVFOK_qhCrYeQOpIuHKuZuMk3J88Uz_bShzM8.png
            AvatarList:
              type: array
              items:
                $ref: '#/definitions/Avatar'
              example:
                - size: original
                  url: ../avatars/izcQTdRVFOK_qhCrYeQOpIuHKuZuMk3J88Uz_bShzM8.png
                - size: small
                  url: >-
                    ../avatars/izcQTdRVFOK_qhCrYeQOpIuHKuZuMk3J88Uz_bShzM8_small.png
            UserStatus:
              type: object
              properties:
                status:
                  type: string
                  enum:
                    - ENABLED
                    - DISABLED
                  example: ENABLED
                suspended:
                  type: boolean
                  description: >-
                    An optional attribute indicating whether the user is
                    temporarily suspended or not. Since SBE 20.14.
                  x-since: 20.14
                  example: true
                suspendedUntil:
                  type: integer
                  format: int64
                  description: >-
                    An optional unix timestamp until which the suspension is
                    effective. Since SBE 20.14.
                  x-since: 20.14
                  example: 1601546400
                suspensionReason:
                  type: string
                  description: >-
                    An optional description of the suspension reason. Since SBE
                    20.14.
                  x-since: 20.14
                  example: The user will be OOO due to a mandatory leave
            UserFilter:
              type: object
              properties:
                role:
                  type: string
                  description: The user role
                  example: INDIVIDUAL
                feature:
                  type: string
                status:
                  type: string
                  enum:
                    - ENABLED
                    - DISABLED
            PasswordReset:
              type: object
              properties:
                type:
                  type: string
                  enum:
                    - EMAIL
                  example: EMAIL
            FeatureList:
              type: array
              items:
                $ref: '#/definitions/Feature'
              example:
                - entitlment: canCreatePublicRoom
                  enabled: true
                - entitlment: isExternalRoomEnabled
                  enabled: false
                - entitlment: canUpdateAvatar
                  enabled: true
            Feature:
              description: Entitlement feature record.
              type: object
              properties:
                entitlment:
                  type: string
                  example: canCreatePublicRoom
                enabled:
                  type: boolean
                  description: Whether this entitlement is enabled for the user.
                  example: true
            Group:
              description: Information Barrier Group record.
              type: object
              properties:
                id:
                  type: string
                  example: 571db1f2e4b027c4f055a594
                name:
                  type: string
                  example: Group 1
                active:
                  type: boolean
                  example: true
                memberCount:
                  type: integer
                  format: int32
                  example: 1
                policies:
                  type: array
                  items:
                    type: string
                  example:
                    - 571db2e4e4b012df6341f393
                createdDate:
                  type: integer
                  format: int64
                  example: 1461563890135
                modifiedDate:
                  type: integer
                  format: int64
                  example: 1461563926812
            Product:
              description: Application Product
              type: object
              required:
                - name
                - type
                - subscribed
              properties:
                appId:
                  type: string
                  description: App ID for the Product
                  maxLength: 256
                  minLength: 1
                  example: selerity
                name:
                  type: string
                  minLength: 1
                  maxLength: 50
                  description: Product Name
                  example: Premium
                sku:
                  type: string
                  minLength: 1
                  maxLength: 100
                  description: Product SKU
                  example: AcDccU53SsY
                subscribed:
                  type: boolean
                  description: indicate whether the product is subscribed or not
                  example: false
                type:
                  type: string
                  description: Product Type (default or premium)
                  example: premium
            ProductList:
              type: array
              items:
                $ref: '#/definitions/Product'
              example:
                - appId: selerity
                  name: Standard
                  subscribed: true
                  type: default
                - appId: selerity
                  name: Premium
                  sku: AcDccU53SsY
                  subscribed: false
                  type: premium
            PolicyList:
              type: array
              items:
                $ref: '#/definitions/Policy'
              example:
                - id: 56e9df05e4b00737e3d3b82d
                  policyType: BLOCK
                  active: true
                  groups:
                    - 56e9def8e4b0b406041812e6
                    - 56e9deffe4b0b406041812e7
                  createdDate: 1458167557358
                  modifiedDate: 1458330606752
                - id: 571cd64de4b042aaf06d2d8b
                  policyType: BLOCK
                  active: true
                  groups:
                    - 571cd646e4b042aaf06d2d84
                    - 571cd64ce4b042aaf06d2d8a
                  createdDate: 1461507661146
                  modifiedDate: 1461507661146
            Policy:
              description: Information Barrier Policy record.
              type: object
              properties:
                id:
                  type: string
                  example: 56e9df05e4b00737e3d3b82d
                policyType:
                  type: string
                  enum:
                    - BLOCK
                    - ALLOW
                  example: BLOCK
                active:
                  type: boolean
                  example: true
                memberCount:
                  type: integer
                  format: int32
                  example: 3
                groups:
                  type: array
                  items:
                    type: string
                  example:
                    - 56e9deffe4b0b406041812e6
                    - 56e9deffe4b0b406041812e7
                createdDate:
                  type: integer
                  format: int64
                  example: 1458167557358
                modifiedDate:
                  type: integer
                  format: int64
                  example: 1458330606752
            UserAppEntitlement:
              description: Application Entitlements for the user
              type: object
              required:
                - appId
                - listed
                - install
              properties:
                appId:
                  type: string
                  description: Unique ID for the Application
                  maxLength: 256
                  minLength: 1
                  example: selerity
                appName:
                  type: string
                  description: Name for this Application
                  maxLength: 50
                  minLength: 1
                  example: Selerity Context
                listed:
                  type: boolean
                  description: >-
                    if true, this application will be listed in the appstore for
                    this user.  Otherwise, this application will be hidden in
                    the appstore.
                  example: true
                install:
                  type: boolean
                  description: >-
                    if true, it indicate this application is installed for this
                    user.  Otherwise, this user does not have this application
                    installed.
                  example: true
                products:
                  $ref: '#/definitions/ProductList'
            PodAppEntitlement:
              description: Application Entitlements for the company
              type: object
              required:
                - appId
                - appName
                - enable
                - listed
                - install
              properties:
                appId:
                  type: string
                  description: Unique ID for the Application
                  maxLength: 256
                  minLength: 1
                  example: djApp
                appName:
                  type: string
                  description: Name for this Application
                  maxLength: 50
                  minLength: 1
                  example: Dow Jones
                enable:
                  type: boolean
                  example: true
                listed:
                  type: boolean
                  description: >-
                    if true, this application will be listed in the appstore for
                    everyone.  Otherwise, this application will be hidden in the
                    appstore.
                  example: true
                install:
                  type: boolean
                  description: >-
                    if true, the entitlement is set to automatic for the
                    company.  Otherwise, it is set to manual.
                  example: true
            Role:
              description: Role record.
              type: object
              properties:
                id:
                  type: string
                  format: long
                name:
                  type: string
                description:
                  type: string
            RoleDetailList:
              type: array
              items:
                $ref: '#/definitions/RoleDetail'
              example:
                - id: CONTENT_MANAGEMENT
                  name: Content Management
                  userTypes:
                    - SYSTEM
                    - NORMAL
                  optionalActions:
                    - MONITOR_ROOMS
                - id: COMPLIANCE_OFFICER
                  name: Compliance Officer
                  userTypes:
                    - NORMAL
                  optionalActions:
                    - BAN_AND_UNBAN_ROOM_MEMBER
                    - LOCK_AND_UNLOCK_ROOM
                    - MONITOR_ROOMS
                    - MONITOR_WALL_POSTS
            RoleDetail:
              description: Role detailed.
              type: object
              properties:
                id:
                  type: string
                  example: CONTENT_MANAGEMENT
                name:
                  type: string
                  example: Content Management
                userTypes:
                  type: array
                  items:
                    type: string
                  example:
                    - NORMAL
                    - SYSTEM
                optionalActions:
                  type: array
                  items:
                    type: string
                  example:
                    - MONITOR_ROOMS
                    - MONITOR_WALL_POSTS
            GroupList:
              type: array
              items:
                $ref: '#/definitions/Group'
              example:
                - id: 571db1f2e4b027c4f055a594
                  name: Group 1
                  active: true
                  memberCount: 1
                  policies:
                    - 571db2e4e4b012df6341f393
                  createdDate: 1461563890135
                  modifiedDate: 1461563926812
                - id: 571db20ae4b012df6341f391
                  name: Group 2
                  active: true
                  memberCount: 1
                  policies:
                    - 571db2e4e4b012df6341f393
                  createdDate: 1461563914581
                  modifiedDate: 1461564112286
            UserAppEntitlementsPatchList:
              description: Array of app entitlements to patch for a user
              type: array
              items:
                $ref: '#/definitions/UserAppEntitlementPatch'
            UserAppEntitlementPatchEnum:
              type: object
              default: KEEP
              description: null
              properties:
                type:
                  type: string
                  enum: &ref_0
                    - 'TRUE'
                    - 'FALSE'
                    - KEEP
                    - REMOVE
                  description: |
                    UserAppEntitlementPatchEnum type :
                     * TRUE - The parameter should be set to true.
                     * FALSE - The parameter should be set to false.
                     * KEEP - The parameter should not be updated, the current value will be kept.
                     * REMOVE - The parameter should be reverted to tenant level's value.
                  example: KEEP
            UserAppEntitlementPatch:
              description: Application Entitlements to patch for the user
              type: object
              required:
                - appId
              properties:
                appId:
                  type: string
                  description: Unique ID for the Application
                  maxLength: 256
                  minLength: 1
                  example: selerity
                listed:
                  type: string
                  enum: *ref_0
                  default: KEEP
                  description: >-
                    If "TRUE", this application will be listed in the appstore
                    for this user. If "FALSE", this application will be hidden
                    in the appstore. If "KEEP" or not set, the current value is
                    kept. If "REMOVE", it will be removed from user settings and
                    the pod level setting's value will be used.
                  example: KEEP
                install:
                  type: string
                  enum: *ref_0
                  default: KEEP
                  description: >-
                    If "TRUE", this application will be installed for this user.
                    If "FALSE", this application will not be installed for this
                    user. If "KEEP" or not set, the current value is kept. If
                    "REMOVE", it will be removed from user settings and the pod
                    level setting's value will be used.
                  example: true
                product:
                  $ref: '#/definitions/Product'
            UserAppEntitlementList:
              type: array
              items:
                $ref: '#/definitions/UserAppEntitlement'
              example:
                - appId: djApp
                  appName: Dow Jones
                  listed: true
                  install: false
                - appId: selerity
                  appName: Selerity Context
                  listed: true
                  install: true
                  products:
                    - appId: selerity
                      name: Standard
                      subscribed: true
                      type: default
                    - appId: selerity
                      name: Premium
                      sku: AcDccU53SsY
                      subscribed: false
                      type: premium
            PodAppEntitlementList:
              type: array
              items:
                $ref: '#/definitions/PodAppEntitlement'
              example:
                - appId: djApp
                  appName: Dow Jones
                  enable: true
                  listed: true
                  install: false
                - appId: selerity
                  appName: Selerity Context
                  enable: false
                  listed: true
                  install: true
            RoleList:
              type: array
              items:
                $ref: '#/definitions/Role'
            IntegerList:
              type: array
              items:
                type: integer
                format: int64
              example:
                - 1461508270000
                - 7215545057281
            StringList:
              type: array
              items:
                type: string
              example:
                - ftp
                - mailto
                - fdsup
                - skype
            DisclaimerList:
              type: array
              items:
                $ref: '#/definitions/Disclaimer'
              example:
                - id: 571d2052e4b042aaf06d2e7a
                  name: Enterprise Disclaimer
                  content: This is a disclaimer for the enterprise.
                  frequencyInHours: 24
                  isDefault: false
                  isActive: true
                  createdDate: 1461526610846
                  modifiedDate: 1461526610846
                - id: 571d20dae4b042aaf06d2e7c
                  name: New Enterprise Disclaimer
                  content: This is a second enterprise disclaimer.
                  frequencyInHours: 168
                  isDefault: false
                  isActive: true
                  createdDate: 1461526746875
                  modifiedDate: 1461526746875
            Disclaimer:
              type: object
              properties:
                id:
                  type: string
                  example: 571d20dae4b042aaf06d2e7c
                name:
                  type: string
                  example: New Enterprise Disclaimer
                content:
                  type: string
                  example: This is a second enterprise disclaimer.
                frequencyInHours:
                  type: integer
                  format: int32
                  example: 168
                isDefault:
                  type: boolean
                  example: false
                isActive:
                  type: boolean
                  example: true
                createdDate:
                  type: integer
                  format: int64
                  example: 1461526746875
                modifiedDate:
                  type: integer
                  format: int64
                  example: 1461526746875
                format:
                  type: string
                  enum:
                    - TEXT
                    - XML
                  example: TEXT
            DelegateAction:
              type: object
              properties:
                userId:
                  type: integer
                  format: int64
                  example: 7215545078461
                action:
                  type: string
                  enum:
                    - ADD
                    - REMOVE
                  example: ADD
            UserInfo:
              description: User record.
              type: object
              properties:
                user:
                  $ref: '#/definitions/UserAttributes'
                userSystemInfo:
                  $ref: '#/definitions/UserSystemInfo'
            UserAttributes:
              description: User record.
              type: object
              properties:
                emailAddress:
                  type: string
                  example: janedoe@symphony.com
                firstName:
                  type: string
                  example: Jane
                lastName:
                  type: string
                  example: Doe
                userName:
                  type: string
                  example: jane.doe
                displayName:
                  type: string
                  example: Jane Doe
                companyName:
                  type: string
                  example: Company
                department:
                  type: string
                  example: Department
                division:
                  type: string
                  example: Division
                title:
                  type: string
                  example: Trader
                workPhoneNumber:
                  type: string
                  example: '+12349999999'
                mobilePhoneNumber:
                  type: string
                  example: '+12349999999'
                smsNumber:
                  type: string
                  example: '+12349999999'
                accountType:
                  type: string
                  enum:
                    - NORMAL
                    - SYSTEM
                    - SDL
                  example: NORMAL
                location:
                  type: string
                  example: New York
                jobFunction:
                  type: string
                  example: Trader
                assetClasses:
                  type: array
                  items:
                    type: string
                  example:
                    - Commodities
                industries:
                  type: array
                  items:
                    type: string
                  example:
                    - Financials
                    - Services
            V2UserDetail:
              description: V2 Detailed User record.
              type: object
              properties:
                userAttributes:
                  $ref: '#/definitions/V2UserAttributes'
                userSystemInfo:
                  $ref: '#/definitions/UserSystemInfo'
                features:
                  $ref: '#/definitions/IntegerList'
                apps:
                  $ref: '#/definitions/IntegerList'
                groups:
                  $ref: '#/definitions/IntegerList'
                roles:
                  $ref: '#/definitions/StringList'
                disclaimers:
                  $ref: '#/definitions/IntegerList'
                avatar:
                  $ref: '#/definitions/Avatar'
            V2UserAttributes:
              description: V2 User record.
              type: object
              properties:
                emailAddress:
                  type: string
                  example: johndoe@symphony.com
                firstName:
                  type: string
                  example: John
                lastName:
                  type: string
                  example: Doe
                userName:
                  type: string
                  example: johndoe
                displayName:
                  type: string
                  example: John Doe
                companyName:
                  type: string
                  example: Company
                department:
                  type: string
                  example: Department
                division:
                  type: string
                  example: Division
                title:
                  type: string
                  example: Trader
                workPhoneNumber:
                  type: string
                  example: '+15419999999'
                mobilePhoneNumber:
                  type: string
                  example: '+15419999999'
                twoFactorAuthPhone:
                  type: string
                  example: '+15419999999'
                smsNumber:
                  type: string
                  example: '+15419999999'
                accountType:
                  type: string
                  enum:
                    - NORMAL
                    - SYSTEM
                    - SDL
                  example: NORMAL
                location:
                  type: string
                  example: New York
                recommendedLanguage:
                  type: string
                  example: english
                jobFunction:
                  type: string
                  example: Trader
                assetClasses:
                  type: array
                  items:
                    type: string
                  example:
                    - Equities
                industries:
                  type: array
                  items:
                    type: string
                  example:
                    - Healthcare
                    - Technology
                marketCoverage:
                  type: array
                  items:
                    type: string
                  example:
                    - EMEA
                responsibility:
                  type: array
                  items:
                    type: string
                  example:
                    - BAU
                function:
                  type: array
                  items:
                    type: string
                  example:
                    - Trade Processing
                instrument:
                  type: array
                  items:
                    type: string
                  example:
                    - Equities
                currentKey:
                  $ref: '#/definitions/V2UserKeyRequest'
                previousKey:
                  $ref: '#/definitions/V2UserKeyRequest'
            V2UserKeyRequest:
              description: User RSA key information.
              type: object
              properties:
                key:
                  description: User RSA public key.
                  type: string
                  example: >-
                    --BEGIN PUBLIC KEY--\nMIICIANBgkqhw0BAQ...cCAwEAAQ==\n--END
                    PUBLIC KEY--
                expirationDate:
                  description: >-
                    RSA key expiration date. This value is set just for rotated
                    keys.
                  type: integer
                  format: int64
                  example: 1467562406219
                action:
                  description: >
                    Action to be performed on the RSA key.

                    The following actions can be performed onto the user's
                    active RSA key:
                      - SAVE
                      - REVOKE
                    The following actions can be performed onto the user's
                    rotated RSA key:
                      - REVOKE
                      - EXTEND
                  type: string
                  example: SAVE
            V2UserCreate:
              description: >
                V2 User Creation Object.

                After creation, modify roles, features etc via the specific API
                calls.
              type: object
              properties:
                userAttributes:
                  $ref: '#/definitions/V2UserAttributes'
                password:
                  $ref: '#/definitions/Password'
                roles:
                  type: array
                  items:
                    type: string
                  example:
                    - INDIVIDUAL
                    - COMPLIANCE_OFFICER
            V2UserDetailList:
              type: array
              items:
                $ref: '#/definitions/V2UserDetail'
              example:
                - userAttributes:
                    emailAddress: nexus.user@email.com
                    userName: nexus.user
                    displayName: nexus.user
                    accountType: SYSTEM
                  userSystemInfo:
                    id: 9826885173290
                    status: ENABLED
                    suspended: false
                    createdDate: 1499375475000
                    createdBy: '9826885173255'
                    lastUpdatedDate: 1499375475852
                    lastLoginDate: 1504899124191
                  roles:
                    - USER_PROVISIONING
                    - CONTENT_MANAGEMENT
                    - INDIVIDUAL
                - userAttributes:
                    emailAddress: admin@mail.com
                    firstName: admin
                    lastName: admin
                    userName: admin@mail.com
                    displayName: Admin Admin
                    companyName: Company Name
                    department: Departament
                    division: Division
                    title: Administrator
                    twoFactorAuthPhone: '+15419999999'
                    workPhoneNumber: '+15419999999'
                    mobilePhoneNumber: '+15419999999'
                    accountType: NORMAL
                    assetClasses:
                      - Currencies
                    industries:
                      - Technology
                  userSystemInfo:
                    id: 7696581394433
                    status: ENABLED
                    suspended: false
                    createdDate: 1438054194000
                    lastUpdatedDate: 1527532171729
                    lastLoginDate: 1523912043015
                  roles:
                    - SUPER_COMPLIANCE_OFFICER
                    - INDIVIDUAL
                    - SUPER_ADMINISTRATOR
            UserSystemInfo:
              description: User Status Information.
              type: object
              properties:
                id:
                  type: integer
                  format: int64
                  example: 7215545078461
                status:
                  type: string
                  enum:
                    - ENABLED
                    - DISABLED
                  example: ENABLED
                suspended:
                  type: boolean
                  description: >-
                    An optional attribute indicating whether the user is
                    temporarily suspended or not. Since SBE 20.14.
                  x-since: 20.14
                  example: true
                suspendedUntil:
                  type: integer
                  format: int64
                  description: >-
                    An optional unix timestamp until which the suspension is
                    effective. Since SBE 20.14.
                  x-since: 20.14
                  example: 1601546400
                suspensionReason:
                  type: string
                  description: >-
                    An optional description of the suspension reason. Since SBE
                    20.14.
                  x-since: 20.14
                  example: The user will be OOO due to a mandatory leave
                createdDate:
                  type: integer
                  format: int64
                  example: 1461508270000
                createdBy:
                  type: string
                  example: '7215545057281'
                lastUpdatedDate:
                  type: integer
                  format: int64
                  example: 1461508270000
                lastLoginDate:
                  type: integer
                  format: int64
                  example: 1461508270000
                lastPasswordReset:
                  type: integer
                  format: int64
                  example: 1461508270000
                deactivatedDate:
                  type: integer
                  format: int64
                  example: 1461508270000
            UserDetailList:
              type: array
              items:
                $ref: '#/definitions/UserDetail'
              example:
                - userAttributes:
                    emailAddress: janedoe@symphony.com
                    firstName: Jane
                    lastName: Doe
                    userName: jane.doe
                    displayName: Jane Doe
                    accountType: NORMAL
                    assetClasses:
                      - Commodities
                    industries:
                      - Financials
                      - Healthcare
                  userSystemInfo:
                    id: 9826885173258
                    status: ENABLED
                    suspended: true
                    suspensionReason: The user will be OOO due to a mandatory leave
                    suspendedUntil: 1601546400
                    createdDate: 1499347606000
                    createdBy: '9826885173252'
                    lastUpdatedDate: 1499348554853
                    lastLoginDate: 1504839044527
                  roles:
                    - INDIVIDUAL
                - userAttributes:
                    emailAddress: nexus.user@email.com
                    userName: nexus.user
                    displayName: nexus.user
                    accountType: SYSTEM
                  userSystemInfo:
                    id: 9826885173290
                    status: ENABLED
                    suspended: false
                    createdDate: 1499375475000
                    createdBy: '9826885173255'
                    lastUpdatedDate: 1499375475852
                    lastLoginDate: 1504899124191
                  roles:
                    - USER_PROVISIONING
                    - CONTENT_MANAGEMENT
                    - INDIVIDUAL
            UserDetail:
              description: Detailed User record.
              type: object
              properties:
                userAttributes:
                  $ref: '#/definitions/UserAttributes'
                userSystemInfo:
                  $ref: '#/definitions/UserSystemInfo'
                features:
                  $ref: '#/definitions/IntegerList'
                apps:
                  $ref: '#/definitions/IntegerList'
                groups:
                  $ref: '#/definitions/IntegerList'
                roles:
                  $ref: '#/definitions/StringList'
                disclaimers:
                  $ref: '#/definitions/IntegerList'
                avatar:
                  $ref: '#/definitions/Avatar'
            Password:
              description: >-
                Password. Stored as derived password in both the Pod and the Key
                Manager using PBKDF2 function. Number of iterations should be
                10000 and desired length 256 bits.
              type: object
              properties:
                hSalt:
                  description: Pod password salt used for PBKDF2 derivation.
                  type: string
                  example: hsalt
                hPassword:
                  description: Pod password derived with PBKDF2.
                  type: string
                  example: hpassword
                khSalt:
                  description: Key Manager password salt used for PBKDF2 derivation.
                  type: string
                  example: khsalt
                khPassword:
                  description: Key Manager password derived with PBKDF2.
                  type: string
                  example: khpassword
            MemberInfo:
              description: Detailed membership record.
              type: object
              properties:
                id:
                  type: integer
                  format: int64
                  example: 7078106103810
                owner:
                  type: boolean
                  example: true
                joinDate:
                  type: integer
                  format: int64
                  example: 1461426797833
                addedThroughGroups:
                  description: >-
                    When the user has been added to the stream through a group
                    (aka SDL), this array contains the group ID which the user
                    belongs to. Since SBE 20.14.
                  x-since: 20.14
                  type: array
                  items:
                    type: integer
                    format: int64
                  example:
                    - 68719476744
            MembershipList:
              description: List of members in a room.
              type: array
              items:
                $ref: '#/definitions/MemberInfo'
              example:
                - id: 7078106103900
                  owner: false
                  joinDate: 1461430710531
                - id: 7078106103809
                  owner: true
                  joinDate: 1461426797875
                - id: 7078106103810
                  owner: true
                  joinDate: 1461426797833
                  addedThroughGroups:
                    - 68719476744
            V2MemberUserDetail:
              description: User detail information for stream membership
              type: object
              properties:
                userId:
                  type: integer
                  format: int64
                  example: 13537736917013
                email:
                  type: string
                  example: dpayet@om.fr
                firstName:
                  type: string
                  example: Dimitri
                lastName:
                  type: string
                  example: Payet
                displayName:
                  type: string
                  description: Display name for the user
                  example: Dimitri Payet
                company:
                  type: string
                  description: Company name
                  example: Mars
                companyId:
                  type: integer
                  description: Company ID
                  example: 13
                isExternal:
                  type: boolean
                  description: true indicate that this user belong to another company
                  example: true
            V2MemberInfo:
              description: Detailed membership record.
              type: object
              properties:
                user:
                  $ref: '#/definitions/V2MemberUserDetail'
                isOwner:
                  type: boolean
                  description: true if this is an owner of the room
                  example: true
                isCreator:
                  type: boolean
                  description: true if this is the creator of the room
                  example: true
                joinDate:
                  description: unix timestamp for join date
                  type: integer
                  format: int64
                  example: 1604494574047
                addedThroughGroups:
                  description: >-
                    When the user has been added to the stream through a group
                    (aka SDL), this array contains the group ID which the user
                    belongs to. Since SBE 20.14.
                  x-since: 20.14
                  type: array
                  items:
                    type: integer
                    format: int64
                  example:
                    - 68719476744
            V2MemberInfoList:
              type: array
              items:
                $ref: '#/definitions/V2MemberInfo'
              example:
                - user:
                    userId: 13537736917000
                    email: john.doe@symphony.com
                    firstName: John
                    lastName: Doe
                    displayName: John Doe
                    company: pod197
                    companyId: 197
                    isExternal: false
                  isOwner: true
                  isCreator: true
                  joinDate: 1604494574047
                - user:
                    userId: 13537736917001
                    email: bot@symphony.com
                    displayName: User Provisioning Bot
                    company: pod197
                    companyId: 197
                    isExternal: false
                  isOwner: false
                  isCreator: false
                  joinDate: 1604494605272
                  addedThroughGroups:
                    - 68719476744
            V2MembershipList:
              description: List of members in the stream.
              type: object
              properties:
                count:
                  type: integer
                  description: total members count
                  example: null
                skip:
                  type: integer
                  description: number of items to skip from the request
                  example: null
                limit:
                  type: integer
                  description: maximum number of items to return
                  example: null
                members:
                  $ref: '#/definitions/V2MemberInfoList'
            MessageSuppressionResponse:
              description: The suppression state of a message
              type: object
              properties:
                messageId:
                  type: string
                  example: _Gj13MiR-5IrVtrmPNl6fn___qvWCYI_dA
                suppressed:
                  type: boolean
                  example: true
                suppressionDate:
                  type: integer
                  format: int64
                  description: The date when this message was suppressed.
                  example: 1461565603191
            BulkActionResult:
              description: >
                The results of list based bulk action. The list contains the
                result messages

                in the same order as submitted. The message will be an empty
                string if the action

                was successful for item in that index.
              properties:
                overallResult:
                  type: string
                  enum:
                    - SUCCESS
                    - FAIL
                  example: SUCCESS
                results:
                  type: array
                  items:
                    type: string
                  example:
                    - ''
            UserConnectionRequest:
              type: object
              description: Request body for the Connection APIs
              properties:
                userId:
                  type: integer
                  format: int64
                  description: user id
                  example: 769658112378
            UserConnection:
              type: object
              description: Connection status between two users
              properties:
                userId:
                  type: integer
                  format: int64
                  description: user id
                  example: 769658112378
                status:
                  type: string
                  description: >-
                    Connection status between the requesting user and the
                    request sender
                  enum:
                    - PENDING_INCOMING
                    - PENDING_OUTGOING
                    - ACCEPTED
                    - REJECTED
                  example: ACCEPTED
                firstRequestedAt:
                  type: integer
                  format: int64
                  description: unix timestamp when the first request was made
                  example: 1470018073812
                updatedAt:
                  type: integer
                  format: int64
                  description: unix timestamp on the last updated date
                  example: 1471018076255
                requestCounter:
                  type: integer
                  format: int32
                  description: number of requests made
                  example: 1
            UserConnectionList:
              type: array
              items:
                $ref: '#/definitions/UserConnection'
              example:
                - userId: 769658112378
                  status: PENDING_OUTGOING
                  firstRequestedAt: 1470018073812
                  updatedAt: 1471018076255
                  requestCounter: 1
                - userId: 7078106103809
                  status: ACCEPTED
            StreamList:
              description: A list of streams of which the requesting user is a member.
              type: array
              items:
                $ref: '#/definitions/StreamAttributes'
            StreamAttributes:
              type: object
              properties:
                id:
                  type: string
                  description: The stream ID.
                crossPod:
                  type: boolean
                  description: If true, this is a cross-pod stream.
                active:
                  type: boolean
                  description: If true, this stream is active.
                streamType:
                  $ref: '#/definitions/StreamType'
                streamAttributes:
                  $ref: '#/definitions/ConversationSpecificStreamAttributes'
                roomAttributes:
                  $ref: '#/definitions/RoomSpecificStreamAttributes'
            StreamType:
              type: object
              properties:
                type:
                  type: string
                  enum:
                    - IM
                    - MIM
                    - ROOM
                    - POST
                  example: ROOM
            ConversationSpecificStreamAttributes:
              type: object
              properties:
                members:
                  $ref: '#/definitions/UserIdList'
            RoomSpecificStreamAttributes:
              type: object
              properties:
                name:
                  type: string
                  description: Room name.
            StreamFilter:
              description: Stream filtering parameters.
              properties:
                streamTypes:
                  description: Types of streams to search for.
                  type: array
                  items:
                    $ref: '#/definitions/StreamType'
                  example:
                    - type: IM
                    - type: ROOM
                includeInactiveStreams:
                  description: Whether to include inactive streams in the list of results.
                  type: boolean
                  example: 'false'
            V2StreamAttributes:
              type: object
              properties:
                id:
                  type: string
                  description: The stream ID.
                  example: BZQYepoT0Zf4vL_jpeMPqn___oEWvVy3dA
                crossPod:
                  type: boolean
                  description: If true, this is a cross-pod stream.
                  example: false
                origin:
                  type: string
                  description: >-
                    INTERNAL if the creator of this stream belongs to the pod,
                    EXTERNAL otherwise
                  example: INTERNAL
                active:
                  type: boolean
                  description: If true, this stream is active.
                  example: true
                lastMessageDate:
                  type: integer
                  format: int64
                  description: unix timestamp of the last message sent in the stream
                  example: 1644590972696
                streamType:
                  description: >-
                    The type of the stream (IM = IM, multi-IM = MIM, chat room =
                    ROOM, user wall = POST).
                  $ref: '#/definitions/V2StreamType'
                streamAttributes:
                  $ref: '#/definitions/V2ConversationSpecificStreamAttributes'
                roomAttributes:
                  $ref: '#/definitions/V2RoomSpecificStreamAttributes'
            V2StreamType:
              type: object
              properties:
                type:
                  type: string
                  example: ROOM
            V2ConversationSpecificStreamAttributes:
              type: object
              properties:
                members:
                  $ref: '#/definitions/UserIdList'
            V2RoomSpecificStreamAttributes:
              type: object
              properties:
                name:
                  type: string
                  description: Room name.
                  example: API room
                groups:
                  description: >-
                    List of groups (aka SDLs) that were added to the room. Since
                    SBE 20.14.
                  x-since: 20.14
                  type: array
                  items:
                    $ref: '#/definitions/GroupItem'
                  example:
                    - id: 68719476744
                      addedBy: 68719476743
            V2AdminStreamFilter:
              description: stream filter criteria
              type: object
              properties:
                streamTypes:
                  description: type of streams to search for
                  type: array
                  items:
                    description: Valid values are IM, MIM or ROOM
                    $ref: '#/definitions/V2AdminStreamType'
                  example:
                    - type: IM
                    - type: ROOM
                scope:
                  description: >
                    Scope of the room. Valid values are INTERNAL or EXTERNAL.

                    If not specified, it will include both Internal and External
                    scope
                  type: string
                  example: INTERNAL
                origin:
                  description: >
                    Origin of the room. It indicates whether the room was
                    created by a user within the company by another company.

                    Valid values are INTERNAL or EXTERNAL.

                    If not specified, it will include both Internal and External
                    origin
                  type: string
                  example: INTERNAL
                status:
                  description: >
                    Status of the room.

                    Valid values are ACTIVE or INACTIVE.

                    If not specified, it will include both Active and Inactive
                    status
                  type: string
                  example: ACTIVE
                privacy:
                  description: >
                    Privacy setting of the stream.

                    Valid values are PUBLIC or PRIVATE.

                    If not specified, it will include both public and private
                    streams
                  type: string
                  example: PRIVATE
                startDate:
                  description: Start date in unix timestamp in millseconds
                  type: integer
                  format: int64
                  example: 1481575056047
                endDate:
                  description: >-
                    End date in unix timestamp in millseconds.  If not
                    specified, it assume to be current time.
                  type: integer
                  format: int64
                  example: 1483038089833
            V2AdminStreamType:
              type: object
              properties:
                type:
                  type: string
                  example: ROOM
            AdminJustifiedUserAction:
              type: object
              properties:
                userId:
                  description: The userId of the target user.
                  type: integer
                  format: int64
                justification:
                  description: The reason for the requested action.
                  type: string
            AdminJustifiedAction:
              type: object
              properties:
                justification:
                  description: The reason for the requested action.
                  type: string
            MessageStatusUser:
              type: object
              properties:
                userId:
                  type: string
                  example: 7078106103901
                firstName:
                  type: string
                  example: Gustav
                lastName:
                  type: string
                  example: Mahler
                displayName:
                  type: string
                  example: Gustav Mahler
                email:
                  type: string
                  example: gustav.mahler@music.org
                userName:
                  type: string
                  example: gmahler
                timestamp:
                  type: string
                  example: 1531968487845
            MessageStatus:
              description: >
                Holds the status of a particular message, indicating which user
                the message has been sent, delivered or read.
              type: object
              properties:
                author:
                  description: User who has sent the message.
                  type: object
                  $ref: '#/definitions/MessageStatusUser'
                read:
                  description: >-
                    All users who have read that message, in any Symphony
                    client.
                  type: array
                  items:
                    $ref: '#/definitions/MessageStatusUser'
                delivered:
                  description: >
                    All users who have at least one Symphony client to which the
                    message has been delivered, and not read yet.
                  type: array
                  items:
                    $ref: '#/definitions/MessageStatusUser'
                sent:
                  description: >
                    All users to whom the message has been sent and received by
                    the Symphony system,

                    but not yet delivered to any user's Symphony client.
                  type: array
                  items:
                    $ref: '#/definitions/MessageStatusUser'
                  example:
                    - userId: 7078106103904
                      firsName: Benjamin
                      lastName: Britten
                      displayName: Benjamin Britten
                      email: benjamin.britten@music.org
                      userName: bbritten
                      timestamp: 1484156123000
                    - userId: 7078106103901
                      firsName: Gustav
                      lastName: Mahler
                      displayName: Gustav Mahler
                      email: gmahler@music.org
                      userName: gmahler
                      timestamp: 1531968487845
            ApplicationInfo:
              description: |
                Required information for creating an application.
              type: object
              properties:
                appId:
                  description: An unique id for the application.
                  type: string
                  maxLength: 256
                  minLength: 1
                name:
                  description: User defined name for the application.
                  type: string
                appUrl:
                  description: The url for the app. Must start with "https://".
                  type: string
                domain:
                  description: Domain for app, that must match app url domain.
                  type: string
                publisher:
                  description: The publisher for this application.
                  type: string
              example:
                appId: my-test-app
                name: my-test-app
                appUrl: https://joe.mydomain.com
                domain: mydomain.com
                publisher: Joe Smith
            ApplicationDetail:
              description: Detailed record of application.
              type: object
              properties:
                applicationInfo:
                  $ref: '#/definitions/ApplicationInfo'
                iconUrl:
                  description: Url to a icon to use for app. Must start with "https://".
                  type: string
                  example: https://myiconUrl.com
                description:
                  description: Description of the application.
                  type: string
                  example: a test app
                allowOrigins:
                  description: >
                    The permitted domains to send or receive a request from.

                    The field is for the purpose of CORS which set the app
                    specific "ALLOW-ORIGIN-DOMAINS" header in HTTP.
                  type: string
                  example: mydomain.com
                permissions:
                  description: >
                    List of application permissions provisioned for the
                    application.

                    In addition to the known ones, custom permissions are
                    accepted.

                    A custom permission should only contain upper case
                    alphanumeric characters and underscore.

                    It should not be empty or only contain spaces and its length
                    is limited to 64 characters.


                    Known permissions:
                      - SEND_MESSAGES
                      - GET_USER_CONNECTIONS
                      - REQUEST_USER_CONNECTIONS
                      - SET_PRESENCE
                      - GET_PRESENCE
                      - GET_BASIC_USER_INFO
                      - GET_EXTENDED_USER_INFO
                      - GET_BASIC_CONTACT_INFO
                      - GET_EXTENDED_CONTACT_INFO
                      - ACT_AS_USER
                      - MANAGE_SIGNALS
                      - MANAGE_USER_FOLLOWING
                      - TRUST_APP
                  type: array
                  items:
                    type: string
                    maxLength: 64
                    minLength: 1
                  example:
                    - ACT_AS_USER
                    - SEND_MESSAGES
                cert:
                  description: The app public certificate in pem format.
                  type: string
                  example: >-
                    --BEGIN PUBLIC KEY--\nMIICIANBgkqhw0BAQ...cCAwEAAQ==\n--END
                    PUBLIC KEY--
                authenticationKeys:
                  $ref: '#/definitions/AppAuthenticationKeys'
                notification:
                  $ref: '#/definitions/AppNotification'
                properties:
                  $ref: '#/definitions/AppProperties'
            V2PresenceList:
              type: array
              items:
                $ref: '#/definitions/V2Presence'
              example:
                - category: AVAILABLE
                  userId: 14568529068038
                  timestamp: 1533928483800
                - category: OFFLINE
                  userId: 974217539631
                  timestamp: 1503286226030
            V2Presence:
              allOf:
                - $ref: '#/definitions/V2UserPresence'
                - type: object
                  properties:
                    timestamp:
                      type: integer
                      format: int64
                      description: >-
                        The time, in milliseconds since Jan 1 1970, when the
                        presence state was set.
                      example: 1533928483800
            V2UserPresence:
              allOf:
                - $ref: '#/definitions/V2PresenceStatus'
                - type: object
                  properties:
                    userId:
                      type: integer
                      format: int64
                      description: The ID of the user to whom the presence state relates.
                      example: 14568529068038
            V2PresenceStatus:
              type: object
              properties:
                category:
                  type: string
                  description: |
                    Presence status. Possible values are:
                      - UNDEFINED
                      - AVAILABLE
                      - BUSY
                      - DO_NOT_DISTURB
                      - ON_THE_PHONE
                      - BE_RIGHT_BACK
                      - IN_A_MEETING
                      - AWAY
                      - OUT_OF_OFFICE
                      - OFF_WORK
                      - OFFLINE
                  example: AWAY
              required:
                - category
            V2AdminStreamList:
              description: list of streams info
              type: object
              properties:
                count:
                  type: integer
                  format: int64
                  description: total number of streams which match the filter criteria
                  example: 4
                skip:
                  type: integer
                  description: number of streams skipped
                  example: 0
                limit:
                  type: integer
                  description: maximum number of streams return
                  example: 50
                filter:
                  $ref: '#/definitions/V2AdminStreamFilter'
                streams:
                  $ref: '#/definitions/V2AdminStreamInfoList'
            V2AdminStreamInfoList:
              type: array
              description: list of stream info
              items:
                $ref: '#/definitions/V2AdminStreamInfo'
              example:
                - id: Q2KYGm7JkljrgymMajYTJ3___qcLPr1UdA
                  isExternal: false
                  isActive: true
                  isPublic: false
                  type: ROOM
                  attributes:
                    roomName: Active Internal Private Room
                    roomDescription: Active Internal Private Room
                    createdByUserId: 8933531975689
                    createdDate: 1481575056047
                    lastModifiedDate: 1481575056047
                    originCompany: Symphony
                    originCompanyId: 130
                    membersCount: 1
                    lastMessageDate: 1516699467959
                - id: _KnoYrMkhEn3H2_8vE0kl3___qb5SANQdA
                  isExternal: true
                  isActive: false
                  isPublic: false
                  type: ROOM
                  attributes:
                    roomName: Inactive External Room
                    roomDescription: Inactive External Room
                    createdByUserId: 8933531975686
                    createdDate: 1481876438194
                    lastModifiedDate: 1481876438194
                    originCompany: Symphony
                    originCompanyId: 130
                    membersCount: 2
                    lastMessageDate: 1516699467959
            V2AdminStreamInfo:
              description: Stream information
              type: object
              properties:
                id:
                  type: string
                  description: stream id
                  example: Q2KYGm7JkljrgymMajYTJ3___qcLPr1UdA
                isExternal:
                  type: boolean
                  description: >-
                    true indicate this stream has the scope of external and
                    false indictate this stream has the scope of internal.
                    Deprecated, use origin
                  example: false
                isActive:
                  type: boolean
                  description: >-
                    true indicate that this stream has the status of active and
                    false indicate this stream has the scope of inactive
                  example: true
                isPublic:
                  type: boolean
                  description: >-
                    true indicate that this stream has a privacy setting of
                    public.  This only apply a ROOM stream type.
                  example: false
                type:
                  type: string
                  description: type of stream (IM, MIM, ROOM)
                  example: ROOM
                crossPod:
                  type: boolean
                  description: If true, this is a cross-pod stream.
                  example: false
                origin:
                  type: string
                  description: >-
                    INTERNAL if the creator of this stream belongs to the pod,
                    EXTERNAL otherwise
                  example: INTERNAL
                attributes:
                  $ref: '#/definitions/V2AdminStreamAttributes'
            V2AdminStreamAttributes:
              description: additional optional properties for the stream
              type: object
              properties:
                roomName:
                  type: string
                  description: room name (room only)
                  example: API room
                roomDescription:
                  type: string
                  description: description of the room (room only)
                  example: Room created via API
                members:
                  type: array
                  description: list of userid who is member of the stream - im or mim only
                  items:
                    type: integer
                    format: int64
                  example:
                    - 8933531975686
                    - 8933531975689
                createdByUserId:
                  type: integer
                  format: int64
                  description: creator user id
                  example: 8933531975689
                createdDate:
                  type: integer
                  format: int64
                  description: created date
                  example: 1481575056047
                lastModifiedDate:
                  type: integer
                  format: int64
                  description: last modified date
                  example: 1481575056047
                originCompany:
                  type: string
                  description: company name of the creator
                  example: Symphony
                originCompanyId:
                  type: integer
                  description: company id of the creator
                  example: 130
                membersCount:
                  type: integer
                  description: total number of members in the stream
                  example: 1
                lastMessageDate:
                  type: integer
                  format: int64
                  description: last date a message was sent in this stream
                  example: 1516699467959
                groupChat:
                  type: boolean
                  description: whether a stream is a group chat or not. Since SBE 20.16.
                  x-since: 20.16
                  example: false
            FileExtension:
              type: object
              required:
                - extension
              properties:
                extension:
                  type: string
                  description: >
                    The file extension that this specific record is for.  This
                    is a unique ID

                    that allows this record to be referenced in the URI.
                  example: .txt
                scope_internal:
                  type: boolean
                  description: |
                    File extension allowed for internal scope
                scope_external:
                  type: boolean
                  description: |
                    File extension allowed for external scope
                scope_xpod:
                  type: boolean
                  description: |
                    File extension allowed to be received from another POD
                  x-since: 24.2
                source:
                  type: string
                  description: >
                    File extension with metadata understood by the system or
                    file extension created by a customer
                  enum:
                    - SYSTEM
                    - CUSTOMER
            Pagination:
              type: object
              required:
                - cursors
              properties:
                cursors:
                  type: object
                  required:
                    - before
                  properties:
                    before:
                      type: string
                      description: >
                        This is the opaque url-safe string that points to the
                        start of the page of data

                        that has been returned.
                      example: MTAxNTExOTQ1MjAwNzI5NDE=
                    after:
                      type: string
                      description: >
                        This is the opaque url-safe string that points to the
                        end of the page of data

                        that has been returned.
                      example: NDMyNzQyODI3OTQw
                previous:
                  type: string
                  description: >
                    API endpoint that will return the previous page of data. If
                    not included, this is

                    the first page of data.
                  example: >-
                    https://tenantapi.d.isym.io/v1/tenantinfo?limit=25&before=MTAxNTExOTQ1MjAwNzI5NDE=
                next:
                  type: string
                  description: >
                    API endpoint that will return the next page of data. If not
                    included, this is the

                    last page of data. Due to how pagination works with
                    visibility and privacy, it is

                    possible that a page may be empty but contain a 'next'
                    paging link. Stop paging when

                    the 'next' link no longer appears.
                  example: >-
                    https://tenantapi.d.isym.io/v1/tenantinfo?limit=25&after=NDMyNzQyODI3OTQw
            FileExtensionsResponse:
              type: object
              required:
                - data
                - paging
              properties:
                data:
                  type: array
                  items:
                    $ref: '#/definitions/FileExtension'
            Protocol:
              type: object
              required:
                - scheme
              properties:
                scheme:
                  type: string
                  description: 'URI protocol scheme (example: http, https, ftp)'
                  example: skype
            AppAuthenticationKeys:
              description: App RSA keys information.
              type: object
              properties:
                current:
                  $ref: '#/definitions/AppAuthenticationKey'
                previous:
                  $ref: '#/definitions/AppAuthenticationKey'
            AppAuthenticationKey:
              description: App RSA key information.
              type: object
              properties:
                key:
                  description: Application RSA public key.
                  type: string
                  example: >-
                    --BEGIN PUBLIC KEY--\nMIICIANBgkqhw0BAQ...cCAwEAAQ==\n--END
                    PUBLIC KEY--
                expirationDate:
                  description: >-
                    RSA key expiration date. This value is set just for rotated
                    keys.
                  type: integer
                  format: int64
                  example: 1700815176000
                action:
                  description: >
                    Action to be performed on the RSA key.

                    The following actions can be performed onto the app's active
                    RSA key:
                      - SAVE
                      - REVOKE
                    The following actions can be performed onto the app's
                    rotated RSA key:
                      - REVOKE
                      - EXTEND
                  type: string
                  example: SAVE
            AppNotification:
              type: object
              description: Application callback information
              properties:
                url:
                  type: string
                  description: callback URL
                  example: https://some.url
                apiKey:
                  type: string
                  description: >-
                    apiKey sent into every callback request, using the X-API-KEY
                    header
                  example: test123456
            AppProperties:
              type: array
              description: >-
                Application configuration properties that are shared with the
                extension application, client side. Do not store sensitive
                information here. Since SBE 20.14.
              x-since: 20.14
              items:
                $ref: '#/definitions/AppProperty'
              example:
                - key: port
                  value: 4000
                - key: url
                  value: https://someother.url
            AppProperty:
              type: object
              description: >-
                Application configuration property that is shared with the
                extension application, client side. Do not store sensitive
                information here.
              properties:
                key:
                  type: string
                  description: >-
                    Name of an application configuration property. It cannot be
                    null or empty and its length is limited to 1024 characters.
                    Keys are unique.
                value:
                  type: string
                  description: >-
                    Value of an application configuration property. It cannot be
                    null and its length is limited to 4096 characters. It can be
                    empty.
              example:
                key: port
                value: 4000
            StreamAttachmentResponse:
              type: array
              items:
                $ref: '#/definitions/StreamAttachmentItem'
            StreamAttachmentItem:
              description: File attachments for a message in a stream
              type: object
              properties:
                messageId:
                  type: string
                  example: PYLHNm/1K6p...peOpj+FbQ
                ingestionDate:
                  type: integer
                  format: int64
                  example: 1548089933946
                userId:
                  type: integer
                  format: int64
                  example: 14568529068038
                fileId:
                  type: string
                  description: The attachment File ID.
                  example: internal_14362
                name:
                  type: string
                  description: The file name.
                  example: butterfly.jpg
                size:
                  type: integer
                  format: int64
                  description: Size in bytes.
                  example: 70186
                content-type:
                  type: string
                  example: image/jpeg
                previews:
                  type: array
                  items:
                    $ref: '#/definitions/AttachmentPreview'
            AttachmentPreview:
              description: Preview file for image attachments
              type: object
              properties:
                fileId:
                  type: string
                  description: The preview file ID
                  example: internal_14362
                width:
                  type: integer
                  description: The preview image width
                  example: 600
            UserGroupCreate:
              description: Body for group creation
              type: object
              properties:
                name:
                  description: Group name
                  type: string
                area:
                  description: Group area
                  type: string
                description:
                  description: Group description
                  type: string
                type:
                  description: Group type
                  type: string
              required:
                - name
                - type
            UserGroupResponse:
              description: Group object response
              type: object
              properties:
                id:
                  description: Group ID
                  type: string
                name:
                  description: Group name
                  type: string
                area:
                  description: An optional string attribute used for categorizing groups
                  type: string
                description:
                  description: Group description
                  type: string
                type:
                  description: Group type
                  type: string
                active:
                  description: Group status
                  type: boolean
                createdDate:
                  description: Date of group creation
                  type: integer
                  format: int64
                modifiedDate:
                  description: Date of group last update
                  type: integer
                  format: int64
                memberCount:
                  description: Number of group members
                  type: integer
                  format: int64
                assigneeCount:
                  description: Number of group assignees
                  type: integer
                  format: int64
            UserGroupResponseList:
              type: object
              properties:
                data:
                  type: array
                  items:
                    $ref: '#/definitions/UserGroupResponse'
                pagination:
                  type: object
                  $ref: '#/definitions/Pagination'
            UserGroupUpdate:
              description: Body for group update
              type: object
              properties:
                name:
                  description: Group name
                  type: string
                area:
                  description: Group area
                  type: string
                description:
                  description: Group description
                  type: string
                active:
                  description: Group status
                  type: boolean
            UserGroupMembershipResponseData:
              description: User object response
              type: object
              properties:
                id:
                  type: string
                groupId:
                  type: string
                group:
                  type: object
                  $ref: '#/definitions/GroupRoleScope'
                userId:
                  type: integer
                  format: int64
                user:
                  type: object
                  $ref: '#/definitions/UserCompp'
                active:
                  type: boolean
                lastAddedDate:
                  type: integer
                  format: int64
                lastRemovedDate:
                  type: integer
                  format: int64
            GroupRoleScope:
              description: User Group info to include in other models
              type: object
              properties:
                id:
                  type: string
                  description: Group ID
                name:
                  type: string
                  description: Group name
                area:
                  type: string
                  description: An optional string attribute used for categorizing groups
                type:
                  type: string
                  description: Group type
                active:
                  type: boolean
                  description: Group status
            UserCompp:
              description: Basic user information to include in other models
              type: object
              properties:
                id:
                  type: integer
                  format: int64
                  description: User ID
                  example: 7215545058329
                username:
                  type: string
                  description: Username
                  example: dpayet
                firstName:
                  type: string
                  description: User first name
                  example: Dimitri
                lastName:
                  type: string
                  description: User last name
                  example: Payet
                emailAddress:
                  type: string
                  description: User email addressIntegrationUserManagerTest
                  example: dpayet@om.fr
            UserGroupMembershipRequest:
              description: Body for user group membership creation
              type: object
              properties:
                active:
                  type: boolean
            UserGroupMembershipData:
              description: Body for user group membership response
              type: object
              properties:
                id:
                  type: string
                groupId:
                  type: string
                userId:
                  type: integer
                  format: int64
                group:
                  type: object
                  $ref: '#/definitions/UserGroupData'
                user:
                  type: object
                  $ref: '#/definitions/MembershipData'
                active:
                  type: boolean
                lastAddedDate:
                  type: integer
                  format: int64
                lastRemovedDate:
                  type: integer
                  format: int64
            MembershipData:
              description: User object response
              type: object
              properties:
                id:
                  type: integer
                  format: int64
                userName:
                  type: string
                firstName:
                  type: string
                lastName:
                  type: string
                emailAddress:
                  type: string
            UserGroupData:
              description: Group object response
              type: object
              properties:
                id:
                  description: Group Id
                  type: string
                name:
                  description: Group name
                  type: string
                area:
                  description: Group area
                  type: string
                type:
                  description: Group type
                  type: string
                active:
                  description: Group Status
                  type: boolean
            UserGroupMembershipResponse:
              type: object
              properties:
                data:
                  type: array
                  items:
                    $ref: '#/definitions/UserGroupMembershipResponseData'
                pagination:
                  type: object
                  $ref: '#/definitions/Pagination'
            UserGroupAssignee:
              description: User group assignee object
              type: object
              properties:
                id:
                  description: Assignee id
                  type: string
                groupId:
                  type: string
                group:
                  description: Group
                  type: object
                  $ref: '#/definitions/GroupRoleScope'
                userId:
                  type: integer
                  format: int64
                user:
                  type: object
                  $ref: '#/definitions/UserCompp'
                userRoles:
                  type: array
                  items:
                    type: string
                active:
                  type: boolean
                lastAddedDate:
                  description: Last added
                  type: integer
                  format: int64
                lastRemovedDate:
                  description: Last removed
                  type: integer
                  format: int64
            UserData:
              description: User object response
              type: object
              properties:
                id:
                  type: integer
                  format: int64
                username:
                  type: string
                firstName:
                  type: string
                lastName:
                  type: string
                emailAddress:
                  type: string
            UserGroupAssigneeResponse:
              description: response
              type: object
              properties:
                data:
                  type: array
                  items:
                    $ref: '#/definitions/UserGroupAssignee'
                pagination:
                  type: object
                  $ref: '#/definitions/Pagination'
            UserGroupAssigneeUpdate:
              description: Body for user group assignee update
              type: object
              properties:
                current:
                  description: Assignee status
                  type: boolean
              required:
                - current
            UserGroupMembershipUpdate:
              description: User Group membership update object
              type: object
              properties:
                active:
                  description: Group membership status
                  type: boolean
            UserGroupAssignmentResponse:
              description: User Group assignment response object
              type: object
              properties:
                id:
                  type: string
                  description: Assignment ID
                groupId:
                  type: string
                  description: Group ID
                group:
                  type: object
                  $ref: '#/definitions/GroupRoleScope'
                userId:
                  type: integer
                  format: int64
                  description: User ID
                user:
                  type: object
                  $ref: '#/definitions/UserCompp'
                userRoles:
                  type: array
                  items:
                    type: string
                active:
                  type: boolean
                  description: Group membership status
                lastAddedDate:
                  type: integer
                  format: int64
                  description: Date of group membership last added
                lastRemovedDate:
                  type: integer
                  format: int64
                  description: Date of group membership last removed
            DownloadReceiptCount:
              type: object
              properties:
                fileName:
                  type: string
                  example: Untitled Document.txt
                timestamp:
                  type: integer
                  format: int64
                  example: 1552999335740
            MessageReceiptDetail:
              description: Message receipt details response object
              type: object
              properties:
                user:
                  $ref: '#/definitions/UserCompp'
                deliveryReceiptTimestamp:
                  description: Timestamp of message delivery receipts
                  type: integer
                  format: int64
                  example: 1552999333784
                readReceiptTimestamp:
                  description: Timestamp of message read receipts
                  type: integer
                  format: int64
                  example: 1552999335114
                emailNotificationTimestamp:
                  description: Timestamp of message email notifications
                  type: integer
                  format: int64
                  example: 1552999335114
                downloadReceiptCounts:
                  type: array
                  items:
                    $ref: '#/definitions/DownloadReceiptCount'
                  example:
                    - fileName: Untitled Document.txt
                      timestamp: 1552999335740
            MessageReceiptDetailResponse:
              description: List of Message receipt details
              type: object
              properties:
                creator:
                  $ref: '#/definitions/MessageUser'
                onBehalfOfUser:
                  $ref: '#/definitions/MessageUser'
                stream:
                  $ref: '#/definitions/MessageStream'
                creationDate:
                  type: integer
                  format: int64
                  example: 1552999333141
                deliveryReceiptCount:
                  type: integer
                  example: 1
                readReceiptCount:
                  type: integer
                  example: 1
                emailNotificationCount:
                  type: integer
                  example: 1
                downloadReceiptCounts:
                  type: array
                  items:
                    $ref: '#/definitions/MessageDownloadReceiptCount'
                  example:
                    - fileName: internal_70781
                      count: 1
                MessageReceiptDetail:
                  type: array
                  items:
                    $ref: '#/definitions/MessageReceiptDetail'
                  example:
                    - user:
                        id: 7215545058329
                        username: dpayet
                        firstName: Dimitri
                        lastName: Payet
                        emailAddress: dpayet@om.fr
                      deliveryReceiptTimestamp: 1552999333784
                      readReceiptTimestamp: 1552999335114
                      emailNotificationTimestamp: 1552999335114
                      downloadReceiptCounts:
                        - fileName: Untitled Document.txt
                          timestamp: 1552999335740
                pagination:
                  $ref: '#/definitions/Pagination'
            MessageUser:
              type: object
              properties:
                id:
                  type: integer
                  format: int64
                  example: 7215545058329
                name:
                  type: string
                  example: User Test
            MessageStream:
              type: object
              properties:
                id:
                  type: string
                  example: lFpyw0ATFmji+Cc/cSzbk3///pZkWpe1dA==
                name:
                  type: string
                  example: Test Room
                streamType:
                  type: string
                  example: ROOM
            MessageDownloadReceiptCount:
              type: object
              properties:
                fileName:
                  type: string
                  example: internal_707810
                count:
                  type: integer
                  format: int64
                  example: 1
            MessageDetail:
              description: Message detail
              type: object
              properties:
                messageId:
                  description: message id
                  type: string
                creator:
                  $ref: '#/definitions/MessageUser'
                onBehalfOfUser:
                  $ref: '#/definitions/MessageUser'
                stream:
                  $ref: '#/definitions/MessageStream'
                creationDate:
                  type: integer
                  format: int64
                deliveryReceiptCount:
                  type: integer
                  format: int64
                readReceiptCount:
                  type: integer
                  format: int64
                emailNotificationCount:
                  type: integer
                  format: int64
                downloadReceiptCounts:
                  type: array
                  items:
                    $ref: '#/definitions/MessageDownloadReceiptCount'
            MessageDetails:
              description: Message details
              type: array
              items:
                $ref: '#/definitions/MessageDetail'
            MessageIds:
              type: object
              properties:
                messageIds:
                  $ref: '#/definitions/StringList'
            AssigneeCandidate:
              description: Assignee Candidate
              type: object
              properties:
                userId:
                  type: integer
                  format: int64
                username:
                  type: string
                firstName:
                  type: string
                surname:
                  type: string
                emailAddress:
                  type: string
                canBeAssigned:
                  type: boolean
                roles:
                  $ref: '#/definitions/StringList'
            AssigneeCandidates:
              description: List of assignee candidate
              type: object
              properties:
                users:
                  type: array
                  items:
                    $ref: '#/definitions/AssigneeCandidate'
                pagination:
                  type: object
                  $ref: '#/definitions/Pagination'
            Languages:
              description: List of languages
              type: object
              properties:
                languages:
                  $ref: '#/definitions/StringList'
            MessageMetadataResponse:
              description: Message metadata
              type: object
              properties:
                messageId:
                  type: string
                parent:
                  type: object
                  properties:
                    messageId:
                      type: string
                      description: Id of the parent message queried
                    relationshipType:
                      type: string
                      enum:
                        - REPLY_FORM
                        - REPLY
                        - FORWARD
                replies:
                  type: array
                  items:
                    type: string
                forwards:
                  type: array
                  items:
                    type: string
                formReplies:
                  type: array
                  items:
                    type: string
            UserSuspension:
              type: object
              properties:
                suspended:
                  type: boolean
                  example: true
                suspendedUntil:
                  type: integer
                  format: int64
                  example: 1601546400
                suspensionReason:
                  type: string
                  example: The user will be OOO due to a mandatory leave
            FollowersList:
              type: object
              properties:
                followers:
                  $ref: '#/definitions/UserIdList'
            FollowersListResponse:
              type: object
              properties:
                count:
                  type: integer
                  format: int64
                  example: 2
                followers:
                  type: array
                  items:
                    type: integer
                    format: int64
                  example:
                    - 13056700579848
                    - 13056700580889
                pagination:
                  $ref: '#/definitions/Pagination'
            FollowingListResponse:
              type: object
              properties:
                count:
                  type: integer
                  format: int64
                  example: 2
                following:
                  type: array
                  items:
                    type: integer
                    format: int64
                  example:
                    - 13056700579848
                    - 13056700580889
                pagination:
                  $ref: '#/definitions/Pagination'
            V1IMAttributes:
              type: object
              properties:
                pinnedMessageId:
                  type: string
                  description: >-
                    UrlSafe message id of the pinned message inside the IM. To
                    perform unpin operation, send an empty string.
                  example: vd7qwNb6hLoUV0BfXXPC43___oPIvkwJbQ
            V1IMDetail:
              type: object
              properties:
                V1IMAttributes:
                  $ref: '#/definitions/V1IMAttributes'
                IMSystemInfo:
                  $ref: '#/definitions/IMSystemInfo'
            IMSystemInfo:
              type: object
              properties:
                id:
                  type: string
                  example: usnBKBkH_BVrGOiVpaupEH___okFfE7QdA
                creationDate:
                  type: integer
                  format: int64
                  description: >-
                    The datetime when the stream was originally created.
                    Milliseconds since Jan 1 1970.
                  example: 1610520703317
                active:
                  type: boolean
                  description: >-
                    If false, no messages can be sent in this stream, and
                    membership is locked.
                  example: true
            ServiceAccountManifest:
              type: object
              properties:
                manifest:
                  type: string
                  maxLength: 6144
                  description: >-
                    Manifest containing commands supported by the service
                    account. Must be valid JSON.
              required:
                - nu
    aid: symphony:symphony-pod-api
    overlays:
      - type: APIs.io Search
        url: overlays/pod-openapi-search.yml
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---