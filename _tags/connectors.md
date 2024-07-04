---
name: Connectors
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/connectors.png
url: https://example.com/apis/connectors.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Connectors
apis:
  - name: appflow
    description: >-
      <p>Welcome to the Amazon AppFlow API reference. This guide is for
      developers who need detailed information about the Amazon AppFlow API
      operations, data types, and errors. </p> <p>Amazon AppFlow is a fully
      managed integration service that enables you to securely transfer data
      between software as a service (SaaS) applications like Salesforce,
      Marketo, Slack, and ServiceNow, and Amazon Web Services like Amazon S3 and
      Amazon Redshift. </p> <p>Use the following links to get started on the
      Amazon AppFlow API:</p> <ul> <li> <p> <a
      href="https://docs.aws.amazon.com/appflow/1.0/APIReference/API_Operations.html">Actions</a>:
      An alphabetical list of all Amazon AppFlow API operations.</p> </li> <li>
      <p> <a
      href="https://docs.aws.amazon.com/appflow/1.0/APIReference/API_Types.html">Data
      types</a>: An alphabetical list of all Amazon AppFlow data types.</p>
      </li> <li> <p> <a
      href="https://docs.aws.amazon.com/appflow/1.0/APIReference/CommonParameters.html">Common
      parameters</a>: Parameters that all Query operations can use.</p> </li>
      <li> <p> <a
      href="https://docs.aws.amazon.com/appflow/1.0/APIReference/CommonErrors.html">Common
      errors</a>: Client and server errors that all operations can return.</p>
      </li> </ul> <p>If you're new to Amazon AppFlow, we recommend that you
      review the <a
      href="https://docs.aws.amazon.com/appflow/latest/userguide/what-is-appflow.html">Amazon
      AppFlow User Guide</a>.</p> <p>Amazon AppFlow API users can use
      vendor-specific mechanisms for OAuth, and include applicable OAuth
      attributes (such as <code>auth-code</code> and <code>redirecturi</code>)
      with the connector-specific <code>ConnectorProfileProperties</code> when
      creating a new connector profile using Amazon AppFlow API operations. For
      example, Salesforce users can refer to the <a
      href="https://help.salesforce.com/articleView?id=remoteaccess_authenticate.htm">
      <i>Authorize Apps with OAuth</i> </a> documentation.</p>
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
            title: appflow
          paths:
            /cancel-flow-executions:
              POST:
                summary: CancelFlowExecutions
                description: >-
                  <p>Cancels active runs for a flow.</p> <p>You can cancel all
                  of the active runs for a flow, or you can cancel specific runs
                  by providing their IDs.</p> <p>You can cancel a flow run only
                  when the run is in progress. You can't cancel a run that has
                  already completed or failed. You also can't cancel a run
                  that's scheduled to occur but hasn't started yet. To prevent a
                  scheduled run, you can deactivate the flow with the
                  <code>StopFlow</code> action.</p> <p>You cannot resume a run
                  after you cancel it.</p> <p>When you send your request, the
                  status for each run becomes <code>CancelStarted</code>. When
                  the cancellation completes, the status becomes
                  <code>Canceled</code>.</p> <note> <p>When you cancel a run,
                  you still incur charges for any data that the run already
                  processed before the cancellation. If the run had already
                  written some data to the flow destination, then that data
                  remains in the destination. If you configured the flow to use
                  a batch API (such as the Salesforce Bulk API 2.0), then the
                  run will finish reading or writing its entire batch of data
                  after the cancellation. For these operations, the data
                  processing charges for Amazon AppFlow apply. For the pricing
                  information, see <a
                  href="http://aws.amazon.com/appflow/pricing/">Amazon AppFlow
                  pricing</a>.</p> </note>
                tags:
                  - Cancel
                  - Flow
                  - Executions
                  - Cancel
                  - Flow
                  - Executions
            /create-connector-profile:
              POST:
                summary: CreateConnectorProfile
                description: >-
                  <p> Creates a new connector profile associated with your
                  Amazon Web Services account. There is a soft quota of 100
                  connector profiles per Amazon Web Services account. If you
                  need more connector profiles than this quota allows, you can
                  submit a request to the Amazon AppFlow team through the Amazon
                  AppFlow support channel. In each connector profile that you
                  create, you can provide the credentials and properties for
                  only one connector.</p>
                tags:
                  - Create
                  - Connectors
                  - Profiles
                  - Cancel
                  - Flow
                  - Executions
                  - Create
                  - Connectors
                  - Profiles
            /create-flow:
              POST:
                summary: CreateFlow
                description: >-
                  <p> Enables your application to create a new flow using Amazon
                  AppFlow. You must create a connector profile before calling
                  this API. Please note that the Request Syntax below shows
                  syntax for multiple destinations, however, you can only
                  transfer data to one item in this list at a time. Amazon
                  AppFlow does not currently support flows to multiple
                  destinations at once. </p>
                tags:
                  - Create
                  - Flow
                  - Cancel
                  - Flow
                  - Executions
                  - Create
                  - Connectors
                  - Profiles
            /delete-connector-profile:
              POST:
                summary: DeleteConnectorProfile
                description: <p> Enables you to delete an existing connector profile. </p>
                tags:
                  - Delete
                  - Connectors
                  - Profiles
                  - Cancel
                  - Flow
                  - Executions
                  - Create
                  - Connectors
                  - Profiles
                  - Delete
            /delete-flow:
              POST:
                summary: DeleteFlow
                description: >-
                  <p> Enables your application to delete an existing flow.
                  Before deleting the flow, Amazon AppFlow validates the request
                  by checking the flow configuration and status. You can delete
                  flows one at a time. </p>
                tags:
                  - Delete
                  - Flow
                  - Cancel
                  - Flow
                  - Executions
                  - Create
                  - Connectors
                  - Profiles
                  - Delete
            /describe-connector:
              POST:
                summary: DescribeConnector
                description: >-
                  <p>Describes the given custom connector registered in your
                  Amazon Web Services account. This API can be used for custom
                  connectors that are registered in your account and also for
                  Amazon authored connectors.</p>
                tags:
                  - Describe
                  - Connectors
                  - Cancel
                  - Flow
                  - Executions
                  - Create
                  - Connectors
                  - Profiles
                  - Delete
                  - Describe
            /describe-connector-entity:
              POST:
                summary: DescribeConnectorEntity
                description: >-
                  <p> Provides details regarding the entity used with the
                  connector, with a description of the data model for each field
                  in that entity. </p>
                tags:
                  - Describe
                  - Connectors
                  - Entities
                  - Cancel
                  - Flow
                  - Executions
                  - Create
                  - Connectors
                  - Profiles
                  - Delete
                  - Describe
                  - Entities
            /describe-connector-profiles:
              POST:
                summary: DescribeConnectorProfiles
                description: >-
                  <p> Returns a list of <code>connector-profile</code> details
                  matching the provided <code>connector-profile</code> names and
                  <code>connector-types</code>. Both input lists are optional,
                  and you can use them to filter the result. </p> <p>If no names
                  or <code>connector-types</code> are provided, returns all
                  connector profiles in a paginated form. If there is no match,
                  this operation returns an empty list.</p>
                tags:
                  - Describe
                  - Connectors
                  - Profiles
                  - Cancel
                  - Flow
                  - Executions
                  - Create
                  - Connectors
                  - Profiles
                  - Delete
                  - Describe
                  - Entities
                  - Profiles
            /describe-connectors:
              POST:
                summary: DescribeConnectors
                description: >-
                  <p> Describes the connectors vended by Amazon AppFlow for
                  specified connector types. If you don't specify a connector
                  type, this operation describes all connectors vended by Amazon
                  AppFlow. If there are more connectors than can be returned in
                  one page, the response contains a <code>nextToken</code>
                  object, which can be be passed in to the next call to the
                  <code>DescribeConnectors</code> API operation to retrieve the
                  next page. </p>
                tags:
                  - Describe
                  - Connectors
                  - Cancel
                  - Flow
                  - Executions
                  - Create
                  - Connectors
                  - Profiles
                  - Delete
                  - Describe
                  - Entities
                  - Profiles
                  - Connectors
            /describe-flow:
              POST:
                summary: DescribeFlow
                description: <p> Provides a description of the specified flow. </p>
                tags:
                  - Describe
                  - Flow
                  - Cancel
                  - Flow
                  - Executions
                  - Create
                  - Connectors
                  - Profiles
                  - Delete
                  - Describe
                  - Entities
                  - Profiles
                  - Connectors
            /describe-flow-execution-records:
              POST:
                summary: DescribeFlowExecutionRecords
                description: <p> Fetches the execution history of the flow. </p>
                tags:
                  - Describe
                  - Flow
                  - Execution
                  - Records
                  - Cancel
                  - Flow
                  - Executions
                  - Create
                  - Connectors
                  - Profiles
                  - Delete
                  - Describe
                  - Entities
                  - Profiles
                  - Connectors
                  - Execution
                  - Records
            /list-connector-entities:
              POST:
                summary: ListConnectorEntities
                description: >-
                  <p> Returns the list of available connector entities supported
                  by Amazon AppFlow. For example, you can query Salesforce for
                  <i>Account</i> and <i>Opportunity</i> entities, or query
                  ServiceNow for the <i>Incident</i> entity. </p>
                tags:
                  - Lists
                  - Connectors
                  - Entities
                  - Cancel
                  - Flow
                  - Executions
                  - Create
                  - Connectors
                  - Profiles
                  - Delete
                  - Describe
                  - Entities
                  - Profiles
                  - Connectors
                  - Execution
                  - Records
                  - Lists
                  - Entities
            /list-connectors:
              POST:
                summary: ListConnectors
                description: >-
                  <p>Returns the list of all registered custom connectors in
                  your Amazon Web Services account. This API lists only custom
                  connectors registered in this account, not the Amazon Web
                  Services authored connectors. </p>
                tags:
                  - Lists
                  - Connectors
                  - Cancel
                  - Flow
                  - Executions
                  - Create
                  - Connectors
                  - Profiles
                  - Delete
                  - Describe
                  - Entities
                  - Profiles
                  - Connectors
                  - Execution
                  - Records
                  - Lists
                  - Entities
            /list-flows:
              POST:
                summary: ListFlows
                description: <p> Lists all of the flows associated with your account. </p>
                tags:
                  - Lists
                  - Flows
                  - Cancel
                  - Flow
                  - Executions
                  - Create
                  - Connectors
                  - Profiles
                  - Delete
                  - Describe
                  - Entities
                  - Profiles
                  - Connectors
                  - Execution
                  - Records
                  - Lists
                  - Entities
                  - Flows
            /tags/{resourceArn}:
              DELETE:
                summary: UntagResource
                description: <p> Removes a tag from the specified flow. </p>
                tags:
                  - Untag
                  - Resources
                  - Cancel
                  - Flow
                  - Executions
                  - Create
                  - Connectors
                  - Profiles
                  - Delete
                  - Describe
                  - Entities
                  - Profiles
                  - Connectors
                  - Execution
                  - Records
                  - Lists
                  - Entities
                  - Flows
                  - ARN
            /register-connector:
              POST:
                summary: RegisterConnector
                description: >-
                  <p>Registers a new custom connector with your Amazon Web
                  Services account. Before you can register the connector, you
                  must deploy the associated AWS lambda function in your
                  account.</p>
                tags:
                  - Register
                  - Connectors
                  - Cancel
                  - Flow
                  - Executions
                  - Create
                  - Connectors
                  - Profiles
                  - Delete
                  - Describe
                  - Entities
                  - Profiles
                  - Connectors
                  - Execution
                  - Records
                  - Lists
                  - Entities
                  - Flows
                  - ARN
                  - Register
            /reset-connector-metadata-cache:
              POST:
                summary: ResetConnectorMetadataCache
                description: >-
                  <p>Resets metadata about your connector entities that Amazon
                  AppFlow stored in its cache. Use this action when you want
                  Amazon AppFlow to return the latest information about the data
                  that you have in a source application.</p> <p>Amazon AppFlow
                  returns metadata about your entities when you use the
                  ListConnectorEntities or DescribeConnectorEntities actions.
                  Following these actions, Amazon AppFlow caches the metadata to
                  reduce the number of API requests that it must send to the
                  source application. Amazon AppFlow automatically resets the
                  cache once every hour, but you can use this action when you
                  want to get the latest metadata right away.</p>
                tags:
                  - Reset
                  - Connectors
                  - Metadata
                  - Cache
                  - Cancel
                  - Flow
                  - Executions
                  - Create
                  - Connectors
                  - Profiles
                  - Delete
                  - Describe
                  - Entities
                  - Profiles
                  - Connectors
                  - Execution
                  - Records
                  - Lists
                  - Entities
                  - Flows
                  - ARN
                  - Register
                  - Reset
                  - Metadata
                  - Cache
            /start-flow:
              POST:
                summary: StartFlow
                description: >-
                  <p> Activates an existing flow. For on-demand flows, this
                  operation runs the flow immediately. For schedule and
                  event-triggered flows, this operation activates the flow. </p>
                tags:
                  - Start
                  - Flow
                  - Cancel
                  - Flow
                  - Executions
                  - Create
                  - Connectors
                  - Profiles
                  - Delete
                  - Describe
                  - Entities
                  - Profiles
                  - Connectors
                  - Execution
                  - Records
                  - Lists
                  - Entities
                  - Flows
                  - ARN
                  - Register
                  - Reset
                  - Metadata
                  - Cache
                  - Start
            /stop-flow:
              POST:
                summary: StopFlow
                description: >-
                  <p> Deactivates the existing flow. For on-demand flows, this
                  operation returns an
                  <code>unsupportedOperationException</code> error message. For
                  schedule and event-triggered flows, this operation deactivates
                  the flow. </p>
                tags:
                  - Stop
                  - Flow
                  - Cancel
                  - Flow
                  - Executions
                  - Create
                  - Connectors
                  - Profiles
                  - Delete
                  - Describe
                  - Entities
                  - Profiles
                  - Connectors
                  - Execution
                  - Records
                  - Lists
                  - Entities
                  - Flows
                  - ARN
                  - Register
                  - Reset
                  - Metadata
                  - Cache
                  - Start
                  - Stop
            /unregister-connector:
              POST:
                summary: UnregisterConnector
                description: >-
                  <p>Unregisters the custom connector registered in your account
                  that matches the connector label provided in the request.</p>
                tags:
                  - Unregister
                  - Connectors
                  - Cancel
                  - Flow
                  - Executions
                  - Create
                  - Connectors
                  - Profiles
                  - Delete
                  - Describe
                  - Entities
                  - Profiles
                  - Connectors
                  - Execution
                  - Records
                  - Lists
                  - Entities
                  - Flows
                  - ARN
                  - Register
                  - Reset
                  - Metadata
                  - Cache
                  - Start
                  - Stop
                  - Unregister
            /update-connector-profile:
              POST:
                summary: UpdateConnectorProfile
                description: >-
                  <p> Updates a given connector profile associated with your
                  account. </p>
                tags:
                  - Update
                  - Connectors
                  - Profiles
                  - Cancel
                  - Flow
                  - Executions
                  - Create
                  - Connectors
                  - Profiles
                  - Delete
                  - Describe
                  - Entities
                  - Profiles
                  - Connectors
                  - Execution
                  - Records
                  - Lists
                  - Entities
                  - Flows
                  - ARN
                  - Register
                  - Reset
                  - Metadata
                  - Cache
                  - Start
                  - Stop
                  - Unregister
                  - Update
            /update-connector-registration:
              POST:
                summary: UpdateConnectorRegistration
                description: >-
                  <p>Updates a custom connector that you've previously
                  registered. This operation updates the connector with one of
                  the following:</p> <ul> <li> <p>The latest version of the AWS
                  Lambda function that's assigned to the connector</p> </li>
                  <li> <p>A new AWS Lambda function that you specify</p> </li>
                  </ul>
                tags:
                  - Update
                  - Connectors
                  - Registrations
                  - Cancel
                  - Flow
                  - Executions
                  - Create
                  - Connectors
                  - Profiles
                  - Delete
                  - Describe
                  - Entities
                  - Profiles
                  - Connectors
                  - Execution
                  - Records
                  - Lists
                  - Entities
                  - Flows
                  - ARN
                  - Register
                  - Reset
                  - Metadata
                  - Cache
                  - Start
                  - Stop
                  - Unregister
                  - Update
                  - Registrations
            /update-flow:
              POST:
                summary: UpdateFlow
                description: <p> Updates an existing
                tags:
                  - Update
                  - Flow
                  - Cancel
                  - Flow
                  - Executions
                  - Create
                  - Connectors
                  - Profiles
                  - Delete
                  - Describe
                  - Entities
                  - Profiles
                  - Connectors
                  - Execution
                  - Records
                  - Lists
                  - Entities
                  - Flows
                  - ARN
                  - Register
                  - Reset
                  - Metadata
                  - Cache
                  - Start
                  - Stop
                  - Unregister
                  - Update
                  - Registrations
    overlays:
      - type: APIs.io Search
        url: overlays/appflow-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/appflow-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:appflow
  - name: chime
    description: >-
      <important> <p> <b>Most of these APIs are no longer supported and will not
      be updated.</b> We recommend using the latest versions in the <a
      href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/welcome.html">Amazon
      Chime SDK API reference</a>, in the Amazon Chime SDK.</p> <p>Using the
      latest versions requires migrating to dedicated namespaces. For more
      information, refer to <a
      href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
      from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK Developer
      Guide</i>.</p> </important> <p>The Amazon Chime application programming
      interface (API) is designed so administrators can perform key tasks, such
      as creating and managing Amazon Chime accounts, users, and Voice
      Connectors. This guide provides detailed information about the Amazon
      Chime API, including operations, types, inputs and outputs, and error
      codes.</p> <p>You can use an AWS SDK, the AWS Command Line Interface (AWS
      CLI), or the REST API to make API calls for Amazon Chime. We recommend
      using an AWS SDK or the AWS CLI. The page for each API action contains a
      <i>See Also</i> section that includes links to information about using the
      action with a language-specific AWS SDK or the AWS CLI.</p> <dl> <dt>Using
      an AWS SDK</dt> <dd> <p> You don't need to write code to calculate a
      signature for request authentication. The SDK clients authenticate your
      requests by using access keys that you provide. For more information about
      AWS SDKs, see the <a href="http://aws.amazon.com/developer/">AWS Developer
      Center</a>. </p> </dd> <dt>Using the AWS CLI</dt> <dd> <p>Use your access
      keys with the AWS CLI to make API calls. For information about setting up
      the AWS CLI, see <a
      href="https://docs.aws.amazon.com/cli/latest/userguide/installing.html">Installing
      the AWS Command Line Interface</a> in the <i>AWS Command Line Interface
      User Guide</i>. For a list of available Amazon Chime commands, see the <a
      href="https://docs.aws.amazon.com/cli/latest/reference/chime/index.html">Amazon
      Chime commands</a> in the <i>AWS CLI Command Reference</i>. </p> </dd>
      <dt>Using REST APIs</dt> <dd> <p>If you use REST to make API calls, you
      must authenticate your request by providing a signature. Amazon Chime
      supports Signature Version 4. For more information, see <a
      href="https://docs.aws.amazon.com/general/latest/gr/signature-version-4.html">Signature
      Version 4 Signing Process</a> in the <i>Amazon Web Services General
      Reference</i>.</p> <p>When making REST API calls, use the service name
      <code>chime</code> and REST endpoint
      <code>https://service.chime.aws.amazon.com</code>.</p> </dd> </dl>
      <p>Administrative permissions are controlled using AWS Identity and Access
      Management (IAM). For more information, see <a
      href="https://docs.aws.amazon.com/chime/latest/ag/security-iam.html">Identity
      and Access Management for Amazon Chime</a> in the <i>Amazon Chime
      Administration Guide</i>.</p>
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
            title: chime
          paths:
            /accounts/{accountId}/users/{userId}?operation=associate-phone-number:
              POST:
                summary: AssociatePhoneNumberWithUser
                description: >-
                  <p>Associates a phone number with the specified Amazon Chime
                  user.</p>
                tags:
                  - Associate
                  - Phone
                  - Numbers
                  - null
                  - Users
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
            /voice-connectors/{voiceConnectorId}?operation=associate-phone-numbers:
              POST:
                summary: AssociatePhoneNumbersWithVoiceConnector
                description: >-
                  <p>Associates phone numbers with the specified Amazon Chime
                  Voice Connector.</p> <important> <p> <b>This API is is no
                  longer supported and will not be updated.</b> We recommend
                  using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_voice-chime_AssociatePhoneNumbersWithVoiceConnector.html">AssociatePhoneNumbersWithVoiceConnector</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Associate
                  - Phone
                  - Numbers
                  - null
                  - null
                  - Connectors
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
            /voice-connector-groups/{voiceConnectorGroupId}?operation=associate-phone-numbers:
              POST:
                summary: AssociatePhoneNumbersWithVoiceConnectorGroup
                description: >-
                  <p>Associates phone numbers with the specified Amazon Chime
                  Voice Connector group.</p> <important> <p> <b>This API is is
                  no longer supported and will not be updated.</b> We recommend
                  using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_voice-chime_AssociatePhoneNumbersWithVoiceConnectorGroup.html">AssociatePhoneNumbersWithVoiceConnectorGroup</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Associate
                  - Phone
                  - Numbers
                  - null
                  - null
                  - Connectors
                  - Group
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
            /accounts/{accountId}?operation=associate-signin-delegate-groups:
              POST:
                summary: AssociateSigninDelegateGroupsWithAccount
                description: >-
                  <p>Associates the specified sign-in delegate groups with the
                  specified Amazon Chime account.</p>
                tags:
                  - Associate
                  - Sign In
                  - Delegate
                  - Groups
                  - null
                  - Account
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
            /meetings/{meetingId}/attendees?operation=batch-create:
              POST:
                summary: BatchCreateAttendee
                description: >-
                  <p>Creates up to 100 new attendees for an active Amazon Chime
                  SDK meeting.</p> <important> <p> <b>This API is is no longer
                  supported and will not be updated.</b> We recommend using the
                  latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_meeting-chime_BatchCreateAttendee.html">BatchCreateAttendee</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important> <p>For more information
                  about the Amazon Chime SDK, see <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/meetings-sdk.html">Using
                  the Amazon Chime SDK</a> in the <i>Amazon Chime SDK Developer
                  Guide</i>. </p>
                tags:
                  - Batches
                  - Create
                  - Attendees
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
            /channels/{channelArn}/memberships?operation=batch-create:
              POST:
                summary: BatchCreateChannelMembership
                description: >-
                  <p>Adds a specified number of users to a channel.</p>
                  <important> <p> <b>This API is is no longer supported and will
                  not be updated.</b> We recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_messaging-chime_BatchCreateChannelMembership.html">BatchCreateChannelMembership</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Batches
                  - Create
                  - Channels
                  - Membership
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
            /accounts/{accountId}/rooms/{roomId}/memberships?operation=batch-create:
              POST:
                summary: BatchCreateRoomMembership
                description: >-
                  <p>Adds up to 50 members to a chat room in an Amazon Chime
                  Enterprise account. Members can be users or bots. The member
                  role designates whether the member is a chat room
                  administrator or a general chat room member.</p>
                tags:
                  - Batches
                  - Create
                  - Rooms
                  - Membership
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
            /phone-numbers?operation=batch-delete:
              POST:
                summary: BatchDeletePhoneNumber
                description: >-
                  <p> Moves phone numbers into the <b>Deletion queue</b>. Phone
                  numbers must be disassociated from any users or Amazon Chime
                  Voice Connectors before they can be deleted. </p> <p> Phone
                  numbers remain in the <b>Deletion queue</b> for 7 days before
                  they are deleted permanently. </p>
                tags:
                  - Batches
                  - Delete
                  - Phone
                  - Numbers
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
            /accounts/{accountId}/users?operation=suspend:
              POST:
                summary: BatchSuspendUser
                description: >-
                  <p>Suspends up to 50 users from a <code>Team</code> or
                  <code>EnterpriseLWA</code> Amazon Chime account. For more
                  information about different account types, see <a
                  href="https://docs.aws.amazon.com/chime/latest/ag/manage-chime-account.html">Managing
                  Your Amazon Chime Accounts</a> in the <i>Amazon Chime
                  Administration Guide</i>.</p> <p>Users suspended from a
                  <code>Team</code> account are disassociated from the
                  account,but they can continue to use Amazon Chime as free
                  users. To remove the suspension from suspended
                  <code>Team</code> account users, invite them to the
                  <code>Team</code> account again. You can use the
                  <a>InviteUsers</a> action to do so.</p> <p>Users suspended
                  from an <code>EnterpriseLWA</code> account are immediately
                  signed out of Amazon Chime and can no longer sign in. To
                  remove the suspension from suspended
                  <code>EnterpriseLWA</code> account users, use the
                  <a>BatchUnsuspendUser</a> action.</p> <p> To sign out users
                  without suspending them, use the <a>LogoutUser</a> action.</p>
                tags:
                  - Batches
                  - Suspend
                  - Users
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
            /accounts/{accountId}/users?operation=unsuspend:
              POST:
                summary: BatchUnsuspendUser
                description: >-
                  <p>Removes the suspension from up to 50 previously suspended
                  users for the specified Amazon Chime
                  <code>EnterpriseLWA</code> account. Only users on
                  <code>EnterpriseLWA</code> accounts can be unsuspended using
                  this action. For more information about different account
                  types, see <a
                  href="https://docs.aws.amazon.com/chime/latest/ag/manage-chime-account.html">
                  Managing Your Amazon Chime Accounts </a> in the account types,
                  in the <i>Amazon Chime Administration Guide</i>. </p>
                  <p>Previously suspended users who are unsuspended using this
                  action are returned to <code>Registered</code> status. Users
                  who are not previously suspended are ignored.</p>
                tags:
                  - Batches
                  - Unsuspend
                  - Users
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
            /phone-numbers?operation=batch-update:
              POST:
                summary: BatchUpdatePhoneNumber
                description: >-
                  <p>Updates phone number product types or calling names. You
                  can update one attribute at a time for each
                  <code>UpdatePhoneNumberRequestItem</code>. For example, you
                  can update the product type or the calling name.</p> <p>For
                  toll-free numbers, you cannot use the Amazon Chime Business
                  Calling product type. For numbers outside the U.S., you must
                  use the Amazon Chime SIP Media Application Dial-In product
                  type.</p> <p>Updates to outbound calling names can take up to
                  72 hours to complete. Pending updates to outbound calling
                  names must be complete before you can request another
                  update.</p>
                tags:
                  - Batches
                  - Update
                  - Phone
                  - Numbers
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
            /accounts/{accountId}/users:
              GET:
                summary: ListUsers
                description: >-
                  <p>Lists the users that belong to the specified Amazon Chime
                  account. You can specify an email address to list only the
                  user that the email address belongs to.</p>
                tags:
                  - Lists
                  - Users
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
            /accounts:
              GET:
                summary: ListAccounts
                description: >-
                  <p>Lists the Amazon Chime accounts under the administrator's
                  AWS account. You can filter accounts by account name prefix.
                  To find out which Amazon Chime account a user belongs to, you
                  can filter by the user's email address, which returns one
                  account result.</p>
                tags:
                  - Lists
                  - Accounts
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
            /app-instances:
              GET:
                summary: ListAppInstances
                description: >-
                  <p>Lists all Amazon Chime <code>AppInstance</code>s created
                  under a single AWS account.</p> <important> <p> <b>This API is
                  is no longer supported and will not be updated.</b> We
                  recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_identity-chime_ListAppInstances.html">ListAppInstances</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Lists
                  - Applications
                  - Instances
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
            /app-instances/{appInstanceArn}/admins:
              GET:
                summary: ListAppInstanceAdmins
                description: >-
                  <p>Returns a list of the administrators in the
                  <code>AppInstance</code>.</p> <important> <p> <b>This API is
                  is no longer supported and will not be updated.</b> We
                  recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_identity-chime_ListAppInstanceAdmins.html">ListAppInstanceAdmins</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Lists
                  - Applications
                  - Instances
                  - Administrator
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
            /app-instance-users:
              GET:
                summary: ListAppInstanceUsers
                description: >-
                  <p>List all <code>AppInstanceUsers</code> created under a
                  single <code>AppInstance</code>. </p> <important> <p> <b>This
                  API is is no longer supported and will not be updated.</b> We
                  recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_identity-chime_ListAppInstanceUsers.html">ListAppInstanceUsers</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Lists
                  - Applications
                  - Instances
                  - Users
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
            /meetings/{meetingId}/attendees:
              GET:
                summary: ListAttendees
                description: >-
                  <p> Lists the attendees for the specified Amazon Chime SDK
                  meeting. For more information about the Amazon Chime SDK, see
                  <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/meetings-sdk.html">Using
                  the Amazon Chime SDK</a> in the <i>Amazon Chime SDK Developer
                  Guide</i>. </p> <important> <p> <b>This API is is no longer
                  supported and will not be updated.</b> We recommend using the
                  latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_meeting-chime_ListAttendees.html">ListAttendees</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Lists
                  - Attendees
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
            /accounts/{accountId}/bots:
              GET:
                summary: ListBots
                description: >-
                  <p>Lists the bots associated with the administrator's Amazon
                  Chime Enterprise account ID.</p>
                tags:
                  - Lists
                  - Bots
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
            /channels:
              GET:
                summary: ListChannels
                description: >-
                  <p>Lists all Channels created under a single Chime App as a
                  paginated list. You can specify filters to narrow results.</p>
                  <p class="title"> <b>Functionality &amp; restrictions</b> </p>
                  <ul> <li> <p>Use privacy = <code>PUBLIC</code> to retrieve all
                  public channels in the account.</p> </li> <li> <p>Only an
                  <code>AppInstanceAdmin</code> can set privacy =
                  <code>PRIVATE</code> to list the private channels in an
                  account.</p> </li> </ul> <note> <p>The
                  <code>x-amz-chime-bearer</code> request header is mandatory.
                  Use the <code>AppInstanceUserArn</code> of the user that makes
                  the API call as the value in the header.</p> </note>
                  <important> <p> <b>This API is is no longer supported and will
                  not be updated.</b> We recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_messaging-chime_ListChannels.html">ListChannels</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Lists
                  - Channels
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
            /channels/{channelArn}/bans:
              GET:
                summary: ListChannelBans
                description: >-
                  <p>Lists all the users banned from a particular channel.</p>
                  <note> <p>The <code>x-amz-chime-bearer</code> request header
                  is mandatory. Use the <code>AppInstanceUserArn</code> of the
                  user that makes the API call as the value in the header.</p>
                  </note> <important> <p> <b>This API is is no longer supported
                  and will not be updated.</b> We recommend using the latest
                  version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_messaging-chime_ListChannelBans.html">ListChannelBans</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Lists
                  - Channels
                  - null
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
            /channels/{channelArn}/memberships:
              GET:
                summary: ListChannelMemberships
                description: >-
                  <p>Lists all channel memberships in a channel.</p> <note>
                  <p>The <code>x-amz-chime-bearer</code> request header is
                  mandatory. Use the <code>AppInstanceUserArn</code> of the user
                  that makes the API call as the value in the header.</p>
                  </note> <important> <p> <b>This API is is no longer supported
                  and will not be updated.</b> We recommend using the latest
                  version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_messaging-chime_ListChannelMemberships.html">ListChannelMemberships</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Lists
                  - Channels
                  - Memberships
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
            /channels/{channelArn}/moderators:
              GET:
                summary: ListChannelModerators
                description: >-
                  <p>Lists all the moderators for a channel.</p> <note> <p>The
                  <code>x-amz-chime-bearer</code> request header is mandatory.
                  Use the <code>AppInstanceUserArn</code> of the user that makes
                  the API call as the value in the header.</p> </note>
                  <important> <p> <b>This API is is no longer supported and will
                  not be updated.</b> We recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_messaging-chime_ListChannelModerators.html">ListChannelModerators</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Lists
                  - Channels
                  - Moderators
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
            /media-capture-pipelines:
              GET:
                summary: ListMediaCapturePipelines
                description: >-
                  <p>Returns a list of media capture pipelines.</p> <important>
                  <p> <b>This API is is no longer supported and will not be
                  updated.</b> We recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_media-pipelines-chime_ListMediaCapturePipelines.html">ListMediaCapturePipelines</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Lists
                  - Media
                  - Capture
                  - Pipelines
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
            /meetings:
              GET:
                summary: ListMeetings
                description: >-
                  <p>Lists up to 100 active Amazon Chime SDK meetings.</p>
                  <important> <p>ListMeetings is not supported in the Amazon
                  Chime SDK Meetings Namespace. Update your application to
                  remove calls to this API.</p> </important> <p>For more
                  information about the Amazon Chime SDK, see <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/meetings-sdk.html">Using
                  the Amazon Chime SDK</a> in the <i>Amazon Chime SDK Developer
                  Guide</i>.</p>
                tags:
                  - Lists
                  - Meetings
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
            /meetings/{meetingId}/dial-outs:
              POST:
                summary: CreateMeetingDialOut
                description: >-
                  <p>Uses the join token and call metadata in a meeting request
                  (From number, To number, and so forth) to initiate an outbound
                  call to a public switched telephone network (PSTN) and join
                  them into a Chime meeting. Also ensures that the From number
                  belongs to the customer.</p> <p>To play welcome audio or
                  implement an interactive voice response (IVR), use the
                  <code>CreateSipMediaApplicationCall</code> action with the
                  corresponding SIP media application ID.</p> <important> <p>
                  <b>This API is is not available in a dedicated namespace.</b>
                  </p> </important>
                tags:
                  - Create
                  - Meetings
                  - Dial
                  - Out
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - null
            /meetings?operation=create-attendees:
              POST:
                summary: CreateMeetingWithAttendees
                description: >-
                  <p> Creates a new Amazon Chime SDK meeting in the specified
                  media Region, with attendees. For more information about
                  specifying media Regions, see <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/chime-sdk-meetings-regions.html">Amazon
                  Chime SDK Media Regions</a> in the <i>Amazon Chime SDK
                  Developer Guide</i> . For more information about the Amazon
                  Chime SDK, see <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/meetings-sdk.html">Using
                  the Amazon Chime SDK</a> in the <i>Amazon Chime SDK Developer
                  Guide</i> . </p> <important> <p> <b>This API is is no longer
                  supported and will not be updated.</b> We recommend using the
                  latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_meeting-chime_CreateMeetingWithAttendees.html">CreateMeetingWithAttendees</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Create
                  - Meetings
                  - null
                  - Attendees
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - null
                  - Meetings
            /phone-number-orders:
              GET:
                summary: ListPhoneNumberOrders
                description: >-
                  <p>Lists the phone number orders for the administrator's
                  Amazon Chime account.</p>
                tags:
                  - Lists
                  - Phone
                  - Numbers
                  - Orders
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - null
                  - Meetings
                  - Orders
            /voice-connectors/{voiceConnectorId}/proxy-sessions:
              GET:
                summary: ListProxySessions
                description: >-
                  <p>Lists the proxy sessions for the specified Amazon Chime
                  Voice Connector.</p> <important> <p> <b>This API is is no
                  longer supported and will not be updated.</b> We recommend
                  using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_voice-chime_ListProxySessions.html">ListProxySessions</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Lists
                  - Proxy
                  - Sessions
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - null
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
            /accounts/{accountId}/rooms:
              GET:
                summary: ListRooms
                description: >-
                  <p>Lists the room details for the specified Amazon Chime
                  Enterprise account. Optionally, filter the results by a member
                  ID (user ID or bot ID) to see a list of rooms that the member
                  belongs to.</p>
                tags:
                  - Lists
                  - Rooms
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - null
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
            /accounts/{accountId}/rooms/{roomId}/memberships:
              GET:
                summary: ListRoomMemberships
                description: >-
                  <p>Lists the membership details for the specified room in an
                  Amazon Chime Enterprise account, such as the members' IDs,
                  email addresses, and names.</p>
                tags:
                  - Lists
                  - Rooms
                  - Memberships
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - null
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
            /sip-media-applications:
              GET:
                summary: ListSipMediaApplications
                description: >-
                  <p>Lists the SIP media applications under the administrator's
                  AWS account.</p> <important> <p> <b>This API is is no longer
                  supported and will not be updated.</b> We recommend using the
                  latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_voice-chime_ListSipMediaApplications.html">ListSipMediaApplications</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Lists
                  - SIP
                  - Media
                  - Applications
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - null
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
            /sip-media-applications/{sipMediaApplicationId}/calls:
              POST:
                summary: CreateSipMediaApplicationCall
                description: >-
                  <p>Creates an outbound call to a phone number from the phone
                  number specified in the request, and it invokes the endpoint
                  of the specified <code>sipMediaApplicationId</code>.</p>
                  <important> <p> <b>This API is is no longer supported and will
                  not be updated.</b> We recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_voice-chime_CreateSipMediaApplicationCall.html">CreateSipMediaApplicationCall</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Create
                  - SIP
                  - Media
                  - Applications
                  - Call
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - null
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
            /sip-rules:
              GET:
                summary: ListSipRules
                description: >-
                  <p>Lists the SIP rules under the administrator's AWS
                  account.</p> <important> <p> <b>This API is is no longer
                  supported and will not be updated.</b> We recommend using the
                  latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_voice-chime_ListSipRules.html">ListSipRules</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Lists
                  - SIP
                  - Rules
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - null
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
            /accounts/{accountId}/users?operation=create:
              POST:
                summary: CreateUser
                description: >-
                  <p>Creates a user under the specified Amazon Chime
                  account.</p>
                tags:
                  - Create
                  - Users
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - null
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
            /voice-connectors:
              GET:
                summary: ListVoiceConnectors
                description: >-
                  <p>Lists the Amazon Chime Voice Connectors for the
                  administrator's AWS account.</p> <important> <p> <b>This API
                  is is no longer supported and will not be updated.</b> We
                  recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_voice-chime_ListVoiceConnectors.html">ListVoiceConnectors</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Lists
                  - null
                  - Connectors
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - null
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - null
                  - Connectors
            /voice-connector-groups:
              GET:
                summary: ListVoiceConnectorGroups
                description: >-
                  <p>Lists the Amazon Chime Voice Connector groups for the
                  administrator's AWS account.</p> <important> <p> <b>This API
                  is is no longer supported and will not be updated.</b> We
                  recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_voice-chime_ListVoiceConnectorGroups.html">ListVoiceConnectorGroups</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Lists
                  - null
                  - Connectors
                  - Groups
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - null
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - null
                  - Connectors
            /accounts/{accountId}:
              POST:
                summary: UpdateAccount
                description: >-
                  <p>Updates account details for the specified Amazon Chime
                  account. Currently, only account name and default license
                  updates are supported for this action.</p>
                tags:
                  - Update
                  - Account
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - null
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - null
                  - Connectors
            /app-instances/{appInstanceArn}:
              PUT:
                summary: UpdateAppInstance
                description: >-
                  <p>Updates <code>AppInstance</code> metadata.</p> <important>
                  <p> <b>This API is is no longer supported and will not be
                  updated.</b> We recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_identity-chime_UpdateAppInstance.html">UpdateAppInstance</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Update
                  - Applications
                  - Instances
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - null
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - null
                  - Connectors
            /app-instances/{appInstanceArn}/admins/{appInstanceAdminArn}:
              GET:
                summary: DescribeAppInstanceAdmin
                description: >-
                  <p>Returns the full details of an
                  <code>AppInstanceAdmin</code>.</p> <important> <p> <b>This API
                  is is no longer supported and will not be updated.</b> We
                  recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_identity-chime_DescribeAppInstanceAdmin.html">DescribeAppInstanceAdmin</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Describe
                  - Applications
                  - Instances
                  - Administrative
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - null
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - null
                  - Connectors
                  - Administrative
            /app-instances/{appInstanceArn}/streaming-configurations:
              PUT:
                summary: PutAppInstanceStreamingConfigurations
                description: >-
                  <p>The data streaming configurations of an
                  <code>AppInstance</code>.</p> <important> <p> <b>This API is
                  is no longer supported and will not be updated.</b> We
                  recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_messaging-chime_PutMessagingStreamingConfigurations.html">PutMessagingStreamingConfigurations</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Put
                  - Applications
                  - Instances
                  - Streaming
                  - Configurations
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - null
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - null
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
            /app-instance-users/{appInstanceUserArn}:
              PUT:
                summary: UpdateAppInstanceUser
                description: >-
                  <p>Updates the details of an <code>AppInstanceUser</code>. You
                  can update names and metadata.</p> <important> <p> <b>This API
                  is is no longer supported and will not be updated.</b> We
                  recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_identity-chime_UpdateAppInstanceUser.html">UpdateAppInstanceUser</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Update
                  - Applications
                  - Instances
                  - Users
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - null
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - null
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
            /meetings/{meetingId}/attendees/{attendeeId}:
              GET:
                summary: GetAttendee
                description: >-
                  <p> Gets the Amazon Chime SDK attendee details for a specified
                  meeting ID and attendee ID. For more information about the
                  Amazon Chime SDK, see <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/meetings-sdk.html">Using
                  the Amazon Chime SDK</a> in the <i>Amazon Chime SDK Developer
                  Guide</i>. </p> <important> <p> <b>This API is is no longer
                  supported and will not be updated.</b> We recommend using the
                  latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_meeting-chime_GetAttendee.html">GetAttendee</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Get
                  - Attendees
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - null
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - null
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
            /channels/{channelArn}:
              PUT:
                summary: UpdateChannel
                description: >-
                  <p>Update a channel's attributes.</p> <p> <b>Restriction</b>:
                  You can't change a channel's privacy. </p> <note> <p>The
                  <code>x-amz-chime-bearer</code> request header is mandatory.
                  Use the <code>AppInstanceUserArn</code> of the user that makes
                  the API call as the value in the header.</p> </note>
                  <important> <p> <b>This API is is no longer supported and will
                  not be updated.</b> We recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_messaging-chime_UpdateChannel.html">UpdateChannel</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Update
                  - Channels
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - null
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - null
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
            /channels/{channelArn}/bans/{memberArn}:
              GET:
                summary: DescribeChannelBan
                description: >-
                  <p>Returns the full details of a channel ban.</p> <note>
                  <p>The <code>x-amz-chime-bearer</code> request header is
                  mandatory. Use the <code>AppInstanceUserArn</code> of the user
                  that makes the API call as the value in the header.</p>
                  </note> <important> <p> <b>This API is is no longer supported
                  and will not be updated.</b> We recommend using the latest
                  version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_messaging-chime_DescribeChannelBan.html">DescribeChannelBan</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Describe
                  - Channels
                  - null
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - null
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - null
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
            /channels/{channelArn}/memberships/{memberArn}:
              GET:
                summary: DescribeChannelMembership
                description: >-
                  <p>Returns the full details of a user's channel
                  membership.</p> <note> <p>The <code>x-amz-chime-bearer</code>
                  request header is mandatory. Use the
                  <code>AppInstanceUserArn</code> of the user that makes the API
                  call as the value in the header.</p> </note> <important> <p>
                  <b>This API is is no longer supported and will not be
                  updated.</b> We recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_messaging-chime_DescribeChannelMembership.html">DescribeChannelMembership</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Describe
                  - Channels
                  - Membership
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - null
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - null
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
            /channels/{channelArn}/messages/{messageId}:
              PUT:
                summary: UpdateChannelMessage
                description: >-
                  <p>Updates the content of a message.</p> <note> <p>The
                  <code>x-amz-chime-bearer</code> request header is mandatory.
                  Use the <code>AppInstanceUserArn</code> of the user that makes
                  the API call as the value in the header.</p> </note>
                  <important> <p> <b>This API is is no longer supported and will
                  not be updated.</b> We recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_messaging-chime_UpdateChannelMessage.html">UpdateChannelMessage</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Update
                  - Channels
                  - Messages
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - null
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - null
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
            /channels/{channelArn}/moderators/{channelModeratorArn}:
              GET:
                summary: DescribeChannelModerator
                description: >-
                  <p>Returns the full details of a single ChannelModerator.</p>
                  <note> <p>The <code>x-amz-chime-bearer</code> request header
                  is mandatory. Use the <code>AppInstanceUserArn</code> of the
                  user that makes the API call as the value in the header.</p>
                  </note> <important> <p> <b>This API is is no longer supported
                  and will not be updated.</b> We recommend using the latest
                  version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_messaging-chime_DescribeChannelModerator.html">DescribeChannelModerator</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Describe
                  - Channels
                  - Moderators
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - null
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - null
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
            /accounts/{accountId}/bots/{botId}/events-configuration:
              PUT:
                summary: PutEventsConfiguration
                description: >-
                  <p>Creates an events configuration that allows a bot to
                  receive outgoing events sent by Amazon Chime. Choose either an
                  HTTPS endpoint or a Lambda function ARN. For more information,
                  see <a>Bot</a>.</p>
                tags:
                  - Put
                  - Events
                  - Configurations
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - null
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - null
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
            /media-capture-pipelines/{mediaPipelineId}:
              GET:
                summary: GetMediaCapturePipeline
                description: >-
                  <p>Gets an existing media capture pipeline.</p> <important>
                  <p> <b>This API is is no longer supported and will not be
                  updated.</b> We recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_media-pipelines-chime_GetMediaCapturePipeline.html">GetMediaCapturePipeline</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Get
                  - Media
                  - Capture
                  - Pipelines
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - null
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - null
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
            /meetings/{meetingId}:
              GET:
                summary: GetMeeting
                description: >-
                  <important> <p> <b>This API is is no longer supported and will
                  not be updated.</b> We recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_meeting-chime_GetMeeting.html">GetMeeting</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important> <p> Gets the Amazon
                  Chime SDK meeting details for the specified meeting ID. For
                  more information about the Amazon Chime SDK, see <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/meetings-sdk.html">Using
                  the Amazon Chime SDK</a> in the <i>Amazon Chime SDK Developer
                  Guide</i> . </p>
                tags:
                  - Get
                  - Meetings
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - null
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - null
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
            /phone-numbers/{phoneNumberId}:
              POST:
                summary: UpdatePhoneNumber
                description: >-
                  <p>Updates phone number details, such as product type or
                  calling name, for the specified phone number ID. You can
                  update one phone number detail at a time. For example, you can
                  update either the product type or the calling name in one
                  action.</p> <p>For toll-free numbers, you cannot use the
                  Amazon Chime Business Calling product type. For numbers
                  outside the U.S., you must use the Amazon Chime SIP Media
                  Application Dial-In product type.</p> <p>Updates to outbound
                  calling names can take 72 hours to complete. Pending updates
                  to outbound calling names must be complete before you can
                  request another update.</p>
                tags:
                  - Update
                  - Phone
                  - Numbers
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - null
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - null
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
            /voice-connectors/{voiceConnectorId}/proxy-sessions/{proxySessionId}:
              POST:
                summary: UpdateProxySession
                description: >-
                  <p>Updates the specified proxy session details, such as voice
                  or SMS capabilities.</p> <important> <p> <b>This API is is no
                  longer supported and will not be updated.</b> We recommend
                  using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_voice-chime_UpdateProxySession.html">UpdateProxySession</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Update
                  - Proxy
                  - Sessions
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - null
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - null
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
            /accounts/{accountId}/rooms/{roomId}:
              POST:
                summary: UpdateRoom
                description: >-
                  <p>Updates room details, such as the room name, for a room in
                  an Amazon Chime Enterprise account.</p>
                tags:
                  - Update
                  - Rooms
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - null
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - null
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
            /accounts/{accountId}/rooms/{roomId}/memberships/{memberId}:
              POST:
                summary: UpdateRoomMembership
                description: >-
                  <p>Updates room membership details, such as the member role,
                  for a room in an Amazon Chime Enterprise account. The member
                  role designates whether the member is a chat room
                  administrator or a general chat room member. The member role
                  can be updated only for user IDs.</p>
                tags:
                  - Update
                  - Rooms
                  - Membership
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - null
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - null
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
            /sip-media-applications/{sipMediaApplicationId}:
              PUT:
                summary: UpdateSipMediaApplication
                description: >-
                  <p>Updates the details of the specified SIP media
                  application.</p> <important> <p> <b>This API is is no longer
                  supported and will not be updated.</b> We recommend using the
                  latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_voice-chime_UpdateSipMediaApplication.html">UpdateSipMediaApplication</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Update
                  - SIP
                  - Media
                  - Applications
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - null
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - null
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
            /sip-rules/{sipRuleId}:
              PUT:
                summary: UpdateSipRule
                description: >-
                  <p>Updates the details of the specified SIP rule.</p>
                  <important> <p> <b>This API is is no longer supported and will
                  not be updated.</b> We recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_voice-chime_UpdateSipRule.html">UpdateSipRule</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Update
                  - SIP
                  - Rules
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - null
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - null
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
            /voice-connectors/{voiceConnectorId}:
              PUT:
                summary: UpdateVoiceConnector
                description: >-
                  <p>Updates details for the specified Amazon Chime Voice
                  Connector.</p> <important> <p> <b>This API is is no longer
                  supported and will not be updated.</b> We recommend using the
                  latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_voice-chime_UpdateVoiceConnector.html">UpdateVoiceConnector</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Update
                  - null
                  - Connectors
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - null
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - null
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
            /voice-connectors/{voiceConnectorId}/emergency-calling-configuration:
              PUT:
                summary: PutVoiceConnectorEmergencyCallingConfiguration
                description: >-
                  <p>Puts emergency calling configuration details to the
                  specified Amazon Chime Voice Connector, such as emergency
                  phone numbers and calling countries. Origination and
                  termination settings must be enabled for the Amazon Chime
                  Voice Connector before emergency calling can be
                  configured.</p> <important> <p> <b>This API is is no longer
                  supported and will not be updated.</b> We recommend using the
                  latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_voice-chime_PutVoiceConnectorEmergencyCallingConfiguration.html">PutVoiceConnectorEmergencyCallingConfiguration</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Put
                  - null
                  - Connectors
                  - Emergency
                  - Calling
                  - Configurations
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - null
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - null
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
            /voice-connector-groups/{voiceConnectorGroupId}:
              PUT:
                summary: UpdateVoiceConnectorGroup
                description: >-
                  <p>Updates details of the specified Amazon Chime Voice
                  Connector group, such as the name and Amazon Chime Voice
                  Connector priority ranking.</p> <important> <p> <b>This API is
                  is no longer supported and will not be updated.</b> We
                  recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_voice-chime_UpdateVoiceConnectorGroup.html">UpdateVoiceConnectorGroup</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Update
                  - null
                  - Connectors
                  - Group
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - null
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - null
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
            /voice-connectors/{voiceConnectorId}/origination:
              PUT:
                summary: PutVoiceConnectorOrigination
                description: >-
                  <p>Adds origination settings for the specified Amazon Chime
                  Voice Connector.</p> <note> <p>If emergency calling is
                  configured for the Amazon Chime Voice Connector, it must be
                  deleted prior to turning off origination settings.</p> </note>
                  <important> <p> <b>This API is is no longer supported and will
                  not be updated.</b> We recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_voice-chime_PutVoiceConnectorOrigination.html">PutVoiceConnectorOrigination</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Put
                  - null
                  - Connectors
                  - Origination
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - null
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - null
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
            /voice-connectors/{voiceConnectorId}/programmable-numbers/proxy:
              PUT:
                summary: PutVoiceConnectorProxy
                description: >-
                  <p>Puts the specified proxy configuration to the specified
                  Amazon Chime Voice Connector.</p> <important> <p> <b>This API
                  is is no longer supported and will not be updated.</b> We
                  recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_voice-chime_PutVoiceConnectorProxy.html">PutVoiceConnectorProxy</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Put
                  - null
                  - Connectors
                  - Proxy
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - null
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - null
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
            /voice-connectors/{voiceConnectorId}/streaming-configuration:
              PUT:
                summary: PutVoiceConnectorStreamingConfiguration
                description: >-
                  <p>Adds a streaming configuration for the specified Amazon
                  Chime Voice Connector. The streaming configuration specifies
                  whether media streaming is enabled for sending to Kinesis. It
                  also sets the retention period, in hours, for the Amazon
                  Kinesis data.</p> <important> <p> <b>This API is is no longer
                  supported and will not be updated.</b> We recommend using the
                  latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_voice-chime_PutVoiceConnectorStreamingConfiguration.html">PutVoiceConnectorStreamingConfiguration</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Put
                  - null
                  - Connectors
                  - Streaming
                  - Configurations
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - null
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - null
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
            /voice-connectors/{voiceConnectorId}/termination:
              PUT:
                summary: PutVoiceConnectorTermination
                description: >-
                  <p>Adds termination settings for the specified Amazon Chime
                  Voice Connector.</p> <note> <p>If emergency calling is
                  configured for the Amazon Chime Voice Connector, it must be
                  deleted prior to turning off termination settings.</p> </note>
                  <important> <p> <b>This API is is no longer supported and will
                  not be updated.</b> We recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_voice-chime_PutVoiceConnectorTermination.html">PutVoiceConnectorTermination</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Put
                  - null
                  - Connectors
                  - Termination
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - null
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - null
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
            /voice-connectors/{voiceConnectorId}/termination/credentials?operation=delete:
              POST:
                summary: DeleteVoiceConnectorTerminationCredentials
                description: >-
                  <p>Deletes the specified SIP credentials used by your
                  equipment to authenticate during call termination.</p>
                  <important> <p> <b>This API is is no longer supported and will
                  not be updated.</b> We recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_voice-chime_DeleteVoiceConnectorTerminationCredentials.html">DeleteVoiceConnectorTerminationCredentials</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Delete
                  - null
                  - Connectors
                  - Termination
                  - Credentials
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - null
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - null
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
            /channels/{channelArn}?scope=app-instance-user-membership:
              GET:
                summary: DescribeChannelMembershipForAppInstanceUser
                description: >-
                  <p> Returns the details of a channel based on the membership
                  of the specified <code>AppInstanceUser</code>.</p> <note>
                  <p>The <code>x-amz-chime-bearer</code> request header is
                  mandatory. Use the <code>AppInstanceUserArn</code> of the user
                  that makes the API call as the value in the header.</p>
                  </note> <important> <p> <b>This API is is no longer supported
                  and will not be updated.</b> We recommend using the latest
                  version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_messaging-chime_DescribeChannelMembershipForAppInstanceUser.html">DescribeChannelMembershipForAppInstanceUser</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Describe
                  - Channels
                  - Membership
                  - For
                  - Applications
                  - Instances
                  - Users
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - null
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - null
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
            /channels/{channelArn}?scope=app-instance-user-moderated-channel:
              GET:
                summary: DescribeChannelModeratedByAppInstanceUser
                description: >-
                  <p>Returns the full details of a channel moderated by the
                  specified <code>AppInstanceUser</code>.</p> <note> <p>The
                  <code>x-amz-chime-bearer</code> request header is mandatory.
                  Use the <code>AppInstanceUserArn</code> of the user that makes
                  the API call as the value in the header.</p> </note>
                  <important> <p> <b>This API is is no longer supported and will
                  not be updated.</b> We recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_messaging-chime_DescribeChannelModeratedByAppInstanceUser.html">DescribeChannelModeratedByAppInstanceUser</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Describe
                  - Channels
                  - Moderated
                  - By
                  - Applications
                  - Instances
                  - Users
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - null
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - null
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
            /accounts/{accountId}/users/{userId}?operation=disassociate-phone-number:
              POST:
                summary: DisassociatePhoneNumberFromUser
                description: >-
                  <p>Disassociates the primary provisioned phone number from the
                  specified Amazon Chime user.</p>
                tags:
                  - Disassociate
                  - Phone
                  - Numbers
                  - From
                  - Users
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - null
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - null
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
            /voice-connectors/{voiceConnectorId}?operation=disassociate-phone-numbers:
              POST:
                summary: DisassociatePhoneNumbersFromVoiceConnector
                description: >-
                  <p>Disassociates the specified phone numbers from the
                  specified Amazon Chime Voice Connector.</p> <important> <p>
                  <b>This API is is no longer supported and will not be
                  updated.</b> We recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_voice-chime_DisassociatePhoneNumbersFromVoiceConnector.html">DisassociatePhoneNumbersFromVoiceConnector</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Disassociate
                  - Phone
                  - Numbers
                  - From
                  - null
                  - Connectors
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - null
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - null
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
            /voice-connector-groups/{voiceConnectorGroupId}?operation=disassociate-phone-numbers:
              POST:
                summary: DisassociatePhoneNumbersFromVoiceConnectorGroup
                description: >-
                  <p>Disassociates the specified phone numbers from the
                  specified Amazon Chime Voice Connector group.</p> <important>
                  <p> <b>This API is is no longer supported and will not be
                  updated.</b> We recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_voice-chime_DisassociatePhoneNumbersFromVoiceConnectorGroup.html">DisassociatePhoneNumbersFromVoiceConnectorGroup</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Disassociate
                  - Phone
                  - Numbers
                  - From
                  - null
                  - Connectors
                  - Group
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - null
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - null
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
            /accounts/{accountId}?operation=disassociate-signin-delegate-groups:
              POST:
                summary: DisassociateSigninDelegateGroupsFromAccount
                description: >-
                  <p>Disassociates the specified sign-in delegate groups from
                  the specified Amazon Chime account.</p>
                tags:
                  - Disassociate
                  - Sign In
                  - Delegate
                  - Groups
                  - From
                  - Account
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - null
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - null
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
            /accounts/{accountId}/settings:
              PUT:
                summary: UpdateAccountSettings
                description: >-
                  <p>Updates the settings for the specified Amazon Chime
                  account. You can update settings for remote control of shared
                  screens, or for the dial-out option. For more information
                  about these settings, see <a
                  href="https://docs.aws.amazon.com/chime/latest/ag/policies.html">Use
                  the Policies Page</a> in the <i>Amazon Chime Administration
                  Guide</i>.</p>
                tags:
                  - Update
                  - Account
                  - Settings
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - null
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - null
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
            /app-instances/{appInstanceArn}/retention-settings:
              PUT:
                summary: PutAppInstanceRetentionSettings
                description: >-
                  <p>Sets the amount of time in days that a given
                  <code>AppInstance</code> retains data.</p> <important> <p>
                  <b>This API is is no longer supported and will not be
                  updated.</b> We recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_identity-chime_PutAppInstanceRetentionSettings.html">PutAppInstanceRetentionSettings</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Put
                  - Applications
                  - Instances
                  - Retention
                  - Settings
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - null
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - null
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
            /accounts/{accountId}/bots/{botId}:
              POST:
                summary: UpdateBot
                description: >-
                  <p>Updates the status of the specified bot, such as starting
                  or stopping the bot from running in your Amazon Chime
                  Enterprise account.</p>
                tags:
                  - Update
                  - Bot
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - null
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - null
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
            /settings:
              PUT:
                summary: UpdateGlobalSettings
                description: >-
                  <p>Updates global settings for the administrator's AWS
                  account, such as Amazon Chime Business Calling and Amazon
                  Chime Voice Connector settings.</p>
                tags:
                  - Update
                  - Global
                  - Settings
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - null
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - null
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
            /endpoints/messaging-session:
              GET:
                summary: GetMessagingSessionEndpoint
                description: >-
                  <p>The details of the endpoint for the messaging session.</p>
                  <important> <p> <b>This API is is no longer supported and will
                  not be updated.</b> We recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_messaging-chime_GetMessagingSessionEndpoint.html">GetMessagingSessionEndpoint</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Get
                  - Messaging
                  - Sessions
                  - Endpoints
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - null
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - null
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
            /phone-number-orders/{phoneNumberOrderId}:
              GET:
                summary: GetPhoneNumberOrder
                description: >-
                  <p>Retrieves details for the specified phone number order,
                  such as the order creation timestamp, phone numbers in E.164
                  format, product type, and order status.</p>
                tags:
                  - Get
                  - Phone
                  - Numbers
                  - Orders
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - null
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - null
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
            /settings/phone-number:
              PUT:
                summary: UpdatePhoneNumberSettings
                description: >-
                  <p>Updates the phone number settings for the administrator's
                  AWS account, such as the default outbound calling name. You
                  can update the default outbound calling name once every seven
                  days. Outbound calling names can take up to 72 hours to
                  update.</p>
                tags:
                  - Update
                  - Phone
                  - Numbers
                  - Settings
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - null
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - null
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
            /accounts/{accountId}/retention-settings:
              PUT:
                summary: PutRetentionSettings
                description: >-
                  <p> Puts retention settings for the specified Amazon Chime
                  Enterprise account. We recommend using AWS CloudTrail to
                  monitor usage of this API for your account. For more
                  information, see <a
                  href="https://docs.aws.amazon.com/chime/latest/ag/cloudtrail.html">Logging
                  Amazon Chime API Calls with AWS CloudTrail</a> in the
                  <i>Amazon Chime Administration Guide</i>.</p> <p> To turn off
                  existing retention settings, remove the number of days from
                  the corresponding <b>RetentionDays</b> field in the
                  <b>RetentionSettings</b> object. For more information about
                  retention settings, see <a
                  href="https://docs.aws.amazon.com/chime/latest/ag/chat-retention.html">Managing
                  Chat Retention Policies</a> in the <i>Amazon Chime
                  Administration Guide</i>.</p>
                tags:
                  - Put
                  - Retention
                  - Settings
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - null
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - null
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
            /sip-media-applications/{sipMediaApplicationId}/logging-configuration:
              PUT:
                summary: PutSipMediaApplicationLoggingConfiguration
                description: >-
                  <p>Updates the logging configuration for the specified SIP
                  media application.</p> <important> <p> <b>This API is is no
                  longer supported and will not be updated.</b> We recommend
                  using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_voice-chime_PutSipMediaApplicationLoggingConfiguration.html">PutSipMediaApplicationLoggingConfiguration</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Put
                  - SIP
                  - Media
                  - Applications
                  - Logging
                  - Configurations
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - null
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - null
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
            /accounts/{accountId}/users/{userId}:
              POST:
                summary: UpdateUser
                description: >-
                  <p>Updates user details for a specified user ID. Currently,
                  only <code>LicenseType</code> updates are supported for this
                  action.</p>
                tags:
                  - Update
                  - Users
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - null
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - null
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
            /accounts/{accountId}/users/{userId}/settings:
              PUT:
                summary: UpdateUserSettings
                description: >-
                  <p>Updates the settings for the specified user, such as phone
                  number settings.</p>
                tags:
                  - Update
                  - Users
                  - Settings
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - null
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - null
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
            /voice-connectors/{voiceConnectorId}/logging-configuration:
              PUT:
                summary: PutVoiceConnectorLoggingConfiguration
                description: >-
                  <p>Adds a logging configuration for the specified Amazon Chime
                  Voice Connector. The logging configuration specifies whether
                  SIP message logs are enabled for sending to Amazon CloudWatch
                  Logs.</p> <important> <p> <b>This API is is no longer
                  supported and will not be updated.</b> We recommend using the
                  latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_voice-chime_PutVoiceConnectorLoggingConfiguration.html">PutVoiceConnectorLoggingConfiguration</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Put
                  - null
                  - Connectors
                  - Logging
                  - Configurations
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - null
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - null
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
            /voice-connectors/{voiceConnectorId}/termination/health:
              GET:
                summary: GetVoiceConnectorTerminationHealth
                description: >-
                  <important> <p> <b>This API is is no longer supported and will
                  not be updated.</b> We recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_voice-chime_GetVoiceConnectorTerminationHealth.html">GetVoiceConnectorTerminationHealth</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important> <p>Retrieves information
                  about the last time a SIP <code>OPTIONS</code> ping was
                  received from your SIP infrastructure for the specified Amazon
                  Chime Voice Connector.</p>
                tags:
                  - Get
                  - null
                  - Connectors
                  - Termination
                  - Health
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - null
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - null
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
            /accounts/{accountId}/users?operation=add:
              POST:
                summary: InviteUsers
                description: >-
                  <p>Sends email to a maximum of 50 users, inviting them to the
                  specified Amazon Chime <code>Team</code> account. Only
                  <code>Team</code> account types are currently supported for
                  this action.</p>
                tags:
                  - Invite
                  - Users
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - null
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - null
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
                  - Users
            /meetings/{meetingId}/attendees/{attendeeId}/tags:
              GET:
                summary: ListAttendeeTags
                description: >-
                  <p>Lists the tags applied to an Amazon Chime SDK attendee
                  resource.</p> <important> <p>ListAttendeeTags is not supported
                  in the Amazon Chime SDK Meetings Namespace. Update your
                  application to remove calls to this API.</p> </important>
                tags:
                  - Lists
                  - Attendees
                  - Tags
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - null
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - null
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
                  - Users
                  - Tags
            /channels?scope=app-instance-user-memberships:
              GET:
                summary: ListChannelMembershipsForAppInstanceUser
                description: >-
                  <p> Lists all channels that a particular
                  <code>AppInstanceUser</code> is a part of. Only an
                  <code>AppInstanceAdmin</code> can call the API with a user ARN
                  that is not their own. </p> <note> <p>The
                  <code>x-amz-chime-bearer</code> request header is mandatory.
                  Use the <code>AppInstanceUserArn</code> of the user that makes
                  the API call as the value in the header.</p> </note>
                  <important> <p> <b>This API is is no longer supported and will
                  not be updated.</b> We recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_messaging-chime_ListChannelMembershipsForAppInstanceUser.html">ListChannelMembershipsForAppInstanceUser</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Lists
                  - Channels
                  - Memberships
                  - For
                  - Applications
                  - Instances
                  - Users
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - null
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - null
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
                  - Users
                  - Tags
                  - Channels
            /channels/{channelArn}/messages:
              POST:
                summary: SendChannelMessage
                description: >-
                  <p>Sends a message to a particular channel that the member is
                  a part of.</p> <note> <p>The <code>x-amz-chime-bearer</code>
                  request header is mandatory. Use the
                  <code>AppInstanceUserArn</code> of the user that makes the API
                  call as the value in the header.</p> <p>Also,
                  <code>STANDARD</code> messages can contain 4KB of data and the
                  1KB of metadata. <code>CONTROL</code> messages can contain 30
                  bytes of data and no metadata.</p> </note> <important> <p>
                  <b>This API is is no longer supported and will not be
                  updated.</b> We recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_messaging-chime_SendChannelMessage.html">SendChannelMessage</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Send
                  - Channels
                  - Messages
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - null
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - null
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
                  - Users
                  - Tags
                  - Channels
            /channels?scope=app-instance-user-moderated-channels:
              GET:
                summary: ListChannelsModeratedByAppInstanceUser
                description: >-
                  <p>A list of the channels moderated by an
                  <code>AppInstanceUser</code>.</p> <note> <p>The
                  <code>x-amz-chime-bearer</code> request header is mandatory.
                  Use the <code>AppInstanceUserArn</code> of the user that makes
                  the API call as the value in the header.</p> </note>
                  <important> <p> <b>This API is is no longer supported and will
                  not be updated.</b> We recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_messaging-chime_ListChannelsModeratedByAppInstanceUser.html">ListChannelsModeratedByAppInstanceUser</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Lists
                  - Channels
                  - Moderated
                  - By
                  - Applications
                  - Instances
                  - Users
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - null
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - null
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
                  - Users
                  - Tags
                  - Channels
            /meetings/{meetingId}/tags:
              GET:
                summary: ListMeetingTags
                description: >-
                  <p>Lists the tags applied to an Amazon Chime SDK meeting
                  resource.</p> <important> <p> <b>This API is is no longer
                  supported and will not be updated.</b> We recommend using the
                  latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_meeting-chime_ListTagsForResource.html">ListTagsForResource</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Lists
                  - Meetings
                  - Tags
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - null
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - null
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
                  - Users
                  - Tags
                  - Channels
            /phone-numbers:
              GET:
                summary: ListPhoneNumbers
                description: >-
                  <p>Lists the phone numbers for the specified Amazon Chime
                  account, Amazon Chime user, Amazon Chime Voice Connector, or
                  Amazon Chime Voice Connector group.</p>
                tags:
                  - Lists
                  - Phone
                  - Numbers
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - null
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - null
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
                  - Users
                  - Tags
                  - Channels
            /phone-number-countries:
              GET:
                summary: ListSupportedPhoneNumberCountries
                description: <p>Lists supported phone number countries.</p>
                tags:
                  - Lists
                  - Supported
                  - Phone
                  - Numbers
                  - Countries
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - null
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - null
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
                  - Users
                  - Tags
                  - Channels
                  - Countries
            /tags:
              GET:
                summary: ListTagsForResource
                description: >-
                  <p>Lists the tags applied to an Amazon Chime SDK meeting and
                  messaging resources.</p> <important> <p> <b>This API is is no
                  longer supported and will not be updated.</b> We recommend
                  using the applicable latest version in the Amazon Chime
                  SDK.</p> <ul> <li> <p>For meetings: <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_meeting-chime_ListTagsForResource.html">ListTagsForResource</a>.</p>
                  </li> <li> <p>For messaging: <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_messaging-chime_ListTagsForResource.html">ListTagsForResource</a>.</p>
                  </li> </ul> <p>Using the latest version requires migrating to
                  a dedicated namespace. For more information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Lists
                  - Tags
                  - For
                  - Resources
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - null
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - null
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
                  - Users
                  - Tags
                  - Channels
                  - Countries
            /voice-connectors/{voiceConnectorId}/termination/credentials:
              GET:
                summary: ListVoiceConnectorTerminationCredentials
                description: >-
                  <p>Lists the SIP credentials for the specified Amazon Chime
                  Voice Connector.</p> <important> <p> <b>This API is is no
                  longer supported and will not be updated.</b> We recommend
                  using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_voice-chime_ListVoiceConnectorTerminationCredentials.html">ListVoiceConnectorTerminationCredentials</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Lists
                  - null
                  - Connectors
                  - Termination
                  - Credentials
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - null
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - null
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
                  - Users
                  - Tags
                  - Channels
                  - Countries
                  - Credentials
            /accounts/{accountId}/users/{userId}?operation=logout:
              POST:
                summary: LogoutUser
                description: >-
                  <p>Logs out the specified user from all of the devices they
                  are currently logged into.</p>
                tags:
                  - Logout
                  - Users
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - null
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - null
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
                  - Users
                  - Tags
                  - Channels
                  - Countries
                  - Credentials
                  - '?operation=logout'
            /voice-connectors/{voiceConnectorId}/termination/credentials?operation=put:
              POST:
                summary: PutVoiceConnectorTerminationCredentials
                description: >-
                  <p>Adds termination SIP credentials for the specified Amazon
                  Chime Voice Connector.</p> <important> <p> <b>This API is is
                  no longer supported and will not be updated.</b> We recommend
                  using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_voice-chime_PutVoiceConnectorTerminationCredentials.html">PutVoiceConnectorTerminationCredentials</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Put
                  - null
                  - Connectors
                  - Termination
                  - Credentials
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - null
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - null
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
                  - Users
                  - Tags
                  - Channels
                  - Countries
                  - Credentials
                  - '?operation=logout'
                  - Credentials
            /channels/{channelArn}/messages/{messageId}?operation=redact:
              POST:
                summary: RedactChannelMessage
                description: >-
                  <p>Redacts message content, but not metadata. The message
                  exists in the back end, but the action returns null content,
                  and the state shows as redacted.</p> <note> <p>The
                  <code>x-amz-chime-bearer</code> request header is mandatory.
                  Use the <code>AppInstanceUserArn</code> of the user that makes
                  the API call as the value in the header.</p> </note>
                  <important> <p> <b>This API is is no longer supported and will
                  not be updated.</b> We recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_messaging-chime_RedactChannelMessage.html">RedactChannelMessage</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Redact
                  - Channels
                  - Messages
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - null
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - null
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
                  - Users
                  - Tags
                  - Channels
                  - Countries
                  - Credentials
                  - '?operation=logout'
                  - Credentials
                  - '?operation=redact'
            /accounts/{accountId}/conversations/{conversationId}/messages/{messageId}?operation=redact:
              POST:
                summary: RedactConversationMessage
                description: >-
                  <p>Redacts the specified message from the specified Amazon
                  Chime conversation.</p>
                tags:
                  - Redact
                  - Conversations
                  - Messages
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - null
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - null
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
                  - Users
                  - Tags
                  - Channels
                  - Countries
                  - Credentials
                  - '?operation=logout'
                  - Credentials
                  - '?operation=redact'
                  - Conversations
                  - Conversations
            /accounts/{accountId}/rooms/{roomId}/messages/{messageId}?operation=redact:
              POST:
                summary: RedactRoomMessage
                description: >-
                  <p>Redacts the specified message from the specified Amazon
                  Chime channel.</p>
                tags:
                  - Redact
                  - Rooms
                  - Messages
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - null
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - null
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
                  - Users
                  - Tags
                  - Channels
                  - Countries
                  - Credentials
                  - '?operation=logout'
                  - Credentials
                  - '?operation=redact'
                  - Conversations
                  - Conversations
            /accounts/{accountId}/bots/{botId}?operation=regenerate-security-token:
              POST:
                summary: RegenerateSecurityToken
                description: <p>Regenerates the security token for a bot.</p>
                tags:
                  - Regenerate
                  - Security
                  - Tokens
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - null
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - null
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
                  - Users
                  - Tags
                  - Channels
                  - Countries
                  - Credentials
                  - '?operation=logout'
                  - Credentials
                  - '?operation=redact'
                  - Conversations
                  - Conversations
                  - '?operation=regenerate'
                  - Security
                  - Tokens
            /accounts/{accountId}/users/{userId}?operation=reset-personal-pin:
              POST:
                summary: ResetPersonalPIN
                description: >-
                  <p>Resets the personal meeting PIN for the specified user on
                  an Amazon Chime account. Returns the <a>User</a> object with
                  the updated personal meeting PIN.</p>
                tags:
                  - Reset
                  - Personal
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - null
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - null
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
                  - Users
                  - Tags
                  - Channels
                  - Countries
                  - Credentials
                  - '?operation=logout'
                  - Credentials
                  - '?operation=redact'
                  - Conversations
                  - Conversations
                  - '?operation=regenerate'
                  - Security
                  - Tokens
                  - '?operation=reset'
                  - Personal
                  - Pin
            /phone-numbers/{phoneNumberId}?operation=restore:
              POST:
                summary: RestorePhoneNumber
                description: >-
                  <p>Moves a phone number from the <b>Deletion queue</b> back
                  into the phone number <b>Inventory</b>.</p>
                tags:
                  - Restore
                  - Phone
                  - Numbers
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - null
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - null
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
                  - Users
                  - Tags
                  - Channels
                  - Countries
                  - Credentials
                  - '?operation=logout'
                  - Credentials
                  - '?operation=redact'
                  - Conversations
                  - Conversations
                  - '?operation=regenerate'
                  - Security
                  - Tokens
                  - '?operation=reset'
                  - Personal
                  - Pin
                  - '?operation=restore'
            /search?type=phone-numbers:
              GET:
                summary: SearchAvailablePhoneNumbers
                description: >-
                  <p>Searches for phone numbers that can be ordered. For US
                  numbers, provide at least one of the following search filters:
                  <code>AreaCode</code>, <code>City</code>, <code>State</code>,
                  or <code>TollFreePrefix</code>. If you provide
                  <code>City</code>, you must also provide <code>State</code>.
                  Numbers outside the US only support the
                  <code>PhoneNumberType</code> filter, which you must use.</p>
                tags:
                  - Search
                  - Available
                  - Phone
                  - Numbers
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - null
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - null
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
                  - Users
                  - Tags
                  - Channels
                  - Countries
                  - Credentials
                  - '?operation=logout'
                  - Credentials
                  - '?operation=redact'
                  - Conversations
                  - Conversations
                  - '?operation=regenerate'
                  - Security
                  - Tokens
                  - '?operation=reset'
                  - Personal
                  - Pin
                  - '?operation=restore'
                  - Search
            /meetings/{meetingId}/transcription?operation=start:
              POST:
                summary: StartMeetingTranscription
                description: >-
                  <p>Starts transcription for the specified
                  <code>meetingId</code>. For more information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/meeting-transcription.html">
                  Using Amazon Chime SDK live transcription </a> in the
                  <i>Amazon Chime SDK Developer Guide</i>.</p> <p>If you specify
                  an invalid configuration, a <code>TranscriptFailed</code>
                  event will be sent with the contents of the
                  <code>BadRequestException</code> generated by Amazon
                  Transcribe. For more information on each parameter and which
                  combinations are valid, refer to the <a
                  href="https://docs.aws.amazon.com/transcribe/latest/APIReference/API_streaming_StartStreamTranscription.html">StartStreamTranscription</a>
                  API in the <i>Amazon Transcribe Developer Guide</i>.</p>
                  <note> <p>Amazon Chime SDK live transcription is powered by
                  Amazon Transcribe. Use of Amazon Transcribe is subject to the
                  <a href="https://aws.amazon.com/service-terms/">AWS Service
                  Terms</a>, including the terms specific to the AWS Machine
                  Learning and Artificial Intelligence Services.</p> </note>
                  <important> <p> <b>This API is is no longer supported and will
                  not be updated.</b> We recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_meeting-chime_StartMeetingTranscription.html">StartMeetingTranscription</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Start
                  - Meetings
                  - Transcriptions
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - null
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - null
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
                  - Users
                  - Tags
                  - Channels
                  - Countries
                  - Credentials
                  - '?operation=logout'
                  - Credentials
                  - '?operation=redact'
                  - Conversations
                  - Conversations
                  - '?operation=regenerate'
                  - Security
                  - Tokens
                  - '?operation=reset'
                  - Personal
                  - Pin
                  - '?operation=restore'
                  - Search
                  - Transcriptions
            /meetings/{meetingId}/transcription?operation=stop:
              POST:
                summary: StopMeetingTranscription
                description: >-
                  <p>Stops transcription for the specified
                  <code>meetingId</code>.</p> <important> <p> <b>This API is is
                  no longer supported and will not be updated.</b> We recommend
                  using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_meeting-chime_StopMeetingTranscription.html">StopMeetingTranscription</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Stop
                  - Meetings
                  - Transcriptions
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - null
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - null
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
                  - Users
                  - Tags
                  - Channels
                  - Countries
                  - Credentials
                  - '?operation=logout'
                  - Credentials
                  - '?operation=redact'
                  - Conversations
                  - Conversations
                  - '?operation=regenerate'
                  - Security
                  - Tokens
                  - '?operation=reset'
                  - Personal
                  - Pin
                  - '?operation=restore'
                  - Search
                  - Transcriptions
                  - Transcriptions
            /meetings/{meetingId}/attendees/{attendeeId}/tags?operation=add:
              POST:
                summary: TagAttendee
                description: >-
                  <p>Applies the specified tags to the specified Amazon Chime
                  attendee.</p> <important> <p>TagAttendee is not supported in
                  the Amazon Chime SDK Meetings Namespace. Update your
                  application to remove calls to this API.</p> </important>
                tags:
                  - Tags
                  - Attendees
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - null
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - null
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
                  - Users
                  - Tags
                  - Channels
                  - Countries
                  - Credentials
                  - '?operation=logout'
                  - Credentials
                  - '?operation=redact'
                  - Conversations
                  - Conversations
                  - '?operation=regenerate'
                  - Security
                  - Tokens
                  - '?operation=reset'
                  - Personal
                  - Pin
                  - '?operation=restore'
                  - Search
                  - Transcriptions
                  - Transcriptions
                  - Tags
            /meetings/{meetingId}/tags?operation=add:
              POST:
                summary: TagMeeting
                description: >-
                  <p>Applies the specified tags to the specified Amazon Chime
                  SDK meeting.</p> <important> <p> <b>This API is is no longer
                  supported and will not be updated.</b> We recommend using the
                  latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_meeting-chime_TagResource.html">TagResource</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Tags
                  - Meetings
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - null
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - null
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
                  - Users
                  - Tags
                  - Channels
                  - Countries
                  - Credentials
                  - '?operation=logout'
                  - Credentials
                  - '?operation=redact'
                  - Conversations
                  - Conversations
                  - '?operation=regenerate'
                  - Security
                  - Tokens
                  - '?operation=reset'
                  - Personal
                  - Pin
                  - '?operation=restore'
                  - Search
                  - Transcriptions
                  - Transcriptions
                  - Tags
            /tags?operation=tag-resource:
              POST:
                summary: TagResource
                description: >-
                  <p>Applies the specified tags to the specified Amazon Chime
                  SDK meeting resource.</p> <important> <p> <b>This API is is no
                  longer supported and will not be updated.</b> We recommend
                  using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_meeting-chime_TagResource.html">TagResource</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Tags
                  - Resources
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - null
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - null
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
                  - Users
                  - Tags
                  - Channels
                  - Countries
                  - Credentials
                  - '?operation=logout'
                  - Credentials
                  - '?operation=redact'
                  - Conversations
                  - Conversations
                  - '?operation=regenerate'
                  - Security
                  - Tokens
                  - '?operation=reset'
                  - Personal
                  - Pin
                  - '?operation=restore'
                  - Search
                  - Transcriptions
                  - Transcriptions
                  - Tags
                  - Tags
                  - Resources
            /meetings/{meetingId}/attendees/{attendeeId}/tags?operation=delete:
              POST:
                summary: UntagAttendee
                description: >-
                  <p>Untags the specified tags from the specified Amazon Chime
                  SDK attendee.</p> <important> <p>UntagAttendee is not
                  supported in the Amazon Chime SDK Meetings Namespace. Update
                  your application to remove calls to this API.</p> </important>
                tags:
                  - Untag
                  - Attendees
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - null
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - null
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
                  - Users
                  - Tags
                  - Channels
                  - Countries
                  - Credentials
                  - '?operation=logout'
                  - Credentials
                  - '?operation=redact'
                  - Conversations
                  - Conversations
                  - '?operation=regenerate'
                  - Security
                  - Tokens
                  - '?operation=reset'
                  - Personal
                  - Pin
                  - '?operation=restore'
                  - Search
                  - Transcriptions
                  - Transcriptions
                  - Tags
                  - Tags
                  - Resources
                  - Tags
            /meetings/{meetingId}/tags?operation=delete:
              POST:
                summary: UntagMeeting
                description: >-
                  <p>Untags the specified tags from the specified Amazon Chime
                  SDK meeting.</p> <important> <p> <b>This API is is no longer
                  supported and will not be updated.</b> We recommend using the
                  latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_meeting-chime_UntagResource.html">UntagResource</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Untag
                  - Meetings
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - null
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - null
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
                  - Users
                  - Tags
                  - Channels
                  - Countries
                  - Credentials
                  - '?operation=logout'
                  - Credentials
                  - '?operation=redact'
                  - Conversations
                  - Conversations
                  - '?operation=regenerate'
                  - Security
                  - Tokens
                  - '?operation=reset'
                  - Personal
                  - Pin
                  - '?operation=restore'
                  - Search
                  - Transcriptions
                  - Transcriptions
                  - Tags
                  - Tags
                  - Resources
                  - Tags
            /tags?operation=untag-resource:
              POST:
                summary: UntagResource
                description: >-
                  <p>Untags the specified tags from the specified Amazon Chime
                  SDK meeting resource.</p> <p>Applies the specified tags to the
                  specified Amazon Chime SDK meeting resource.</p> <important>
                  <p> <b>This API is is no longer supported and will not be
                  updated.</b> We recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_meeting-chime_UntagResource.html">UntagResource</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Untag
                  - Resources
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - null
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - null
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
                  - Users
                  - Tags
                  - Channels
                  - Countries
                  - Credentials
                  - '?operation=logout'
                  - Credentials
                  - '?operation=redact'
                  - Conversations
                  - Conversations
                  - '?operation=regenerate'
                  - Security
                  - Tokens
                  - '?operation=reset'
                  - Personal
                  - Pin
                  - '?operation=restore'
                  - Search
                  - Transcriptions
                  - Transcriptions
                  - Tags
                  - Tags
                  - Resources
                  - Tags
                  - Tags
            /channels/{channelArn}/readMarker:
              PUT:
                summary: UpdateChannelReadMarker
                description: >-
                  <p>The details of the time when a user last read messages in a
                  channel.</p> <note> <p>The <code>x-amz-chime-bearer</code>
                  request header is mandatory. Use the
                  <code>AppInstanceUserArn</code> of the user that makes the API
                  call as the value in the header.</p> </note> <important> <p>
                  <b>This API is is no longer supported and will not be
                  updated.</b> We recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_messaging-chime_UpdateChannelReadMarker.html">UpdateChannelReadMarker</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Update
                  - Channels
                  - Read
                  - Marker
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - null
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - null
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
                  - Users
                  - Tags
                  - Channels
                  - Countries
                  - Credentials
                  - '?operation=logout'
                  - Credentials
                  - '?operation=redact'
                  - Conversations
                  - Conversations
                  - '?operation=regenerate'
                  - Security
                  - Tokens
                  - '?operation=reset'
                  - Personal
                  - Pin
                  - '?operation=restore'
                  - Search
                  - Transcriptions
                  - Transcriptions
                  - Tags
                  - Tags
                  - Resources
                  - Tags
                  - Tags
                  - Read
                  - Marker
            /sip-media-applications/{sipMediaApplicationId}/calls/{transactionId}:
              POST:
                summary: UpdateSipMediaApplicationCall
                description: >-
                  <p>Invokes the AWS Lambda function associated with the SIP
                  media application and transaction ID in an update request. The
                  Lambda function can then return a new set of actions.</p>
                  <important> <p> <b>This API is is no longer supported and will
                  not be updated.</b> We recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_voice-chime_UpdateSipMediaApplicationCall.html">UpdateSipMediaApplicationCall</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Update
                  - SIP
                  - Media
                  - Applications
                  - Call
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - null
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - null
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
                  - Users
                  - Tags
                  - Channels
                  - Countries
                  - Credentials
                  - '?operation=logout'
                  - Credentials
                  - '?operation=redact'
                  - Conversations
                  - Conversations
                  - '?operation=regenerate'
                  - Security
                  - Tokens
                  - '?operation=reset'
                  - Personal
                  - Pin
                  - '?operation=restore'
                  - Search
                  - Transcriptions
                  - Transcriptions
                  - Tags
                  - Tags
                  - Resources
                  - Tags
                  - Tags
                  - Read
                  - Marker
                  - Transactions
            /emergency-calling/address:
              POST:
                summary: ValidateE911Address
                description: >-
                  <p>Validates an address to be used for 911 calls made with
                  Amazon Chime Voice Connectors. You can use validated addresses
                  in a Presence Information Data Format Location Object file
                  that you include in SIP requests. That helps ensure that
                  addresses are routed to the appropriate Public Safety
                  Answering Point.</p> <important> <p> <b>This API is is no
                  longer supported and will not be updated.</b> We recommend
                  using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_voice-chime_ValidateE911Address.html">ValidateE911Address</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </
                tags:
                  - Validate
                  - E911
                  - Addresses
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - null
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - null
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - null
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
                  - Users
                  - Tags
                  - Channels
                  - Countries
                  - Credentials
                  - '?operation=logout'
                  - Credentials
                  - '?operation=redact'
                  - Conversations
                  - Conversations
                  - '?operation=regenerate'
                  - Security
                  - Tokens
                  - '?operation=reset'
                  - Personal
                  - Pin
                  - '?operation=restore'
                  - Search
                  - Transcriptions
                  - Transcriptions
                  - Tags
                  - Tags
                  - Resources
                  - Tags
                  - Tags
                  - Read
                  - Marker
                  - Transactions
                  - Addresses''
    overlays:
      - type: APIs.io Search
        url: overlays/chime-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/chime-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:chime
  - name: chime-sdk-media-pipelines
    description: >-
      <p>The Amazon Chime SDK media pipeline APIs in this section allow software
      developers to create Amazon Chime SDK media pipelines that capture,
      concatenate, or stream your Amazon Chime SDK meetings. For more
      information about media pipelines, see <a
      href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_Operations_Amazon_Chime_SDK_Media_Pipelines.html">Amazon
      Chime SDK media pipelines</a>. </p>
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
            title: chime-sdk-media-pipelines
          paths:
            /sdk-media-capture-pipelines:
              GET:
                summary: ListMediaCapturePipelines
                description: <p>Returns a list of media pipelines.</p>
                tags:
                  - Lists
                  - Media
                  - Capture
                  - Pipelines
                  - SDKs
                  - Media
                  - Capture
                  - Pipelines
            /sdk-media-concatenation-pipelines:
              POST:
                summary: CreateMediaConcatenationPipeline
                description: <p>Creates a media concatenation pipeline.</p>
                tags:
                  - Create
                  - Media
                  - Concatenation
                  - Pipelines
                  - SDKs
                  - Media
                  - Capture
                  - Pipelines
                  - Concatenation
            /media-insights-pipelines:
              POST:
                summary: CreateMediaInsightsPipeline
                description: <p>Creates a media insights pipeline.</p>
                tags:
                  - Create
                  - Media
                  - Insights
                  - Pipelines
                  - SDKs
                  - Media
                  - Capture
                  - Pipelines
                  - Concatenation
                  - Insights
            /media-insights-pipeline-configurations:
              GET:
                summary: ListMediaInsightsPipelineConfigurations
                description: >-
                  <p>Lists the available media insights pipeline
                  configurations.</p>
                tags:
                  - Lists
                  - Media
                  - Insights
                  - Pipelines
                  - Configurations
                  - SDKs
                  - Media
                  - Capture
                  - Pipelines
                  - Concatenation
                  - Insights
                  - Pipelines
                  - Configurations
            /sdk-media-live-connector-pipelines:
              POST:
                summary: CreateMediaLiveConnectorPipeline
                description: >-
                  <p>Creates a media live connector pipeline in an Amazon Chime
                  SDK meeting.</p>
                tags:
                  - Create
                  - Media
                  - Live
                  - Connectors
                  - Pipelines
                  - SDKs
                  - Media
                  - Capture
                  - Pipelines
                  - Concatenation
                  - Insights
                  - Pipelines
                  - Configurations
                  - Live
                  - Connectors
            /media-pipeline-kinesis-video-stream-pools:
              GET:
                summary: ListMediaPipelineKinesisVideoStreamPools
                description: <p>Lists the video stream pools in the media pipeline.</p>
                tags:
                  - Lists
                  - Media
                  - Pipelines
                  - Kinesis
                  - Videos
                  - Stream
                  - Pools
                  - SDKs
                  - Media
                  - Capture
                  - Pipelines
                  - Concatenation
                  - Insights
                  - Pipelines
                  - Configurations
                  - Live
                  - Connectors
                  - Kinesis
                  - Videos
                  - Stream
                  - Pools
            /sdk-media-stream-pipelines:
              POST:
                summary: CreateMediaStreamPipeline
                description: <p>Creates a streaming media pipeline.</p>
                tags:
                  - Create
                  - Media
                  - Stream
                  - Pipelines
                  - SDKs
                  - Media
                  - Capture
                  - Pipelines
                  - Concatenation
                  - Insights
                  - Pipelines
                  - Configurations
                  - Live
                  - Connectors
                  - Kinesis
                  - Videos
                  - Stream
                  - Pools
            /sdk-media-capture-pipelines/{mediaPipelineId}:
              GET:
                summary: GetMediaCapturePipeline
                description: <p>Gets an existing media pipeline.</p>
                tags:
                  - Get
                  - Media
                  - Capture
                  - Pipelines
                  - SDKs
                  - Media
                  - Capture
                  - Pipelines
                  - Concatenation
                  - Insights
                  - Pipelines
                  - Configurations
                  - Live
                  - Connectors
                  - Kinesis
                  - Videos
                  - Stream
                  - Pools
                  - Identifiers
            /media-insights-pipeline-configurations/{identifier}:
              PUT:
                summary: UpdateMediaInsightsPipelineConfiguration
                description: >-
                  <p>Updates the media insights pipeline's configuration
                  settings.</p>
                tags:
                  - Update
                  - Media
                  - Insights
                  - Pipelines
                  - Configurations
                  - SDKs
                  - Media
                  - Capture
                  - Pipelines
                  - Concatenation
                  - Insights
                  - Pipelines
                  - Configurations
                  - Live
                  - Connectors
                  - Kinesis
                  - Videos
                  - Stream
                  - Pools
                  - Identifiers
                  - Identifiers
            /sdk-media-pipelines/{mediaPipelineId}:
              GET:
                summary: GetMediaPipeline
                description: <p>Gets an existing media pipeline.</p>
                tags:
                  - Get
                  - Media
                  - Pipelines
                  - SDKs
                  - Media
                  - Capture
                  - Pipelines
                  - Concatenation
                  - Insights
                  - Pipelines
                  - Configurations
                  - Live
                  - Connectors
                  - Kinesis
                  - Videos
                  - Stream
                  - Pools
                  - Identifiers
                  - Identifiers
            /media-pipeline-kinesis-video-stream-pools/{identifier}:
              PUT:
                summary: UpdateMediaPipelineKinesisVideoStreamPool
                description: >-
                  <p>Updates an Kinesis video stream pool in a media
                  pipeline.</p>
                tags:
                  - Update
                  - Media
                  - Pipelines
                  - Kinesis
                  - Videos
                  - Stream
                  - Pools
                  - SDKs
                  - Media
                  - Capture
                  - Pipelines
                  - Concatenation
                  - Insights
                  - Pipelines
                  - Configurations
                  - Live
                  - Connectors
                  - Kinesis
                  - Videos
                  - Stream
                  - Pools
                  - Identifiers
                  - Identifiers
            /media-insights-pipelines/{identifier}/speaker-search-tasks/{speakerSearchTaskId}:
              GET:
                summary: GetSpeakerSearchTask
                description: >-
                  <p>Retrieves the details of the specified speaker search
                  task.</p>
                tags:
                  - Get
                  - Speakers
                  - Search
                  - Tasks
                  - SDKs
                  - Media
                  - Capture
                  - Pipelines
                  - Concatenation
                  - Insights
                  - Pipelines
                  - Configurations
                  - Live
                  - Connectors
                  - Kinesis
                  - Videos
                  - Stream
                  - Pools
                  - Identifiers
                  - Identifiers
                  - Search
                  - Tasks
            /media-insights-pipelines/{identifier}/voice-tone-analysis-tasks/{voiceToneAnalysisTaskId}:
              GET:
                summary: GetVoiceToneAnalysisTask
                description: <p>Retrieves the details of a voice tone analysis task.</p>
                tags:
                  - Get
                  - null
                  - Tone
                  - Analysis
                  - Tasks
                  - SDKs
                  - Media
                  - Capture
                  - Pipelines
                  - Concatenation
                  - Insights
                  - Pipelines
                  - Configurations
                  - Live
                  - Connectors
                  - Kinesis
                  - Videos
                  - Stream
                  - Pools
                  - Identifiers
                  - Identifiers
                  - Search
                  - Tasks
                  - Tone
                  - Analysis
            /sdk-media-pipelines:
              GET:
                summary: ListMediaPipelines
                description: <p>Returns a list of media pipelines.</p>
                tags:
                  - Lists
                  - Media
                  - Pipelines
                  - SDKs
                  - Media
                  - Capture
                  - Pipelines
                  - Concatenation
                  - Insights
                  - Pipelines
                  - Configurations
                  - Live
                  - Connectors
                  - Kinesis
                  - Videos
                  - Stream
                  - Pools
                  - Identifiers
                  - Identifiers
                  - Search
                  - Tasks
                  - Tone
                  - Analysis
            /tags:
              GET:
                summary: ListTagsForResource
                description: <p>Lists the tags available for a media pipeline.</p>
                tags:
                  - Lists
                  - Tags
                  - For
                  - Resources
                  - SDKs
                  - Media
                  - Capture
                  - Pipelines
                  - Concatenation
                  - Insights
                  - Pipelines
                  - Configurations
                  - Live
                  - Connectors
                  - Kinesis
                  - Videos
                  - Stream
                  - Pools
                  - Identifiers
                  - Identifiers
                  - Search
                  - Tasks
                  - Tone
                  - Analysis
                  - Tags
            /media-insights-pipelines/{identifier}/speaker-search-tasks?operation=start:
              POST:
                summary: StartSpeakerSearchTask
                description: >-
                  <p>Starts a speaker search task.</p> <important> <p>Before
                  starting any speaker search tasks, you must provide all
                  notices and obtain all consents from the speaker as required
                  under applicable privacy and biometrics laws, and as required
                  under the <a href="https://aws.amazon.com/service-terms/">AWS
                  service terms</a> for the Amazon Chime SDK.</p> </important>
                tags:
                  - Start
                  - Speakers
                  - Search
                  - Tasks
                  - SDKs
                  - Media
                  - Capture
                  - Pipelines
                  - Concatenation
                  - Insights
                  - Pipelines
                  - Configurations
                  - Live
                  - Connectors
                  - Kinesis
                  - Videos
                  - Stream
                  - Pools
                  - Identifiers
                  - Identifiers
                  - Search
                  - Tasks
                  - Tone
                  - Analysis
                  - Tags
                  - Speakers
                  - Tasks
            /media-insights-pipelines/{identifier}/voice-tone-analysis-tasks?operation=start:
              POST:
                summary: StartVoiceToneAnalysisTask
                description: >-
                  <p>Starts a voice tone analysis task. For more information
                  about voice tone analysis, see <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/voice-analytics.html">Using
                  Amazon Chime SDK voice analytics</a> in the <i>Amazon Chime
                  SDK Developer Guide</i>.</p> <important> <p>Before starting
                  any voice tone analysis tasks, you must provide all notices
                  and obtain all consents from the speaker as required under
                  applicable privacy and biometrics laws, and as required under
                  the <a href="https://aws.amazon.com/service-terms/">AWS
                  service terms</a> for the Amazon Chime SDK.</p> </important>
                tags:
                  - Start
                  - null
                  - Tone
                  - Analysis
                  - Tasks
                  - SDKs
                  - Media
                  - Capture
                  - Pipelines
                  - Concatenation
                  - Insights
                  - Pipelines
                  - Configurations
                  - Live
                  - Connectors
                  - Kinesis
                  - Videos
                  - Stream
                  - Pools
                  - Identifiers
                  - Identifiers
                  - Search
                  - Tasks
                  - Tone
                  - Analysis
                  - Tags
                  - Speakers
                  - Tasks
                  - null
            /media-insights-pipelines/{identifier}/speaker-search-tasks/{speakerSearchTaskId}?operation=stop:
              POST:
                summary: StopSpeakerSearchTask
                description: <p>Stops a speaker search task.</p>
                tags:
                  - Stop
                  - Speakers
                  - Search
                  - Tasks
                  - SDKs
                  - Media
                  - Capture
                  - Pipelines
                  - Concatenation
                  - Insights
                  - Pipelines
                  - Configurations
                  - Live
                  - Connectors
                  - Kinesis
                  - Videos
                  - Stream
                  - Pools
                  - Identifiers
                  - Identifiers
                  - Search
                  - Tasks
                  - Tone
                  - Analysis
                  - Tags
                  - Speakers
                  - Tasks
                  - null
                  - '?operation=stop'
            /media-insights-pipelines/{identifier}/voice-tone-analysis-tasks/{voiceToneAnalysisTaskId}?operation=stop:
              POST:
                summary: StopVoiceToneAnalysisTask
                description: <p>Stops a voice tone analysis task.</p>
                tags:
                  - Stop
                  - null
                  - Tone
                  - Analysis
                  - Tasks
                  - SDKs
                  - Media
                  - Capture
                  - Pipelines
                  - Concatenation
                  - Insights
                  - Pipelines
                  - Configurations
                  - Live
                  - Connectors
                  - Kinesis
                  - Videos
                  - Stream
                  - Pools
                  - Identifiers
                  - Identifiers
                  - Search
                  - Tasks
                  - Tone
                  - Analysis
                  - Tags
                  - Speakers
                  - Tasks
                  - null
                  - '?operation=stop'
            /tags?operation=tag-resource:
              POST:
                summary: TagResource
                description: >-
                  <p>The ARN of the media pipeline that you want to tag.
                  Consists of the pipeline's endpoint region, resource ID, and
                  pipeline ID.</p>
                tags:
                  - Tags
                  - Resources
                  - SDKs
                  - Media
                  - Capture
                  - Pipelines
                  - Concatenation
                  - Insights
                  - Pipelines
                  - Configurations
                  - Live
                  - Connectors
                  - Kinesis
                  - Videos
                  - Stream
                  - Pools
                  - Identifiers
                  - Identifiers
                  - Search
                  - Tasks
                  - Tone
                  - Analysis
                  - Tags
                  - Speakers
                  - Tasks
                  - null
                  - '?operation=stop'
                  - Tags
                  - Resources
            /tags?operation=untag-resource:
              POST:
                summary: UntagResource
                description: <p>Removes any tags from a media pipeline.</p>
                tags:
                  - Untag
                  - Resources
                  - SDKs
                  - Media
                  - Capture
                  - Pipelines
                  - Concatenation
                  - Insights
                  - Pipelines
                  - Configurations
                  - Live
                  - Connectors
                  - Kinesis
                  - Videos
                  - Stream
                  - Pools
                  - Identifiers
                  - Identifiers
                  - Search
                  - Tasks
                  - Tone
                  - Analysis
                  - Tags
                  - Speakers
                  - Tasks
                  - null
                  - '?operation=stop'
                  - Tags
                  - Resources
                  - Tags
            /media-insights-pipeline-status/{identifier}:
              PUT:
                summary: UpdateMediaInsightsPipelineStatus
                description: <p>Updates the status of a media insights pip
                tags:
                  - Update
                  - Media
                  - Insights
                  - Pipelines
                  - Status
                  - SDKs
                  - Media
                  - Capture
                  - Pipelines
                  - Concatenation
                  - Insights
                  - Pipelines
                  - Configurations
                  - Live
                  - Connectors
                  - Kinesis
                  - Videos
                  - Stream
                  - Pools
                  - Identifiers
                  - Identifiers
                  - Search
                  - Tasks
                  - Tone
                  - Analysis
                  - Tags
                  - Speakers
                  - Tasks
                  - null
                  - '?operation=stop'
                  - Tags
                  - Resources
                  - Tags
                  - null
    overlays:
      - type: APIs.io Search
        url: overlays/chime-sdk-media-pipelines-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/chime-sdk-media-pipelines-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:chime-sdk-media-pipelines
  - name: chime-sdk-voice
    description: >-
      <p>The Amazon Chime SDK telephony APIs in this section enable developers
      to create PSTN calling solutions that use Amazon Chime SDK Voice
      Connectors, and Amazon Chime SDK SIP media applications. Developers can
      also order and manage phone numbers, create and manage Voice Connectors
      and SIP media applications, and run voice analytics.</p>
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
            title: chime-sdk-voice
          paths:
            /voice-connectors/{voiceConnectorId}?operation=associate-phone-numbers:
              POST:
                summary: AssociatePhoneNumbersWithVoiceConnector
                description: >-
                  <p>Associates phone numbers with the specified Amazon Chime
                  SDK Voice Connector.</p>
                tags:
                  - Associate
                  - Phone
                  - Numbers
                  - null
                  - null
                  - Connectors
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
            /voice-connector-groups/{voiceConnectorGroupId}?operation=associate-phone-numbers:
              POST:
                summary: AssociatePhoneNumbersWithVoiceConnectorGroup
                description: >-
                  <p>Associates phone numbers with the specified Amazon Chime
                  SDK Voice Connector group.</p>
                tags:
                  - Associate
                  - Phone
                  - Numbers
                  - null
                  - null
                  - Connectors
                  - Group
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
            /phone-numbers?operation=batch-delete:
              POST:
                summary: BatchDeletePhoneNumber
                description: >-
                  <p> Moves phone numbers into the <b>Deletion queue</b>. Phone
                  numbers must be disassociated from any users or Amazon Chime
                  SDK Voice Connectors before they can be deleted. </p> <p>
                  Phone numbers remain in the <b>Deletion queue</b> for 7 days
                  before they are deleted permanently. </p>
                tags:
                  - Batches
                  - Delete
                  - Phone
                  - Numbers
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
            /phone-numbers?operation=batch-update:
              POST:
                summary: BatchUpdatePhoneNumber
                description: <p>Updates one or more phone numbers.</p>
                tags:
                  - Batches
                  - Update
                  - Phone
                  - Numbers
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
            /phone-number-orders:
              GET:
                summary: ListPhoneNumberOrders
                description: >-
                  <p>Lists the phone numbers for an administrator's Amazon Chime
                  SDK account.</p>
                tags:
                  - Lists
                  - Phone
                  - Numbers
                  - Orders
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
            /voice-connectors/{voiceConnectorId}/proxy-sessions:
              GET:
                summary: ListProxySessions
                description: >-
                  <p>Lists the proxy sessions for the specified Amazon Chime SDK
                  Voice Connector.</p>
                tags:
                  - Lists
                  - Proxy
                  - Sessions
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
            /sip-media-applications:
              GET:
                summary: ListSipMediaApplications
                description: >-
                  <p>Lists the SIP media applications under the administrator's
                  AWS account.</p>
                tags:
                  - Lists
                  - SIP
                  - Media
                  - Applications
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
            /sip-media-applications/{sipMediaApplicationId}/calls:
              POST:
                summary: CreateSipMediaApplicationCall
                description: >-
                  <p>Creates an outbound call to a phone number from the phone
                  number specified in the request, and it invokes the endpoint
                  of the specified <code>sipMediaApplicationId</code>.</p>
                tags:
                  - Create
                  - SIP
                  - Media
                  - Applications
                  - Call
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
            /sip-rules:
              GET:
                summary: ListSipRules
                description: >-
                  <p>Lists the SIP rules under the administrator's AWS
                  account.</p>
                tags:
                  - Lists
                  - SIP
                  - Rules
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
            /voice-connectors:
              GET:
                summary: ListVoiceConnectors
                description: >-
                  <p>Lists the Amazon Chime SDK Voice Connectors in the
                  administrators AWS account.</p>
                tags:
                  - Lists
                  - null
                  - Connectors
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - null
                  - Connectors
            /voice-connector-groups:
              GET:
                summary: ListVoiceConnectorGroups
                description: >-
                  <p>Lists the Amazon Chime SDK Voice Connector groups in the
                  administrator's AWS account.</p>
                tags:
                  - Lists
                  - null
                  - Connectors
                  - Groups
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - null
                  - Connectors
                  - Groups
            /voice-profiles:
              GET:
                summary: ListVoiceProfiles
                description: <p>Lists the voice profiles in a voice profile domain.</p>
                tags:
                  - Lists
                  - null
                  - Profiles
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - null
                  - Connectors
                  - Groups
                  - Profiles
            /voice-profile-domains:
              GET:
                summary: ListVoiceProfileDomains
                description: >-
                  <p>Lists the specified voice profile domains in the
                  administrator's AWS account. </p>
                tags:
                  - Lists
                  - null
                  - Profiles
                  - Domains
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - null
                  - Connectors
                  - Groups
                  - Profiles
                  - Profiles
                  - Domains
            /phone-numbers/{phoneNumberId}:
              POST:
                summary: UpdatePhoneNumber
                description: >-
                  <p>Updates phone number details, such as product type or
                  calling name, for the specified phone number ID. You can
                  update one phone number detail at a time. For example, you can
                  update either the product type or the calling name in one
                  action.</p> <p>For numbers outside the U.S., you must use the
                  Amazon Chime SDK SIP Media Application Dial-In product
                  type.</p> <p>Updates to outbound calling names can take 72
                  hours to complete. Pending updates to outbound calling names
                  must be complete before you can request another update.</p>
                tags:
                  - Update
                  - Phone
                  - Numbers
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - null
                  - Connectors
                  - Groups
                  - Profiles
                  - Profiles
                  - Domains
            /voice-connectors/{voiceConnectorId}/proxy-sessions/{proxySessionId}:
              POST:
                summary: UpdateProxySession
                description: >-
                  <p>Updates the specified proxy session details, such as voice
                  or SMS capabilities.</p>
                tags:
                  - Update
                  - Proxy
                  - Sessions
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - null
                  - Connectors
                  - Groups
                  - Profiles
                  - Profiles
                  - Domains
                  - Sessions
            /sip-media-applications/{sipMediaApplicationId}:
              PUT:
                summary: UpdateSipMediaApplication
                description: >-
                  <p>Updates the details of the specified SIP media
                  application.</p>
                tags:
                  - Update
                  - SIP
                  - Media
                  - Applications
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - null
                  - Connectors
                  - Groups
                  - Profiles
                  - Profiles
                  - Domains
                  - Sessions
            /sip-rules/{sipRuleId}:
              PUT:
                summary: UpdateSipRule
                description: <p>Updates the details of the specified SIP rule.</p>
                tags:
                  - Update
                  - SIP
                  - Rules
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - null
                  - Connectors
                  - Groups
                  - Profiles
                  - Profiles
                  - Domains
                  - Sessions
                  - Rules
            /voice-connectors/{voiceConnectorId}:
              PUT:
                summary: UpdateVoiceConnector
                description: >-
                  <p>Updates the details for the specified Amazon Chime SDK
                  Voice Connector.</p>
                tags:
                  - Update
                  - null
                  - Connectors
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - null
                  - Connectors
                  - Groups
                  - Profiles
                  - Profiles
                  - Domains
                  - Sessions
                  - Rules
            /voice-connectors/{voiceConnectorId}/emergency-calling-configuration:
              PUT:
                summary: PutVoiceConnectorEmergencyCallingConfiguration
                description: >-
                  <p>Updates a Voice Connector's emergency calling
                  configuration.</p>
                tags:
                  - Put
                  - null
                  - Connectors
                  - Emergency
                  - Calling
                  - Configurations
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - null
                  - Connectors
                  - Groups
                  - Profiles
                  - Profiles
                  - Domains
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Configurations
            /voice-connector-groups/{voiceConnectorGroupId}:
              PUT:
                summary: UpdateVoiceConnectorGroup
                description: >-
                  <p>Updates the settings for the specified Amazon Chime SDK
                  Voice Connector group.</p>
                tags:
                  - Update
                  - null
                  - Connectors
                  - Group
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - null
                  - Connectors
                  - Groups
                  - Profiles
                  - Profiles
                  - Domains
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Configurations
            /voice-connectors/{voiceConnectorId}/origination:
              PUT:
                summary: PutVoiceConnectorOrigination
                description: <p>Updates a Voice Connector's origination settings.</p>
                tags:
                  - Put
                  - null
                  - Connectors
                  - Origination
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - null
                  - Connectors
                  - Groups
                  - Profiles
                  - Profiles
                  - Domains
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Configurations
                  - Origination
            /voice-connectors/{voiceConnectorId}/programmable-numbers/proxy:
              PUT:
                summary: PutVoiceConnectorProxy
                description: >-
                  <p>Puts the specified proxy configuration to the specified
                  Amazon Chime SDK Voice Connector.</p>
                tags:
                  - Put
                  - null
                  - Connectors
                  - Proxy
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - null
                  - Connectors
                  - Groups
                  - Profiles
                  - Profiles
                  - Domains
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Configurations
                  - Origination
                  - Programmable
            /voice-connectors/{voiceConnectorId}/streaming-configuration:
              PUT:
                summary: PutVoiceConnectorStreamingConfiguration
                description: >-
                  <p>Updates a Voice Connector's streaming configuration
                  settings.</p>
                tags:
                  - Put
                  - null
                  - Connectors
                  - Streaming
                  - Configurations
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - null
                  - Connectors
                  - Groups
                  - Profiles
                  - Profiles
                  - Domains
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Configurations
                  - Origination
                  - Programmable
                  - Streaming
            /voice-connectors/{voiceConnectorId}/termination:
              PUT:
                summary: PutVoiceConnectorTermination
                description: <p>Updates a Voice Connector's termination settings.</p>
                tags:
                  - Put
                  - null
                  - Connectors
                  - Termination
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - null
                  - Connectors
                  - Groups
                  - Profiles
                  - Profiles
                  - Domains
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Configurations
                  - Origination
                  - Programmable
                  - Streaming
                  - Termination
            /voice-connectors/{voiceConnectorId}/termination/credentials?operation=delete:
              POST:
                summary: DeleteVoiceConnectorTerminationCredentials
                description: >-
                  <p>Deletes the specified SIP credentials used by your
                  equipment to authenticate during call termination.</p>
                tags:
                  - Delete
                  - null
                  - Connectors
                  - Termination
                  - Credentials
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - null
                  - Connectors
                  - Groups
                  - Profiles
                  - Profiles
                  - Domains
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Configurations
                  - Origination
                  - Programmable
                  - Streaming
                  - Termination
                  - Credentials
            /voice-profiles/{VoiceProfileId}:
              PUT:
                summary: UpdateVoiceProfile
                description: >-
                  <p>Updates the specified voice profile’s voice print and
                  refreshes its expiration timestamp.</p> <important> <p>As a
                  condition of using this feature, you acknowledge that the
                  collection, use, storage, and retention of your caller’s
                  biometric identifiers and biometric information (“biometric
                  data”) in the form of a digital voiceprint requires the
                  caller’s informed consent via a written release. Such consent
                  is required under various state laws, including biometrics
                  laws in Illinois, Texas, Washington and other state privacy
                  laws.</p> <p>You must provide a written release to each caller
                  through a process that clearly reflects each caller’s informed
                  consent before using Amazon Chime SDK Voice Insights service,
                  as required under the terms of your agreement with AWS
                  governing your use of the service.</p> </important>
                tags:
                  - Update
                  - null
                  - Profiles
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - null
                  - Connectors
                  - Groups
                  - Profiles
                  - Profiles
                  - Domains
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Configurations
                  - Origination
                  - Programmable
                  - Streaming
                  - Termination
                  - Credentials
            /voice-profile-domains/{VoiceProfileDomainId}:
              PUT:
                summary: UpdateVoiceProfileDomain
                description: >-
                  <p>Updates the settings for the specified voice profile
                  domain.</p>
                tags:
                  - Update
                  - null
                  - Profiles
                  - Domains
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - null
                  - Connectors
                  - Groups
                  - Profiles
                  - Profiles
                  - Domains
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Configurations
                  - Origination
                  - Programmable
                  - Streaming
                  - Termination
                  - Credentials
                  - Domains
            /voice-connectors/{voiceConnectorId}?operation=disassociate-phone-numbers:
              POST:
                summary: DisassociatePhoneNumbersFromVoiceConnector
                description: >-
                  <p>Disassociates the specified phone numbers from the
                  specified Amazon Chime SDK Voice Connector.</p>
                tags:
                  - Disassociate
                  - Phone
                  - Numbers
                  - From
                  - null
                  - Connectors
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - null
                  - Connectors
                  - Groups
                  - Profiles
                  - Profiles
                  - Domains
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Configurations
                  - Origination
                  - Programmable
                  - Streaming
                  - Termination
                  - Credentials
                  - Domains
                  - '?operation=disassociate'
            /voice-connector-groups/{voiceConnectorGroupId}?operation=disassociate-phone-numbers:
              POST:
                summary: DisassociatePhoneNumbersFromVoiceConnectorGroup
                description: >-
                  <p>Disassociates the specified phone numbers from the
                  specified Amazon Chime SDK Voice Connector group.</p>
                tags:
                  - Disassociate
                  - Phone
                  - Numbers
                  - From
                  - null
                  - Connectors
                  - Group
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - null
                  - Connectors
                  - Groups
                  - Profiles
                  - Profiles
                  - Domains
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Configurations
                  - Origination
                  - Programmable
                  - Streaming
                  - Termination
                  - Credentials
                  - Domains
                  - '?operation=disassociate'
            /settings:
              PUT:
                summary: UpdateGlobalSettings
                description: >-
                  <p>Updates global settings for the Amazon Chime SDK Voice
                  Connectors in an AWS account.</p>
                tags:
                  - Update
                  - Global
                  - Settings
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - null
                  - Connectors
                  - Groups
                  - Profiles
                  - Profiles
                  - Domains
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Configurations
                  - Origination
                  - Programmable
                  - Streaming
                  - Termination
                  - Credentials
                  - Domains
                  - '?operation=disassociate'
                  - Settings
            /phone-number-orders/{phoneNumberOrderId}:
              GET:
                summary: GetPhoneNumberOrder
                description: >-
                  <p>Retrieves details for the specified phone number order,
                  such as the order creation timestamp, phone numbers in E.164
                  format, product type, and order status.</p>
                tags:
                  - Get
                  - Phone
                  - Numbers
                  - Orders
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - null
                  - Connectors
                  - Groups
                  - Profiles
                  - Profiles
                  - Domains
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Configurations
                  - Origination
                  - Programmable
                  - Streaming
                  - Termination
                  - Credentials
                  - Domains
                  - '?operation=disassociate'
                  - Settings
                  - Orders
            /settings/phone-number:
              PUT:
                summary: UpdatePhoneNumberSettings
                description: >-
                  <p>Updates the phone number settings for the administrator's
                  AWS account, such as the default outbound calling name. You
                  can update the default outbound calling name once every seven
                  days. Outbound calling names can take up to 72 hours to
                  update.</p>
                tags:
                  - Update
                  - Phone
                  - Numbers
                  - Settings
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - null
                  - Connectors
                  - Groups
                  - Profiles
                  - Profiles
                  - Domains
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Configurations
                  - Origination
                  - Programmable
                  - Streaming
                  - Termination
                  - Credentials
                  - Domains
                  - '?operation=disassociate'
                  - Settings
                  - Orders
            /sip-media-applications/{sipMediaApplicationId}/alexa-skill-configuration:
              PUT:
                summary: PutSipMediaApplicationAlexaSkillConfiguration
                description: >-
                  <p>Updates the Alexa Skill configuration for the SIP media
                  application.</p>
                tags:
                  - Put
                  - SIP
                  - Media
                  - Applications
                  - Alexa
                  - Skills
                  - Configurations
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - null
                  - Connectors
                  - Groups
                  - Profiles
                  - Profiles
                  - Domains
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Configurations
                  - Origination
                  - Programmable
                  - Streaming
                  - Termination
                  - Credentials
                  - Domains
                  - '?operation=disassociate'
                  - Settings
                  - Orders
                  - Alexa
                  - Skills
            /sip-media-applications/{sipMediaApplicationId}/logging-configuration:
              PUT:
                summary: PutSipMediaApplicationLoggingConfiguration
                description: >-
                  <p>Updates the logging configuration for the specified SIP
                  media application.</p>
                tags:
                  - Put
                  - SIP
                  - Media
                  - Applications
                  - Logging
                  - Configurations
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - null
                  - Connectors
                  - Groups
                  - Profiles
                  - Profiles
                  - Domains
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Configurations
                  - Origination
                  - Programmable
                  - Streaming
                  - Termination
                  - Credentials
                  - Domains
                  - '?operation=disassociate'
                  - Settings
                  - Orders
                  - Alexa
                  - Skills
                  - Logging
            /voice-connectors/{VoiceConnectorId}/speaker-search-tasks/{SpeakerSearchTaskId}:
              GET:
                summary: GetSpeakerSearchTask
                description: >-
                  <p>Retrieves the details of the specified speaker search
                  task.</p>
                tags:
                  - Get
                  - Speakers
                  - Search
                  - Tasks
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - null
                  - Connectors
                  - Groups
                  - Profiles
                  - Profiles
                  - Domains
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Configurations
                  - Origination
                  - Programmable
                  - Streaming
                  - Termination
                  - Credentials
                  - Domains
                  - '?operation=disassociate'
                  - Settings
                  - Orders
                  - Alexa
                  - Skills
                  - Logging
                  - Speakers
                  - Search
                  - Tasks
                  - Tasks
            /voice-connectors/{voiceConnectorId}/logging-configuration:
              PUT:
                summary: PutVoiceConnectorLoggingConfiguration
                description: <p>Updates a Voice Connector's logging configuration.</p>
                tags:
                  - Put
                  - null
                  - Connectors
                  - Logging
                  - Configurations
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - null
                  - Connectors
                  - Groups
                  - Profiles
                  - Profiles
                  - Domains
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Configurations
                  - Origination
                  - Programmable
                  - Streaming
                  - Termination
                  - Credentials
                  - Domains
                  - '?operation=disassociate'
                  - Settings
                  - Orders
                  - Alexa
                  - Skills
                  - Logging
                  - Speakers
                  - Search
                  - Tasks
                  - Tasks
            /voice-connectors/{voiceConnectorId}/termination/health:
              GET:
                summary: GetVoiceConnectorTerminationHealth
                description: >-
                  <p>Retrieves information about the last time a <code>SIP
                  OPTIONS</code> ping was received from your SIP infrastructure
                  for the specified Amazon Chime SDK Voice Connector.</p>
                tags:
                  - Get
                  - null
                  - Connectors
                  - Termination
                  - Health
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - null
                  - Connectors
                  - Groups
                  - Profiles
                  - Profiles
                  - Domains
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Configurations
                  - Origination
                  - Programmable
                  - Streaming
                  - Termination
                  - Credentials
                  - Domains
                  - '?operation=disassociate'
                  - Settings
                  - Orders
                  - Alexa
                  - Skills
                  - Logging
                  - Speakers
                  - Search
                  - Tasks
                  - Tasks
                  - Health
            /voice-connectors/{VoiceConnectorId}/voice-tone-analysis-tasks/{VoiceToneAnalysisTaskId}:
              GET:
                summary: GetVoiceToneAnalysisTask
                description: <p>Retrieves the details of a voice tone analysis task.</p>
                tags:
                  - Get
                  - null
                  - Tone
                  - Analysis
                  - Tasks
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - null
                  - Connectors
                  - Groups
                  - Profiles
                  - Profiles
                  - Domains
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Configurations
                  - Origination
                  - Programmable
                  - Streaming
                  - Termination
                  - Credentials
                  - Domains
                  - '?operation=disassociate'
                  - Settings
                  - Orders
                  - Alexa
                  - Skills
                  - Logging
                  - Speakers
                  - Search
                  - Tasks
                  - Tasks
                  - Health
                  - Tone
                  - Analysis
            /voice-connector-regions:
              GET:
                summary: ListAvailableVoiceConnectorRegions
                description: >-
                  <p>Lists the available AWS Regions in which you can create an
                  Amazon Chime SDK Voice Connector.</p>
                tags:
                  - Lists
                  - Available
                  - null
                  - Connectors
                  - Regions
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - null
                  - Connectors
                  - Groups
                  - Profiles
                  - Profiles
                  - Domains
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Configurations
                  - Origination
                  - Programmable
                  - Streaming
                  - Termination
                  - Credentials
                  - Domains
                  - '?operation=disassociate'
                  - Settings
                  - Orders
                  - Alexa
                  - Skills
                  - Logging
                  - Speakers
                  - Search
                  - Tasks
                  - Tasks
                  - Health
                  - Tone
                  - Analysis
                  - Regions
            /phone-numbers:
              GET:
                summary: ListPhoneNumbers
                description: >-
                  <p>Lists the phone numbers for the specified Amazon Chime SDK
                  account, Amazon Chime SDK user, Amazon Chime SDK Voice
                  Connector, or Amazon Chime SDK Voice Connector group.</p>
                tags:
                  - Lists
                  - Phone
                  - Numbers
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - null
                  - Connectors
                  - Groups
                  - Profiles
                  - Profiles
                  - Domains
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Configurations
                  - Origination
                  - Programmable
                  - Streaming
                  - Termination
                  - Credentials
                  - Domains
                  - '?operation=disassociate'
                  - Settings
                  - Orders
                  - Alexa
                  - Skills
                  - Logging
                  - Speakers
                  - Search
                  - Tasks
                  - Tasks
                  - Health
                  - Tone
                  - Analysis
                  - Regions
            /phone-number-countries:
              GET:
                summary: ListSupportedPhoneNumberCountries
                description: >-
                  <p>Lists the countries that you can order phone numbers
                  from.</p>
                tags:
                  - Lists
                  - Supported
                  - Phone
                  - Numbers
                  - Countries
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - null
                  - Connectors
                  - Groups
                  - Profiles
                  - Profiles
                  - Domains
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Configurations
                  - Origination
                  - Programmable
                  - Streaming
                  - Termination
                  - Credentials
                  - Domains
                  - '?operation=disassociate'
                  - Settings
                  - Orders
                  - Alexa
                  - Skills
                  - Logging
                  - Speakers
                  - Search
                  - Tasks
                  - Tasks
                  - Health
                  - Tone
                  - Analysis
                  - Regions
                  - Countries
            /tags:
              GET:
                summary: ListTagsForResource
                description: <p>Returns a list of the tags in a given resource.</p>
                tags:
                  - Lists
                  - Tags
                  - For
                  - Resources
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - null
                  - Connectors
                  - Groups
                  - Profiles
                  - Profiles
                  - Domains
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Configurations
                  - Origination
                  - Programmable
                  - Streaming
                  - Termination
                  - Credentials
                  - Domains
                  - '?operation=disassociate'
                  - Settings
                  - Orders
                  - Alexa
                  - Skills
                  - Logging
                  - Speakers
                  - Search
                  - Tasks
                  - Tasks
                  - Health
                  - Tone
                  - Analysis
                  - Regions
                  - Countries
                  - Tags
            /voice-connectors/{voiceConnectorId}/termination/credentials:
              GET:
                summary: ListVoiceConnectorTerminationCredentials
                description: >-
                  <p>Lists the SIP credentials for the specified Amazon Chime
                  SDK Voice Connector.</p>
                tags:
                  - Lists
                  - null
                  - Connectors
                  - Termination
                  - Credentials
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - null
                  - Connectors
                  - Groups
                  - Profiles
                  - Profiles
                  - Domains
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Configurations
                  - Origination
                  - Programmable
                  - Streaming
                  - Termination
                  - Credentials
                  - Domains
                  - '?operation=disassociate'
                  - Settings
                  - Orders
                  - Alexa
                  - Skills
                  - Logging
                  - Speakers
                  - Search
                  - Tasks
                  - Tasks
                  - Health
                  - Tone
                  - Analysis
                  - Regions
                  - Countries
                  - Tags
                  - Credentials
            /voice-connectors/{voiceConnectorId}/termination/credentials?operation=put:
              POST:
                summary: PutVoiceConnectorTerminationCredentials
                description: <p>Updates a Voice Connector's termination credentials.</p>
                tags:
                  - Put
                  - null
                  - Connectors
                  - Termination
                  - Credentials
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - null
                  - Connectors
                  - Groups
                  - Profiles
                  - Profiles
                  - Domains
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Configurations
                  - Origination
                  - Programmable
                  - Streaming
                  - Termination
                  - Credentials
                  - Domains
                  - '?operation=disassociate'
                  - Settings
                  - Orders
                  - Alexa
                  - Skills
                  - Logging
                  - Speakers
                  - Search
                  - Tasks
                  - Tasks
                  - Health
                  - Tone
                  - Analysis
                  - Regions
                  - Countries
                  - Tags
                  - Credentials
                  - Credentials
            /phone-numbers/{phoneNumberId}?operation=restore:
              POST:
                summary: RestorePhoneNumber
                description: <p>Restores a deleted phone number.</p>
                tags:
                  - Restore
                  - Phone
                  - Numbers
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - null
                  - Connectors
                  - Groups
                  - Profiles
                  - Profiles
                  - Domains
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Configurations
                  - Origination
                  - Programmable
                  - Streaming
                  - Termination
                  - Credentials
                  - Domains
                  - '?operation=disassociate'
                  - Settings
                  - Orders
                  - Alexa
                  - Skills
                  - Logging
                  - Speakers
                  - Search
                  - Tasks
                  - Tasks
                  - Health
                  - Tone
                  - Analysis
                  - Regions
                  - Countries
                  - Tags
                  - Credentials
                  - Credentials
                  - '?operation=restore'
            /search?type=phone-numbers:
              GET:
                summary: SearchAvailablePhoneNumbers
                description: >-
                  <p>Searches the provisioned phone numbers in an
                  organization.</p>
                tags:
                  - Search
                  - Available
                  - Phone
                  - Numbers
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - null
                  - Connectors
                  - Groups
                  - Profiles
                  - Profiles
                  - Domains
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Configurations
                  - Origination
                  - Programmable
                  - Streaming
                  - Termination
                  - Credentials
                  - Domains
                  - '?operation=disassociate'
                  - Settings
                  - Orders
                  - Alexa
                  - Skills
                  - Logging
                  - Speakers
                  - Search
                  - Tasks
                  - Tasks
                  - Health
                  - Tone
                  - Analysis
                  - Regions
                  - Countries
                  - Tags
                  - Credentials
                  - Credentials
                  - '?operation=restore'
                  - Search
            /voice-connectors/{VoiceConnectorId}/speaker-search-tasks:
              POST:
                summary: StartSpeakerSearchTask
                description: >-
                  <p>Starts a speaker search task.</p> <important> <p>Before
                  starting any speaker search tasks, you must provide all
                  notices and obtain all consents from the speaker as required
                  under applicable privacy and biometrics laws, and as required
                  under the <a href="https://aws.amazon.com/service-terms/">AWS
                  service terms</a> for the Amazon Chime SDK.</p> </important>
                tags:
                  - Start
                  - Speakers
                  - Search
                  - Tasks
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - null
                  - Connectors
                  - Groups
                  - Profiles
                  - Profiles
                  - Domains
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Configurations
                  - Origination
                  - Programmable
                  - Streaming
                  - Termination
                  - Credentials
                  - Domains
                  - '?operation=disassociate'
                  - Settings
                  - Orders
                  - Alexa
                  - Skills
                  - Logging
                  - Speakers
                  - Search
                  - Tasks
                  - Tasks
                  - Health
                  - Tone
                  - Analysis
                  - Regions
                  - Countries
                  - Tags
                  - Credentials
                  - Credentials
                  - '?operation=restore'
                  - Search
            /voice-connectors/{VoiceConnectorId}/voice-tone-analysis-tasks:
              POST:
                summary: StartVoiceToneAnalysisTask
                description: >-
                  <p>Starts a voice tone analysis task. For more information
                  about voice tone analysis, see <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/pstn-voice-analytics.html">Using
                  Amazon Chime SDK voice analytics</a> in the <i>Amazon Chime
                  SDK Developer Guide</i>.</p> <important> <p>Before starting
                  any voice tone analysis tasks, you must provide all notices
                  and obtain all consents from the speaker as required under
                  applicable privacy and biometrics laws, and as required under
                  the <a href="https://aws.amazon.com/service-terms/">AWS
                  service terms</a> for the Amazon Chime SDK.</p> </important>
                tags:
                  - Start
                  - null
                  - Tone
                  - Analysis
                  - Tasks
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - null
                  - Connectors
                  - Groups
                  - Profiles
                  - Profiles
                  - Domains
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Configurations
                  - Origination
                  - Programmable
                  - Streaming
                  - Termination
                  - Credentials
                  - Domains
                  - '?operation=disassociate'
                  - Settings
                  - Orders
                  - Alexa
                  - Skills
                  - Logging
                  - Speakers
                  - Search
                  - Tasks
                  - Tasks
                  - Health
                  - Tone
                  - Analysis
                  - Regions
                  - Countries
                  - Tags
                  - Credentials
                  - Credentials
                  - '?operation=restore'
                  - Search
            /voice-connectors/{VoiceConnectorId}/speaker-search-tasks/{SpeakerSearchTaskId}?operation=stop:
              POST:
                summary: StopSpeakerSearchTask
                description: <p>Stops a speaker search task.</p>
                tags:
                  - Stop
                  - Speakers
                  - Search
                  - Tasks
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - null
                  - Connectors
                  - Groups
                  - Profiles
                  - Profiles
                  - Domains
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Configurations
                  - Origination
                  - Programmable
                  - Streaming
                  - Termination
                  - Credentials
                  - Domains
                  - '?operation=disassociate'
                  - Settings
                  - Orders
                  - Alexa
                  - Skills
                  - Logging
                  - Speakers
                  - Search
                  - Tasks
                  - Tasks
                  - Health
                  - Tone
                  - Analysis
                  - Regions
                  - Countries
                  - Tags
                  - Credentials
                  - Credentials
                  - '?operation=restore'
                  - Search
                  - '?operation=stop'
            /voice-connectors/{VoiceConnectorId}/voice-tone-analysis-tasks/{VoiceToneAnalysisTaskId}?operation=stop:
              POST:
                summary: StopVoiceToneAnalysisTask
                description: <p>Stops a voice tone analysis task.</p>
                tags:
                  - Stop
                  - null
                  - Tone
                  - Analysis
                  - Tasks
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - null
                  - Connectors
                  - Groups
                  - Profiles
                  - Profiles
                  - Domains
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Configurations
                  - Origination
                  - Programmable
                  - Streaming
                  - Termination
                  - Credentials
                  - Domains
                  - '?operation=disassociate'
                  - Settings
                  - Orders
                  - Alexa
                  - Skills
                  - Logging
                  - Speakers
                  - Search
                  - Tasks
                  - Tasks
                  - Health
                  - Tone
                  - Analysis
                  - Regions
                  - Countries
                  - Tags
                  - Credentials
                  - Credentials
                  - '?operation=restore'
                  - Search
                  - '?operation=stop'
            /tags?operation=tag-resource:
              POST:
                summary: TagResource
                description: <p>Adds a tag to the specified resource.</p>
                tags:
                  - Tags
                  - Resources
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - null
                  - Connectors
                  - Groups
                  - Profiles
                  - Profiles
                  - Domains
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Configurations
                  - Origination
                  - Programmable
                  - Streaming
                  - Termination
                  - Credentials
                  - Domains
                  - '?operation=disassociate'
                  - Settings
                  - Orders
                  - Alexa
                  - Skills
                  - Logging
                  - Speakers
                  - Search
                  - Tasks
                  - Tasks
                  - Health
                  - Tone
                  - Analysis
                  - Regions
                  - Countries
                  - Tags
                  - Credentials
                  - Credentials
                  - '?operation=restore'
                  - Search
                  - '?operation=stop'
                  - Tags
                  - Resources
            /tags?operation=untag-resource:
              POST:
                summary: UntagResource
                description: <p>Removes tags from a resource.</p>
                tags:
                  - Untag
                  - Resources
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - null
                  - Connectors
                  - Groups
                  - Profiles
                  - Profiles
                  - Domains
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Configurations
                  - Origination
                  - Programmable
                  - Streaming
                  - Termination
                  - Credentials
                  - Domains
                  - '?operation=disassociate'
                  - Settings
                  - Orders
                  - Alexa
                  - Skills
                  - Logging
                  - Speakers
                  - Search
                  - Tasks
                  - Tasks
                  - Health
                  - Tone
                  - Analysis
                  - Regions
                  - Countries
                  - Tags
                  - Credentials
                  - Credentials
                  - '?operation=restore'
                  - Search
                  - '?operation=stop'
                  - Tags
                  - Resources
                  - Tags
            /sip-media-applications/{sipMediaApplicationId}/calls/{transactionId}:
              POST:
                summary: UpdateSipMediaApplicationCall
                description: >-
                  <p>Invokes the AWS Lambda function associated with the SIP
                  media application and transaction ID in an update request. The
                  Lambda function can then return a new set of actions.</p>
                tags:
                  - Update
                  - SIP
                  - Media
                  - Applications
                  - Call
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - null
                  - Connectors
                  - Groups
                  - Profiles
                  - Profiles
                  - Domains
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Configurations
                  - Origination
                  - Programmable
                  - Streaming
                  - Termination
                  - Credentials
                  - Domains
                  - '?operation=disassociate'
                  - Settings
                  - Orders
                  - Alexa
                  - Skills
                  - Logging
                  - Speakers
                  - Search
                  - Tasks
                  - Tasks
                  - Health
                  - Tone
                  - Analysis
                  - Regions
                  - Countries
                  - Tags
                  - Credentials
                  - Credentials
                  - '?operation=restore'
                  - Search
                  - '?operation=stop'
                  - Tags
                  - Resources
                  - Tags
                  - Transactions
            /emergency-calling/address:
              POST:
                summary: ValidateE911Address
                description: >-
                  <p>Validates an address to be used for 911 calls made with
                  Amazon Chime SDK Voice Connectors. You can use validated
                  addresses in a Presence Information Data Format Location
                  Object file that you include in SIP requests. That helps
                  ensure that addresses are routed to the appropriate Public
                  Safety Answering 
                tags:
                  - Validate
                  - E911
                  - Addresses
                  - Connectors
                  - Identifiers
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Group
                  - Numbers?operation=batch
                  - Delete
                  - Update
                  - Numbers
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Media
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - null
                  - Connectors
                  - Groups
                  - Profiles
                  - Profiles
                  - Domains
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Configurations
                  - Origination
                  - Programmable
                  - Streaming
                  - Termination
                  - Credentials
                  - Domains
                  - '?operation=disassociate'
                  - Settings
                  - Orders
                  - Alexa
                  - Skills
                  - Logging
                  - Speakers
                  - Search
                  - Tasks
                  - Tasks
                  - Health
                  - Tone
                  - Analysis
                  - Regions
                  - Countries
                  - Tags
                  - Credentials
                  - Credentials
                  - '?operation=restore'
                  - Search
                  - '?operation=stop'
                  - Tags
                  - Resources
                  - Tags
                  - Transactions
                  - Addresses''
    overlays:
      - type: APIs.io Search
        url: overlays/chime-sdk-voice-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/chime-sdk-voice-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:chime-sdk-voice
  - name: greengrass
    description: >-
      AWS IoT Greengrass seamlessly extends AWS onto physical devices so they
      can act locally on the data they generate, while still using the cloud for
      management, analytics, and durable storage. AWS IoT Greengrass ensures
      your devices can respond quickly to local events and operate with
      intermittent connectivity. AWS IoT Greengrass minimizes the cost of
      transmitting data to the cloud by allowing you to author AWS Lambda
      functions that execute locally.
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
            title: greengrass
          paths:
            /greengrass/groups/{GroupId}/role:
              GET:
                summary: GetAssociatedRole
                description: Retrieves the role associated with a particular group.
                tags:
                  - Get
                  - Associated
                  - Roles
                  - Group
                  - Identifiers
                  - Roles
            /greengrass/servicerole:
              GET:
                summary: GetServiceRoleForAccount
                description: Retrieves the service role that is attached to your account.
                tags:
                  - Get
                  - Services
                  - Roles
                  - For
                  - Account
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
            /greengrass/definition/connectors:
              GET:
                summary: ListConnectorDefinitions
                description: Retrieves a list of connector definitions.
                tags:
                  - Lists
                  - Connectors
                  - Definitions
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
            /greengrass/definition/connectors/{ConnectorDefinitionId}/versions:
              GET:
                summary: ListConnectorDefinitionVersions
                description: >-
                  Lists the versions of a connector definition, which are
                  containers for connectors. Connectors run on the Greengrass
                  core and contain built-in integration with local
                  infrastructure, device protocols, AWS, and other cloud
                  services.
                tags:
                  - Lists
                  - Connectors
                  - Definitions
                  - Versions
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
            /greengrass/definition/cores:
              GET:
                summary: ListCoreDefinitions
                description: Retrieves a list of core definitions.
                tags:
                  - Lists
                  - Core
                  - Definitions
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
            /greengrass/definition/cores/{CoreDefinitionId}/versions:
              GET:
                summary: ListCoreDefinitionVersions
                description: Lists the versions of a core definition.
                tags:
                  - Lists
                  - Core
                  - Definitions
                  - Versions
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
            /greengrass/groups/{GroupId}/deployments:
              GET:
                summary: ListDeployments
                description: Returns a history of deployments for the group.
                tags:
                  - Lists
                  - Deployments
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
            /greengrass/definition/devices:
              GET:
                summary: ListDeviceDefinitions
                description: Retrieves a list of device definitions.
                tags:
                  - Lists
                  - Device
                  - Definitions
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
            /greengrass/definition/devices/{DeviceDefinitionId}/versions:
              GET:
                summary: ListDeviceDefinitionVersions
                description: Lists the versions of a device definition.
                tags:
                  - Lists
                  - Device
                  - Definitions
                  - Versions
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
            /greengrass/definition/functions:
              GET:
                summary: ListFunctionDefinitions
                description: Retrieves a list of Lambda function definitions.
                tags:
                  - Lists
                  - Functions
                  - Definitions
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
            /greengrass/definition/functions/{FunctionDefinitionId}/versions:
              GET:
                summary: ListFunctionDefinitionVersions
                description: Lists the versions of a Lambda function definition.
                tags:
                  - Lists
                  - Functions
                  - Definitions
                  - Versions
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
            /greengrass/groups:
              GET:
                summary: ListGroups
                description: Retrieves a list of groups.
                tags:
                  - Lists
                  - Groups
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
            /greengrass/groups/{GroupId}/certificateauthorities:
              GET:
                summary: ListGroupCertificateAuthorities
                description: Retrieves the current CAs for a group.
                tags:
                  - Lists
                  - Group
                  - Certificates
                  - Authorities
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
            /greengrass/groups/{GroupId}/versions:
              GET:
                summary: ListGroupVersions
                description: Lists the versions of a group.
                tags:
                  - Lists
                  - Group
                  - Versions
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
            /greengrass/definition/loggers:
              GET:
                summary: ListLoggerDefinitions
                description: Retrieves a list of logger definitions.
                tags:
                  - Lists
                  - Loggers
                  - Definitions
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
            /greengrass/definition/loggers/{LoggerDefinitionId}/versions:
              GET:
                summary: ListLoggerDefinitionVersions
                description: Lists the versions of a logger definition.
                tags:
                  - Lists
                  - Loggers
                  - Definitions
                  - Versions
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
            /greengrass/definition/resources:
              GET:
                summary: ListResourceDefinitions
                description: Retrieves a list of resource definitions.
                tags:
                  - Lists
                  - Resources
                  - Definitions
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
            /greengrass/definition/resources/{ResourceDefinitionId}/versions:
              GET:
                summary: ListResourceDefinitionVersions
                description: Lists the versions of a resource definition.
                tags:
                  - Lists
                  - Resources
                  - Definitions
                  - Versions
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
            /greengrass/updates:
              POST:
                summary: CreateSoftwareUpdateJob
                description: >-
                  Creates a software update for a core or group of cores
                  (specified as an IoT thing group.) Use this to update the OTA
                  Agent as well as the Greengrass core software. It makes use of
                  the IoT Jobs feature which provides additional commands to
                  manage a Greengrass core software update job.
                tags:
                  - Create
                  - Software
                  - Update
                  - Jobs
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
                  - Updates
            /greengrass/definition/subscriptions:
              GET:
                summary: ListSubscriptionDefinitions
                description: Retrieves a list of subscription definitions.
                tags:
                  - Lists
                  - Subscriptions
                  - Definitions
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
                  - Updates
                  - Subscriptions
            /greengrass/definition/subscriptions/{SubscriptionDefinitionId}/versions:
              GET:
                summary: ListSubscriptionDefinitionVersions
                description: Lists the versions of a subscription definition.
                tags:
                  - Lists
                  - Subscriptions
                  - Definitions
                  - Versions
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
                  - Updates
                  - Subscriptions
                  - Subscriptions
            /greengrass/definition/connectors/{ConnectorDefinitionId}:
              PUT:
                summary: UpdateConnectorDefinition
                description: Updates a connector definition.
                tags:
                  - Update
                  - Connectors
                  - Definitions
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
                  - Updates
                  - Subscriptions
                  - Subscriptions
            /greengrass/definition/cores/{CoreDefinitionId}:
              PUT:
                summary: UpdateCoreDefinition
                description: Updates a core definition.
                tags:
                  - Update
                  - Core
                  - Definitions
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
                  - Updates
                  - Subscriptions
                  - Subscriptions
            /greengrass/definition/devices/{DeviceDefinitionId}:
              PUT:
                summary: UpdateDeviceDefinition
                description: Updates a device definition.
                tags:
                  - Update
                  - Device
                  - Definitions
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
                  - Updates
                  - Subscriptions
                  - Subscriptions
            /greengrass/definition/functions/{FunctionDefinitionId}:
              PUT:
                summary: UpdateFunctionDefinition
                description: Updates a Lambda function definition.
                tags:
                  - Update
                  - Functions
                  - Definitions
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
                  - Updates
                  - Subscriptions
                  - Subscriptions
            /greengrass/groups/{GroupId}:
              PUT:
                summary: UpdateGroup
                description: Updates a group.
                tags:
                  - Update
                  - Group
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
                  - Updates
                  - Subscriptions
                  - Subscriptions
            /greengrass/definition/loggers/{LoggerDefinitionId}:
              PUT:
                summary: UpdateLoggerDefinition
                description: Updates a logger definition.
                tags:
                  - Update
                  - Loggers
                  - Definitions
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
                  - Updates
                  - Subscriptions
                  - Subscriptions
            /greengrass/definition/resources/{ResourceDefinitionId}:
              PUT:
                summary: UpdateResourceDefinition
                description: Updates a resource definition.
                tags:
                  - Update
                  - Resources
                  - Definitions
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
                  - Updates
                  - Subscriptions
                  - Subscriptions
            /greengrass/definition/subscriptions/{SubscriptionDefinitionId}:
              PUT:
                summary: UpdateSubscriptionDefinition
                description: Updates a subscription definition.
                tags:
                  - Update
                  - Subscriptions
                  - Definitions
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
                  - Updates
                  - Subscriptions
                  - Subscriptions
            /greengrass/bulk/deployments/{BulkDeploymentId}/status:
              GET:
                summary: GetBulkDeploymentStatus
                description: Returns the status of a bulk deployment.
                tags:
                  - Get
                  - Bulk
                  - Deployments
                  - Status
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
                  - Updates
                  - Subscriptions
                  - Subscriptions
                  - Bulk
                  - Deployments
                  - Status
            /greengrass/things/{ThingName}/connectivityInfo:
              PUT:
                summary: UpdateConnectivityInfo
                description: >-
                  Updates the connectivity information for the core. Any devices
                  that belong to the group which has this core will receive this
                  information in order to find the location of the core and
                  connect to it.
                tags:
                  - Update
                  - Connectivity
                  - Info
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
                  - Updates
                  - Subscriptions
                  - Subscriptions
                  - Bulk
                  - Deployments
                  - Status
                  - Things
                  - Names
                  - Connectivity
                  - Info
            /greengrass/definition/connectors/{ConnectorDefinitionId}/versions/{ConnectorDefinitionVersionId}:
              GET:
                summary: GetConnectorDefinitionVersion
                description: >-
                  Retrieves information about a connector definition version,
                  including the connectors that the version contains. Connectors
                  are prebuilt modules that interact with local infrastructure,
                  device protocols, AWS, and other cloud services.
                tags:
                  - Get
                  - Connectors
                  - Definitions
                  - Versions
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
                  - Updates
                  - Subscriptions
                  - Subscriptions
                  - Bulk
                  - Deployments
                  - Status
                  - Things
                  - Names
                  - Connectivity
                  - Info
                  - Versions
            /greengrass/definition/cores/{CoreDefinitionId}/versions/{CoreDefinitionVersionId}:
              GET:
                summary: GetCoreDefinitionVersion
                description: Retrieves information about a core definition version.
                tags:
                  - Get
                  - Core
                  - Definitions
                  - Versions
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
                  - Updates
                  - Subscriptions
                  - Subscriptions
                  - Bulk
                  - Deployments
                  - Status
                  - Things
                  - Names
                  - Connectivity
                  - Info
                  - Versions
            /greengrass/groups/{GroupId}/deployments/{DeploymentId}/status:
              GET:
                summary: GetDeploymentStatus
                description: Returns the status of a deployment.
                tags:
                  - Get
                  - Deployments
                  - Status
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
                  - Updates
                  - Subscriptions
                  - Subscriptions
                  - Bulk
                  - Deployments
                  - Status
                  - Things
                  - Names
                  - Connectivity
                  - Info
                  - Versions
            /greengrass/definition/devices/{DeviceDefinitionId}/versions/{DeviceDefinitionVersionId}:
              GET:
                summary: GetDeviceDefinitionVersion
                description: Retrieves information about a device definition version.
                tags:
                  - Get
                  - Device
                  - Definitions
                  - Versions
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
                  - Updates
                  - Subscriptions
                  - Subscriptions
                  - Bulk
                  - Deployments
                  - Status
                  - Things
                  - Names
                  - Connectivity
                  - Info
                  - Versions
            /greengrass/definition/functions/{FunctionDefinitionId}/versions/{FunctionDefinitionVersionId}:
              GET:
                summary: GetFunctionDefinitionVersion
                description: >-
                  Retrieves information about a Lambda function definition
                  version, including which Lambda functions are included in the
                  version and their configurations.
                tags:
                  - Get
                  - Functions
                  - Definitions
                  - Versions
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
                  - Updates
                  - Subscriptions
                  - Subscriptions
                  - Bulk
                  - Deployments
                  - Status
                  - Things
                  - Names
                  - Connectivity
                  - Info
                  - Versions
            /greengrass/groups/{GroupId}/certificateauthorities/{CertificateAuthorityId}:
              GET:
                summary: GetGroupCertificateAuthority
                description: >-
                  Retreives the CA associated with a group. Returns the public
                  key of the CA.
                tags:
                  - Get
                  - Group
                  - Certificates
                  - Authority
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
                  - Updates
                  - Subscriptions
                  - Subscriptions
                  - Bulk
                  - Deployments
                  - Status
                  - Things
                  - Names
                  - Connectivity
                  - Info
                  - Versions
                  - Certificates
                  - Authority
            /greengrass/groups/{GroupId}/certificateauthorities/configuration/expiry:
              PUT:
                summary: UpdateGroupCertificateConfiguration
                description: Updates the Certificate expiry time for a group.
                tags:
                  - Update
                  - Group
                  - Certificates
                  - Configurations
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
                  - Updates
                  - Subscriptions
                  - Subscriptions
                  - Bulk
                  - Deployments
                  - Status
                  - Things
                  - Names
                  - Connectivity
                  - Info
                  - Versions
                  - Certificates
                  - Authority
                  - Configurations
                  - Expiry
            /greengrass/groups/{GroupId}/versions/{GroupVersionId}:
              GET:
                summary: GetGroupVersion
                description: Retrieves information about a group version.
                tags:
                  - Get
                  - Group
                  - Versions
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
                  - Updates
                  - Subscriptions
                  - Subscriptions
                  - Bulk
                  - Deployments
                  - Status
                  - Things
                  - Names
                  - Connectivity
                  - Info
                  - Versions
                  - Certificates
                  - Authority
                  - Configurations
                  - Expiry
            /greengrass/definition/loggers/{LoggerDefinitionId}/versions/{LoggerDefinitionVersionId}:
              GET:
                summary: GetLoggerDefinitionVersion
                description: Retrieves information about a logger definition version.
                tags:
                  - Get
                  - Loggers
                  - Definitions
                  - Versions
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
                  - Updates
                  - Subscriptions
                  - Subscriptions
                  - Bulk
                  - Deployments
                  - Status
                  - Things
                  - Names
                  - Connectivity
                  - Info
                  - Versions
                  - Certificates
                  - Authority
                  - Configurations
                  - Expiry
            /greengrass/definition/resources/{ResourceDefinitionId}/versions/{ResourceDefinitionVersionId}:
              GET:
                summary: GetResourceDefinitionVersion
                description: >-
                  Retrieves information about a resource definition version,
                  including which resources are included in the version.
                tags:
                  - Get
                  - Resources
                  - Definitions
                  - Versions
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
                  - Updates
                  - Subscriptions
                  - Subscriptions
                  - Bulk
                  - Deployments
                  - Status
                  - Things
                  - Names
                  - Connectivity
                  - Info
                  - Versions
                  - Certificates
                  - Authority
                  - Configurations
                  - Expiry
            /greengrass/definition/subscriptions/{SubscriptionDefinitionId}/versions/{SubscriptionDefinitionVersionId}:
              GET:
                summary: GetSubscriptionDefinitionVersion
                description: Retrieves information about a subscription definition version.
                tags:
                  - Get
                  - Subscriptions
                  - Definitions
                  - Versions
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
                  - Updates
                  - Subscriptions
                  - Subscriptions
                  - Bulk
                  - Deployments
                  - Status
                  - Things
                  - Names
                  - Connectivity
                  - Info
                  - Versions
                  - Certificates
                  - Authority
                  - Configurations
                  - Expiry
            /greengrass/things/{ThingName}/runtimeconfig:
              PUT:
                summary: UpdateThingRuntimeConfiguration
                description: Updates the runtime configuration of a thing.
                tags:
                  - Update
                  - Things
                  - Runtime
                  - Configurations
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
                  - Updates
                  - Subscriptions
                  - Subscriptions
                  - Bulk
                  - Deployments
                  - Status
                  - Things
                  - Names
                  - Connectivity
                  - Info
                  - Versions
                  - Certificates
                  - Authority
                  - Configurations
                  - Expiry
                  - Runtime Configurations
            /greengrass/bulk/deployments/{BulkDeploymentId}/detailed-reports:
              GET:
                summary: ListBulkDeploymentDetailedReports
                description: >-
                  Gets a paginated list of the deployments that have been
                  started in a bulk deployment operation, and their current
                  deployment status.
                tags:
                  - Lists
                  - Bulk
                  - Deployments
                  - Detailed
                  - Reports
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
                  - Updates
                  - Subscriptions
                  - Subscriptions
                  - Bulk
                  - Deployments
                  - Status
                  - Things
                  - Names
                  - Connectivity
                  - Info
                  - Versions
                  - Certificates
                  - Authority
                  - Configurations
                  - Expiry
                  - Runtime Configurations
                  - Detailed
                  - Reports
            /greengrass/bulk/deployments:
              POST:
                summary: StartBulkDeployment
                description: >-
                  Deploys multiple groups in one operation. This action starts
                  the bulk deployment of a specified set of group versions. Each
                  group version deployment will be triggered with an adaptive
                  rate that has a fixed upper limit. We recommend that you
                  include an ''X-Amzn-Client-Token'' token in every
                  ''StartBulkDeployment'' request. These requests are idempotent
                  with respect to the token and the request parameters.
                tags:
                  - Start
                  - Bulk
                  - Deployments
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
                  - Updates
                  - Subscriptions
                  - Subscriptions
                  - Bulk
                  - Deployments
                  - Status
                  - Things
                  - Names
                  - Connectivity
                  - Info
                  - Versions
                  - Certificates
                  - Authority
                  - Configurations
                  - Expiry
                  - Runtime Configurations
                  - Detailed
                  - Reports
            /tags/{resource-arn}:
              DELETE:
                summary: UntagResource
                description: Remove resource tags from a Greengrass Resource.
                tags:
                  - Untag
                  - Resources
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
                  - Updates
                  - Subscriptions
                  - Subscriptions
                  - Bulk
                  - Deployments
                  - Status
                  - Things
                  - Names
                  - Connectivity
                  - Info
                  - Versions
                  - Certificates
                  - Authority
                  - Configurations
                  - Expiry
                  - Runtime Configurations
                  - Detailed
                  - Reports
                  - Tags
                  - ARN
            /greengrass/groups/{GroupId}/deployments/$reset:
              POST:
                summary: ResetDeployments
                description: Resets a group's deployments.
                tags:
                  - Reset
                  - Deployments
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
                  - Updates
                  - Subscriptions
                  - Subscriptions
                  - Bulk
                  - Deployments
                  - Status
                  - Things
                  - Names
                  - Connectivity
                  - Info
                  - Versions
                  - Certificates
                  - Authority
                  - Configurations
                  - Expiry
                  - Runtime Configurations
                  - Detailed
                  - Reports
                  - Tags
                  - ARN
                  - $reset
            /greengrass/bulk/deployments/{BulkDeploymentId}/$stop:
              PUT:
                summary: StopBulkDeployment
                description: >-
                  Stops the execution of a bulk deployment. This action returns
                  a status of ''Stopping'' until the deployment is stopped. You
                  cannot start a new bulk deployment while a previous deployment
                  is in the ''Stopping'' state. This action doesn't rollback
                  completed deployments or cancel pending de
                tags:
                  - Stop
                  - Bulk
                  - Deployments
                  - Group
                  - Identifiers
                  - Roles
                  - Green Grass
                  - Service Roles
                  - Definitions
                  - Connectors
                  - Connectors
                  - Versions
                  - Cores
                  - Core
                  - Deployments
                  - Devices
                  - Device
                  - Functions
                  - Functions
                  - Groups
                  - Certificate Authorities
                  - Loggers
                  - Loggers
                  - Resources
                  - Resources
                  - Updates
                  - Subscriptions
                  - Subscriptions
                  - Bulk
                  - Deployments
                  - Status
                  - Things
                  - Names
                  - Connectivity
                  - Info
                  - Versions
                  - Certificates
                  - Authority
                  - Configurations
                  - Expiry
                  - Runtime Configurations
                  - Detailed
                  - Reports
                  - Tags
                  - ARN
                  - $reset
                  - $st
    overlays:
      - type: APIs.io Search
        url: overlays/greengrass-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/greengrass-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:greengrass
  - name: kafkaconnect
    description: <p/>
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
            title: kafkaconnect
          paths:
            /v1/connectors:
              GET:
                summary: ListConnectors
                description: >-
                  <p>Returns a list of all the connectors in this account and
                  Region. The list is limited to connectors whose name starts
                  with the specified prefix. The response also includes a
                  description of each of the listed connectors.</p>
                tags:
                  - Lists
                  - Connectors
                  - V1
                  - Connectors
            /v1/custom-plugins:
              GET:
                summary: ListCustomPlugins
                description: >-
                  <p>Returns a list of all of the custom plugins in this account
                  and Region.</p>
                tags:
                  - Lists
                  - Custom
                  - Plugins
                  - V1
                  - Connectors
                  - Custom
                  - Plugins
            /v1/worker-configurations:
              GET:
                summary: ListWorkerConfigurations
                description: >-
                  <p>Returns a list of all of the worker configurations in this
                  account and Region.</p>
                tags:
                  - Lists
                  - Workers
                  - Configurations
                  - V1
                  - Connectors
                  - Custom
                  - Plugins
                  - Workers
                  - Configurations
            /v1/connectors/{connectorArn}:
              PUT:
                summary: UpdateConnector
                description: <p>Updates the specified connector.</p>
                tags:
                  - Update
                  - Connectors
                  - V1
                  - Connectors
                  - Custom
                  - Plugins
                  - Workers
                  - Configurations
                  - ARN
            /v1/custom-plugins/{customPluginArn}:
              GET:
                summary: DescribeCustomPlugin
                description: <p>A summary description of the custom plugin.</p>
                tags:
                  - Describe
                  - Custom
                  - Plugins
                  - V1
                  - Connectors
                  - Custom
                  - Plugins
                  - Workers
                  - Configurations
                  - ARN
                  - Plugins
            /v1/worker-configurations/{workerConfigurationArn}:
              GET:
                summary: DescribeWorkerConfiguration
                description: <p>Returns information about a worker configur
                tags:
                  - Describe
                  - Workers
                  - Configurations
                  - V1
                  - Connectors
                  - Custom
                  - Plugins
                  - Workers
                  - Configurations
                  - ARN
                  - Plugins
                  - Configurations
    overlays:
      - type: APIs.io Search
        url: overlays/kafkaconnect-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/kafkaconnect-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:kafkaconnect
  - name: mgn
    description: <p>The Application Migration Service service.</p>
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
            title: mgn
          paths:
            /ArchiveApplication:
              POST:
                summary: ArchiveApplication
                description: <p>Archive application.</p>
                tags:
                  - Archive
                  - Applications
                  - Archive
                  - Applications
            /ArchiveWave:
              POST:
                summary: ArchiveWave
                description: <p>Archive wave.</p>
                tags:
                  - Archive
                  - Waves
                  - Archive
                  - Applications
                  - Waves
            /AssociateApplications:
              POST:
                summary: AssociateApplications
                description: <p>Associate applications to wave.</p>
                tags:
                  - Associate
                  - Applications
                  - Archive
                  - Applications
                  - Waves
                  - Associate
                  - Applications
            /AssociateSourceServers:
              POST:
                summary: AssociateSourceServers
                description: <p>Associate source servers to application.</p>
                tags:
                  - Associate
                  - Source
                  - Servers
                  - Archive
                  - Applications
                  - Waves
                  - Associate
                  - Applications
                  - Source
                  - Servers
            /ChangeServerLifeCycleState:
              POST:
                summary: ChangeServerLifeCycleState
                description: >-
                  <p>Allows the user to set the SourceServer.LifeCycle.state
                  property for specific Source Server IDs to one of the
                  following: READY_FOR_TEST or READY_FOR_CUTOVER. This command
                  only works if the Source Server is already launchable
                  (dataReplicationInfo.lagDuration is not null.)</p>
                tags:
                  - Change
                  - Server
                  - Life
                  - Cycle
                  - States
                  - Archive
                  - Applications
                  - Waves
                  - Associate
                  - Applications
                  - Source
                  - Servers
                  - Change
                  - Server
                  - Life
                  - Cycle
                  - States
            /CreateApplication:
              POST:
                summary: CreateApplication
                description: <p>Create application.</p>
                tags:
                  - Create
                  - Applications
                  - Archive
                  - Applications
                  - Waves
                  - Associate
                  - Applications
                  - Source
                  - Servers
                  - Change
                  - Server
                  - Life
                  - Cycle
                  - States
                  - Create
            /CreateConnector:
              POST:
                summary: CreateConnector
                description: <p>Create Connector.</p>
                tags:
                  - Create
                  - Connectors
                  - Archive
                  - Applications
                  - Waves
                  - Associate
                  - Applications
                  - Source
                  - Servers
                  - Change
                  - Server
                  - Life
                  - Cycle
                  - States
                  - Create
                  - Connectors
            /CreateLaunchConfigurationTemplate:
              POST:
                summary: CreateLaunchConfigurationTemplate
                description: <p>Creates a new Launch Configuration Template.</p>
                tags:
                  - Create
                  - Launch
                  - Configurations
                  - Templates
                  - Archive
                  - Applications
                  - Waves
                  - Associate
                  - Applications
                  - Source
                  - Servers
                  - Change
                  - Server
                  - Life
                  - Cycle
                  - States
                  - Create
                  - Connectors
                  - Launch
                  - Configurations
                  - Templates
            /CreateReplicationConfigurationTemplate:
              POST:
                summary: CreateReplicationConfigurationTemplate
                description: <p>Creates a new ReplicationConfigurationTemplate.</p>
                tags:
                  - Create
                  - Replication
                  - Configurations
                  - Templates
                  - Archive
                  - Applications
                  - Waves
                  - Associate
                  - Applications
                  - Source
                  - Servers
                  - Change
                  - Server
                  - Life
                  - Cycle
                  - States
                  - Create
                  - Connectors
                  - Launch
                  - Configurations
                  - Templates
                  - Replication
            /CreateWave:
              POST:
                summary: CreateWave
                description: <p>Create wave.</p>
                tags:
                  - Create
                  - Waves
                  - Archive
                  - Applications
                  - Waves
                  - Associate
                  - Applications
                  - Source
                  - Servers
                  - Change
                  - Server
                  - Life
                  - Cycle
                  - States
                  - Create
                  - Connectors
                  - Launch
                  - Configurations
                  - Templates
                  - Replication
            /DeleteApplication:
              POST:
                summary: DeleteApplication
                description: <p>Delete application.</p>
                tags:
                  - Delete
                  - Applications
                  - Archive
                  - Applications
                  - Waves
                  - Associate
                  - Applications
                  - Source
                  - Servers
                  - Change
                  - Server
                  - Life
                  - Cycle
                  - States
                  - Create
                  - Connectors
                  - Launch
                  - Configurations
                  - Templates
                  - Replication
                  - Delete
            /DeleteConnector:
              POST:
                summary: DeleteConnector
                description: <p>Delete Connector.</p>
                tags:
                  - Delete
                  - Connectors
                  - Archive
                  - Applications
                  - Waves
                  - Associate
                  - Applications
                  - Source
                  - Servers
                  - Change
                  - Server
                  - Life
                  - Cycle
                  - States
                  - Create
                  - Connectors
                  - Launch
                  - Configurations
                  - Templates
                  - Replication
                  - Delete
            /DeleteJob:
              POST:
                summary: DeleteJob
                description: <p>Deletes a single Job by ID.</p>
                tags:
                  - Delete
                  - Jobs
                  - Archive
                  - Applications
                  - Waves
                  - Associate
                  - Applications
                  - Source
                  - Servers
                  - Change
                  - Server
                  - Life
                  - Cycle
                  - States
                  - Create
                  - Connectors
                  - Launch
                  - Configurations
                  - Templates
                  - Replication
                  - Delete
                  - Jobs
            /DeleteLaunchConfigurationTemplate:
              POST:
                summary: DeleteLaunchConfigurationTemplate
                description: <p>Deletes a single Launch Configuration Template by ID.</p>
                tags:
                  - Delete
                  - Launch
                  - Configurations
                  - Templates
                  - Archive
                  - Applications
                  - Waves
                  - Associate
                  - Applications
                  - Source
                  - Servers
                  - Change
                  - Server
                  - Life
                  - Cycle
                  - States
                  - Create
                  - Connectors
                  - Launch
                  - Configurations
                  - Templates
                  - Replication
                  - Delete
                  - Jobs
            /DeleteReplicationConfigurationTemplate:
              POST:
                summary: DeleteReplicationConfigurationTemplate
                description: >-
                  <p>Deletes a single Replication Configuration Template by
                  ID</p>
                tags:
                  - Delete
                  - Replication
                  - Configurations
                  - Templates
                  - Archive
                  - Applications
                  - Waves
                  - Associate
                  - Applications
                  - Source
                  - Servers
                  - Change
                  - Server
                  - Life
                  - Cycle
                  - States
                  - Create
                  - Connectors
                  - Launch
                  - Configurations
                  - Templates
                  - Replication
                  - Delete
                  - Jobs
            /DeleteSourceServer:
              POST:
                summary: DeleteSourceServer
                description: <p>Deletes a single source server by ID.</p>
                tags:
                  - Delete
                  - Source
                  - Server
                  - Archive
                  - Applications
                  - Waves
                  - Associate
                  - Applications
                  - Source
                  - Servers
                  - Change
                  - Server
                  - Life
                  - Cycle
                  - States
                  - Create
                  - Connectors
                  - Launch
                  - Configurations
                  - Templates
                  - Replication
                  - Delete
                  - Jobs
            /DeleteVcenterClient:
              POST:
                summary: DeleteVcenterClient
                description: <p>Deletes a given vCenter client by ID.</p>
                tags:
                  - Delete
                  - Vcenter
                  - Client
                  - Archive
                  - Applications
                  - Waves
                  - Associate
                  - Applications
                  - Source
                  - Servers
                  - Change
                  - Server
                  - Life
                  - Cycle
                  - States
                  - Create
                  - Connectors
                  - Launch
                  - Configurations
                  - Templates
                  - Replication
                  - Delete
                  - Jobs
                  - Vcenter
                  - Client
            /DeleteWave:
              POST:
                summary: DeleteWave
                description: <p>Delete wave.</p>
                tags:
                  - Delete
                  - Waves
                  - Archive
                  - Applications
                  - Waves
                  - Associate
                  - Applications
                  - Source
                  - Servers
                  - Change
                  - Server
                  - Life
                  - Cycle
                  - States
                  - Create
                  - Connectors
                  - Launch
                  - Configurations
                  - Templates
                  - Replication
                  - Delete
                  - Jobs
                  - Vcenter
                  - Client
            /DescribeJobLogItems:
              POST:
                summary: DescribeJobLogItems
                description: <p>Retrieves detailed job log items with paging.</p>
                tags:
                  - Describe
                  - Jobs
                  - Logs
                  - Items
                  - Archive
                  - Applications
                  - Waves
                  - Associate
                  - Applications
                  - Source
                  - Servers
                  - Change
                  - Server
                  - Life
                  - Cycle
                  - States
                  - Create
                  - Connectors
                  - Launch
                  - Configurations
                  - Templates
                  - Replication
                  - Delete
                  - Jobs
                  - Vcenter
                  - Client
                  - Describe
                  - Logs
                  - Items
            /DescribeJobs:
              POST:
                summary: DescribeJobs
                description: >-
                  <p>Returns a list of Jobs. Use the JobsID and fromDate and
                  toData filters to limit which jobs are returned. The response
                  is sorted by creationDataTime - latest date first. Jobs are
                  normally created by the StartTest, StartCutover, and
                  TerminateTargetInstances APIs. Jobs are also created by
                  DiagnosticLaunch and TerminateDiagnosticInstances, which are
                  APIs available only to *Support* and only used in response to
                  relevant support tickets.</p>
                tags:
                  - Describe
                  - Jobs
                  - Archive
                  - Applications
                  - Waves
                  - Associate
                  - Applications
                  - Source
                  - Servers
                  - Change
                  - Server
                  - Life
                  - Cycle
                  - States
                  - Create
                  - Connectors
                  - Launch
                  - Configurations
                  - Templates
                  - Replication
                  - Delete
                  - Jobs
                  - Vcenter
                  - Client
                  - Describe
                  - Logs
                  - Items
                  - Jobs
            /DescribeLaunchConfigurationTemplates:
              POST:
                summary: DescribeLaunchConfigurationTemplates
                description: >-
                  <p>Lists all Launch Configuration Templates, filtered by
                  Launch Configuration Template IDs</p>
                tags:
                  - Describe
                  - Launch
                  - Configurations
                  - Templates
                  - Archive
                  - Applications
                  - Waves
                  - Associate
                  - Applications
                  - Source
                  - Servers
                  - Change
                  - Server
                  - Life
                  - Cycle
                  - States
                  - Create
                  - Connectors
                  - Launch
                  - Configurations
                  - Templates
                  - Replication
                  - Delete
                  - Jobs
                  - Vcenter
                  - Client
                  - Describe
                  - Logs
                  - Items
                  - Jobs
                  - Templates
            /DescribeReplicationConfigurationTemplates:
              POST:
                summary: DescribeReplicationConfigurationTemplates
                description: >-
                  <p>Lists all ReplicationConfigurationTemplates, filtered by
                  Source Server IDs.</p>
                tags:
                  - Describe
                  - Replication
                  - Configurations
                  - Templates
                  - Archive
                  - Applications
                  - Waves
                  - Associate
                  - Applications
                  - Source
                  - Servers
                  - Change
                  - Server
                  - Life
                  - Cycle
                  - States
                  - Create
                  - Connectors
                  - Launch
                  - Configurations
                  - Templates
                  - Replication
                  - Delete
                  - Jobs
                  - Vcenter
                  - Client
                  - Describe
                  - Logs
                  - Items
                  - Jobs
                  - Templates
            /DescribeSourceServers:
              POST:
                summary: DescribeSourceServers
                description: >-
                  <p>Retrieves all SourceServers or multiple SourceServers by
                  ID.</p>
                tags:
                  - Describe
                  - Source
                  - Servers
                  - Archive
                  - Applications
                  - Waves
                  - Associate
                  - Applications
                  - Source
                  - Servers
                  - Change
                  - Server
                  - Life
                  - Cycle
                  - States
                  - Create
                  - Connectors
                  - Launch
                  - Configurations
                  - Templates
                  - Replication
                  - Delete
                  - Jobs
                  - Vcenter
                  - Client
                  - Describe
                  - Logs
                  - Items
                  - Jobs
                  - Templates
            /DescribeVcenterClients:
              GET:
                summary: DescribeVcenterClients
                description: <p>Returns a list of the installed vCenter clients.</p>
                tags:
                  - Describe
                  - Vcenter
                  - Clients
                  - Archive
                  - Applications
                  - Waves
                  - Associate
                  - Applications
                  - Source
                  - Servers
                  - Change
                  - Server
                  - Life
                  - Cycle
                  - States
                  - Create
                  - Connectors
                  - Launch
                  - Configurations
                  - Templates
                  - Replication
                  - Delete
                  - Jobs
                  - Vcenter
                  - Client
                  - Describe
                  - Logs
                  - Items
                  - Jobs
                  - Templates
                  - Clients
            /DisassociateApplications:
              POST:
                summary: DisassociateApplications
                description: <p>Disassociate applications from wave.</p>
                tags:
                  - Disassociate
                  - Applications
                  - Archive
                  - Applications
                  - Waves
                  - Associate
                  - Applications
                  - Source
                  - Servers
                  - Change
                  - Server
                  - Life
                  - Cycle
                  - States
                  - Create
                  - Connectors
                  - Launch
                  - Configurations
                  - Templates
                  - Replication
                  - Delete
                  - Jobs
                  - Vcenter
                  - Client
                  - Describe
                  - Logs
                  - Items
                  - Jobs
                  - Templates
                  - Clients
                  - Disassociate
            /DisassociateSourceServers:
              POST:
                summary: DisassociateSourceServers
                description: <p>Disassociate source servers from application.</p>
                tags:
                  - Disassociate
                  - Source
                  - Servers
                  - Archive
                  - Applications
                  - Waves
                  - Associate
                  - Applications
                  - Source
                  - Servers
                  - Change
                  - Server
                  - Life
                  - Cycle
                  - States
                  - Create
                  - Connectors
                  - Launch
                  - Configurations
                  - Templates
                  - Replication
                  - Delete
                  - Jobs
                  - Vcenter
                  - Client
                  - Describe
                  - Logs
                  - Items
                  - Jobs
                  - Templates
                  - Clients
                  - Disassociate
            /DisconnectFromService:
              POST:
                summary: DisconnectFromService
                description: >-
                  <p>Disconnects specific Source Servers from Application
                  Migration Service. Data replication is stopped immediately.
                  All AWS resources created by Application Migration Service for
                  enabling the replication of these source servers will be
                  terminated / deleted within 90 minutes. Launched Test or
                  Cutover instances will NOT be terminated. If the agent on the
                  source server has not been prevented from communicating with
                  the Application Migration Service service, then it will
                  receive a command to uninstall itself (within approximately 10
                  minutes). The following properties of the SourceServer will be
                  changed immediately: dataReplicationInfo.dataReplicationState
                  will be set to DISCONNECTED; The totalStorageBytes property
                  for each of dataReplicationInfo.replicatedDisks will be set to
                  zero; dataReplicationInfo.lagDuration and
                  dataReplicationInfo.lagDuration will be nullified.</p>
                tags:
                  - Disconnect
                  - From
                  - Services
                  - Archive
                  - Applications
                  - Waves
                  - Associate
                  - Applications
                  - Source
                  - Servers
                  - Change
                  - Server
                  - Life
                  - Cycle
                  - States
                  - Create
                  - Connectors
                  - Launch
                  - Configurations
                  - Templates
                  - Replication
                  - Delete
                  - Jobs
                  - Vcenter
                  - Client
                  - Describe
                  - Logs
                  - Items
                  - Jobs
                  - Templates
                  - Clients
                  - Disassociate
                  - Disconnect
                  - From
                  - Services
            /FinalizeCutover:
              POST:
                summary: FinalizeCutover
                description: >-
                  <p>Finalizes the cutover immediately for specific Source
                  Servers. All AWS resources created by Application Migration
                  Service for enabling the replication of these source servers
                  will be terminated / deleted within 90 minutes. Launched Test
                  or Cutover instances will NOT be terminated. The AWS
                  Replication Agent will receive a command to uninstall itself
                  (within 10 minutes). The following properties of the
                  SourceServer will be changed immediately:
                  dataReplicationInfo.dataReplicationState will be changed to
                  DISCONNECTED; The SourceServer.lifeCycle.state will be changed
                  to CUTOVER; The totalStorageBytes property fo each of
                  dataReplicationInfo.replicatedDisks will be set to zero;
                  dataReplicationInfo.lagDuration and
                  dataReplicationInfo.lagDuration will be nullified.</p>
                tags:
                  - Finalize
                  - Cutover
                  - Archive
                  - Applications
                  - Waves
                  - Associate
                  - Applications
                  - Source
                  - Servers
                  - Change
                  - Server
                  - Life
                  - Cycle
                  - States
                  - Create
                  - Connectors
                  - Launch
                  - Configurations
                  - Templates
                  - Replication
                  - Delete
                  - Jobs
                  - Vcenter
                  - Client
                  - Describe
                  - Logs
                  - Items
                  - Jobs
                  - Templates
                  - Clients
                  - Disassociate
                  - Disconnect
                  - From
                  - Services
                  - Finalize
                  - Cutover
            /GetLaunchConfiguration:
              POST:
                summary: GetLaunchConfiguration
                description: >-
                  <p>Lists all LaunchConfigurations available, filtered by
                  Source Server IDs.</p>
                tags:
                  - Get
                  - Launch
                  - Configurations
                  - Archive
                  - Applications
                  - Waves
                  - Associate
                  - Applications
                  - Source
                  - Servers
                  - Change
                  - Server
                  - Life
                  - Cycle
                  - States
                  - Create
                  - Connectors
                  - Launch
                  - Configurations
                  - Templates
                  - Replication
                  - Delete
                  - Jobs
                  - Vcenter
                  - Client
                  - Describe
                  - Logs
                  - Items
                  - Jobs
                  - Templates
                  - Clients
                  - Disassociate
                  - Disconnect
                  - From
                  - Services
                  - Finalize
                  - Cutover
                  - Get
            /GetReplicationConfiguration:
              POST:
                summary: GetReplicationConfiguration
                description: >-
                  <p>Lists all ReplicationConfigurations, filtered by Source
                  Server ID.</p>
                tags:
                  - Get
                  - Replication
                  - Configurations
                  - Archive
                  - Applications
                  - Waves
                  - Associate
                  - Applications
                  - Source
                  - Servers
                  - Change
                  - Server
                  - Life
                  - Cycle
                  - States
                  - Create
                  - Connectors
                  - Launch
                  - Configurations
                  - Templates
                  - Replication
                  - Delete
                  - Jobs
                  - Vcenter
                  - Client
                  - Describe
                  - Logs
                  - Items
                  - Jobs
                  - Templates
                  - Clients
                  - Disassociate
                  - Disconnect
                  - From
                  - Services
                  - Finalize
                  - Cutover
                  - Get
            /InitializeService:
              POST:
                summary: InitializeService
                description: <p>Initialize Application Migration Service.</p>
                tags:
                  - Initialize
                  - Services
                  - Archive
                  - Applications
                  - Waves
                  - Associate
                  - Applications
                  - Source
                  - Servers
                  - Change
                  - Server
                  - Life
                  - Cycle
                  - States
                  - Create
                  - Connectors
                  - Launch
                  - Configurations
                  - Templates
                  - Replication
                  - Delete
                  - Jobs
                  - Vcenter
                  - Client
                  - Describe
                  - Logs
                  - Items
                  - Jobs
                  - Templates
                  - Clients
                  - Disassociate
                  - Disconnect
                  - From
                  - Services
                  - Finalize
                  - Cutover
                  - Get
                  - Initialize
            /ListApplications:
              POST:
                summary: ListApplications
                description: >-
                  <p>Retrieves all applications or multiple applications by
                  ID.</p>
                tags:
                  - Lists
                  - Applications
                  - Archive
                  - Applications
                  - Waves
                  - Associate
                  - Applications
                  - Source
                  - Servers
                  - Change
                  - Server
                  - Life
                  - Cycle
                  - States
                  - Create
                  - Connectors
                  - Launch
                  - Configurations
                  - Templates
                  - Replication
                  - Delete
                  - Jobs
                  - Vcenter
                  - Client
                  - Describe
                  - Logs
                  - Items
                  - Jobs
                  - Templates
                  - Clients
                  - Disassociate
                  - Disconnect
                  - From
                  - Services
                  - Finalize
                  - Cutover
                  - Get
                  - Initialize
                  - Lists
            /ListConnectors:
              POST:
                summary: ListConnectors
                description: <p>List Connectors.</p>
                tags:
                  - Lists
                  - Connectors
                  - Archive
                  - Applications
                  - Waves
                  - Associate
                  - Applications
                  - Source
                  - Servers
                  - Change
                  - Server
                  - Life
                  - Cycle
                  - States
                  - Create
                  - Connectors
                  - Launch
                  - Configurations
                  - Templates
                  - Replication
                  - Delete
                  - Jobs
                  - Vcenter
                  - Client
                  - Describe
                  - Logs
                  - Items
                  - Jobs
                  - Templates
                  - Clients
                  - Disassociate
                  - Disconnect
                  - From
                  - Services
                  - Finalize
                  - Cutover
                  - Get
                  - Initialize
                  - Lists
                  - Connectors
            /ListExportErrors:
              POST:
                summary: ListExportErrors
                description: <p>List export errors.</p>
                tags:
                  - Lists
                  - Export
                  - Errors
                  - Archive
                  - Applications
                  - Waves
                  - Associate
                  - Applications
                  - Source
                  - Servers
                  - Change
                  - Server
                  - Life
                  - Cycle
                  - States
                  - Create
                  - Connectors
                  - Launch
                  - Configurations
                  - Templates
                  - Replication
                  - Delete
                  - Jobs
                  - Vcenter
                  - Client
                  - Describe
                  - Logs
                  - Items
                  - Jobs
                  - Templates
                  - Clients
                  - Disassociate
                  - Disconnect
                  - From
                  - Services
                  - Finalize
                  - Cutover
                  - Get
                  - Initialize
                  - Lists
                  - Connectors
                  - Export
                  - Errors
            /ListExports:
              POST:
                summary: ListExports
                description: <p>List exports.</p>
                tags:
                  - Lists
                  - Exports
                  - Archive
                  - Applications
                  - Waves
                  - Associate
                  - Applications
                  - Source
                  - Servers
                  - Change
                  - Server
                  - Life
                  - Cycle
                  - States
                  - Create
                  - Connectors
                  - Launch
                  - Configurations
                  - Templates
                  - Replication
                  - Delete
                  - Jobs
                  - Vcenter
                  - Client
                  - Describe
                  - Logs
                  - Items
                  - Jobs
                  - Templates
                  - Clients
                  - Disassociate
                  - Disconnect
                  - From
                  - Services
                  - Finalize
                  - Cutover
                  - Get
                  - Initialize
                  - Lists
                  - Connectors
                  - Export
                  - Errors
                  - Exports
            /ListImportErrors:
              POST:
                summary: ListImportErrors
                description: <p>List import errors.</p>
                tags:
                  - Lists
                  - Import
                  - Errors
                  - Archive
                  - Applications
                  - Waves
                  - Associate
                  - Applications
                  - Source
                  - Servers
                  - Change
                  - Server
                  - Life
                  - Cycle
                  - States
                  - Create
                  - Connectors
                  - Launch
                  - Configurations
                  - Templates
                  - Replication
                  - Delete
                  - Jobs
                  - Vcenter
                  - Client
                  - Describe
                  - Logs
                  - Items
                  - Jobs
                  - Templates
                  - Clients
                  - Disassociate
                  - Disconnect
                  - From
                  - Services
                  - Finalize
                  - Cutover
                  - Get
                  - Initialize
                  - Lists
                  - Connectors
                  - Export
                  - Errors
                  - Exports
                  - Import
            /ListImports:
              POST:
                summary: ListImports
                description: <p>List imports.</p>
                tags:
                  - Lists
                  - Imports
                  - Archive
                  - Applications
                  - Waves
                  - Associate
                  - Applications
                  - Source
                  - Servers
                  - Change
                  - Server
                  - Life
                  - Cycle
                  - States
                  - Create
                  - Connectors
                  - Launch
                  - Configurations
                  - Templates
                  - Replication
                  - Delete
                  - Jobs
                  - Vcenter
                  - Client
                  - Describe
                  - Logs
                  - Items
                  - Jobs
                  - Templates
                  - Clients
                  - Disassociate
                  - Disconnect
                  - From
                  - Services
                  - Finalize
                  - Cutover
                  - Get
                  - Initialize
                  - Lists
                  - Connectors
                  - Export
                  - Errors
                  - Exports
                  - Import
                  - Imports
            /ListManagedAccounts:
              POST:
                summary: ListManagedAccounts
                description: <p>List Managed Accounts.</p>
                tags:
                  - Lists
                  - Managed
                  - Accounts
                  - Archive
                  - Applications
                  - Waves
                  - Associate
                  - Applications
                  - Source
                  - Servers
                  - Change
                  - Server
                  - Life
                  - Cycle
                  - States
                  - Create
                  - Connectors
                  - Launch
                  - Configurations
                  - Templates
                  - Replication
                  - Delete
                  - Jobs
                  - Vcenter
                  - Client
                  - Describe
                  - Logs
                  - Items
                  - Jobs
                  - Templates
                  - Clients
                  - Disassociate
                  - Disconnect
                  - From
                  - Services
                  - Finalize
                  - Cutover
                  - Get
                  - Initialize
                  - Lists
                  - Connectors
                  - Export
                  - Errors
                  - Exports
                  - Import
                  - Imports
                  - Managed
                  - Accounts
            /ListSourceServerActions:
              POST:
                summary: ListSourceServerActions
                description: <p>List source server post migration custom actions.</p>
                tags:
                  - Lists
                  - Source
                  - Server
                  - Actions
                  - Archive
                  - Applications
                  - Waves
                  - Associate
                  - Applications
                  - Source
                  - Servers
                  - Change
                  - Server
                  - Life
                  - Cycle
                  - States
                  - Create
                  - Connectors
                  - Launch
                  - Configurations
                  - Templates
                  - Replication
                  - Delete
                  - Jobs
                  - Vcenter
                  - Client
                  - Describe
                  - Logs
                  - Items
                  - Jobs
                  - Templates
                  - Clients
                  - Disassociate
                  - Disconnect
                  - From
                  - Services
                  - Finalize
                  - Cutover
                  - Get
                  - Initialize
                  - Lists
                  - Connectors
                  - Export
                  - Errors
                  - Exports
                  - Import
                  - Imports
                  - Managed
                  - Accounts
                  - Actions
            /tags/{resourceArn}:
              DELETE:
                summary: UntagResource
                description: >-
                  <p>Deletes the specified set of tags from the specified set of
                  Application Migration Service resources.</p>
                tags:
                  - Untag
                  - Resources
                  - Archive
                  - Applications
                  - Waves
                  - Associate
                  - Applications
                  - Source
                  - Servers
                  - Change
                  - Server
                  - Life
                  - Cycle
                  - States
                  - Create
                  - Connectors
                  - Launch
                  - Configurations
                  - Templates
                  - Replication
                  - Delete
                  - Jobs
                  - Vcenter
                  - Client
                  - Describe
                  - Logs
                  - Items
                  - Jobs
                  - Templates
                  - Clients
                  - Disassociate
                  - Disconnect
                  - From
                  - Services
                  - Finalize
                  - Cutover
                  - Get
                  - Initialize
                  - Lists
                  - Connectors
                  - Export
                  - Errors
                  - Exports
                  - Import
                  - Imports
                  - Managed
                  - Accounts
                  - Actions
                  - ARN
            /ListTemplateActions:
              POST:
                summary: ListTemplateActions
                description: <p>List template post migration custom actions.</p>
                tags:
                  - Lists
                  - Templates
                  - Actions
                  - Archive
                  - Applications
                  - Waves
                  - Associate
                  - Applications
                  - Source
                  - Servers
                  - Change
                  - Server
                  - Life
                  - Cycle
                  - States
                  - Create
                  - Connectors
                  - Launch
                  - Configurations
                  - Templates
                  - Replication
                  - Delete
                  - Jobs
                  - Vcenter
                  - Client
                  - Describe
                  - Logs
                  - Items
                  - Jobs
                  - Templates
                  - Clients
                  - Disassociate
                  - Disconnect
                  - From
                  - Services
                  - Finalize
                  - Cutover
                  - Get
                  - Initialize
                  - Lists
                  - Connectors
                  - Export
                  - Errors
                  - Exports
                  - Import
                  - Imports
                  - Managed
                  - Accounts
                  - Actions
                  - ARN
            /ListWaves:
              POST:
                summary: ListWaves
                description: <p>Retrieves all waves or multiple waves by ID.</p>
                tags:
                  - Lists
                  - Waves
                  - Archive
                  - Applications
                  - Waves
                  - Associate
                  - Applications
                  - Source
                  - Servers
                  - Change
                  - Server
                  - Life
                  - Cycle
                  - States
                  - Create
                  - Connectors
                  - Launch
                  - Configurations
                  - Templates
                  - Replication
                  - Delete
                  - Jobs
                  - Vcenter
                  - Client
                  - Describe
                  - Logs
                  - Items
                  - Jobs
                  - Templates
                  - Clients
                  - Disassociate
                  - Disconnect
                  - From
                  - Services
                  - Finalize
                  - Cutover
                  - Get
                  - Initialize
                  - Lists
                  - Connectors
                  - Export
                  - Errors
                  - Exports
                  - Import
                  - Imports
                  - Managed
                  - Accounts
                  - Actions
                  - ARN
                  - Waves
            /MarkAsArchived:
              POST:
                summary: MarkAsArchived
                description: >-
                  <p>Archives specific Source Servers by setting the
                  SourceServer.isArchived property to true for specified
                  SourceServers by ID. This command only works for SourceServers
                  with a lifecycle. state which equals DISCONNECTED or
                  CUTOVER.</p>
                tags:
                  - Mark
                  - As
                  - Archived
                  - Archive
                  - Applications
                  - Waves
                  - Associate
                  - Applications
                  - Source
                  - Servers
                  - Change
                  - Server
                  - Life
                  - Cycle
                  - States
                  - Create
                  - Connectors
                  - Launch
                  - Configurations
                  - Templates
                  - Replication
                  - Delete
                  - Jobs
                  - Vcenter
                  - Client
                  - Describe
                  - Logs
                  - Items
                  - Jobs
                  - Templates
                  - Clients
                  - Disassociate
                  - Disconnect
                  - From
                  - Services
                  - Finalize
                  - Cutover
                  - Get
                  - Initialize
                  - Lists
                  - Connectors
                  - Export
                  - Errors
                  - Exports
                  - Import
                  - Imports
                  - Managed
                  - Accounts
                  - Actions
                  - ARN
                  - Waves
                  - Mark
                  - As
                  - Archived
            /PauseReplication:
              POST:
                summary: PauseReplication
                description: <p>Pause Replication.</p>
                tags:
                  - Pause
                  - Replication
                  - Archive
                  - Applications
                  - Waves
                  - Associate
                  - Applications
                  - Source
                  - Servers
                  - Change
                  - Server
                  - Life
                  - Cycle
                  - States
                  - Create
                  - Connectors
                  - Launch
                  - Configurations
                  - Templates
                  - Replication
                  - Delete
                  - Jobs
                  - Vcenter
                  - Client
                  - Describe
                  - Logs
                  - Items
                  - Jobs
                  - Templates
                  - Clients
                  - Disassociate
                  - Disconnect
                  - From
                  - Services
                  - Finalize
                  - Cutover
                  - Get
                  - Initialize
                  - Lists
                  - Connectors
                  - Export
                  - Errors
                  - Exports
                  - Import
                  - Imports
                  - Managed
                  - Accounts
                  - Actions
                  - ARN
                  - Waves
                  - Mark
                  - As
                  - Archived
                  - Pause
            /PutSourceServerAction:
              POST:
                summary: PutSourceServerAction
                description: <p>Put source server post migration custom action.</p>
                tags:
                  - Put
                  - Source
                  - Server
                  - Actions
                  - Archive
                  - Applications
                  - Waves
                  - Associate
                  - Applications
                  - Source
                  - Servers
                  - Change
                  - Server
                  - Life
                  - Cycle
                  - States
                  - Create
                  - Connectors
                  - Launch
                  - Configurations
                  - Templates
                  - Replication
                  - Delete
                  - Jobs
                  - Vcenter
                  - Client
                  - Describe
                  - Logs
                  - Items
                  - Jobs
                  - Templates
                  - Clients
                  - Disassociate
                  - Disconnect
                  - From
                  - Services
                  - Finalize
                  - Cutover
                  - Get
                  - Initialize
                  - Lists
                  - Connectors
                  - Export
                  - Errors
                  - Exports
                  - Import
                  - Imports
                  - Managed
                  - Accounts
                  - Actions
                  - ARN
                  - Waves
                  - Mark
                  - As
                  - Archived
                  - Pause
                  - Put
                  - Actions
            /PutTemplateAction:
              POST:
                summary: PutTemplateAction
                description: <p>Put template post migration custom action.</p>
                tags:
                  - Put
                  - Templates
                  - Actions
                  - Archive
                  - Applications
                  - Waves
                  - Associate
                  - Applications
                  - Source
                  - Servers
                  - Change
                  - Server
                  - Life
                  - Cycle
                  - States
                  - Create
                  - Connectors
                  - Launch
                  - Configurations
                  - Templates
                  - Replication
                  - Delete
                  - Jobs
                  - Vcenter
                  - Client
                  - Describe
                  - Logs
                  - Items
                  - Jobs
                  - Templates
                  - Clients
                  - Disassociate
                  - Disconnect
                  - From
                  - Services
                  - Finalize
                  - Cutover
                  - Get
                  - Initialize
                  - Lists
                  - Connectors
                  - Export
                  - Errors
                  - Exports
                  - Import
                  - Imports
                  - Managed
                  - Accounts
                  - Actions
                  - ARN
                  - Waves
                  - Mark
                  - As
                  - Archived
                  - Pause
                  - Put
                  - Actions
            /RemoveSourceServerAction:
              POST:
                summary: RemoveSourceServerAction
                description: <p>Remove source server post migration custom action.</p>
                tags:
                  - Removes
                  - Source
                  - Server
                  - Actions
                  - Archive
                  - Applications
                  - Waves
                  - Associate
                  - Applications
                  - Source
                  - Servers
                  - Change
                  - Server
                  - Life
                  - Cycle
                  - States
                  - Create
                  - Connectors
                  - Launch
                  - Configurations
                  - Templates
                  - Replication
                  - Delete
                  - Jobs
                  - Vcenter
                  - Client
                  - Describe
                  - Logs
                  - Items
                  - Jobs
                  - Templates
                  - Clients
                  - Disassociate
                  - Disconnect
                  - From
                  - Services
                  - Finalize
                  - Cutover
                  - Get
                  - Initialize
                  - Lists
                  - Connectors
                  - Export
                  - Errors
                  - Exports
                  - Import
                  - Imports
                  - Managed
                  - Accounts
                  - Actions
                  - ARN
                  - Waves
                  - Mark
                  - As
                  - Archived
                  - Pause
                  - Put
                  - Actions
                  - Removes
            /RemoveTemplateAction:
              POST:
                summary: RemoveTemplateAction
                description: <p>Remove template post migration custom action.</p>
                tags:
                  - Removes
                  - Templates
                  - Actions
                  - Archive
                  - Applications
                  - Waves
                  - Associate
                  - Applications
                  - Source
                  - Servers
                  - Change
                  - Server
                  - Life
                  - Cycle
                  - States
                  - Create
                  - Connectors
                  - Launch
                  - Configurations
                  - Templates
                  - Replication
                  - Delete
                  - Jobs
                  - Vcenter
                  - Client
                  - Describe
                  - Logs
                  - Items
                  - Jobs
                  - Templates
                  - Clients
                  - Disassociate
                  - Disconnect
                  - From
                  - Services
                  - Finalize
                  - Cutover
                  - Get
                  - Initialize
                  - Lists
                  - Connectors
                  - Export
                  - Errors
                  - Exports
                  - Import
                  - Imports
                  - Managed
                  - Accounts
                  - Actions
                  - ARN
                  - Waves
                  - Mark
                  - As
                  - Archived
                  - Pause
                  - Put
                  - Actions
                  - Removes
            /ResumeReplication:
              POST:
                summary: ResumeReplication
                description: <p>Resume Replication.</p>
                tags:
                  - Resume
                  - Replication
                  - Archive
                  - Applications
                  - Waves
                  - Associate
                  - Applications
                  - Source
                  - Servers
                  - Change
                  - Server
                  - Life
                  - Cycle
                  - States
                  - Create
                  - Connectors
                  - Launch
                  - Configurations
                  - Templates
                  - Replication
                  - Delete
                  - Jobs
                  - Vcenter
                  - Client
                  - Describe
                  - Logs
                  - Items
                  - Jobs
                  - Templates
                  - Clients
                  - Disassociate
                  - Disconnect
                  - From
                  - Services
                  - Finalize
                  - Cutover
                  - Get
                  - Initialize
                  - Lists
                  - Connectors
                  - Export
                  - Errors
                  - Exports
                  - Import
                  - Imports
                  - Managed
                  - Accounts
                  - Actions
                  - ARN
                  - Waves
                  - Mark
                  - As
                  - Archived
                  - Pause
                  - Put
                  - Actions
                  - Removes
                  - Resume
            /RetryDataReplication:
              POST:
                summary: RetryDataReplication
                description: >-
                  <p>Causes the data replication initiation sequence to begin
                  immediately upon next Handshake for specified SourceServer
                  IDs, regardless of when the previous initiation started. This
                  command will not work if the SourceServer is not stalled or is
                  in a DISCONNECTED or STOPPED state.</p>
                tags:
                  - Retry
                  - Data
                  - Replication
                  - Archive
                  - Applications
                  - Waves
                  - Associate
                  - Applications
                  - Source
                  - Servers
                  - Change
                  - Server
                  - Life
                  - Cycle
                  - States
                  - Create
                  - Connectors
                  - Launch
                  - Configurations
                  - Templates
                  - Replication
                  - Delete
                  - Jobs
                  - Vcenter
                  - Client
                  - Describe
                  - Logs
                  - Items
                  - Jobs
                  - Templates
                  - Clients
                  - Disassociate
                  - Disconnect
                  - From
                  - Services
                  - Finalize
                  - Cutover
                  - Get
                  - Initialize
                  - Lists
                  - Connectors
                  - Export
                  - Errors
                  - Exports
                  - Import
                  - Imports
                  - Managed
                  - Accounts
                  - Actions
                  - ARN
                  - Waves
                  - Mark
                  - As
                  - Archived
                  - Pause
                  - Put
                  - Actions
                  - Removes
                  - Resume
                  - Retry
                  - Data
            /StartCutover:
              POST:
                summary: StartCutover
                description: >-
                  <p>Launches a Cutover Instance for specific Source Servers.
                  This command starts a LAUNCH job whose initiatedBy property is
                  StartCutover and changes the SourceServer.lifeCycle.state
                  property to CUTTING_OVER.</p>
                tags:
                  - Start
                  - Cutover
                  - Archive
                  - Applications
                  - Waves
                  - Associate
                  - Applications
                  - Source
                  - Servers
                  - Change
                  - Server
                  - Life
                  - Cycle
                  - States
                  - Create
                  - Connectors
                  - Launch
                  - Configurations
                  - Templates
                  - Replication
                  - Delete
                  - Jobs
                  - Vcenter
                  - Client
                  - Describe
                  - Logs
                  - Items
                  - Jobs
                  - Templates
                  - Clients
                  - Disassociate
                  - Disconnect
                  - From
                  - Services
                  - Finalize
                  - Cutover
                  - Get
                  - Initialize
                  - Lists
                  - Connectors
                  - Export
                  - Errors
                  - Exports
                  - Import
                  - Imports
                  - Managed
                  - Accounts
                  - Actions
                  - ARN
                  - Waves
                  - Mark
                  - As
                  - Archived
                  - Pause
                  - Put
                  - Actions
                  - Removes
                  - Resume
                  - Retry
                  - Data
                  - Start
            /StartExport:
              POST:
                summary: StartExport
                description: <p>Start export.</p>
                tags:
                  - Start
                  - Export
                  - Archive
                  - Applications
                  - Waves
                  - Associate
                  - Applications
                  - Source
                  - Servers
                  - Change
                  - Server
                  - Life
                  - Cycle
                  - States
                  - Create
                  - Connectors
                  - Launch
                  - Configurations
                  - Templates
                  - Replication
                  - Delete
                  - Jobs
                  - Vcenter
                  - Client
                  - Describe
                  - Logs
                  - Items
                  - Jobs
                  - Templates
                  - Clients
                  - Disassociate
                  - Disconnect
                  - From
                  - Services
                  - Finalize
                  - Cutover
                  - Get
                  - Initialize
                  - Lists
                  - Connectors
                  - Export
                  - Errors
                  - Exports
                  - Import
                  - Imports
                  - Managed
                  - Accounts
                  - Actions
                  - ARN
                  - Waves
                  - Mark
                  - As
                  - Archived
                  - Pause
                  - Put
                  - Actions
                  - Removes
                  - Resume
                  - Retry
                  - Data
                  - Start
            /StartImport:
              POST:
                summary: StartImport
                description: <p>Start import.</p>
                tags:
                  - Start
                  - Import
                  - Archive
                  - Applications
                  - Waves
                  - Associate
                  - Applications
                  - Source
                  - Servers
                  - Change
                  - Server
                  - Life
                  - Cycle
                  - States
                  - Create
                  - Connectors
                  - Launch
                  - Configurations
                  - Templates
                  - Replication
                  - Delete
                  - Jobs
                  - Vcenter
                  - Client
                  - Describe
                  - Logs
                  - Items
                  - Jobs
                  - Templates
                  - Clients
                  - Disassociate
                  - Disconnect
                  - From
                  - Services
                  - Finalize
                  - Cutover
                  - Get
                  - Initialize
                  - Lists
                  - Connectors
                  - Export
                  - Errors
                  - Exports
                  - Import
                  - Imports
                  - Managed
                  - Accounts
                  - Actions
                  - ARN
                  - Waves
                  - Mark
                  - As
                  - Archived
                  - Pause
                  - Put
                  - Actions
                  - Removes
                  - Resume
                  - Retry
                  - Data
                  - Start
            /StartReplication:
              POST:
                summary: StartReplication
                description: <p>Starts replication for SNAPSHOT_SHIPPING agents.</p>
                tags:
                  - Start
                  - Replication
                  - Archive
                  - Applications
                  - Waves
                  - Associate
                  - Applications
                  - Source
                  - Servers
                  - Change
                  - Server
                  - Life
                  - Cycle
                  - States
                  - Create
                  - Connectors
                  - Launch
                  - Configurations
                  - Templates
                  - Replication
                  - Delete
                  - Jobs
                  - Vcenter
                  - Client
                  - Describe
                  - Logs
                  - Items
                  - Jobs
                  - Templates
                  - Clients
                  - Disassociate
                  - Disconnect
                  - From
                  - Services
                  - Finalize
                  - Cutover
                  - Get
                  - Initialize
                  - Lists
                  - Connectors
                  - Export
                  - Errors
                  - Exports
                  - Import
                  - Imports
                  - Managed
                  - Accounts
                  - Actions
                  - ARN
                  - Waves
                  - Mark
                  - As
                  - Archived
                  - Pause
                  - Put
                  - Actions
                  - Removes
                  - Resume
                  - Retry
                  - Data
                  - Start
            /StartTest:
              POST:
                summary: StartTest
                description: >-
                  <p>Launches a Test Instance for specific Source Servers. This
                  command starts a LAUNCH job whose initiatedBy property is
                  StartTest and changes the SourceServer.lifeCycle.state
                  property to TESTING.</p>
                tags:
                  - Start
                  - Tests
                  - Archive
                  - Applications
                  - Waves
                  - Associate
                  - Applications
                  - Source
                  - Servers
                  - Change
                  - Server
                  - Life
                  - Cycle
                  - States
                  - Create
                  - Connectors
                  - Launch
                  - Configurations
                  - Templates
                  - Replication
                  - Delete
                  - Jobs
                  - Vcenter
                  - Client
                  - Describe
                  - Logs
                  - Items
                  - Jobs
                  - Templates
                  - Clients
                  - Disassociate
                  - Disconnect
                  - From
                  - Services
                  - Finalize
                  - Cutover
                  - Get
                  - Initialize
                  - Lists
                  - Connectors
                  - Export
                  - Errors
                  - Exports
                  - Import
                  - Imports
                  - Managed
                  - Accounts
                  - Actions
                  - ARN
                  - Waves
                  - Mark
                  - As
                  - Archived
                  - Pause
                  - Put
                  - Actions
                  - Removes
                  - Resume
                  - Retry
                  - Data
                  - Start
                  - Tests
            /StopReplication:
              POST:
                summary: StopReplication
                description: <p>Stop Replication.</p>
                tags:
                  - Stop
                  - Replication
                  - Archive
                  - Applications
                  - Waves
                  - Associate
                  - Applications
                  - Source
                  - Servers
                  - Change
                  - Server
                  - Life
                  - Cycle
                  - States
                  - Create
                  - Connectors
                  - Launch
                  - Configurations
                  - Templates
                  - Replication
                  - Delete
                  - Jobs
                  - Vcenter
                  - Client
                  - Describe
                  - Logs
                  - Items
                  - Jobs
                  - Templates
                  - Clients
                  - Disassociate
                  - Disconnect
                  - From
                  - Services
                  - Finalize
                  - Cutover
                  - Get
                  - Initialize
                  - Lists
                  - Connectors
                  - Export
                  - Errors
                  - Exports
                  - Import
                  - Imports
                  - Managed
                  - Accounts
                  - Actions
                  - ARN
                  - Waves
                  - Mark
                  - As
                  - Archived
                  - Pause
                  - Put
                  - Actions
                  - Removes
                  - Resume
                  - Retry
                  - Data
                  - Start
                  - Tests
                  - Stop
            /TerminateTargetInstances:
              POST:
                summary: TerminateTargetInstances
                description: >-
                  <p>Starts a job that terminates specific launched EC2 Test and
                  Cutover instances. This command will not work for any Source
                  Server with a lifecycle.state of TESTING, CUTTING_OVER, or
                  CUTOVER.</p>
                tags:
                  - Terminate
                  - Target
                  - Instances
                  - Archive
                  - Applications
                  - Waves
                  - Associate
                  - Applications
                  - Source
                  - Servers
                  - Change
                  - Server
                  - Life
                  - Cycle
                  - States
                  - Create
                  - Connectors
                  - Launch
                  - Configurations
                  - Templates
                  - Replication
                  - Delete
                  - Jobs
                  - Vcenter
                  - Client
                  - Describe
                  - Logs
                  - Items
                  - Jobs
                  - Templates
                  - Clients
                  - Disassociate
                  - Disconnect
                  - From
                  - Services
                  - Finalize
                  - Cutover
                  - Get
                  - Initialize
                  - Lists
                  - Connectors
                  - Export
                  - Errors
                  - Exports
                  - Import
                  - Imports
                  - Managed
                  - Accounts
                  - Actions
                  - ARN
                  - Waves
                  - Mark
                  - As
                  - Archived
                  - Pause
                  - Put
                  - Actions
                  - Removes
                  - Resume
                  - Retry
                  - Data
                  - Start
                  - Tests
                  - Stop
                  - Terminate
                  - Target
                  - Instances
            /UnarchiveApplication:
              POST:
                summary: UnarchiveApplication
                description: <p>Unarchive application.</p>
                tags:
                  - Unarchive
                  - Applications
                  - Archive
                  - Applications
                  - Waves
                  - Associate
                  - Applications
                  - Source
                  - Servers
                  - Change
                  - Server
                  - Life
                  - Cycle
                  - States
                  - Create
                  - Connectors
                  - Launch
                  - Configurations
                  - Templates
                  - Replication
                  - Delete
                  - Jobs
                  - Vcenter
                  - Client
                  - Describe
                  - Logs
                  - Items
                  - Jobs
                  - Templates
                  - Clients
                  - Disassociate
                  - Disconnect
                  - From
                  - Services
                  - Finalize
                  - Cutover
                  - Get
                  - Initialize
                  - Lists
                  - Connectors
                  - Export
                  - Errors
                  - Exports
                  - Import
                  - Imports
                  - Managed
                  - Accounts
                  - Actions
                  - ARN
                  - Waves
                  - Mark
                  - As
                  - Archived
                  - Pause
                  - Put
                  - Actions
                  - Removes
                  - Resume
                  - Retry
                  - Data
                  - Start
                  - Tests
                  - Stop
                  - Terminate
                  - Target
                  - Instances
                  - Unarchive
            /UnarchiveWave:
              POST:
                summary: UnarchiveWave
                description: <p>Unarchive wave.</p>
                tags:
                  - Unarchive
                  - Waves
                  - Archive
                  - Applications
                  - Waves
                  - Associate
                  - Applications
                  - Source
                  - Servers
                  - Change
                  - Server
                  - Life
                  - Cycle
                  - States
                  - Create
                  - Connectors
                  - Launch
                  - Configurations
                  - Templates
                  - Replication
                  - Delete
                  - Jobs
                  - Vcenter
                  - Client
                  - Describe
                  - Logs
                  - Items
                  - Jobs
                  - Templates
                  - Clients
                  - Disassociate
                  - Disconnect
                  - From
                  - Services
                  - Finalize
                  - Cutover
                  - Get
                  - Initialize
                  - Lists
                  - Connectors
                  - Export
                  - Errors
                  - Exports
                  - Import
                  - Imports
                  - Managed
                  - Accounts
                  - Actions
                  - ARN
                  - Waves
                  - Mark
                  - As
                  - Archived
                  - Pause
                  - Put
                  - Actions
                  - Removes
                  - Resume
                  - Retry
                  - Data
                  - Start
                  - Tests
                  - Stop
                  - Terminate
                  - Target
                  - Instances
                  - Unarchive
            /UpdateApplication:
              POST:
                summary: UpdateApplication
                description: <p>Update application.</p>
                tags:
                  - Update
                  - Applications
                  - Archive
                  - Applications
                  - Waves
                  - Associate
                  - Applications
                  - Source
                  - Servers
                  - Change
                  - Server
                  - Life
                  - Cycle
                  - States
                  - Create
                  - Connectors
                  - Launch
                  - Configurations
                  - Templates
                  - Replication
                  - Delete
                  - Jobs
                  - Vcenter
                  - Client
                  - Describe
                  - Logs
                  - Items
                  - Jobs
                  - Templates
                  - Clients
                  - Disassociate
                  - Disconnect
                  - From
                  - Services
                  - Finalize
                  - Cutover
                  - Get
                  - Initialize
                  - Lists
                  - Connectors
                  - Export
                  - Errors
                  - Exports
                  - Import
                  - Imports
                  - Managed
                  - Accounts
                  - Actions
                  - ARN
                  - Waves
                  - Mark
                  - As
                  - Archived
                  - Pause
                  - Put
                  - Actions
                  - Removes
                  - Resume
                  - Retry
                  - Data
                  - Start
                  - Tests
                  - Stop
                  - Terminate
                  - Target
                  - Instances
                  - Unarchive
                  - Update
            /UpdateConnector:
              POST:
                summary: UpdateConnector
                description: <p>Update Connector.</p>
                tags:
                  - Update
                  - Connectors
                  - Archive
                  - Applications
                  - Waves
                  - Associate
                  - Applications
                  - Source
                  - Servers
                  - Change
                  - Server
                  - Life
                  - Cycle
                  - States
                  - Create
                  - Connectors
                  - Launch
                  - Configurations
                  - Templates
                  - Replication
                  - Delete
                  - Jobs
                  - Vcenter
                  - Client
                  - Describe
                  - Logs
                  - Items
                  - Jobs
                  - Templates
                  - Clients
                  - Disassociate
                  - Disconnect
                  - From
                  - Services
                  - Finalize
                  - Cutover
                  - Get
                  - Initialize
                  - Lists
                  - Connectors
                  - Export
                  - Errors
                  - Exports
                  - Import
                  - Imports
                  - Managed
                  - Accounts
                  - Actions
                  - ARN
                  - Waves
                  - Mark
                  - As
                  - Archived
                  - Pause
                  - Put
                  - Actions
                  - Removes
                  - Resume
                  - Retry
                  - Data
                  - Start
                  - Tests
                  - Stop
                  - Terminate
                  - Target
                  - Instances
                  - Unarchive
                  - Update
            /UpdateLaunchConfiguration:
              POST:
                summary: UpdateLaunchConfiguration
                description: >-
                  <p>Updates multiple LaunchConfigurations by Source Server
                  ID.</p>
                tags:
                  - Update
                  - Launch
                  - Configurations
                  - Archive
                  - Applications
                  - Waves
                  - Associate
                  - Applications
                  - Source
                  - Servers
                  - Change
                  - Server
                  - Life
                  - Cycle
                  - States
                  - Create
                  - Connectors
                  - Launch
                  - Configurations
                  - Templates
                  - Replication
                  - Delete
                  - Jobs
                  - Vcenter
                  - Client
                  - Describe
                  - Logs
                  - Items
                  - Jobs
                  - Templates
                  - Clients
                  - Disassociate
                  - Disconnect
                  - From
                  - Services
                  - Finalize
                  - Cutover
                  - Get
                  - Initialize
                  - Lists
                  - Connectors
                  - Export
                  - Errors
                  - Exports
                  - Import
                  - Imports
                  - Managed
                  - Accounts
                  - Actions
                  - ARN
                  - Waves
                  - Mark
                  - As
                  - Archived
                  - Pause
                  - Put
                  - Actions
                  - Removes
                  - Resume
                  - Retry
                  - Data
                  - Start
                  - Tests
                  - Stop
                  - Terminate
                  - Target
                  - Instances
                  - Unarchive
                  - Update
            /UpdateLaunchConfigurationTemplate:
              POST:
                summary: UpdateLaunchConfigurationTemplate
                description: >-
                  <p>Updates an existing Launch Configuration Template by
                  ID.</p>
                tags:
                  - Update
                  - Launch
                  - Configurations
                  - Templates
                  - Archive
                  - Applications
                  - Waves
                  - Associate
                  - Applications
                  - Source
                  - Servers
                  - Change
                  - Server
                  - Life
                  - Cycle
                  - States
                  - Create
                  - Connectors
                  - Launch
                  - Configurations
                  - Templates
                  - Replication
                  - Delete
                  - Jobs
                  - Vcenter
                  - Client
                  - Describe
                  - Logs
                  - Items
                  - Jobs
                  - Templates
                  - Clients
                  - Disassociate
                  - Disconnect
                  - From
                  - Services
                  - Finalize
                  - Cutover
                  - Get
                  - Initialize
                  - Lists
                  - Connectors
                  - Export
                  - Errors
                  - Exports
                  - Import
                  - Imports
                  - Managed
                  - Accounts
                  - Actions
                  - ARN
                  - Waves
                  - Mark
                  - As
                  - Archived
                  - Pause
                  - Put
                  - Actions
                  - Removes
                  - Resume
                  - Retry
                  - Data
                  - Start
                  - Tests
                  - Stop
                  - Terminate
                  - Target
                  - Instances
                  - Unarchive
                  - Update
            /UpdateReplicationConfiguration:
              POST:
                summary: UpdateReplicationConfiguration
                description: >-
                  <p>Allows you to update multiple ReplicationConfigurations by
                  Source Server ID.</p>
                tags:
                  - Update
                  - Replication
                  - Configurations
                  - Archive
                  - Applications
                  - Waves
                  - Associate
                  - Applications
                  - Source
                  - Servers
                  - Change
                  - Server
                  - Life
                  - Cycle
                  - States
                  - Create
                  - Connectors
                  - Launch
                  - Configurations
                  - Templates
                  - Replication
                  - Delete
                  - Jobs
                  - Vcenter
                  - Client
                  - Describe
                  - Logs
                  - Items
                  - Jobs
                  - Templates
                  - Clients
                  - Disassociate
                  - Disconnect
                  - From
                  - Services
                  - Finalize
                  - Cutover
                  - Get
                  - Initialize
                  - Lists
                  - Connectors
                  - Export
                  - Errors
                  - Exports
                  - Import
                  - Imports
                  - Managed
                  - Accounts
                  - Actions
                  - ARN
                  - Waves
                  - Mark
                  - As
                  - Archived
                  - Pause
                  - Put
                  - Actions
                  - Removes
                  - Resume
                  - Retry
                  - Data
                  - Start
                  - Tests
                  - Stop
                  - Terminate
                  - Target
                  - Instances
                  - Unarchive
                  - Update
            /UpdateReplicationConfigurationTemplate:
              POST:
                summary: UpdateReplicationConfigurationTemplate
                description: >-
                  <p>Updates multiple ReplicationConfigurationTemplates by
                  ID.</p>
                tags:
                  - Update
                  - Replication
                  - Configurations
                  - Templates
                  - Archive
                  - Applications
                  - Waves
                  - Associate
                  - Applications
                  - Source
                  - Servers
                  - Change
                  - Server
                  - Life
                  - Cycle
                  - States
                  - Create
                  - Connectors
                  - Launch
                  - Configurations
                  - Templates
                  - Replication
                  - Delete
                  - Jobs
                  - Vcenter
                  - Client
                  - Describe
                  - Logs
                  - Items
                  - Jobs
                  - Templates
                  - Clients
                  - Disassociate
                  - Disconnect
                  - From
                  - Services
                  - Finalize
                  - Cutover
                  - Get
                  - Initialize
                  - Lists
                  - Connectors
                  - Export
                  - Errors
                  - Exports
                  - Import
                  - Imports
                  - Managed
                  - Accounts
                  - Actions
                  - ARN
                  - Waves
                  - Mark
                  - As
                  - Archived
                  - Pause
                  - Put
                  - Actions
                  - Removes
                  - Resume
                  - Retry
                  - Data
                  - Start
                  - Tests
                  - Stop
                  - Terminate
                  - Target
                  - Instances
                  - Unarchive
                  - Update
            /UpdateSourceServer:
              POST:
                summary: UpdateSourceServer
                description: <p>Update Source Server.</p>
                tags:
                  - Update
                  - Source
                  - Server
                  - Archive
                  - Applications
                  - Waves
                  - Associate
                  - Applications
                  - Source
                  - Servers
                  - Change
                  - Server
                  - Life
                  - Cycle
                  - States
                  - Create
                  - Connectors
                  - Launch
                  - Configurations
                  - Templates
                  - Replication
                  - Delete
                  - Jobs
                  - Vcenter
                  - Client
                  - Describe
                  - Logs
                  - Items
                  - Jobs
                  - Templates
                  - Clients
                  - Disassociate
                  - Disconnect
                  - From
                  - Services
                  - Finalize
                  - Cutover
                  - Get
                  - Initialize
                  - Lists
                  - Connectors
                  - Export
                  - Errors
                  - Exports
                  - Import
                  - Imports
                  - Managed
                  - Accounts
                  - Actions
                  - ARN
                  - Waves
                  - Mark
                  - As
                  - Archived
                  - Pause
                  - Put
                  - Actions
                  - Removes
                  - Resume
                  - Retry
                  - Data
                  - Start
                  - Tests
                  - Stop
                  - Terminate
                  - Target
                  - Instances
                  - Unarchive
                  - Update
            /UpdateSourceServerReplicationType:
              POST:
                summary: UpdateSourceServerReplicationType
                description: >-
                  <p>Allows you to change between the AGENT_BASED replication
                  type and the SNAPSHOT_SHIPPING replication type.</p>
                tags:
                  - Update
                  - Source
                  - Server
                  - Replication
                  - Types
                  - Archive
                  - Applications
                  - Waves
                  - Associate
                  - Applications
                  - Source
                  - Servers
                  - Change
                  - Server
                  - Life
                  - Cycle
                  - States
                  - Create
                  - Connectors
                  - Launch
                  - Configurations
                  - Templates
                  - Replication
                  - Delete
                  - Jobs
                  - Vcenter
                  - Client
                  - Describe
                  - Logs
                  - Items
                  - Jobs
                  - Templates
                  - Clients
                  - Disassociate
                  - Disconnect
                  - From
                  - Services
                  - Finalize
                  - Cutover
                  - Get
                  - Initialize
                  - Lists
                  - Connectors
                  - Export
                  - Errors
                  - Exports
                  - Import
                  - Imports
                  - Managed
                  - Accounts
                  - Actions
                  - ARN
                  - Waves
                  - Mark
                  - As
                  - Archived
                  - Pause
                  - Put
                  - Actions
                  - Removes
                  - Resume
                  - Retry
                  - Data
                  - Start
                  - Tests
                  - Stop
                  - Terminate
                  - Target
                  - Instances
                  - Unarchive
                  - Update
                  - Types
            /UpdateWave:
              POST:
                summary: UpdateWave
                description: <p>Update
                tags:
                  - Update
                  - Waves
                  - Archive
                  - Applications
                  - Waves
                  - Associate
                  - Applications
                  - Source
                  - Servers
                  - Change
                  - Server
                  - Life
                  - Cycle
                  - States
                  - Create
                  - Connectors
                  - Launch
                  - Configurations
                  - Templates
                  - Replication
                  - Delete
                  - Jobs
                  - Vcenter
                  - Client
                  - Describe
                  - Logs
                  - Items
                  - Jobs
                  - Templates
                  - Clients
                  - Disassociate
                  - Disconnect
                  - From
                  - Services
                  - Finalize
                  - Cutover
                  - Get
                  - Initialize
                  - Lists
                  - Connectors
                  - Export
                  - Errors
                  - Exports
                  - Import
                  - Imports
                  - Managed
                  - Accounts
                  - Actions
                  - ARN
                  - Waves
                  - Mark
                  - As
                  - Archived
                  - Pause
                  - Put
                  - Actions
                  - Removes
                  - Resume
                  - Retry
                  - Data
                  - Start
                  - Tests
                  - Stop
                  - Terminate
                  - Target
                  - Instances
                  - Unarchive
                  - Update
                  - Types
    overlays:
      - type: APIs.io Search
        url: overlays/mgn-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/mgn-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:mgn
  - name: pca-connector-ad
    description: >-
      <p>Amazon Web Services Private CA Connector for Active Directory creates a
      connector between Amazon Web Services Private CA and Active Directory (AD)
      that enables you to provision security certificates for AD signed by a
      private CA that you own. For more information, see <a
      href="https://docs.aws.amazon.com/privateca/latest/userguide/ad-connector.html">Amazon
      Web Services Private CA Connector for Active Directory</a>.</p>
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
            title: pca-connector-ad
          paths:
            /connectors:
              GET:
                summary: ListConnectors
                description: >-
                  <p>Lists the connectors that you created by using the <a
                  href="https://docs.aws.amazon.com/pca-connector-ad/latest/APIReference/API_CreateConnector">https://docs.aws.amazon.com/pca-connector-ad/latest/APIReference/API_CreateConnector</a>
                  action.</p>
                tags:
                  - Lists
                  - Connectors
                  - Connectors
            /directoryRegistrations:
              GET:
                summary: ListDirectoryRegistrations
                description: >-
                  <p>Lists the directory registrations that you created by using
                  the <a
                  href="https://docs.aws.amazon.com/pca-connector-ad/latest/APIReference/API_CreateDirectoryRegistration">https://docs.aws.amazon.com/pca-connector-ad/latest/APIReference/API_CreateDirectoryRegistration</a>
                  action.</p>
                tags:
                  - Lists
                  - Directory
                  - Registrations
                  - Connectors
                  - Registrations
            /directoryRegistrations/{DirectoryRegistrationArn}/servicePrincipalNames/{ConnectorArn}:
              GET:
                summary: GetServicePrincipalName
                description: >-
                  <p>Lists the service principal name that the connector uses to
                  authenticate with Active Directory.</p>
                tags:
                  - Get
                  - Services
                  - Principals
                  - Names
                  - Connectors
                  - Registrations
                  - Directory
                  - Registrations
                  - ARN
                  - Services
                  - Principals
                  - Names
                  - Connectors
            /templates:
              GET:
                summary: ListTemplates
                description: >-
                  <p>Lists the templates, if any, that are associated with a
                  connector.</p>
                tags:
                  - Lists
                  - Templates
                  - Connectors
                  - Registrations
                  - Directory
                  - Registrations
                  - ARN
                  - Services
                  - Principals
                  - Names
                  - Connectors
                  - Templates
            /templates/{TemplateArn}/accessControlEntries:
              GET:
                summary: ListTemplateGroupAccessControlEntries
                description: <p>Lists group access control entries you created. </p>
                tags:
                  - Lists
                  - Templates
                  - Group
                  - Access
                  - Control
                  - Entries
                  - Connectors
                  - Registrations
                  - Directory
                  - Registrations
                  - ARN
                  - Services
                  - Principals
                  - Names
                  - Connectors
                  - Templates
                  - Templates
                  - Access
                  - Control
                  - Entries
            /connectors/{ConnectorArn}:
              GET:
                summary: GetConnector
                description: >-
                  <p>Lists information about your connector. You specify the
                  connector on input by its ARN (Amazon Resource Name). </p>
                tags:
                  - Get
                  - Connectors
                  - Connectors
                  - Registrations
                  - Directory
                  - Registrations
                  - ARN
                  - Services
                  - Principals
                  - Names
                  - Connectors
                  - Templates
                  - Templates
                  - Access
                  - Control
                  - Entries
            /directoryRegistrations/{DirectoryRegistrationArn}:
              GET:
                summary: GetDirectoryRegistration
                description: >-
                  <p>A structure that contains information about your directory
                  registration.</p>
                tags:
                  - Get
                  - Directory
                  - Registrations
                  - Connectors
                  - Registrations
                  - Directory
                  - Registrations
                  - ARN
                  - Services
                  - Principals
                  - Names
                  - Connectors
                  - Templates
                  - Templates
                  - Access
                  - Control
                  - Entries
            /templates/{TemplateArn}:
              PATCH:
                summary: UpdateTemplate
                description: >-
                  <p>Update template configuration to define the information
                  included in certificates.</p>
                tags:
                  - Update
                  - Templates
                  - Connectors
                  - Registrations
                  - Directory
                  - Registrations
                  - ARN
                  - Services
                  - Principals
                  - Names
                  - Connectors
                  - Templates
                  - Templates
                  - Access
                  - Control
                  - Entries
            /templates/{TemplateArn}/accessControlEntries/{GroupSecurityIdentifier}:
              PATCH:
                summary: UpdateTemplateGroupAccessControlEntry
                description: >-
                  <p>Update a group access control entry you created using <a
                  href="https://docs.aws.amazon.com/pca-connector-ad/latest/APIReference/API_CreateTemplateGroupAccessControlEntry.html">CreateTemplateGroupAccessControlEntry</a>.
                  </p>
                tags:
                  - Update
                  - Templates
                  - Group
                  - Access
                  - Control
                  - Entry
                  - Connectors
                  - Registrations
                  - Directory
                  - Registrations
                  - ARN
                  - Services
                  - Principals
                  - Names
                  - Connectors
                  - Templates
                  - Templates
                  - Access
                  - Control
                  - Entries
                  - Group
                  - Security
                  - Identifiers
            /directoryRegistrations/{DirectoryRegistrationArn}/servicePrincipalNames:
              GET:
                summary: ListServicePrincipalNames
                description: >-
                  <p>Lists the service principal names that the connector uses
                  to authenticate with Active Directory.</p>
                tags:
                  - Lists
                  - Services
                  - Principals
                  - Names
                  - Connectors
                  - Registrations
                  - Directory
                  - Registrations
                  - ARN
                  - Services
                  - Principals
                  - Names
                  - Connectors
                  - Templates
                  - Templates
                  - Access
                  - Control
                  - Entries
                  - Group
                  - Security
                  - Identifiers
            /tags/{ResourceArn}:
              DELETE:
                summary: UntagResource
                description: <p>Removes one or more tags from your res
                tags:
                  - Untag
                  - Resources
                  - Connectors
                  - Registrations
                  - Directory
                  - Registrations
                  - ARN
                  - Services
                  - Principals
                  - Names
                  - Connectors
                  - Templates
                  - Templates
                  - Access
                  - Control
                  - Entries
                  - Group
                  - Security
                  - Identifiers
                  - Resour
    overlays:
      - type: APIs.io Search
        url: overlays/pca-connector-ad-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/pca-connector-ad-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:pca-connector-ad
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---