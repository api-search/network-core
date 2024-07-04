---
name: Contacts
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/contacts.png
url: https://example.com/apis/contacts.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Contacts
apis:
  - name: account
    description: <p>Operations for Amazon Web Services Account Management</p>
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
            title: account
          paths:
            /deleteAlternateContact:
              POST:
                summary: DeleteAlternateContact
                description: >-
                  <p>Deletes the specified alternate contact from an Amazon Web
                  Services account.</p> <p>For complete details about how to use
                  the alternate contact operations, see <a
                  href="https://docs.aws.amazon.com/accounts/latest/reference/manage-acct-update-contact.html">Access
                  or updating the alternate contacts</a>.</p> <note> <p>Before
                  you can update the alternate contact information for an Amazon
                  Web Services account that is managed by Organizations, you
                  must first enable integration between Amazon Web Services
                  Account Management and Organizations. For more information,
                  see <a
                  href="https://docs.aws.amazon.com/accounts/latest/reference/using-orgs-trusted-access.html">Enabling
                  trusted access for Amazon Web Services Account
                  Management</a>.</p> </note>
                tags:
                  - Delete
                  - Alternate
                  - Contacts
                  - Alternate
                  - Contacts
            /disableRegion:
              POST:
                summary: DisableRegion
                description: <p>Disables (opts-out) a particular Region for an account.</p>
                tags:
                  - Disable
                  - Regions
                  - Alternate
                  - Contacts
                  - Regions
            /enableRegion:
              POST:
                summary: EnableRegion
                description: <p>Enables (opts-in) a particular Region for an account.</p>
                tags:
                  - Enable
                  - Regions
                  - Alternate
                  - Contacts
                  - Regions
            /getAlternateContact:
              POST:
                summary: GetAlternateContact
                description: >-
                  <p>Retrieves the specified alternate contact attached to an
                  Amazon Web Services account.</p> <p>For complete details about
                  how to use the alternate contact operations, see <a
                  href="https://docs.aws.amazon.com/accounts/latest/reference/manage-acct-update-contact.html">Access
                  or updating the alternate contacts</a>.</p> <note> <p>Before
                  you can update the alternate contact information for an Amazon
                  Web Services account that is managed by Organizations, you
                  must first enable integration between Amazon Web Services
                  Account Management and Organizations. For more information,
                  see <a
                  href="https://docs.aws.amazon.com/accounts/latest/reference/using-orgs-trusted-access.html">Enabling
                  trusted access for Amazon Web Services Account
                  Management</a>.</p> </note>
                tags:
                  - Get
                  - Alternate
                  - Contacts
                  - Alternate
                  - Contacts
                  - Regions
            /getContactInformation:
              POST:
                summary: GetContactInformation
                description: >-
                  <p>Retrieves the primary contact information of an Amazon Web
                  Services account.</p> <p>For complete details about how to use
                  the primary contact operations, see <a
                  href="https://docs.aws.amazon.com/accounts/latest/reference/manage-acct-update-contact.html">Update
                  the primary and alternate contact information</a>.</p>
                tags:
                  - Get
                  - Contacts
                  - Information
                  - Alternate
                  - Contacts
                  - Regions
                  - Information
            /getRegionOptStatus:
              POST:
                summary: GetRegionOptStatus
                description: <p>Retrieves the opt-in status of a particular Region.</p>
                tags:
                  - Get
                  - Regions
                  - Opt
                  - Status
                  - Alternate
                  - Contacts
                  - Regions
                  - Information
                  - Opt
                  - Status
            /listRegions:
              POST:
                summary: ListRegions
                description: >-
                  <p>Lists all the Regions for a given account and their
                  respective opt-in statuses. Optionally, this list can be
                  filtered by the <code>region-opt-status-contains</code>
                  parameter. </p>
                tags:
                  - Lists
                  - Regions
                  - Alternate
                  - Contacts
                  - Regions
                  - Information
                  - Opt
                  - Status
                  - Regions
            /putAlternateContact:
              POST:
                summary: PutAlternateContact
                description: >-
                  <p>Modifies the specified alternate contact attached to an
                  Amazon Web Services account.</p> <p>For complete details about
                  how to use the alternate contact operations, see <a
                  href="https://docs.aws.amazon.com/accounts/latest/reference/manage-acct-update-contact.html">Access
                  or updating the alternate contacts</a>.</p> <note> <p>Before
                  you can update the alternate contact information for an Amazon
                  Web Services account that is managed by Organizations, you
                  must first enable integration between Amazon Web Services
                  Account Management and Organizations. For more information,
                  see <a
                  href="https://docs.aws.amazon.com/accounts/latest/reference/using-orgs-trusted-access.html">Enabling
                  trusted access for Amazon Web Services Account
                  Management</a>.</p> </note>
                tags:
                  - Put
                  - Alternate
                  - Contacts
                  - Alternate
                  - Contacts
                  - Regions
                  - Information
                  - Opt
                  - Status
                  - Regions
            /putContactInformation:
              POST:
                summary: PutContactInformation
                description: >-
                  <p>Updates the primary contact information of an Amazon Web
                  Services account.</p> <p>For complete details about how to use
                  the primary contact operations, see <a
                  href="https://docs.aws.amazon.com/accounts/latest/reference/manage-acct-update-contact.html">Update
                  the primary and alternate contact informatio
                tags:
                  - Put
                  - Contacts
                  - Information
                  - Alternate
                  - Contacts
                  - Regions
                  - Information
                  - Opt
                  - Status
                  - Regions
    overlays:
      - type: APIs.io Search
        url: overlays/account-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/account-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:account
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
                  - null
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
                  - null
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
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
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
                  - null
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - null
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
                  - null
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
                  - null
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
  - name: connect-contact-lens
    description: >-
      <p>Contact Lens for Amazon Connect enables you to analyze conversations
      between customer and agents, by using speech transcription, natural
      language processing, and intelligent search capabilities. It performs
      sentiment analysis, detects issues, and enables you to automatically
      categorize contacts.</p> <p>Contact Lens for Amazon Connect provides both
      real-time and post-call analytics of customer-agent conversations. For
      more information, see <a
      href="https://docs.aws.amazon.com/connect/latest/adminguide/analyze-conversations.html">Analyze
      conversations using Contact Lens</a> in the <i>Amazon Connect
      Administrator Guide</i>. </p>
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
            title: connect-contact-lens
          paths:
            /realtime-contact-analysis/analysis-segments:
              POST:
                summary: ListRealtimeContactAnalysisSegments
                description: >-
                  <p>Provides a list of analysis segments for a real-time
                  analysis se
                tags:
                  - Lists
                  - Real Time
                  - Contacts
                  - Analysis
                  - Segments
                  - Real Time
                  - Contacts
                  - Analysis
                  - Segments
    overlays:
      - type: APIs.io Search
        url: overlays/connect-contact-lens-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/connect-contact-lens-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:connect-contact-lens
  - name: connectcases
    description: >-
      <p>With Amazon Connect Cases, your agents can track and manage customer
      issues that require multiple interactions, follow-up tasks, and teams in
      your contact center. A case represents a customer issue. It records the
      issue, the steps and interactions taken to resolve the issue, and the
      outcome. For more information, see <a
      href="https://docs.aws.amazon.com/connect/latest/adminguide/cases.html">Amazon
      Connect Cases</a> in the <i>Amazon Connect Administrator Guide</i>.</p>
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
            title: connectcases
          paths:
            /domains/{domainId}/fields-batch:
              POST:
                summary: BatchGetField
                description: >-
                  <p>Returns the description for the list of fields in the
                  request parameters. </p>
                tags:
                  - Batches
                  - Get
                  - Fields
                  - Identifiers
                  - Fields
                  - Batches
            /domains/{domainId}/fields/{fieldId}/options:
              PUT:
                summary: BatchPutFieldOptions
                description: >-
                  <p>Creates and updates a set of field options for a single
                  select field in a Cases domain.</p>
                tags:
                  - Batches
                  - Put
                  - Fields
                  - Options
                  - Identifiers
                  - Fields
                  - Batches
                  - Fields
                  - Options
            /domains/{domainId}/cases:
              POST:
                summary: CreateCase
                description: >-
                  <note> <p>If you provide a value for
                  <code>PerformedBy.UserArn</code> you must also have <a
                  href="https://docs.aws.amazon.com/connect/latest/APIReference/API_DescribeUser.html">connect:DescribeUser</a>
                  permission on the User ARN resource that you provide</p>
                  </note> <pre><code> &lt;p&gt;Creates a case in the specified
                  Cases domain. Case system and custom fields are taken as an
                  array id/value pairs with a declared data types.&lt;/p&gt;
                  &lt;p&gt;The following fields are required when creating a
                  case:&lt;/p&gt; &lt;ul&gt; &lt;li&gt; &lt;p&gt;
                  &lt;code&gt;customer_id&lt;/code&gt; - You must provide the
                  full customer profile ARN in this format:
                  &lt;code&gt;arn:aws:profile:your_AWS_Region:your_AWS_account
                  ID:domains/your_profiles_domain_name/profiles/profile_ID&lt;/code&gt;
                  &lt;/p&gt; &lt;/li&gt; &lt;li&gt; &lt;p&gt;
                  &lt;code&gt;title&lt;/code&gt; &lt;/p&gt; &lt;/li&gt;
                  &lt;/ul&gt; </code></pre>
                tags:
                  - Create
                  - Case
                  - Identifiers
                  - Fields
                  - Batches
                  - Fields
                  - Options
                  - Cases
            /domains:
              POST:
                summary: CreateDomain
                description: >-
                  <p>Creates a domain, which is a container for all case data,
                  such as cases, fields, templates and layouts. Each Amazon
                  Connect instance can be associated with only one Cases
                  domain.</p> <important> <p>This will not associate your
                  connect instance to Cases domain. Instead, use the Amazon
                  Connect <a
                  href="https://docs.aws.amazon.com/connect/latest/APIReference/API_CreateIntegrationAssociation.html">CreateIntegrationAssociation</a>
                  API. You need specific IAM permissions to successfully
                  associate the Cases domain. For more information, see <a
                  href="https://docs.aws.amazon.com/connect/latest/adminguide/required-permissions-iam-cases.html#onboard-cases-iam">Onboard
                  to Cases</a>.</p> <pre><code> &lt;/important&gt; </code></pre>
                tags:
                  - Create
                  - Domains
                  - Identifiers
                  - Fields
                  - Batches
                  - Fields
                  - Options
                  - Cases
                  - Domains
            /domains/{domainId}/fields:
              POST:
                summary: CreateField
                description: >-
                  <p>Creates a field in the Cases domain. This field is used to
                  define the case object model (that is, defines what data can
                  be captured on cases) in a Cases domain. </p>
                tags:
                  - Create
                  - Fields
                  - Identifiers
                  - Fields
                  - Batches
                  - Fields
                  - Options
                  - Cases
                  - Domains
            /domains/{domainId}/layouts:
              POST:
                summary: CreateLayout
                description: >-
                  <p>Creates a layout in the Cases domain. Layouts define the
                  following configuration in the top section and More Info tab
                  of the Cases user interface:</p> <ul> <li> <p>Fields to
                  display to the users</p> </li> <li> <p>Field ordering</p>
                  </li> </ul> <note> <p>Title and Status fields cannot be part
                  of layouts since they are not configurable.</p> </note>
                tags:
                  - Create
                  - Layouts
                  - Identifiers
                  - Fields
                  - Batches
                  - Fields
                  - Options
                  - Cases
                  - Domains
                  - Layouts
            /domains/{domainId}/cases/{caseId}/related-items/:
              POST:
                summary: CreateRelatedItem
                description: >-
                  <p>Creates a related item (comments, tasks, and contacts) and
                  associates it with a case.</p> <note> <ul> <li> <p>A Related
                  Item is a resource that is associated with a case. It may or
                  may not have an external identifier linking it to an external
                  resource (for example, a <code>contactArn</code>). All Related
                  Items have their own internal identifier, the
                  <code>relatedItemArn</code>. Examples of related items include
                  <code>comments</code> and <code>contacts</code>.</p> </li>
                  <li> <p>If you provide a value for
                  <code>performedBy.userArn</code> you must also have <a
                  href="https://docs.aws.amazon.com/connect/latest/APIReference/API_DescribeUser.html">DescribeUser</a>
                  permission on the ARN of the user that you provide.</p> </li>
                  </ul> <pre><code> &lt;/note&gt; </code></pre>
                tags:
                  - Create
                  - Related
                  - Items
                  - Identifiers
                  - Fields
                  - Batches
                  - Fields
                  - Options
                  - Cases
                  - Domains
                  - Layouts
                  - Case
                  - Related
                  - Items
            /domains/{domainId}/templates:
              POST:
                summary: CreateTemplate
                description: >-
                  <p>Creates a template in the Cases domain. This template is
                  used to define the case object model (that is, to define what
                  data can be captured on cases) in a Cases domain. A template
                  must have a unique name within a domain, and it must reference
                  existing field IDs and layout IDs. Additionally, multiple
                  fields with same IDs are not allowed within the same Template.
                  A template can be either Active or Inactive, as indicated by
                  its status. Inactive templates cannot be used to create
                  cases.</p>
                tags:
                  - Create
                  - Templates
                  - Identifiers
                  - Fields
                  - Batches
                  - Fields
                  - Options
                  - Cases
                  - Domains
                  - Layouts
                  - Case
                  - Related
                  - Items
                  - Templates
            /domains/{domainId}:
              POST:
                summary: GetDomain
                description: >-
                  <p>Returns information about a specific domain if it exists.
                  </p>
                tags:
                  - Get
                  - Domains
                  - Identifiers
                  - Fields
                  - Batches
                  - Fields
                  - Options
                  - Cases
                  - Domains
                  - Layouts
                  - Case
                  - Related
                  - Items
                  - Templates
            /domains/{domainId}/cases/{caseId}:
              PUT:
                summary: UpdateCase
                description: >-
                  <note> <p>If you provide a value for
                  <code>PerformedBy.UserArn</code> you must also have <a
                  href="https://docs.aws.amazon.com/connect/latest/APIReference/API_DescribeUser.html">connect:DescribeUser</a>
                  permission on the User ARN resource that you provide</p>
                  </note> <pre><code> &lt;p&gt;Updates the values of fields on a
                  case. Fields to be updated are received as an array of
                  id/value pairs identical to the
                  &lt;code&gt;CreateCase&lt;/code&gt; input .&lt;/p&gt;
                  &lt;p&gt;If the action is successful, the service sends back
                  an HTTP 200 response with an empty HTTP body.&lt;/p&gt;
                  </code></pre>
                tags:
                  - Update
                  - Case
                  - Identifiers
                  - Fields
                  - Batches
                  - Fields
                  - Options
                  - Cases
                  - Domains
                  - Layouts
                  - Case
                  - Related
                  - Items
                  - Templates
            /domains/{domainId}/cases/{caseId}/audit-history:
              POST:
                summary: GetCaseAuditEvents
                description: >-
                  <p>Returns the audit history about a specific case if it
                  exists.</p>
                tags:
                  - Get
                  - Case
                  - Audit
                  - Events
                  - Identifiers
                  - Fields
                  - Batches
                  - Fields
                  - Options
                  - Cases
                  - Domains
                  - Layouts
                  - Case
                  - Related
                  - Items
                  - Templates
                  - Audit
                  - History
            /domains/{domainId}/case-event-configuration:
              PUT:
                summary: PutCaseEventConfiguration
                description: >-
                  <p>Adds case event publishing configuration. For a complete
                  list of fields you can add to the event message, see <a
                  href="https://docs.aws.amazon.com/connect/latest/adminguide/case-fields.html">Create
                  case fields</a> in the <i>Amazon Connect Administrator
                  Guide</i> </p>
                tags:
                  - Put
                  - Case
                  - Events
                  - Configurations
                  - Identifiers
                  - Fields
                  - Batches
                  - Fields
                  - Options
                  - Cases
                  - Domains
                  - Layouts
                  - Case
                  - Related
                  - Items
                  - Templates
                  - Audit
                  - History
                  - Events
                  - Configurations
            /domains/{domainId}/layouts/{layoutId}:
              PUT:
                summary: UpdateLayout
                description: >-
                  <p>Updates the attributes of an existing layout.</p> <p>If the
                  action is successful, the service sends back an HTTP 200
                  response with an empty HTTP body.</p> <p>A
                  <code>ValidationException</code> is returned when you add
                  non-existent <code>fieldIds</code> to a layout.</p> <note>
                  <p>Title and Status fields cannot be part of layouts because
                  they are not configurable.</p> </note>
                tags:
                  - Update
                  - Layouts
                  - Identifiers
                  - Fields
                  - Batches
                  - Fields
                  - Options
                  - Cases
                  - Domains
                  - Layouts
                  - Case
                  - Related
                  - Items
                  - Templates
                  - Audit
                  - History
                  - Events
                  - Configurations
                  - Layouts
            /domains/{domainId}/templates/{templateId}:
              PUT:
                summary: UpdateTemplate
                description: >-
                  <p>Updates the attributes of an existing template. The
                  template attributes that can be modified include
                  <code>name</code>, <code>description</code>,
                  <code>layoutConfiguration</code>, <code>requiredFields</code>,
                  and <code>status</code>. At least one of these attributes must
                  not be null. If a null value is provided for a given
                  attribute, that attribute is ignored and its current value is
                  preserved.</p>
                tags:
                  - Update
                  - Templates
                  - Identifiers
                  - Fields
                  - Batches
                  - Fields
                  - Options
                  - Cases
                  - Domains
                  - Layouts
                  - Case
                  - Related
                  - Items
                  - Templates
                  - Audit
                  - History
                  - Events
                  - Configurations
                  - Layouts
                  - Templates
            /domains/{domainId}/list-cases-for-contact:
              POST:
                summary: ListCasesForContact
                description: <p>Lists cases for a given contact.</p>
                tags:
                  - Lists
                  - Cases
                  - For
                  - Contacts
                  - Identifiers
                  - Fields
                  - Batches
                  - Fields
                  - Options
                  - Cases
                  - Domains
                  - Layouts
                  - Case
                  - Related
                  - Items
                  - Templates
                  - Audit
                  - History
                  - Events
                  - Configurations
                  - Layouts
                  - Templates
                  - Lists
                  - For
                  - Contacts
            /domains-list:
              POST:
                summary: ListDomains
                description: >-
                  <p>Lists all cases domains in the Amazon Web Services account.
                  Each list item is a condensed summary object of the
                  domain.</p>
                tags:
                  - Lists
                  - Domains
                  - Identifiers
                  - Fields
                  - Batches
                  - Fields
                  - Options
                  - Cases
                  - Domains
                  - Layouts
                  - Case
                  - Related
                  - Items
                  - Templates
                  - Audit
                  - History
                  - Events
                  - Configurations
                  - Layouts
                  - Templates
                  - Lists
                  - For
                  - Contacts
            /domains/{domainId}/fields/{fieldId}/options-list:
              POST:
                summary: ListFieldOptions
                description: >-
                  <p>Lists all of the field options for a field identifier in
                  the domain. </p>
                tags:
                  - Lists
                  - Fields
                  - Options
                  - Identifiers
                  - Fields
                  - Batches
                  - Fields
                  - Options
                  - Cases
                  - Domains
                  - Layouts
                  - Case
                  - Related
                  - Items
                  - Templates
                  - Audit
                  - History
                  - Events
                  - Configurations
                  - Layouts
                  - Templates
                  - Lists
                  - For
                  - Contacts
            /domains/{domainId}/fields-list:
              POST:
                summary: ListFields
                description: <p>Lists all fields in a Cases domain.</p>
                tags:
                  - Lists
                  - Fields
                  - Identifiers
                  - Fields
                  - Batches
                  - Fields
                  - Options
                  - Cases
                  - Domains
                  - Layouts
                  - Case
                  - Related
                  - Items
                  - Templates
                  - Audit
                  - History
                  - Events
                  - Configurations
                  - Layouts
                  - Templates
                  - Lists
                  - For
                  - Contacts
            /domains/{domainId}/layouts-list:
              POST:
                summary: ListLayouts
                description: >-
                  <p>Lists all layouts in the given cases domain. Each list item
                  is a condensed summary object of the layout.</p>
                tags:
                  - Lists
                  - Layouts
                  - Identifiers
                  - Fields
                  - Batches
                  - Fields
                  - Options
                  - Cases
                  - Domains
                  - Layouts
                  - Case
                  - Related
                  - Items
                  - Templates
                  - Audit
                  - History
                  - Events
                  - Configurations
                  - Layouts
                  - Templates
                  - Lists
                  - For
                  - Contacts
            /tags/{arn}:
              DELETE:
                summary: UntagResource
                description: <p>Untags a resource.</p>
                tags:
                  - Untag
                  - Resources
                  - Identifiers
                  - Fields
                  - Batches
                  - Fields
                  - Options
                  - Cases
                  - Domains
                  - Layouts
                  - Case
                  - Related
                  - Items
                  - Templates
                  - Audit
                  - History
                  - Events
                  - Configurations
                  - Layouts
                  - Templates
                  - Lists
                  - For
                  - Contacts
                  - Tags
                  - ARN
            /domains/{domainId}/templates-list:
              POST:
                summary: ListTemplates
                description: >-
                  <p>Lists all of the templates in a Cases domain. Each list
                  item is a condensed summary object of the template. </p>
                tags:
                  - Lists
                  - Templates
                  - Identifiers
                  - Fields
                  - Batches
                  - Fields
                  - Options
                  - Cases
                  - Domains
                  - Layouts
                  - Case
                  - Related
                  - Items
                  - Templates
                  - Audit
                  - History
                  - Events
                  - Configurations
                  - Layouts
                  - Templates
                  - Lists
                  - For
                  - Contacts
                  - Tags
                  - ARN
            /domains/{domainId}/cases-search:
              POST:
                summary: SearchCases
                description: >-
                  <p>Searches for cases within their associated Cases domain.
                  Search results are returned as a paginated list of abridged
                  case documents.</p> <note> <p>For <code>customer_id</code> you
                  must provide the full customer profile ARN in this format:
                  <code> arn:aws:profile:your AWS Region:your AWS account
                  ID:domains/profiles domain name/profiles/profile ID</code>.
                  </p> </note>
                tags:
                  - Search
                  - Cases
                  - Identifiers
                  - Fields
                  - Batches
                  - Fields
                  - Options
                  - Cases
                  - Domains
                  - Layouts
                  - Case
                  - Related
                  - Items
                  - Templates
                  - Audit
                  - History
                  - Events
                  - Configurations
                  - Layouts
                  - Templates
                  - Lists
                  - For
                  - Contacts
                  - Tags
                  - ARN
                  - Search
            /domains/{domainId}/cases/{caseId}/related-items-search:
              POST:
                summary: SearchRelatedItems
                description: >-
                  <p>Searches for related items that are associated with a
                  case.</p> <note> <p>If no filters are provided, this returns
                  all related items associated with a case.</p> </note>
                tags:
                  - Search
                  - Related
                  - Items
                  - Identifiers
                  - Fields
                  - Batches
                  - Fields
                  - Options
                  - Cases
                  - Domains
                  - Layouts
                  - Case
                  - Related
                  - Items
                  - Templates
                  - Audit
                  - History
                  - Events
                  - Configurations
                  - Layouts
                  - Templates
                  - Lists
                  - For
                  - Contacts
                  - Tags
                  - ARN
                  - Search
            /domains/{domainId}/fields/{fieldId}:
              PUT:
                summary: UpdateField
                description: <p>Updates the properties of an existing
                tags:
                  - Update
                  - Fields
                  - Identifiers
                  - Fields
                  - Batches
                  - Fields
                  - Options
                  - Cases
                  - Domains
                  - Layouts
                  - Case
                  - Related
                  - Items
                  - Templates
                  - Audit
                  - History
                  - Events
                  - Configurations
                  - Layouts
                  - Templates
                  - Lists
                  - For
                  - Contacts
                  - Tags
                  - ARN
                  - Search
    overlays:
      - type: APIs.io Search
        url: overlays/connectcases-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/connectcases-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:connectcases
  - name: groundstation
    description: >-
      <p>Welcome to the AWS Ground Station API Reference. AWS Ground Station is
      a fully managed service that enables you to control satellite
      communications, downlink and process satellite data, and scale your
      satellite operations efficiently and cost-effectively without having to
      build or manage your own ground station infrastructure.</p>
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
            title: groundstation
          paths:
            /contact/{contactId}:
              GET:
                summary: DescribeContact
                description: <p>Describes an existing contact.</p>
                tags:
                  - Describe
                  - Contacts
                  - Identifiers
            /config:
              GET:
                summary: ListConfigs
                description: <p>Returns a list of <code>Config</code> objects.</p>
                tags:
                  - Lists
                  - Configurations
                  - Identifiers
                  - Configurations
            /dataflowEndpointGroup:
              GET:
                summary: ListDataflowEndpointGroups
                description: <p>Returns a list of <code>DataflowEndpoint</code> groups.</p>
                tags:
                  - Lists
                  - Dataflow
                  - Endpoints
                  - Groups
                  - Identifiers
                  - Configurations
                  - Endpoints
                  - Group
            /ephemeris:
              POST:
                summary: CreateEphemeris
                description: >-
                  <p>Creates an Ephemeris with the specified
                  <code>EphemerisData</code>.</p>
                tags:
                  - Create
                  - Ephemeris
                  - Identifiers
                  - Configurations
                  - Endpoints
                  - Group
                  - Ephemeris
            /missionprofile:
              GET:
                summary: ListMissionProfiles
                description: <p>Returns a list of mission profiles.</p>
                tags:
                  - Lists
                  - Mission
                  - Profiles
                  - Identifiers
                  - Configurations
                  - Endpoints
                  - Group
                  - Ephemeris
                  - Mission Profile
            /config/{configType}/{configId}:
              PUT:
                summary: UpdateConfig
                description: >-
                  <p>Updates the <code>Config</code> used when scheduling
                  contacts.</p> <p>Updating a <code>Config</code> will not
                  update the execution parameters for existing future contacts
                  scheduled with this <code>Config</code>.</p>
                tags:
                  - Update
                  - Configurations
                  - Identifiers
                  - Configurations
                  - Endpoints
                  - Group
                  - Ephemeris
                  - Mission Profile
                  - Types
            /dataflowEndpointGroup/{dataflowEndpointGroupId}:
              GET:
                summary: GetDataflowEndpointGroup
                description: <p>Returns the dataflow endpoint group.</p>
                tags:
                  - Get
                  - Dataflow
                  - Endpoints
                  - Group
                  - Identifiers
                  - Configurations
                  - Endpoints
                  - Group
                  - Ephemeris
                  - Mission Profile
                  - Types
                  - Dataflow
            /ephemeris/{ephemerisId}:
              PUT:
                summary: UpdateEphemeris
                description: <p>Updates an existing ephemeris</p>
                tags:
                  - Update
                  - Ephemeris
                  - Identifiers
                  - Configurations
                  - Endpoints
                  - Group
                  - Ephemeris
                  - Mission Profile
                  - Types
                  - Dataflow
            /missionprofile/{missionProfileId}:
              PUT:
                summary: UpdateMissionProfile
                description: >-
                  <p>Updates a mission profile.</p> <p>Updating a mission
                  profile will not update the execution parameters for existing
                  future contacts.</p>
                tags:
                  - Update
                  - Mission
                  - Profiles
                  - Identifiers
                  - Configurations
                  - Endpoints
                  - Group
                  - Ephemeris
                  - Mission Profile
                  - Types
                  - Dataflow
                  - Profiles
            /agent/{agentId}/configuration:
              GET:
                summary: GetAgentConfiguration
                description: >-
                  <note> <p> For use by AWS Ground Station Agent and shouldn't
                  be called directly.</p> </note> <p>Gets the latest
                  configuration information for a registered agent.</p>
                tags:
                  - Get
                  - Agent
                  - Configurations
                  - Identifiers
                  - Configurations
                  - Endpoints
                  - Group
                  - Ephemeris
                  - Mission Profile
                  - Types
                  - Dataflow
                  - Profiles
                  - Configurations
            /minute-usage:
              POST:
                summary: GetMinuteUsage
                description: <p>Returns the number of reserved minutes used by account.</p>
                tags:
                  - Get
                  - Minute
                  - Usage
                  - Identifiers
                  - Configurations
                  - Endpoints
                  - Group
                  - Ephemeris
                  - Mission Profile
                  - Types
                  - Dataflow
                  - Profiles
                  - Configurations
                  - Minute
                  - Usage
            /satellite/{satelliteId}:
              GET:
                summary: GetSatellite
                description: <p>Returns a satellite.</p>
                tags:
                  - Get
                  - Satellites
                  - Identifiers
                  - Configurations
                  - Endpoints
                  - Group
                  - Ephemeris
                  - Mission Profile
                  - Types
                  - Dataflow
                  - Profiles
                  - Configurations
                  - Minute
                  - Usage
            /contacts:
              POST:
                summary: ListContacts
                description: >-
                  <p>Returns a list of contacts.</p> <p>If
                  <code>statusList</code> contains AVAILABLE, the request must
                  include <code>groundStation</code>,
                  <code>missionprofileArn</code>, and <code>satelliteArn</code>.
                  </p>
                tags:
                  - Lists
                  - Contacts
                  - Identifiers
                  - Configurations
                  - Endpoints
                  - Group
                  - Ephemeris
                  - Mission Profile
                  - Types
                  - Dataflow
                  - Profiles
                  - Configurations
                  - Minute
                  - Usage
                  - Contacts
            /ephemerides:
              POST:
                summary: ListEphemerides
                description: <p>List existing ephemerides.</p>
                tags:
                  - Lists
                  - Ephemerides
                  - Identifiers
                  - Configurations
                  - Endpoints
                  - Group
                  - Ephemeris
                  - Mission Profile
                  - Types
                  - Dataflow
                  - Profiles
                  - Configurations
                  - Minute
                  - Usage
                  - Contacts
                  - Ephemerides
            /groundstation:
              GET:
                summary: ListGroundStations
                description: <p>Returns a list of ground stations. </p>
                tags:
                  - Lists
                  - Ground
                  - Stations
                  - Identifiers
                  - Configurations
                  - Endpoints
                  - Group
                  - Ephemeris
                  - Mission Profile
                  - Types
                  - Dataflow
                  - Profiles
                  - Configurations
                  - Minute
                  - Usage
                  - Contacts
                  - Ephemerides
                  - Groundstation
            /satellite:
              GET:
                summary: ListSatellites
                description: <p>Returns a list of satellites.</p>
                tags:
                  - Lists
                  - Satellites
                  - Identifiers
                  - Configurations
                  - Endpoints
                  - Group
                  - Ephemeris
                  - Mission Profile
                  - Types
                  - Dataflow
                  - Profiles
                  - Configurations
                  - Minute
                  - Usage
                  - Contacts
                  - Ephemerides
                  - Groundstation
                  - Satellites
            /tags/{resourceArn}:
              DELETE:
                summary: UntagResource
                description: <p>Deassigns a resource tag.</p>
                tags:
                  - Untag
                  - Resources
                  - Identifiers
                  - Configurations
                  - Endpoints
                  - Group
                  - Ephemeris
                  - Mission Profile
                  - Types
                  - Dataflow
                  - Profiles
                  - Configurations
                  - Minute
                  - Usage
                  - Contacts
                  - Ephemerides
                  - Groundstation
                  - Satellites
                  - ARN
            /agent:
              POST:
                summary: RegisterAgent
                description: >-
                  <note> <p> For use by AWS Ground Station Agent and shouldn't
                  be called directly.</p> </note> <p> Registers a new agent with
                  AWS Ground Station. </p>
                tags:
                  - Register
                  - Agent
                  - Identifiers
                  - Configurations
                  - Endpoints
                  - Group
                  - Ephemeris
                  - Mission Profile
                  - Types
                  - Dataflow
                  - Profiles
                  - Configurations
                  - Minute
                  - Usage
                  - Contacts
                  - Ephemerides
                  - Groundstation
                  - Satellites
                  - ARN
                  - Agent
            /contact:
              POST:
                summary: ReserveContact
                description: <p>Reserves a contact using specified parameters.</p>
                tags:
                  - Reserve
                  - Contacts
                  - Identifiers
                  - Configurations
                  - Endpoints
                  - Group
                  - Ephemeris
                  - Mission Profile
                  - Types
                  - Dataflow
                  - Profiles
                  - Configurations
                  - Minute
                  - Usage
                  - Contacts
                  - Ephemerides
                  - Groundstation
                  - Satellites
                  - ARN
                  - Agent
                  - Contacts
            /agent/{agentId}:
              PUT:
                summary: UpdateAgentStatus
                description: >-
                  <note> <p> For use by AWS Ground Station Agent and shouldn't
                  be called directly.</p> </note> <p>Update the status of the 
                tags:
                  - Update
                  - Agent
                  - Status
                  - Identifiers
                  - Configurations
                  - Endpoints
                  - Group
                  - Ephemeris
                  - Mission Profile
                  - Types
                  - Dataflow
                  - Profiles
                  - Configurations
                  - Minute
                  - Usage
                  - Contacts
                  - Ephemerides
                  - Groundstation
                  - Satellites
                  - ARN
                  - Agent
                  - Conta
    overlays:
      - type: APIs.io Search
        url: overlays/groundstation-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/groundstation-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:groundstation
  - name: sesv2
    description: >-
      <fullname>Amazon SES API v2</fullname> <p> <a
      href="http://aws.amazon.com/ses">Amazon SES</a> is an Amazon Web Services
      service that you can use to send email messages to your customers.</p>
      <p>If you're new to Amazon SES API v2, you might find it helpful to review
      the <a
      href="https://docs.aws.amazon.com/ses/latest/DeveloperGuide/">Amazon
      Simple Email Service Developer Guide</a>. The <i>Amazon SES Developer
      Guide</i> provides information and code samples that demonstrate how to
      use Amazon SES API v2 features programmatically.</p>
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
            title: sesv2
          paths:
            /v2/email/metrics/batch:
              POST:
                summary: BatchGetMetricData
                description: >-
                  <p>Retrieves batches of metric data collected based on your
                  sending activity.</p> <p>You can execute this operation no
                  more than 16 times per second, and with at most 160 queries
                  from the batches per second (cumulative).</p>
                tags:
                  - Batches
                  - Get
                  - Metrics
                  - Data
                  - V2
                  - Email
                  - Metrics
                  - Batches
            /v2/email/export-jobs/{JobId}/cancel:
              PUT:
                summary: CancelExportJob
                description: <p>Cancels an export job.</p>
                tags:
                  - Cancel
                  - Export
                  - Jobs
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
            /v2/email/configuration-sets:
              GET:
                summary: ListConfigurationSets
                description: >-
                  <p>List all of the configuration sets associated with your
                  account in the current region.</p> <p> <i>Configuration
                  sets</i> are groups of rules that you can apply to the emails
                  you send. You apply a configuration set to an email by
                  including a reference to the configuration set in the headers
                  of the email. When you apply a configuration set to an email,
                  all of the rules in that configuration set are applied to the
                  email.</p>
                tags:
                  - Lists
                  - Configurations
                  - Sets
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
            /v2/email/configuration-sets/{ConfigurationSetName}/event-destinations:
              GET:
                summary: GetConfigurationSetEventDestinations
                description: >-
                  <p>Retrieve a list of event destinations that are associated
                  with a configuration set.</p> <p> <i>Events</i> include
                  message sends, deliveries, opens, clicks, bounces, and
                  complaints. <i>Event destinations</i> are places that you can
                  send information about these events to. For example, you can
                  send event data to Amazon SNS to receive notifications when
                  you receive bounces or complaints, or you can use Amazon
                  Kinesis Data Firehose to stream data to Amazon S3 for
                  long-term storage.</p>
                tags:
                  - Get
                  - Configurations
                  - Sets
                  - Events
                  - Destinations
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
            /v2/email/contact-lists/{ContactListName}/contacts:
              GET:
                summary: ListContacts
                description: <p>Lists the contacts present in a specific contact list.</p>
                tags:
                  - Lists
                  - Contacts
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
            /v2/email/contact-lists:
              GET:
                summary: ListContactLists
                description: <p>Lists all of the contact lists available.</p>
                tags:
                  - Lists
                  - Contacts
                  - Lists
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
            /v2/email/custom-verification-email-templates:
              GET:
                summary: ListCustomVerificationEmailTemplates
                description: >-
                  <p>Lists the existing custom verification email templates for
                  your account in the current Amazon Web Services Region.</p>
                  <p>For more information about custom verification email
                  templates, see <a
                  href="https://docs.aws.amazon.com/ses/latest/dg/creating-identities.html#send-email-verify-address-custom">Using
                  custom verification email templates</a> in the <i>Amazon SES
                  Developer Guide</i>.</p> <p>You can execute this operation no
                  more than once per second.</p>
                tags:
                  - Lists
                  - Custom
                  - Verification
                  - Email
                  - Templates
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
            /v2/email/dedicated-ip-pools:
              GET:
                summary: ListDedicatedIpPools
                description: >-
                  <p>List all of the dedicated IP pools that exist in your
                  Amazon Web Services account in the current Region.</p>
                tags:
                  - Lists
                  - Dedicated
                  - IP
                  - Pools
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
            /v2/email/deliverability-dashboard/test:
              POST:
                summary: CreateDeliverabilityTestReport
                description: >-
                  <p>Create a new predictive inbox placement test. Predictive
                  inbox placement tests can help you predict how your messages
                  will be handled by various email providers around the world.
                  When you perform a predictive inbox placement test, you
                  provide a sample message that contains the content that you
                  plan to send to your customers. Amazon SES then sends that
                  message to special email addresses spread across several major
                  email providers. After about 24 hours, the test is complete,
                  and you can use the <code>GetDeliverabilityTestReport</code>
                  operation to view the results of the test.</p>
                tags:
                  - Create
                  - Deliverability
                  - Tests
                  - Reports
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
            /v2/email/identities:
              GET:
                summary: ListEmailIdentities
                description: >-
                  <p>Returns a list of all of the email identities that are
                  associated with your Amazon Web Services account. An identity
                  can be either an email address or a domain. This operation
                  returns identities that are verified as well as those that
                  aren't. This operation returns identities that are associated
                  with Amazon SES and Amazon Pinpoint.</p>
                tags:
                  - Lists
                  - Email
                  - Identities
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
            /v2/email/identities/{EmailIdentity}/policies/{PolicyName}:
              PUT:
                summary: UpdateEmailIdentityPolicy
                description: >-
                  <p>Updates the specified sending authorization policy for the
                  given identity (an email address or a domain). This API
                  returns successfully even if a policy with the specified name
                  does not exist.</p> <note> <p>This API is for the identity
                  owner only. If you have not verified the identity, this API
                  will return an error.</p> </note> <p>Sending authorization is
                  a feature that enables an identity owner to authorize other
                  senders to use its identities. For information about using
                  sending authorization, see the <a
                  href="https://docs.aws.amazon.com/ses/latest/DeveloperGuide/sending-authorization.html">Amazon
                  SES Developer Guide</a>.</p> <p>You can execute this operation
                  no more than once per second.</p>
                tags:
                  - Update
                  - Email
                  - Identity
                  - Policies
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
            /v2/email/templates:
              GET:
                summary: ListEmailTemplates
                description: >-
                  <p>Lists the email templates present in your Amazon SES
                  account in the current Amazon Web Services Region.</p> <p>You
                  can execute this operation no more than once per second.</p>
                tags:
                  - Lists
                  - Email
                  - Templates
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
            /v2/email/export-jobs:
              POST:
                summary: CreateExportJob
                description: >-
                  <p>Creates an export job for a data source and
                  destination.</p> <p>You can execute this operation no more
                  than once per second.</p>
                tags:
                  - Create
                  - Export
                  - Jobs
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
            /v2/email/import-jobs:
              GET:
                summary: ListImportJobs
                description: <p>Lists all of the import jobs.</p>
                tags:
                  - Lists
                  - Import
                  - Jobs
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
            /v2/email/configuration-sets/{ConfigurationSetName}:
              GET:
                summary: GetConfigurationSet
                description: >-
                  <p>Get information about an existing configuration set,
                  including the dedicated IP pool that it's associated with,
                  whether or not it's enabled for sending email, and more.</p>
                  <p> <i>Configuration sets</i> are groups of rules that you can
                  apply to the emails you send. You apply a configuration set to
                  an email by including a reference to the configuration set in
                  the headers of the email. When you apply a configuration set
                  to an email, all of the rules in that configuration set are
                  applied to the email.</p>
                tags:
                  - Get
                  - Configurations
                  - Sets
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
            /v2/email/configuration-sets/{ConfigurationSetName}/event-destinations/{EventDestinationName}:
              PUT:
                summary: UpdateConfigurationSetEventDestination
                description: >-
                  <p>Update the configuration of an event destination for a
                  configuration set.</p> <p> <i>Events</i> include message
                  sends, deliveries, opens, clicks, bounces, and complaints.
                  <i>Event destinations</i> are places that you can send
                  information about these events to. For example, you can send
                  event data to Amazon SNS to receive notifications when you
                  receive bounces or complaints, or you can use Amazon Kinesis
                  Data Firehose to stream data to Amazon S3 for long-term
                  storage.</p>
                tags:
                  - Update
                  - Configurations
                  - Sets
                  - Events
                  - Destinations
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
            /v2/email/contact-lists/{ContactListName}/contacts/{EmailAddress}:
              PUT:
                summary: UpdateContact
                description: >-
                  <p>Updates a contact's preferences for a list. It is not
                  necessary to specify all existing topic preferences in the
                  TopicPreferences object, just the ones that need updating.</p>
                tags:
                  - Update
                  - Contacts
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
            /v2/email/contact-lists/{ContactListName}:
              PUT:
                summary: UpdateContactList
                description: >-
                  <p>Updates contact list metadata. This operation does a
                  complete replacement.</p>
                tags:
                  - Update
                  - Contacts
                  - Lists
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
            /v2/email/custom-verification-email-templates/{TemplateName}:
              PUT:
                summary: UpdateCustomVerificationEmailTemplate
                description: >-
                  <p>Updates an existing custom verification email template.</p>
                  <p>For more information about custom verification email
                  templates, see <a
                  href="https://docs.aws.amazon.com/ses/latest/dg/creating-identities.html#send-email-verify-address-custom">Using
                  custom verification email templates</a> in the <i>Amazon SES
                  Developer Guide</i>.</p> <p>You can execute this operation no
                  more than once per second.</p>
                tags:
                  - Update
                  - Custom
                  - Verification
                  - Email
                  - Templates
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
            /v2/email/dedicated-ip-pools/{PoolName}:
              GET:
                summary: GetDedicatedIpPool
                description: <p>Retrieve information about the dedicated pool.</p>
                tags:
                  - Get
                  - Dedicated
                  - IP
                  - Pools
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
                  - Pools
            /v2/email/identities/{EmailIdentity}:
              GET:
                summary: GetEmailIdentity
                description: >-
                  <p>Provides information about a specific identity, including
                  the identity's verification status, sending authorization
                  policies, its DKIM authentication status, and its custom
                  Mail-From settings.</p>
                tags:
                  - Get
                  - Email
                  - Identity
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
                  - Pools
            /v2/email/templates/{TemplateName}:
              PUT:
                summary: UpdateEmailTemplate
                description: >-
                  <p>Updates an email template. Email templates enable you to
                  send personalized email to one or more destinations in a
                  single API operation. For more information, see the <a
                  href="https://docs.aws.amazon.com/ses/latest/DeveloperGuide/send-personalized-email-api.html">Amazon
                  SES Developer Guide</a>.</p> <p>You can execute this operation
                  no more than once per second.</p>
                tags:
                  - Update
                  - Email
                  - Templates
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
                  - Pools
            /v2/email/suppression/addresses/{EmailAddress}:
              GET:
                summary: GetSuppressedDestination
                description: >-
                  <p>Retrieves information about a specific email address that's
                  on the suppression list for your account.</p>
                tags:
                  - Get
                  - Suppressed
                  - Destinations
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
                  - Pools
            /v2/email/account:
              GET:
                summary: GetAccount
                description: >-
                  <p>Obtain information about the email-sending status and
                  capabilities of your Amazon SES account in the current Amazon
                  Web Services Region.</p>
                tags:
                  - Get
                  - Account
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
                  - Pools
                  - Account
            /v2/email/deliverability-dashboard/blacklist-report:
              GET:
                summary: GetBlacklistReports
                description: >-
                  <p>Retrieve a list of the blacklists that your dedicated IP
                  addresses appear on.</p>
                tags:
                  - Get
                  - Blacklist
                  - Reports
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
                  - Pools
                  - Account
                  - Blacklist
                  - Reports
            /v2/email/dedicated-ips/{IP}:
              GET:
                summary: GetDedicatedIp
                description: >-
                  <p>Get information about a dedicated IP address, including the
                  name of the dedicated IP pool that it's associated with, as
                  well information about the automatic warm-up process for the
                  address.</p>
                tags:
                  - Get
                  - Dedicated
                  - IP
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
                  - Pools
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
            /v2/email/dedicated-ips:
              GET:
                summary: GetDedicatedIps
                description: >-
                  <p>List the dedicated IP addresses that are associated with
                  your Amazon Web Services account.</p>
                tags:
                  - Get
                  - Dedicated
                  - IP Addresses
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
                  - Pools
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
            /v2/email/deliverability-dashboard:
              PUT:
                summary: PutDeliverabilityDashboardOption
                description: >-
                  <p>Enable or disable the Deliverability dashboard. When you
                  enable the Deliverability dashboard, you gain access to
                  reputation, deliverability, and other metrics for the domains
                  that you use to send email. You also gain the ability to
                  perform predictive inbox placement tests.</p> <p>When you use
                  the Deliverability dashboard, you pay a monthly subscription
                  charge, in addition to any other fees that you accrue by using
                  Amazon SES and other Amazon Web Services services. For more
                  information about the features and cost of a Deliverability
                  dashboard subscription, see <a
                  href="http://aws.amazon.com/ses/pricing/">Amazon SES
                  Pricing</a>.</p>
                tags:
                  - Put
                  - Deliverability
                  - Dashboard
                  - Options
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
                  - Pools
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
            /v2/email/deliverability-dashboard/test-reports/{ReportId}:
              GET:
                summary: GetDeliverabilityTestReport
                description: >-
                  <p>Retrieve the results of a predictive inbox placement
                  test.</p>
                tags:
                  - Get
                  - Deliverability
                  - Tests
                  - Reports
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
                  - Pools
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
            /v2/email/deliverability-dashboard/campaigns/{CampaignId}:
              GET:
                summary: GetDomainDeliverabilityCampaign
                description: >-
                  <p>Retrieve all the deliverability data for a specific
                  campaign. This data is available for a campaign only if the
                  campaign sent email by using a domain that the Deliverability
                  dashboard is enabled for.</p>
                tags:
                  - Get
                  - Domains
                  - Deliverability
                  - Campaigns
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
                  - Pools
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Campaigns
            /v2/email/deliverability-dashboard/statistics-report/{Domain}:
              GET:
                summary: GetDomainStatisticsReport
                description: >-
                  <p>Retrieve inbox placement and engagement rates for the
                  domains that you use to send email.</p>
                tags:
                  - Get
                  - Domains
                  - Statistics
                  - Reports
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
                  - Pools
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Campaigns
                  - Domains
            /v2/email/identities/{EmailIdentity}/policies:
              GET:
                summary: GetEmailIdentityPolicies
                description: >-
                  <p>Returns the requested sending authorization policies for
                  the given identity (an email address or a domain). The
                  policies are returned as a map of policy names to policy
                  contents. You can retrieve a maximum of 20 policies at a
                  time.</p> <note> <p>This API is for the identity owner only.
                  If you have not verified the identity, this API will return an
                  error.</p> </note> <p>Sending authorization is a feature that
                  enables an identity owner to authorize other senders to use
                  its identities. For information about using sending
                  authorization, see the <a
                  href="https://docs.aws.amazon.com/ses/latest/DeveloperGuide/sending-authorization.html">Amazon
                  SES Developer Guide</a>.</p> <p>You can execute this operation
                  no more than once per second.</p>
                tags:
                  - Get
                  - Email
                  - Identity
                  - Policies
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
                  - Pools
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Campaigns
                  - Domains
            /v2/email/export-jobs/{JobId}:
              GET:
                summary: GetExportJob
                description: <p>Provides information about an export job.</p>
                tags:
                  - Get
                  - Export
                  - Jobs
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
                  - Pools
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Campaigns
                  - Domains
            /v2/email/import-jobs/{JobId}:
              GET:
                summary: GetImportJob
                description: <p>Provides information about an import job.</p>
                tags:
                  - Get
                  - Import
                  - Jobs
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
                  - Pools
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Campaigns
                  - Domains
            /v2/email/insights/{MessageId}/:
              GET:
                summary: GetMessageInsights
                description: >-
                  <p>Provides information about a specific message, including
                  the from address, the subject, the recipient address, email
                  tags, as well as events associated with the message.</p>
                  <p>You can execute this operation no more than once per
                  second.</p>
                tags:
                  - Get
                  - Messages
                  - Insights
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
                  - Pools
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Campaigns
                  - Domains
                  - Messages
            /v2/email/deliverability-dashboard/test-reports:
              GET:
                summary: ListDeliverabilityTestReports
                description: >-
                  <p>Show a list of the predictive inbox placement tests that
                  you've performed, regardless of their statuses. For predictive
                  inbox placement tests that are complete, you can use the
                  <code>GetDeliverabilityTestReport</code> operation to view the
                  results.</p>
                tags:
                  - Lists
                  - Deliverability
                  - Tests
                  - Reports
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
                  - Pools
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Campaigns
                  - Domains
                  - Messages
                  - Reports
            /v2/email/deliverability-dashboard/domains/{SubscribedDomain}/campaigns:
              GET:
                summary: ListDomainDeliverabilityCampaigns
                description: >-
                  <p>Retrieve deliverability data for all the campaigns that
                  used a specific domain to send email during a specified time
                  range. This data is available for a domain only if you enabled
                  the Deliverability dashboard for the domain.</p>
                tags:
                  - Lists
                  - Domains
                  - Deliverability
                  - Campaigns
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
                  - Pools
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Campaigns
                  - Domains
                  - Messages
                  - Reports
                  - Subscribed
                  - Campaigns
            /v2/email/list-export-jobs:
              POST:
                summary: ListExportJobs
                description: <p>Lists all of the export jobs.</p>
                tags:
                  - Lists
                  - Export
                  - Jobs
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
                  - Pools
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Campaigns
                  - Domains
                  - Messages
                  - Reports
                  - Subscribed
                  - Campaigns
            /v2/email/vdm/recommendations:
              POST:
                summary: ListRecommendations
                description: >-
                  <p>Lists the recommendations present in your Amazon SES
                  account in the current Amazon Web Services Region.</p> <p>You
                  can execute this operation no more than once per second.</p>
                tags:
                  - Lists
                  - Recommendations
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
                  - Pools
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Campaigns
                  - Domains
                  - Messages
                  - Reports
                  - Subscribed
                  - Campaigns
                  - Vdm
                  - Recommendations
            /v2/email/suppression/addresses:
              PUT:
                summary: PutSuppressedDestination
                description: >-
                  <p>Adds an email address to the suppression list for your
                  account.</p>
                tags:
                  - Put
                  - Suppressed
                  - Destinations
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
                  - Pools
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Campaigns
                  - Domains
                  - Messages
                  - Reports
                  - Subscribed
                  - Campaigns
                  - Vdm
                  - Recommendations
                  - Suppressions
                  - Addresses
            /v2/email/tags:
              DELETE:
                summary: UntagResource
                description: >-
                  <p>Remove one or more tags (keys and values) from a specified
                  resource.</p>
                tags:
                  - Untag
                  - Resources
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
                  - Pools
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Campaigns
                  - Domains
                  - Messages
                  - Reports
                  - Subscribed
                  - Campaigns
                  - Vdm
                  - Recommendations
                  - Suppressions
                  - Addresses
                  - Tags
            /v2/email/account/dedicated-ips/warmup:
              PUT:
                summary: PutAccountDedicatedIpWarmupAttributes
                description: >-
                  <p>Enable or disable the automatic warm-up feature for
                  dedicated IP addresses.</p>
                tags:
                  - Put
                  - Account
                  - Dedicated
                  - IP
                  - Warmup
                  - Attributes
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
                  - Pools
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Campaigns
                  - Domains
                  - Messages
                  - Reports
                  - Subscribed
                  - Campaigns
                  - Vdm
                  - Recommendations
                  - Suppressions
                  - Addresses
                  - Tags
                  - Warmup
            /v2/email/account/details:
              POST:
                summary: PutAccountDetails
                description: <p>Update your Amazon SES account details.</p>
                tags:
                  - Put
                  - Account
                  - Details
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
                  - Pools
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Campaigns
                  - Domains
                  - Messages
                  - Reports
                  - Subscribed
                  - Campaigns
                  - Vdm
                  - Recommendations
                  - Suppressions
                  - Addresses
                  - Tags
                  - Warmup
                  - Details
            /v2/email/account/sending:
              PUT:
                summary: PutAccountSendingAttributes
                description: >-
                  <p>Enable or disable the ability of your account to send
                  email.</p>
                tags:
                  - Put
                  - Account
                  - Sending
                  - Attributes
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
                  - Pools
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Campaigns
                  - Domains
                  - Messages
                  - Reports
                  - Subscribed
                  - Campaigns
                  - Vdm
                  - Recommendations
                  - Suppressions
                  - Addresses
                  - Tags
                  - Warmup
                  - Details
                  - Sending
            /v2/email/account/suppression:
              PUT:
                summary: PutAccountSuppressionAttributes
                description: >-
                  <p>Change the settings for the account-level suppression
                  list.</p>
                tags:
                  - Put
                  - Account
                  - Suppressions
                  - Attributes
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
                  - Pools
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Campaigns
                  - Domains
                  - Messages
                  - Reports
                  - Subscribed
                  - Campaigns
                  - Vdm
                  - Recommendations
                  - Suppressions
                  - Addresses
                  - Tags
                  - Warmup
                  - Details
                  - Sending
            /v2/email/account/vdm:
              PUT:
                summary: PutAccountVdmAttributes
                description: >-
                  <p>Update your Amazon SES account VDM attributes.</p> <p>You
                  can execute this operation no more than once per second.</p>
                tags:
                  - Put
                  - Account
                  - Vdm
                  - Attributes
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
                  - Pools
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Campaigns
                  - Domains
                  - Messages
                  - Reports
                  - Subscribed
                  - Campaigns
                  - Vdm
                  - Recommendations
                  - Suppressions
                  - Addresses
                  - Tags
                  - Warmup
                  - Details
                  - Sending
            /v2/email/configuration-sets/{ConfigurationSetName}/delivery-options:
              PUT:
                summary: PutConfigurationSetDeliveryOptions
                description: >-
                  <p>Associate a configuration set with a dedicated IP pool. You
                  can use dedicated IP pools to create groups of dedicated IP
                  addresses for sending specific types of email.</p>
                tags:
                  - Put
                  - Configurations
                  - Sets
                  - Deliveries
                  - Options
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
                  - Pools
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Campaigns
                  - Domains
                  - Messages
                  - Reports
                  - Subscribed
                  - Campaigns
                  - Vdm
                  - Recommendations
                  - Suppressions
                  - Addresses
                  - Tags
                  - Warmup
                  - Details
                  - Sending
                  - Deliveries
                  - Options
            /v2/email/configuration-sets/{ConfigurationSetName}/reputation-options:
              PUT:
                summary: PutConfigurationSetReputationOptions
                description: >-
                  <p>Enable or disable collection of reputation metrics for
                  emails that you send using a particular configuration set in a
                  specific Amazon Web Services Region.</p>
                tags:
                  - Put
                  - Configurations
                  - Sets
                  - Reputation
                  - Options
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
                  - Pools
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Campaigns
                  - Domains
                  - Messages
                  - Reports
                  - Subscribed
                  - Campaigns
                  - Vdm
                  - Recommendations
                  - Suppressions
                  - Addresses
                  - Tags
                  - Warmup
                  - Details
                  - Sending
                  - Deliveries
                  - Options
                  - Reputation
            /v2/email/configuration-sets/{ConfigurationSetName}/sending:
              PUT:
                summary: PutConfigurationSetSendingOptions
                description: >-
                  <p>Enable or disable email sending for messages that use a
                  particular configuration set in a specific Amazon Web Services
                  Region.</p>
                tags:
                  - Put
                  - Configurations
                  - Sets
                  - Sending
                  - Options
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
                  - Pools
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Campaigns
                  - Domains
                  - Messages
                  - Reports
                  - Subscribed
                  - Campaigns
                  - Vdm
                  - Recommendations
                  - Suppressions
                  - Addresses
                  - Tags
                  - Warmup
                  - Details
                  - Sending
                  - Deliveries
                  - Options
                  - Reputation
            /v2/email/configuration-sets/{ConfigurationSetName}/suppression-options:
              PUT:
                summary: PutConfigurationSetSuppressionOptions
                description: >-
                  <p>Specify the account suppression list preferences for a
                  configuration set.</p>
                tags:
                  - Put
                  - Configurations
                  - Sets
                  - Suppressions
                  - Options
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
                  - Pools
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Campaigns
                  - Domains
                  - Messages
                  - Reports
                  - Subscribed
                  - Campaigns
                  - Vdm
                  - Recommendations
                  - Suppressions
                  - Addresses
                  - Tags
                  - Warmup
                  - Details
                  - Sending
                  - Deliveries
                  - Options
                  - Reputation
            /v2/email/configuration-sets/{ConfigurationSetName}/tracking-options:
              PUT:
                summary: PutConfigurationSetTrackingOptions
                description: >-
                  <p>Specify a custom domain to use for open and click tracking
                  elements in email that you send.</p>
                tags:
                  - Put
                  - Configurations
                  - Sets
                  - Tracking
                  - Options
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
                  - Pools
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Campaigns
                  - Domains
                  - Messages
                  - Reports
                  - Subscribed
                  - Campaigns
                  - Vdm
                  - Recommendations
                  - Suppressions
                  - Addresses
                  - Tags
                  - Warmup
                  - Details
                  - Sending
                  - Deliveries
                  - Options
                  - Reputation
                  - Tracking
            /v2/email/configuration-sets/{ConfigurationSetName}/vdm-options:
              PUT:
                summary: PutConfigurationSetVdmOptions
                description: >-
                  <p>Specify VDM preferences for email that you send using the
                  configuration set.</p> <p>You can execute this operation no
                  more than once per second.</p>
                tags:
                  - Put
                  - Configurations
                  - Sets
                  - Vdm
                  - Options
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
                  - Pools
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Campaigns
                  - Domains
                  - Messages
                  - Reports
                  - Subscribed
                  - Campaigns
                  - Vdm
                  - Recommendations
                  - Suppressions
                  - Addresses
                  - Tags
                  - Warmup
                  - Details
                  - Sending
                  - Deliveries
                  - Options
                  - Reputation
                  - Tracking
            /v2/email/dedicated-ips/{IP}/pool:
              PUT:
                summary: PutDedicatedIpInPool
                description: >-
                  <p>Move a dedicated IP address to an existing dedicated IP
                  pool.</p> <note> <p>The dedicated IP address that you specify
                  must already exist, and must be associated with your Amazon
                  Web Services account. </p> <p>The dedicated IP pool you
                  specify must already exist. You can create a new pool by using
                  the <code>CreateDedicatedIpPool</code> operation.</p> </note>
                tags:
                  - Put
                  - Dedicated
                  - IP
                  - In
                  - Pools
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
                  - Pools
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Campaigns
                  - Domains
                  - Messages
                  - Reports
                  - Subscribed
                  - Campaigns
                  - Vdm
                  - Recommendations
                  - Suppressions
                  - Addresses
                  - Tags
                  - Warmup
                  - Details
                  - Sending
                  - Deliveries
                  - Options
                  - Reputation
                  - Tracking
            /v2/email/dedicated-ip-pools/{PoolName}/scaling:
              PUT:
                summary: PutDedicatedIpPoolScalingAttributes
                description: >-
                  <p>Used to convert a dedicated IP pool to a different scaling
                  mode.</p> <note> <p> <code>MANAGED</code> pools cannot be
                  converted to <code>STANDARD</code> scaling mode.</p> </note>
                tags:
                  - Put
                  - Dedicated
                  - IP
                  - Pools
                  - Scaling
                  - Attributes
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
                  - Pools
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Campaigns
                  - Domains
                  - Messages
                  - Reports
                  - Subscribed
                  - Campaigns
                  - Vdm
                  - Recommendations
                  - Suppressions
                  - Addresses
                  - Tags
                  - Warmup
                  - Details
                  - Sending
                  - Deliveries
                  - Options
                  - Reputation
                  - Tracking
                  - Scaling
            /v2/email/dedicated-ips/{IP}/warmup:
              PUT:
                summary: PutDedicatedIpWarmupAttributes
                description: <p/>
                tags:
                  - Put
                  - Dedicated
                  - IP
                  - Warmup
                  - Attributes
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
                  - Pools
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Campaigns
                  - Domains
                  - Messages
                  - Reports
                  - Subscribed
                  - Campaigns
                  - Vdm
                  - Recommendations
                  - Suppressions
                  - Addresses
                  - Tags
                  - Warmup
                  - Details
                  - Sending
                  - Deliveries
                  - Options
                  - Reputation
                  - Tracking
                  - Scaling
            /v2/email/identities/{EmailIdentity}/configuration-set:
              PUT:
                summary: PutEmailIdentityConfigurationSetAttributes
                description: >-
                  <p>Used to associate a configuration set with an email
                  identity.</p>
                tags:
                  - Put
                  - Email
                  - Identity
                  - Configurations
                  - Sets
                  - Attributes
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
                  - Pools
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Campaigns
                  - Domains
                  - Messages
                  - Reports
                  - Subscribed
                  - Campaigns
                  - Vdm
                  - Recommendations
                  - Suppressions
                  - Addresses
                  - Tags
                  - Warmup
                  - Details
                  - Sending
                  - Deliveries
                  - Options
                  - Reputation
                  - Tracking
                  - Scaling
            /v2/email/identities/{EmailIdentity}/dkim:
              PUT:
                summary: PutEmailIdentityDkimAttributes
                description: >-
                  <p>Used to enable or disable DKIM authentication for an email
                  identity.</p>
                tags:
                  - Put
                  - Email
                  - Identity
                  - DKIM
                  - Attributes
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
                  - Pools
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Campaigns
                  - Domains
                  - Messages
                  - Reports
                  - Subscribed
                  - Campaigns
                  - Vdm
                  - Recommendations
                  - Suppressions
                  - Addresses
                  - Tags
                  - Warmup
                  - Details
                  - Sending
                  - Deliveries
                  - Options
                  - Reputation
                  - Tracking
                  - Scaling
                  - DKIM
            /v1/email/identities/{EmailIdentity}/dkim/signing:
              PUT:
                summary: PutEmailIdentityDkimSigningAttributes
                description: >-
                  <p>Used to configure or change the DKIM authentication
                  settings for an email domain identity. You can use this
                  operation to do any of the following:</p> <ul> <li> <p>Update
                  the signing attributes for an identity that uses Bring Your
                  Own DKIM (BYODKIM).</p> </li> <li> <p>Update the key length
                  that should be used for Easy DKIM.</p> </li> <li> <p>Change
                  from using no DKIM authentication to using Easy DKIM.</p>
                  </li> <li> <p>Change from using no DKIM authentication to
                  using BYODKIM.</p> </li> <li> <p>Change from using Easy DKIM
                  to using BYODKIM.</p> </li> <li> <p>Change from using BYODKIM
                  to using Easy DKIM.</p> </li> </ul>
                tags:
                  - Put
                  - Email
                  - Identity
                  - DKIM
                  - Signing
                  - Attributes
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
                  - Pools
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Campaigns
                  - Domains
                  - Messages
                  - Reports
                  - Subscribed
                  - Campaigns
                  - Vdm
                  - Recommendations
                  - Suppressions
                  - Addresses
                  - Tags
                  - Warmup
                  - Details
                  - Sending
                  - Deliveries
                  - Options
                  - Reputation
                  - Tracking
                  - Scaling
                  - DKIM
                  - Signing
            /v2/email/identities/{EmailIdentity}/feedback:
              PUT:
                summary: PutEmailIdentityFeedbackAttributes
                description: >-
                  <p>Used to enable or disable feedback forwarding for an
                  identity. This setting determines what happens when an
                  identity is used to send an email that results in a bounce or
                  complaint event.</p> <p>If the value is <code>true</code>, you
                  receive email notifications when bounce or complaint events
                  occur. These notifications are sent to the address that you
                  specified in the <code>Return-Path</code> header of the
                  original email.</p> <p>You're required to have a method of
                  tracking bounces and complaints. If you haven't set up another
                  mechanism for receiving bounce or complaint notifications (for
                  example, by setting up an event destination), you receive an
                  email notification when these events occur (even if this
                  setting is disabled).</p>
                tags:
                  - Put
                  - Email
                  - Identity
                  - Feedback
                  - Attributes
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
                  - Pools
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Campaigns
                  - Domains
                  - Messages
                  - Reports
                  - Subscribed
                  - Campaigns
                  - Vdm
                  - Recommendations
                  - Suppressions
                  - Addresses
                  - Tags
                  - Warmup
                  - Details
                  - Sending
                  - Deliveries
                  - Options
                  - Reputation
                  - Tracking
                  - Scaling
                  - DKIM
                  - Signing
                  - Feedback
            /v2/email/identities/{EmailIdentity}/mail-from:
              PUT:
                summary: PutEmailIdentityMailFromAttributes
                description: >-
                  <p>Used to enable or disable the custom Mail-From domain
                  configuration for an email identity.</p>
                tags:
                  - Put
                  - Email
                  - Identity
                  - Mail
                  - From
                  - Attributes
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
                  - Pools
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Campaigns
                  - Domains
                  - Messages
                  - Reports
                  - Subscribed
                  - Campaigns
                  - Vdm
                  - Recommendations
                  - Suppressions
                  - Addresses
                  - Tags
                  - Warmup
                  - Details
                  - Sending
                  - Deliveries
                  - Options
                  - Reputation
                  - Tracking
                  - Scaling
                  - DKIM
                  - Signing
                  - Feedback
                  - Mail
                  - From
            /v2/email/outbound-bulk-emails:
              POST:
                summary: SendBulkEmail
                description: <p>Composes an email message to multiple destinations.</p>
                tags:
                  - Send
                  - Bulk
                  - Email
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
                  - Pools
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Campaigns
                  - Domains
                  - Messages
                  - Reports
                  - Subscribed
                  - Campaigns
                  - Vdm
                  - Recommendations
                  - Suppressions
                  - Addresses
                  - Tags
                  - Warmup
                  - Details
                  - Sending
                  - Deliveries
                  - Options
                  - Reputation
                  - Tracking
                  - Scaling
                  - DKIM
                  - Signing
                  - Feedback
                  - Mail
                  - From
                  - Outbound
                  - Bulk
                  - Emails
            /v2/email/outbound-custom-verification-emails:
              POST:
                summary: SendCustomVerificationEmail
                description: >-
                  <p>Adds an email address to the list of identities for your
                  Amazon SES account in the current Amazon Web Services Region
                  and attempts to verify it. As a result of executing this
                  operation, a customized verification email is sent to the
                  specified address.</p> <p>To use this operation, you must
                  first create a custom verification email template. For more
                  information about creating and using custom verification email
                  templates, see <a
                  href="https://docs.aws.amazon.com/ses/latest/dg/creating-identities.html#send-email-verify-address-custom">Using
                  custom verification email templates</a> in the <i>Amazon SES
                  Developer Guide</i>.</p> <p>You can execute this operation no
                  more than once per second.</p>
                tags:
                  - Send
                  - Custom
                  - Verification
                  - Email
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
                  - Pools
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Campaigns
                  - Domains
                  - Messages
                  - Reports
                  - Subscribed
                  - Campaigns
                  - Vdm
                  - Recommendations
                  - Suppressions
                  - Addresses
                  - Tags
                  - Warmup
                  - Details
                  - Sending
                  - Deliveries
                  - Options
                  - Reputation
                  - Tracking
                  - Scaling
                  - DKIM
                  - Signing
                  - Feedback
                  - Mail
                  - From
                  - Outbound
                  - Bulk
                  - Emails
            /v2/email/outbound-emails:
              POST:
                summary: SendEmail
                description: >-
                  <p>Sends an email message. You can use the Amazon SES API v2
                  to send the following types of messages:</p> <ul> <li> <p>
                  <b>Simple</b> – A standard email message. When you create this
                  type of message, you specify the sender, the recipient, and
                  the message body, and Amazon SES assembles the message for
                  you.</p> </li> <li> <p> <b>Raw</b> – A raw, MIME-formatted
                  email message. When you send this type of email, you have to
                  specify all of the message headers, as well as the message
                  body. You can use this message type to send messages that
                  contain attachments. The message that you specify has to be a
                  valid MIME message.</p> </li> <li> <p> <b>Templated</b> – A
                  message that contains personalization tags. When you send this
                  type of email, Amazon SES API v2 automatically replaces the
                  tags with values that you specify.</p> </li> </ul>
                tags:
                  - Send
                  - Email
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
                  - Pools
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Campaigns
                  - Domains
                  - Messages
                  - Reports
                  - Subscribed
                  - Campaigns
                  - Vdm
                  - Recommendations
                  - Suppressions
                  - Addresses
                  - Tags
                  - Warmup
                  - Details
                  - Sending
                  - Deliveries
                  - Options
                  - Reputation
                  - Tracking
                  - Scaling
                  - DKIM
                  - Signing
                  - Feedback
                  - Mail
                  - From
                  - Outbound
                  - Bulk
                  - Emails
            /v2/email/templates/{TemplateName}/render:
              POST:
                summary: TestRenderEmailTemplate
                description: >-
                  <p>Creates a preview of the MIME content of an email when
                  provided with a template and a set of replacement data.</p>
                  <p>You can execute this operation no more than once per s
                tags:
                  - Tests
                  - Render
                  - Email
                  - Templates
                  - V2
                  - Email
                  - Metrics
                  - Batches
                  - Jobs
                  - Identifiers
                  - Cancel
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Contacts
                  - Lists
                  - Contacts
                  - Lists
                  - Custom
                  - Verification
                  - Templates
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Identity
                  - Policies
                  - Policies
                  - Export
                  - Jobs
                  - Import
                  - Destinations
                  - Addresses
                  - Templates
                  - Pools
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Campaigns
                  - Domains
                  - Messages
                  - Reports
                  - Subscribed
                  - Campaigns
                  - Vdm
                  - Recommendations
                  - Suppressions
                  - Addresses
                  - Tags
                  - Warmup
                  - Details
                  - Sending
                  - Deliveries
                  - Options
                  - Reputation
                  - Tracking
                  - Scaling
                  - DKIM
                  - Signing
                  - Feedback
                  - Mail
                  - From
                  - Outbound
                  - Bulk
                  - Emails
                  - Rend
    overlays:
      - type: APIs.io Search
        url: overlays/sesv2-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/sesv2-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:sesv2
  - name: FactSet IRN Contacts API
    description: >-
      Contacts API allows users to create, update and delete Contacts as well as
      configure settings in the Internal Research Notes Contacts application.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.factset.com/api-catalog/irn-contacts-api
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: https://developer.factset.com/api-catalog/irn-contacts-api#overview
      - type: SDKs
        url: https://developer.factset.com/api-catalog/irn-contacts-api#sdkLibrary
      - type: Jupyter Notebooks
        url: https://developer.factset.com/api-catalog/irn-contacts-api#notebooks
      - type: Code Snippets
        url: https://developer.factset.com/api-catalog/irn-contacts-api#codeSnippet
      - type: Change Log
        url: https://developer.factset.com/api-catalog/irn-contacts-api#changelog
      - type: OpenAPI
        data:
          openapi: 3.0.1
          info:
            title: IRN API v1
          paths:
            /v1/contact-relationships:
              get:
                tags:
                  - Get
                  - All
                  - The
                  - Relationships
                  - Where
                  - Given
                  - Symbol
                  - Or
                  - Contact
                  - Identifier
                  - Has
                  - Been
                  - Tagged
                  - In
                  - Relationship
                  - V1
                  - Contact
                  - Relationships
                summary: >-
                  Get all the relationships where the given symbol or contact
                  identifier has been tagged in a relationship
              post:
                tags:
                  - Create
                  - Contact
                  - Relationship
                  - V1
                  - Contact
                  - Relationships
                summary: Create a contact relationship
            /v1/contact-relationships/{contactRelationshipId}:
              get:
                tags:
                  - Get
                  - Details
                  - 'On'
                  - Specific
                  - Contact
                  - Relationship
                  - V1
                  - Contact
                  - Relationships
                  - Relationship
                  - Id
                summary: Get details on a specific contact relationship
              patch:
                tags:
                  - Update
                  - Contact
                  - Relationship
                  - V1
                  - Contact
                  - Relationships
                  - Relationship
                  - Id
                summary: Update a contact relationship
              delete:
                tags:
                  - Delete
                  - Contact
                  - Relationship
                  - V1
                  - Contact
                  - Relationships
                  - Relationship
                  - Id
                summary: Delete a contact relationship
            /v1/contacts:
              get:
                tags:
                  - Get
                  - List
                  - Of
                  - All
                  - Contacts
                  - In
                  - Your
                  - Group
                  - Along
                  - With
                  - Some
                  - Their
                  - Standard
                  - Field
                  - Data
                  - V1
                  - Contact
                  - Relationships
                  - Relationship
                  - Id
                  - Contacts
                summary: >-
                  Get list of all contacts in your group along with some of
                  their standard field data
              post:
                tags:
                  - Create
                  - Contact
                  - V1
                  - Contact
                  - Relationships
                  - Relationship
                  - Id
                  - Contacts
                summary: Create a contact
            /v1/contacts/{contactId}:
              get:
                tags:
                  - Get
                  - All
                  - Custom
                  - Field
                  - And
                  - Standard
                  - Details
                  - 'On'
                  - Specific
                  - Contact
                  - V1
                  - Contact
                  - Relationships
                  - Relationship
                  - Id
                  - Contacts
                summary: >-
                  Get all custom field and standard field details on a specific
                  contact
              patch:
                tags:
                  - Edit
                  - Contact’s
                  - Standard
                  - Field
                  - And
                  - Custom
                  - Data
                  - V1
                  - Contact
                  - Relationships
                  - Relationship
                  - Id
                  - Contacts
                summary: Edit a contact’s standard field and custom field data
              delete:
                tags:
                  - Delete
                  - Contact
                  - V1
                  - Contact
                  - Relationships
                  - Relationship
                  - Id
                  - Contacts
                summary: Delete a contact
            /v1/contacts/{contactId}/about:
              get:
                tags:
                  - Get
                  - The
                  - About
                  - Field
                  - Content
                  - For
                  - Specific
                  - Contact
                  - V1
                  - Contact
                  - Relationships
                  - Relationship
                  - Id
                  - Contacts
                  - About
                summary: Get the About field content for a specific contact
            /v1/contacts/{contactId}/events:
              get:
                tags:
                  - Get
                  - Contact’s
                  - Audit
                  - History
                  - V1
                  - Contact
                  - Relationships
                  - Relationship
                  - Id
                  - Contacts
                  - About
                  - Events
                summary: Get a contact’s audit history
            /v1/contacts/{contactId}/records:
              get:
                tags:
                  - Get
                  - All
                  - Notes
                  - And
                  - Meetings
                  - Where
                  - Specific
                  - Contact
                  - Was
                  - Tagged
                  - V1
                  - Contact
                  - Relationships
                  - Relationship
                  - Id
                  - Contacts
                  - About
                  - Events
                  - Records
                summary: Get all notes and meetings where a specific contact was tagged
            /v1/contacts/{contactId}/relationships:
              get:
                tags:
                  - Returns
                  - List
                  - Of
                  - Contact’s
                  - Relationships
                  - V1
                  - Contact
                  - Relationships
                  - Relationship
                  - Id
                  - Contacts
                  - About
                  - Events
                  - Records
                summary: Returns a list of a contact’s relationships
          tags:
            - name: Contacts
            - name: Cont
    overlays:
      - type: APIs.io Search
        url: overlays/irn-contacts-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/irn-contacts-openapi-api-evangelist-ratings.yml
    aid: factset:factset-irn-contacts-api
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---