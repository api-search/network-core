---
name: Channels
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/channels.png
url: https://example.com/apis/channels.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Channels
apis:
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
                  - With
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
                  - With
                  - Voice
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
                  - With
                  - Voice
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
                  - With
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
                  - Bans
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
                  - Bans
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
                  - Bans
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
                  - Bans
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
                  - Bans
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
                  - Bans
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
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
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
                  - With
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
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
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
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
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
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
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
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
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
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
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
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
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
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
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
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
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
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
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
                  - Voice
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
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
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
                  - Voice
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
                  - Voice
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
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
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
                  - Voice
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
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
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
                  - Voice
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
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
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
                  - Voice
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
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
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
                  - Voice
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
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
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
                  - Voice
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
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
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
                  - Voice
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
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
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
                  - Voice
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
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
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
                  - Voice
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
                  - Ban
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
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
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
                  - Voice
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
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
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
                  - Voice
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
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
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
                  - Voice
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
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
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
                  - Voice
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
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
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
                  - Voice
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
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
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
                  - Voice
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
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
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
                  - Voice
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
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
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
                  - Voice
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
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
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
                  - Voice
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
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
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
                  - Voice
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
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
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
                  - Voice
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
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
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
                  - Voice
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
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
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
                  - Voice
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
                  - Voice
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
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
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
                  - Voice
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
                  - Voice
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
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
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
                  - Voice
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
                  - Voice
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
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
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
                  - Voice
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
                  - Voice
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
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
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
                  - Voice
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
                  - Voice
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
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
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
                  - Voice
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
                  - Voice
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
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
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
                  - Voice
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
                  - Voice
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
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
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
                  - Voice
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
                  - Voice
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
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
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
                  - Voice
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
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
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
                  - Voice
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
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
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
                  - Voice
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
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
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
                  - Voice
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
                  - Voice
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
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
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
                  - Voice
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
                  - Voice
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
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
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
                  - Voice
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
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
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
                  - Voice
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
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
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
                  - Voice
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
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
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
                  - Voice
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
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
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
                  - Voice
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
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
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
                  - Voice
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
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
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
                  - Voice
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
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
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
                  - Voice
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
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
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
                  - Voice
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
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
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
                  - Voice
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
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
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
                  - Voice
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
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
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
                  - Voice
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
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
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
                  - Voice
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
                  - Voice
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
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
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
                  - Voice
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
                  - Voice
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
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
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
                  - Voice
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
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
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
                  - Voice
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
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
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
                  - Voice
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
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
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
                  - Voice
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
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
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
                  - Voice
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
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
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
                  - Voice
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
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
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
                  - Voice
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
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
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
                  - Voice
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
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
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
                  - Voice
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
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
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
                  - Voice
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
                  - Voice
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
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
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
                  - Voice
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
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
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
                  - Voice
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
                  - Voice
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
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
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
                  - Voice
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
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
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
                  - Voice
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
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
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
                  - Voice
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
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
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
                  - Voice
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
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
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
                  - Voice
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
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
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
                  - Voice
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
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
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
                  - Voice
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
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
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
                  - Voice
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
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
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
                  - Voice
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
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
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
                  - Voice
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
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
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
                  - Voice
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
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
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
                  - Voice
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
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
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
                  - Voice
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
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
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
                  - Voice
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
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
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
                  - Voice
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
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
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
                  - Voice
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
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
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
                  - Voice
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
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
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
                  - Voice
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
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
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
                  - Voice
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
  - name: chime-sdk-messaging
    description: >-
      <p>The Amazon Chime SDK messaging APIs in this section allow software
      developers to send and receive messages in custom messaging applications.
      These APIs depend on the frameworks provided by the Amazon Chime SDK
      identity APIs. For more information about the messaging APIs, see <a
      href="https://docs.aws.amazon.com/chime/latest/APIReference/API_Operations_Amazon_Chime_SDK_Messaging.html">Amazon
      Chime SDK messaging</a>.</p>
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
            title: chime-sdk-messaging
          paths:
            /channels/{channelArn}/channel-flow:
              PUT:
                summary: AssociateChannelFlow
                description: >-
                  <p>Associates a channel flow with a channel. Once associated,
                  all messages to that channel go through channel flow
                  processors. To stop processing, use the
                  <code>DisassociateChannelFlow</code> API.</p> <note> <p>Only
                  administrators or channel moderators can associate a channel
                  flow. The <code>x-amz-chime-bearer</code> request header is
                  mandatory. Use the ARN of the <code>AppInstanceUser</code> or
                  <code>AppInstanceBot</code> that makes the API call as the
                  value in the header.</p> </note>
                tags:
                  - Associate
                  - Channels
                  - Flow
                  - ARN
                  - Channels
                  - Flow
            /channels/{channelArn}/memberships?operation=batch-create:
              POST:
                summary: BatchCreateChannelMembership
                description: >-
                  <p>Adds a specified number of users and bots to a channel.
                  </p>
                tags:
                  - Batches
                  - Create
                  - Channels
                  - Membership
                  - ARN
                  - Channels
                  - Flow
                  - Memberships
                  - Create
            /channels/{channelArn}?operation=channel-flow-callback:
              POST:
                summary: ChannelFlowCallback
                description: >-
                  <p>Calls back Amazon Chime SDK messaging with a processing
                  response message. This should be invoked from the processor
                  Lambda. This is a developer API.</p> <p>You can return one of
                  the following processing responses:</p> <ul> <li> <p>Update
                  message content or metadata</p> </li> <li> <p>Deny a
                  message</p> </li> <li> <p>Make no changes to the message</p>
                  </li> </ul>
                tags:
                  - Channels
                  - Flow
                  - Callback
                  - ARN
                  - Channels
                  - Flow
                  - Memberships
                  - Create
                  - '?operation=channel'
                  - Callback
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
                  Use the ARN of the <code>AppInstanceUser</code> or
                  <code>AppInstanceBot</code> that makes the API call as the
                  value in the header.</p> </note>
                tags:
                  - Lists
                  - Channels
                  - ARN
                  - Channels
                  - Flow
                  - Memberships
                  - Create
                  - '?operation=channel'
                  - Callback
                  - Channels
            /channels/{channelArn}/bans:
              GET:
                summary: ListChannelBans
                description: >-
                  <p>Lists all the users and bots banned from a particular
                  channel.</p> <note> <p>The <code>x-amz-chime-bearer</code>
                  request header is mandatory. Use the ARN of the
                  <code>AppInstanceUser</code> or <code>AppInstanceBot</code>
                  that makes the API call as the value in the header.</p>
                  </note>
                tags:
                  - Lists
                  - Channels
                  - Bans
                  - ARN
                  - Channels
                  - Flow
                  - Memberships
                  - Create
                  - '?operation=channel'
                  - Callback
                  - Channels
                  - Bans
            /channel-flows:
              GET:
                summary: ListChannelFlows
                description: >-
                  <p>Returns a paginated lists of all the channel flows created
                  under a single Chime. This is a developer API.</p>
                tags:
                  - Lists
                  - Channels
                  - Flows
                  - ARN
                  - Channels
                  - Flow
                  - Memberships
                  - Create
                  - '?operation=channel'
                  - Callback
                  - Channels
                  - Bans
                  - Flows
            /channels/{channelArn}/memberships:
              GET:
                summary: ListChannelMemberships
                description: >-
                  <p>Lists all channel memberships in a channel.</p> <note>
                  <p>The <code>x-amz-chime-bearer</code> request header is
                  mandatory. Use the ARN of the <code>AppInstanceUser</code> or
                  <code>AppInstanceBot</code> that makes the API call as the
                  value in the header.</p> </note> <p>If you want to list the
                  channels to which a specific app instance user belongs, see
                  the <a
                  href="https://docs.aws.amazon.com/chime/latest/APIReference/API_messaging-chime_ListChannelMembershipsForAppInstanceUser.html">ListChannelMembershipsForAppInstanceUser</a>
                  API.</p>
                tags:
                  - Lists
                  - Channels
                  - Memberships
                  - ARN
                  - Channels
                  - Flow
                  - Memberships
                  - Create
                  - '?operation=channel'
                  - Callback
                  - Channels
                  - Bans
                  - Flows
                  - Memberships
            /channels/{channelArn}/moderators:
              GET:
                summary: ListChannelModerators
                description: >-
                  <p>Lists all the moderators for a channel.</p> <note> <p>The
                  <code>x-amz-chime-bearer</code> request header is mandatory.
                  Use the ARN of the <code>AppInstanceUser</code> or
                  <code>AppInstanceBot</code> that makes the API call as the
                  value in the header.</p> </note>
                tags:
                  - Lists
                  - Channels
                  - Moderators
                  - ARN
                  - Channels
                  - Flow
                  - Memberships
                  - Create
                  - '?operation=channel'
                  - Callback
                  - Channels
                  - Bans
                  - Flows
                  - Memberships
                  - Moderators
            /channels/{channelArn}:
              PUT:
                summary: UpdateChannel
                description: >-
                  <p>Update a channel's attributes.</p> <p> <b>Restriction</b>:
                  You can't change a channel's privacy. </p> <note> <p>The
                  <code>x-amz-chime-bearer</code> request header is mandatory.
                  Use the ARN of the <code>AppInstanceUser</code> or
                  <code>AppInstanceBot</code> that makes the API call as the
                  value in the header.</p> </note>
                tags:
                  - Update
                  - Channels
                  - ARN
                  - Channels
                  - Flow
                  - Memberships
                  - Create
                  - '?operation=channel'
                  - Callback
                  - Channels
                  - Bans
                  - Flows
                  - Memberships
                  - Moderators
            /channels/{channelArn}/bans/{memberArn}:
              GET:
                summary: DescribeChannelBan
                description: >-
                  <p>Returns the full details of a channel ban.</p> <note>
                  <p>The <code>x-amz-chime-bearer</code> request header is
                  mandatory. Use the ARN of the <code>AppInstanceUser</code> or
                  <code>AppInstanceBot</code> that makes the API call as the
                  value in the header.</p> </note>
                tags:
                  - Describe
                  - Channels
                  - Ban
                  - ARN
                  - Channels
                  - Flow
                  - Memberships
                  - Create
                  - '?operation=channel'
                  - Callback
                  - Channels
                  - Bans
                  - Flows
                  - Memberships
                  - Moderators
                  - Members
            /channel-flows/{channelFlowArn}:
              PUT:
                summary: UpdateChannelFlow
                description: >-
                  <p>Updates channel flow attributes. This is a developer
                  API.</p>
                tags:
                  - Update
                  - Channels
                  - Flow
                  - ARN
                  - Channels
                  - Flow
                  - Memberships
                  - Create
                  - '?operation=channel'
                  - Callback
                  - Channels
                  - Bans
                  - Flows
                  - Memberships
                  - Moderators
                  - Members
            /channels/{channelArn}/memberships/{memberArn}:
              GET:
                summary: DescribeChannelMembership
                description: >-
                  <p>Returns the full details of a user's channel
                  membership.</p> <note> <p>The <code>x-amz-chime-bearer</code>
                  request header is mandatory. Use the ARN of the
                  <code>AppInstanceUser</code> or <code>AppInstanceBot</code>
                  that makes the API call as the value in the header.</p>
                  </note>
                tags:
                  - Describe
                  - Channels
                  - Membership
                  - ARN
                  - Channels
                  - Flow
                  - Memberships
                  - Create
                  - '?operation=channel'
                  - Callback
                  - Channels
                  - Bans
                  - Flows
                  - Memberships
                  - Moderators
                  - Members
            /channels/{channelArn}/messages/{messageId}:
              PUT:
                summary: UpdateChannelMessage
                description: >-
                  <p>Updates the content of a message.</p> <note> <p>The
                  <code>x-amz-chime-bearer</code> request header is mandatory.
                  Use the ARN of the <code>AppInstanceUser</code> or
                  <code>AppInstanceBot</code> that makes the API call as the
                  value in the header.</p> </note>
                tags:
                  - Update
                  - Channels
                  - Messages
                  - ARN
                  - Channels
                  - Flow
                  - Memberships
                  - Create
                  - '?operation=channel'
                  - Callback
                  - Channels
                  - Bans
                  - Flows
                  - Memberships
                  - Moderators
                  - Members
                  - Messages
                  - Messages
                  - Identifiers
            /channels/{channelArn}/moderators/{channelModeratorArn}:
              GET:
                summary: DescribeChannelModerator
                description: >-
                  <p>Returns the full details of a single ChannelModerator.</p>
                  <note> <p>The <code>x-amz-chime-bearer</code> request header
                  is mandatory. Use the <code>AppInstanceUserArn</code> of the
                  user that makes the API call as the value in the header.</p>
                  </note>
                tags:
                  - Describe
                  - Channels
                  - Moderators
                  - ARN
                  - Channels
                  - Flow
                  - Memberships
                  - Create
                  - '?operation=channel'
                  - Callback
                  - Channels
                  - Bans
                  - Flows
                  - Memberships
                  - Moderators
                  - Members
                  - Messages
                  - Messages
                  - Identifiers
                  - Moderators
            /app-instances/{appInstanceArn}/streaming-configurations:
              PUT:
                summary: PutMessagingStreamingConfigurations
                description: >-
                  <p>Sets the data streaming configuration for an
                  <code>AppInstance</code>. For more information, see <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/streaming-export.html">Streaming
                  messaging data</a> in the <i>Amazon Chime SDK Developer
                  Guide</i>.</p>
                tags:
                  - Put
                  - Messaging
                  - Streaming
                  - Configurations
                  - ARN
                  - Channels
                  - Flow
                  - Memberships
                  - Create
                  - '?operation=channel'
                  - Callback
                  - Channels
                  - Bans
                  - Flows
                  - Memberships
                  - Moderators
                  - Members
                  - Messages
                  - Messages
                  - Identifiers
                  - Moderators
                  - Instances
                  - Streaming
                  - Configurations
            /channels/{channelArn}?scope=app-instance-user-membership:
              GET:
                summary: DescribeChannelMembershipForAppInstanceUser
                description: >-
                  <p> Returns the details of a channel based on the membership
                  of the specified <code>AppInstanceUser</code> or
                  <code>AppInstanceBot</code>.</p> <note> <p>The
                  <code>x-amz-chime-bearer</code> request header is mandatory.
                  Use the ARN of the <code>AppInstanceUser</code> or
                  <code>AppInstanceBot</code> that makes the API call as the
                  value in the header.</p> </note>
                tags:
                  - Describe
                  - Channels
                  - Membership
                  - For
                  - Applications
                  - Instances
                  - Users
                  - ARN
                  - Channels
                  - Flow
                  - Memberships
                  - Create
                  - '?operation=channel'
                  - Callback
                  - Channels
                  - Bans
                  - Flows
                  - Memberships
                  - Moderators
                  - Members
                  - Messages
                  - Messages
                  - Identifiers
                  - Moderators
                  - Instances
                  - Streaming
                  - Configurations
                  - '?scope=app'
                  - Users
                  - Membership
            /channels/{channelArn}?scope=app-instance-user-moderated-channel:
              GET:
                summary: DescribeChannelModeratedByAppInstanceUser
                description: >-
                  <p>Returns the full details of a channel moderated by the
                  specified <code>AppInstanceUser</code> or
                  <code>AppInstanceBot</code>.</p> <note> <p>The
                  <code>x-amz-chime-bearer</code> request header is mandatory.
                  Use the ARN of the <code>AppInstanceUser</code> or
                  <code>AppInstanceBot</code> that makes the API call as the
                  value in the header.</p> </note>
                tags:
                  - Describe
                  - Channels
                  - Moderated
                  - By
                  - Applications
                  - Instances
                  - Users
                  - ARN
                  - Channels
                  - Flow
                  - Memberships
                  - Create
                  - '?operation=channel'
                  - Callback
                  - Channels
                  - Bans
                  - Flows
                  - Memberships
                  - Moderators
                  - Members
                  - Messages
                  - Messages
                  - Identifiers
                  - Moderators
                  - Instances
                  - Streaming
                  - Configurations
                  - '?scope=app'
                  - Users
                  - Membership
                  - Moderated
            /channels/{channelArn}/channel-flow/{channelFlowArn}:
              DELETE:
                summary: DisassociateChannelFlow
                description: >-
                  <p>Disassociates a channel flow from all its channels. Once
                  disassociated, all messages to that channel stop going through
                  the channel flow processor.</p> <note> <p>Only administrators
                  or channel moderators can disassociate a channel flow.</p>
                  <p>The <code>x-amz-chime-bearer</code> request header is
                  mandatory. Use the ARN of the <code>AppInstanceUser</code> or
                  <code>AppInstanceBot</code> that makes the API call as the
                  value in the header.</p> </note>
                tags:
                  - Disassociate
                  - Channels
                  - Flow
                  - ARN
                  - Channels
                  - Flow
                  - Memberships
                  - Create
                  - '?operation=channel'
                  - Callback
                  - Channels
                  - Bans
                  - Flows
                  - Memberships
                  - Moderators
                  - Members
                  - Messages
                  - Messages
                  - Identifiers
                  - Moderators
                  - Instances
                  - Streaming
                  - Configurations
                  - '?scope=app'
                  - Users
                  - Membership
                  - Moderated
            /channels/{channelArn}/memberships/{memberArn}/preferences:
              PUT:
                summary: PutChannelMembershipPreferences
                description: >-
                  <p>Sets the membership preferences of an
                  <code>AppInstanceUser</code> or <code>AppInstanceBot</code>
                  for the specified channel. The user or bot must be a member of
                  the channel. Only the user or bot who owns the membership can
                  set preferences. Users or bots in the
                  <code>AppInstanceAdmin</code> and channel moderator roles
                  can't set preferences for other users. Banned users or bots
                  can't set membership preferences for the channel from which
                  they are banned.</p> <note> <p>The x-amz-chime-bearer request
                  header is mandatory. Use the ARN of an
                  <code>AppInstanceUser</code> or <code>AppInstanceBot</code>
                  that makes the API call as the value in the header.</p>
                  </note>
                tags:
                  - Put
                  - Channels
                  - Membership
                  - Preferences
                  - ARN
                  - Channels
                  - Flow
                  - Memberships
                  - Create
                  - '?operation=channel'
                  - Callback
                  - Channels
                  - Bans
                  - Flows
                  - Memberships
                  - Moderators
                  - Members
                  - Messages
                  - Messages
                  - Identifiers
                  - Moderators
                  - Instances
                  - Streaming
                  - Configurations
                  - '?scope=app'
                  - Users
                  - Membership
                  - Moderated
                  - Preferences
            /channels/{channelArn}/messages/{messageId}?scope=message-status:
              GET:
                summary: GetChannelMessageStatus
                description: >-
                  <p>Gets message status for a specified <code>messageId</code>.
                  Use this API to determine the intermediate status of messages
                  going through channel flow processing. The API provides an
                  alternative to retrieving message status if the event was not
                  received because a client wasn't connected to a websocket.
                  </p> <p>Messages can have any one of these statuses.</p> <dl>
                  <dt>SENT</dt> <dd> <p>Message processed successfully</p> </dd>
                  <dt>PENDING</dt> <dd> <p>Ongoing processing</p> </dd>
                  <dt>FAILED</dt> <dd> <p>Processing failed</p> </dd>
                  <dt>DENIED</dt> <dd> <p>Message denied by the processor</p>
                  </dd> </dl> <note> <ul> <li> <p>This API does not return
                  statuses for denied messages, because we don't store them once
                  the processor denies them. </p> </li> <li> <p>Only the message
                  sender can invoke this API.</p> </li> <li> <p>The
                  <code>x-amz-chime-bearer</code> request header is mandatory.
                  Use the ARN of the <code>AppInstanceUser</code> or
                  <code>AppInstanceBot</code> that makes the API call as the
                  value in the header.</p> </li> </ul> </note>
                tags:
                  - Get
                  - Channels
                  - Messages
                  - Status
                  - ARN
                  - Channels
                  - Flow
                  - Memberships
                  - Create
                  - '?operation=channel'
                  - Callback
                  - Channels
                  - Bans
                  - Flows
                  - Memberships
                  - Moderators
                  - Members
                  - Messages
                  - Messages
                  - Identifiers
                  - Moderators
                  - Instances
                  - Streaming
                  - Configurations
                  - '?scope=app'
                  - Users
                  - Membership
                  - Moderated
                  - Preferences
                  - '?scope=message'
                  - Status
            /endpoints/messaging-session:
              GET:
                summary: GetMessagingSessionEndpoint
                description: <p>The details of the endpoint for the messaging session.</p>
                tags:
                  - Get
                  - Messaging
                  - Sessions
                  - Endpoints
                  - ARN
                  - Channels
                  - Flow
                  - Memberships
                  - Create
                  - '?operation=channel'
                  - Callback
                  - Channels
                  - Bans
                  - Flows
                  - Memberships
                  - Moderators
                  - Members
                  - Messages
                  - Messages
                  - Identifiers
                  - Moderators
                  - Instances
                  - Streaming
                  - Configurations
                  - '?scope=app'
                  - Users
                  - Membership
                  - Moderated
                  - Preferences
                  - '?scope=message'
                  - Status
                  - Endpoints
                  - Messaging
                  - Sessions
            /channels?scope=app-instance-user-memberships:
              GET:
                summary: ListChannelMembershipsForAppInstanceUser
                description: >-
                  <p> Lists all channels that an <code>AppInstanceUser</code> or
                  <code>AppInstanceBot</code> is a part of. Only an
                  <code>AppInstanceAdmin</code> can call the API with a user ARN
                  that is not their own. </p> <note> <p>The
                  <code>x-amz-chime-bearer</code> request header is mandatory.
                  Use the ARN of the <code>AppInstanceUser</code> or
                  <code>AppInstanceBot</code> that makes the API call as the
                  value in the header.</p> </note>
                tags:
                  - Lists
                  - Channels
                  - Memberships
                  - For
                  - Applications
                  - Instances
                  - Users
                  - ARN
                  - Channels
                  - Flow
                  - Memberships
                  - Create
                  - '?operation=channel'
                  - Callback
                  - Channels
                  - Bans
                  - Flows
                  - Memberships
                  - Moderators
                  - Members
                  - Messages
                  - Messages
                  - Identifiers
                  - Moderators
                  - Instances
                  - Streaming
                  - Configurations
                  - '?scope=app'
                  - Users
                  - Membership
                  - Moderated
                  - Preferences
                  - '?scope=message'
                  - Status
                  - Endpoints
                  - Messaging
                  - Sessions
                  - Channels
            /channels/{channelArn}/messages:
              POST:
                summary: SendChannelMessage
                description: >-
                  <p>Sends a message to a particular channel that the member is
                  a part of.</p> <note> <p>The <code>x-amz-chime-bearer</code>
                  request header is mandatory. Use the ARN of the
                  <code>AppInstanceUser</code> or <code>AppInstanceBot</code>
                  that makes the API call as the value in the header.</p>
                  <p>Also, <code>STANDARD</code> messages can be up to 4KB in
                  size and contain metadata. Metadata is arbitrary, and you can
                  use it in a variety of ways, such as containing a link to an
                  attachment.</p> <p> <code>CONTROL</code> messages are limited
                  to 30 bytes and do not contain metadata.</p> </note>
                tags:
                  - Send
                  - Channels
                  - Messages
                  - ARN
                  - Channels
                  - Flow
                  - Memberships
                  - Create
                  - '?operation=channel'
                  - Callback
                  - Channels
                  - Bans
                  - Flows
                  - Memberships
                  - Moderators
                  - Members
                  - Messages
                  - Messages
                  - Identifiers
                  - Moderators
                  - Instances
                  - Streaming
                  - Configurations
                  - '?scope=app'
                  - Users
                  - Membership
                  - Moderated
                  - Preferences
                  - '?scope=message'
                  - Status
                  - Endpoints
                  - Messaging
                  - Sessions
                  - Channels
            /channels?scope=channel-flow-associations:
              GET:
                summary: ListChannelsAssociatedWithChannelFlow
                description: >-
                  <p>Lists all channels associated with a specified channel
                  flow. You can associate a channel flow with multiple channels,
                  but you can only associate a channel with one channel flow.
                  This is a developer API.</p>
                tags:
                  - Lists
                  - Channels
                  - Associated
                  - With
                  - Channels
                  - Flow
                  - ARN
                  - Channels
                  - Flow
                  - Memberships
                  - Create
                  - '?operation=channel'
                  - Callback
                  - Channels
                  - Bans
                  - Flows
                  - Memberships
                  - Moderators
                  - Members
                  - Messages
                  - Messages
                  - Identifiers
                  - Moderators
                  - Instances
                  - Streaming
                  - Configurations
                  - '?scope=app'
                  - Users
                  - Membership
                  - Moderated
                  - Preferences
                  - '?scope=message'
                  - Status
                  - Endpoints
                  - Messaging
                  - Sessions
                  - Channels
                  - Channels
                  - Associations
            /channels?scope=app-instance-user-moderated-channels:
              GET:
                summary: ListChannelsModeratedByAppInstanceUser
                description: >-
                  <p>A list of the channels moderated by an
                  <code>AppInstanceUser</code>.</p> <note> <p>The
                  <code>x-amz-chime-bearer</code> request header is mandatory.
                  Use the ARN of the <code>AppInstanceUser</code> or
                  <code>AppInstanceBot</code> that makes the API call as the
                  value in the header.</p> </note>
                tags:
                  - Lists
                  - Channels
                  - Moderated
                  - By
                  - Applications
                  - Instances
                  - Users
                  - ARN
                  - Channels
                  - Flow
                  - Memberships
                  - Create
                  - '?operation=channel'
                  - Callback
                  - Channels
                  - Bans
                  - Flows
                  - Memberships
                  - Moderators
                  - Members
                  - Messages
                  - Messages
                  - Identifiers
                  - Moderators
                  - Instances
                  - Streaming
                  - Configurations
                  - '?scope=app'
                  - Users
                  - Membership
                  - Moderated
                  - Preferences
                  - '?scope=message'
                  - Status
                  - Endpoints
                  - Messaging
                  - Sessions
                  - Channels
                  - Channels
                  - Associations
            /channels/{channelArn}/subchannels:
              GET:
                summary: ListSubChannels
                description: >-
                  <p>Lists all the SubChannels in an elastic channel when given
                  a channel ID. Available only to the app instance admins and
                  channel moderators of elastic channels.</p>
                tags:
                  - Lists
                  - Sub
                  - Channels
                  - ARN
                  - Channels
                  - Flow
                  - Memberships
                  - Create
                  - '?operation=channel'
                  - Callback
                  - Channels
                  - Bans
                  - Flows
                  - Memberships
                  - Moderators
                  - Members
                  - Messages
                  - Messages
                  - Identifiers
                  - Moderators
                  - Instances
                  - Streaming
                  - Configurations
                  - '?scope=app'
                  - Users
                  - Membership
                  - Moderated
                  - Preferences
                  - '?scope=message'
                  - Status
                  - Endpoints
                  - Messaging
                  - Sessions
                  - Channels
                  - Channels
                  - Associations
                  - Sub Channels
            /tags:
              GET:
                summary: ListTagsForResource
                description: >-
                  <p>Lists the tags applied to an Amazon Chime SDK messaging
                  resource.</p>
                tags:
                  - Lists
                  - Tags
                  - For
                  - Resources
                  - ARN
                  - Channels
                  - Flow
                  - Memberships
                  - Create
                  - '?operation=channel'
                  - Callback
                  - Channels
                  - Bans
                  - Flows
                  - Memberships
                  - Moderators
                  - Members
                  - Messages
                  - Messages
                  - Identifiers
                  - Moderators
                  - Instances
                  - Streaming
                  - Configurations
                  - '?scope=app'
                  - Users
                  - Membership
                  - Moderated
                  - Preferences
                  - '?scope=message'
                  - Status
                  - Endpoints
                  - Messaging
                  - Sessions
                  - Channels
                  - Channels
                  - Associations
                  - Sub Channels
                  - Tags
            /channels/{channelArn}/expiration-settings:
              PUT:
                summary: PutChannelExpirationSettings
                description: >-
                  <p>Sets the number of days before the channel is automatically
                  deleted.</p> <note> <ul> <li> <p>A background process deletes
                  expired channels within 6 hours of expiration. Actual deletion
                  times may vary.</p> </li> <li> <p>Expired channels that have
                  not yet been deleted appear as active, and you can update
                  their expiration settings. The system honors the new
                  settings.</p> </li> <li> <p>The
                  <code>x-amz-chime-bearer</code> request header is mandatory.
                  Use the ARN of the <code>AppInstanceUser</code> or
                  <code>AppInstanceBot</code> that makes the API call as the
                  value in the header.</p> </li> </ul> </note>
                tags:
                  - Put
                  - Channels
                  - Expiration
                  - Settings
                  - ARN
                  - Channels
                  - Flow
                  - Memberships
                  - Create
                  - '?operation=channel'
                  - Callback
                  - Channels
                  - Bans
                  - Flows
                  - Memberships
                  - Moderators
                  - Members
                  - Messages
                  - Messages
                  - Identifiers
                  - Moderators
                  - Instances
                  - Streaming
                  - Configurations
                  - '?scope=app'
                  - Users
                  - Membership
                  - Moderated
                  - Preferences
                  - '?scope=message'
                  - Status
                  - Endpoints
                  - Messaging
                  - Sessions
                  - Channels
                  - Channels
                  - Associations
                  - Sub Channels
                  - Tags
                  - Expiration
                  - Settings
            /channels/{channelArn}/messages/{messageId}?operation=redact:
              POST:
                summary: RedactChannelMessage
                description: >-
                  <p>Redacts message content, but not metadata. The message
                  exists in the back end, but the action returns null content,
                  and the state shows as redacted.</p> <note> <p>The
                  <code>x-amz-chime-bearer</code> request header is mandatory.
                  Use the ARN of the <code>AppInstanceUser</code> or
                  <code>AppInstanceBot</code> that makes the API call as the
                  value in the header.</p> </note>
                tags:
                  - Redact
                  - Channels
                  - Messages
                  - ARN
                  - Channels
                  - Flow
                  - Memberships
                  - Create
                  - '?operation=channel'
                  - Callback
                  - Channels
                  - Bans
                  - Flows
                  - Memberships
                  - Moderators
                  - Members
                  - Messages
                  - Messages
                  - Identifiers
                  - Moderators
                  - Instances
                  - Streaming
                  - Configurations
                  - '?scope=app'
                  - Users
                  - Membership
                  - Moderated
                  - Preferences
                  - '?scope=message'
                  - Status
                  - Endpoints
                  - Messaging
                  - Sessions
                  - Channels
                  - Channels
                  - Associations
                  - Sub Channels
                  - Tags
                  - Expiration
                  - Settings
                  - '?operation=redact'
            /channels?operation=search:
              POST:
                summary: SearchChannels
                description: >-
                  <p>Allows the <code>ChimeBearer</code> to search channels by
                  channel members. Users or bots can search across the channels
                  that they belong to. Users in the
                  <code>AppInstanceAdmin</code> role can search across all
                  channels.</p> <p>The <code>x-amz-chime-bearer</code> request
                  header is mandatory. Use the ARN of the
                  <code>AppInstanceUser</code> or <code>AppInstanceBot</code>
                  that makes the API call as the value in the header.</p>
                tags:
                  - Search
                  - Channels
                  - ARN
                  - Channels
                  - Flow
                  - Memberships
                  - Create
                  - '?operation=channel'
                  - Callback
                  - Channels
                  - Bans
                  - Flows
                  - Memberships
                  - Moderators
                  - Members
                  - Messages
                  - Messages
                  - Identifiers
                  - Moderators
                  - Instances
                  - Streaming
                  - Configurations
                  - '?scope=app'
                  - Users
                  - Membership
                  - Moderated
                  - Preferences
                  - '?scope=message'
                  - Status
                  - Endpoints
                  - Messaging
                  - Sessions
                  - Channels
                  - Channels
                  - Associations
                  - Sub Channels
                  - Tags
                  - Expiration
                  - Settings
                  - '?operation=redact'
                  - Channels
            /tags?operation=tag-resource:
              POST:
                summary: TagResource
                description: >-
                  <p>Applies the specified tags to the specified Amazon Chime
                  SDK messaging resource.</p>
                tags:
                  - Tags
                  - Resources
                  - ARN
                  - Channels
                  - Flow
                  - Memberships
                  - Create
                  - '?operation=channel'
                  - Callback
                  - Channels
                  - Bans
                  - Flows
                  - Memberships
                  - Moderators
                  - Members
                  - Messages
                  - Messages
                  - Identifiers
                  - Moderators
                  - Instances
                  - Streaming
                  - Configurations
                  - '?scope=app'
                  - Users
                  - Membership
                  - Moderated
                  - Preferences
                  - '?scope=message'
                  - Status
                  - Endpoints
                  - Messaging
                  - Sessions
                  - Channels
                  - Channels
                  - Associations
                  - Sub Channels
                  - Tags
                  - Expiration
                  - Settings
                  - '?operation=redact'
                  - Channels
                  - Tags
                  - Resources
            /tags?operation=untag-resource:
              POST:
                summary: UntagResource
                description: >-
                  <p>Removes the specified tags from the specified Amazon Chime
                  SDK messaging resource.</p>
                tags:
                  - Untag
                  - Resources
                  - ARN
                  - Channels
                  - Flow
                  - Memberships
                  - Create
                  - '?operation=channel'
                  - Callback
                  - Channels
                  - Bans
                  - Flows
                  - Memberships
                  - Moderators
                  - Members
                  - Messages
                  - Messages
                  - Identifiers
                  - Moderators
                  - Instances
                  - Streaming
                  - Configurations
                  - '?scope=app'
                  - Users
                  - Membership
                  - Moderated
                  - Preferences
                  - '?scope=message'
                  - Status
                  - Endpoints
                  - Messaging
                  - Sessions
                  - Channels
                  - Channels
                  - Associations
                  - Sub Channels
                  - Tags
                  - Expiration
                  - Settings
                  - '?operation=redact'
                  - Channels
                  - Tags
                  - Resources
                  - Tags
            /channels/{channelArn}/readMarker:
              PUT:
                summary: UpdateChannelReadMarker
                description: >-
                  <p>The details of the time when a user last read messages in a
                  channel.</p> <note> <p>The <code>x-amz-chime-bearer</code>
                  request header is mandatory. Use the ARN of the
                  <code>AppInstanceUser</code> or <code>AppInstanceBot</code>
                  that makes the API call as the value in the header.</
                tags:
                  - Update
                  - Channels
                  - Read
                  - Marker
                  - ARN
                  - Channels
                  - Flow
                  - Memberships
                  - Create
                  - '?operation=channel'
                  - Callback
                  - Channels
                  - Bans
                  - Flows
                  - Memberships
                  - Moderators
                  - Members
                  - Messages
                  - Messages
                  - Identifiers
                  - Moderators
                  - Instances
                  - Streaming
                  - Configurations
                  - '?scope=app'
                  - Users
                  - Membership
                  - Moderated
                  - Preferences
                  - '?scope=message'
                  - Status
                  - Endpoints
                  - Messaging
                  - Sessions
                  - Channels
                  - Channels
                  - Associations
                  - Sub Channels
                  - Tags
                  - Expiration
                  - Settings
                  - '?operation=redact'
                  - Channels
                  - Tags
                  - Resources
                  - Tags
                  - Read
                  - Mark
    overlays:
      - type: APIs.io Search
        url: overlays/chime-sdk-messaging-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/chime-sdk-messaging-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:chime-sdk-messaging
  - name: codeguruprofiler
    description: >-
      <p> This section provides documentation for the Amazon CodeGuru Profiler
      API operations. </p> <p> Amazon CodeGuru Profiler collects runtime
      performance data from your live applications, and provides recommendations
      that can help you fine-tune your application performance. Using machine
      learning algorithms, CodeGuru Profiler can help you find your most
      expensive lines of code and suggest ways you can improve efficiency and
      remove CPU bottlenecks. </p> <p> Amazon CodeGuru Profiler provides
      different visualizations of profiling data to help you identify what code
      is running on the CPU, see how much time is consumed, and suggest ways to
      reduce CPU utilization. </p> <note> <p>Amazon CodeGuru Profiler currently
      supports applications written in all Java virtual machine (JVM) languages
      and Python. While CodeGuru Profiler supports both visualizations and
      recommendations for applications written in Java, it can also generate
      visualizations and a subset of recommendations for applications written in
      other JVM languages and Python.</p> </note> <p> For more information, see
      <a
      href="https://docs.aws.amazon.com/codeguru/latest/profiler-ug/what-is-codeguru-profiler.html">What
      is Amazon CodeGuru Profiler</a> in the <i>Amazon CodeGuru Profiler User
      Guide</i>. </p>
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
            title: codeguruprofiler
          paths:
            /profilingGroups/{profilingGroupName}/notificationConfiguration:
              GET:
                summary: GetNotificationConfiguration
                description: >-
                  <p>Get the current configuration for anomaly notifications for
                  a profiling group.</p>
                tags:
                  - Get
                  - Notifications
                  - Configurations
                  - Groups
                  - Profiling
                  - Group
                  - Names
                  - Notifications
                  - Configurations
            /profilingGroups/{profilingGroupName}/frames/-/metrics:
              POST:
                summary: BatchGetFrameMetricData
                description: >-
                  <p> Returns the time series of values for a requested list of
                  frame metrics from a time period.</p>
                tags:
                  - Batches
                  - Get
                  - Frames
                  - Metrics
                  - Data
                  - Groups
                  - Profiling
                  - Group
                  - Names
                  - Notifications
                  - Configurations
                  - Frames
                  - Metrics
            /profilingGroups/{profilingGroupName}/configureAgent:
              POST:
                summary: ConfigureAgent
                description: >-
                  <p> Used by profiler agents to report their current state and
                  to receive remote configuration updates. For example,
                  <code>ConfigureAgent</code> can be used to tell an agent
                  whether to profile or not and for how long to return profiling
                  data. </p>
                tags:
                  - Configure
                  - Agent
                  - Groups
                  - Profiling
                  - Group
                  - Names
                  - Notifications
                  - Configurations
                  - Frames
                  - Metrics
                  - Configure
                  - Agent
            /profilingGroups:
              GET:
                summary: ListProfilingGroups
                description: >-
                  <p> Returns a list of profiling groups. The profiling groups
                  are returned as <a
                  href="https://docs.aws.amazon.com/codeguru/latest/profiler-api/API_ProfilingGroupDescription.html">
                  <code>ProfilingGroupDescription</code> </a> objects. </p>
                tags:
                  - Lists
                  - Profiling
                  - Groups
                  - Groups
                  - Profiling
                  - Group
                  - Names
                  - Notifications
                  - Configurations
                  - Frames
                  - Metrics
                  - Configure
                  - Agent
            /profilingGroups/{profilingGroupName}:
              PUT:
                summary: UpdateProfilingGroup
                description: <p>Updates a profiling group.</p>
                tags:
                  - Update
                  - Profiling
                  - Group
                  - Groups
                  - Profiling
                  - Group
                  - Names
                  - Notifications
                  - Configurations
                  - Frames
                  - Metrics
                  - Configure
                  - Agent
            /internal/findingsReports:
              GET:
                summary: GetFindingsReportAccountSummary
                description: >-
                  <p> Returns a list of <a
                  href="https://docs.aws.amazon.com/codeguru/latest/profiler-api/API_FindingsReportSummary.html">
                  <code>FindingsReportSummary</code> </a> objects that contain
                  analysis results for all profiling groups in your AWS account.
                  </p>
                tags:
                  - Get
                  - Findings
                  - Reports
                  - Account
                  - Summaries
                  - Groups
                  - Profiling
                  - Group
                  - Names
                  - Notifications
                  - Configurations
                  - Frames
                  - Metrics
                  - Configure
                  - Agent
                  - Reports
            /profilingGroups/{profilingGroupName}/policy:
              GET:
                summary: GetPolicy
                description: >-
                  <p> Returns the JSON-formatted resource-based policy on a
                  profiling group. </p>
                tags:
                  - Get
                  - Policies
                  - Groups
                  - Profiling
                  - Group
                  - Names
                  - Notifications
                  - Configurations
                  - Frames
                  - Metrics
                  - Configure
                  - Agent
                  - Reports
                  - Policies
            /profilingGroups/{profilingGroupName}/profile:
              GET:
                summary: GetProfile
                description: >-
                  <p> Gets the aggregated profile of a profiling group for a
                  specified time range. Amazon CodeGuru Profiler collects posted
                  agent profiles for a profiling group into aggregated profiles.
                  </p> <pre><code> &lt;note&gt; &lt;p&gt; Because aggregated
                  profiles expire over time &lt;code&gt;GetProfile&lt;/code&gt;
                  is not idempotent. &lt;/p&gt; &lt;/note&gt; &lt;p&gt; Specify
                  the time range for the requested aggregated profile using 1 or
                  2 of the following parameters:
                  &lt;code&gt;startTime&lt;/code&gt;,
                  &lt;code&gt;endTime&lt;/code&gt;,
                  &lt;code&gt;period&lt;/code&gt;. The maximum time range
                  allowed is 7 days. If you specify all 3 parameters, an
                  exception is thrown. If you specify only
                  &lt;code&gt;period&lt;/code&gt;, the latest aggregated profile
                  is returned. &lt;/p&gt; &lt;p&gt; Aggregated profiles are
                  available with aggregation periods of 5 minutes, 1 hour, and 1
                  day, aligned to UTC. The aggregation period of an aggregated
                  profile determines how long it is retained. For more
                  information, see &lt;a
                  href=&quot;https://docs.aws.amazon.com/codeguru/latest/profiler-api/API_AggregatedProfileTime.html&quot;&gt;
                  &lt;code&gt;AggregatedProfileTime&lt;/code&gt; &lt;/a&gt;. The
                  aggregated profile's aggregation period determines how long it
                  is retained by CodeGuru Profiler. &lt;/p&gt; &lt;ul&gt;
                  &lt;li&gt; &lt;p&gt; If the aggregation period is 5 minutes,
                  the aggregated profile is retained for 15 days. &lt;/p&gt;
                  &lt;/li&gt; &lt;li&gt; &lt;p&gt; If the aggregation period is
                  1 hour, the aggregated profile is retained for 60 days.
                  &lt;/p&gt; &lt;/li&gt; &lt;li&gt; &lt;p&gt; If the aggregation
                  period is 1 day, the aggregated profile is retained for 3
                  years. &lt;/p&gt; &lt;/li&gt; &lt;/ul&gt; &lt;p&gt;There are
                  two use cases for calling
                  &lt;code&gt;GetProfile&lt;/code&gt;.&lt;/p&gt; &lt;ol&gt;
                  &lt;li&gt; &lt;p&gt; If you want to return an aggregated
                  profile that already exists, use &lt;a
                  href=&quot;https://docs.aws.amazon.com/codeguru/latest/profiler-api/API_ListProfileTimes.html&quot;&gt;
                  &lt;code&gt;ListProfileTimes&lt;/code&gt; &lt;/a&gt; to view
                  the time ranges of existing aggregated profiles. Use them in a
                  &lt;code&gt;GetProfile&lt;/code&gt; request to return a
                  specific, existing aggregated profile. &lt;/p&gt; &lt;/li&gt;
                  &lt;li&gt; &lt;p&gt; If you want to return an aggregated
                  profile for a time range that doesn't align with an existing
                  aggregated profile, then CodeGuru Profiler makes a best effort
                  to combine existing aggregated profiles from the requested
                  time range and return them as one aggregated profile.
                  &lt;/p&gt; &lt;p&gt; If aggregated profiles do not exist for
                  the full time range requested, then aggregated profiles for a
                  smaller time range are returned. For example, if the requested
                  time range is from 00:00 to 00:20, and the existing aggregated
                  profiles are from 00:15 and 00:25, then the aggregated
                  profiles from 00:15 to 00:20 are returned. &lt;/p&gt;
                  &lt;/li&gt; &lt;/ol&gt; </code></pre>
                tags:
                  - Get
                  - Profiles
                  - Groups
                  - Profiling
                  - Group
                  - Names
                  - Notifications
                  - Configurations
                  - Frames
                  - Metrics
                  - Configure
                  - Agent
                  - Reports
                  - Policies
                  - Profiles
            /internal/profilingGroups/{profilingGroupName}/recommendations:
              GET:
                summary: GetRecommendations
                description: >-
                  <p> Returns a list of <a
                  href="https://docs.aws.amazon.com/codeguru/latest/profiler-api/API_Recommendation.html">
                  <code>Recommendation</code> </a> objects that contain
                  recommendations for a profiling group for a given time period.
                  A list of <a
                  href="https://docs.aws.amazon.com/codeguru/latest/profiler-api/API_Anomaly.html">
                  <code>Anomaly</code> </a> objects that contains details about
                  anomalies detected in the profiling group for the same time
                  period is also returned. </p>
                tags:
                  - Get
                  - Recommendations
                  - Groups
                  - Profiling
                  - Group
                  - Names
                  - Notifications
                  - Configurations
                  - Frames
                  - Metrics
                  - Configure
                  - Agent
                  - Reports
                  - Policies
                  - Profiles
                  - Recommendations
            /internal/profilingGroups/{profilingGroupName}/findingsReports:
              GET:
                summary: ListFindingsReports
                description: >-
                  <p>List the available reports for a given profiling group and
                  time range.</p>
                tags:
                  - Lists
                  - Findings
                  - Reports
                  - Groups
                  - Profiling
                  - Group
                  - Names
                  - Notifications
                  - Configurations
                  - Frames
                  - Metrics
                  - Configure
                  - Agent
                  - Reports
                  - Policies
                  - Profiles
                  - Recommendations
                  - Findings
            /profilingGroups/{profilingGroupName}/profileTimes:
              GET:
                summary: ListProfileTimes
                description: >-
                  <p>Lists the start times of the available aggregated profiles
                  of a profiling group for an aggregation period within the
                  specified time range.</p>
                tags:
                  - Lists
                  - Profiles
                  - Times
                  - Groups
                  - Profiling
                  - Group
                  - Names
                  - Notifications
                  - Configurations
                  - Frames
                  - Metrics
                  - Configure
                  - Agent
                  - Reports
                  - Policies
                  - Profiles
                  - Recommendations
                  - Findings
                  - Times
            /tags/{resourceArn}:
              DELETE:
                summary: UntagResource
                description: <p> Use to remove one or more tags from a resource. </p>
                tags:
                  - Untag
                  - Resources
                  - Groups
                  - Profiling
                  - Group
                  - Names
                  - Notifications
                  - Configurations
                  - Frames
                  - Metrics
                  - Configure
                  - Agent
                  - Reports
                  - Policies
                  - Profiles
                  - Recommendations
                  - Findings
                  - Times
                  - ARN
            /profilingGroups/{profilingGroupName}/agentProfile:
              POST:
                summary: PostAgentProfile
                description: >-
                  <p> Submits profiling data to an aggregated profile of a
                  profiling group. To get an aggregated profile that is created
                  with this profiling data, use <a
                  href="https://docs.aws.amazon.com/codeguru/latest/profiler-api/API_GetProfile.html">
                  <code>GetProfile</code> </a>. </p>
                tags:
                  - Posts
                  - Agent
                  - Profiles
                  - Groups
                  - Profiling
                  - Group
                  - Names
                  - Notifications
                  - Configurations
                  - Frames
                  - Metrics
                  - Configure
                  - Agent
                  - Reports
                  - Policies
                  - Profiles
                  - Recommendations
                  - Findings
                  - Times
                  - ARN
            /profilingGroups/{profilingGroupName}/policy/{actionGroup}:
              DELETE:
                summary: RemovePermission
                description: >-
                  <p> Removes permissions from a profiling group's
                  resource-based policy that are provided using an action group.
                  The one supported action group that can be removed is
                  <code>agentPermission</code> which grants
                  <code>ConfigureAgent</code> and <code>PostAgent</code>
                  permissions. For more information, see <a
                  href="https://docs.aws.amazon.com/codeguru/latest/profiler-ug/resource-based-policies.html">Resource-based
                  policies in CodeGuru Profiler</a> in the <i>Amazon CodeGuru
                  Profiler User Guide</i>, <a
                  href="https://docs.aws.amazon.com/codeguru/latest/profiler-api/API_ConfigureAgent.html">
                  <code>ConfigureAgent</code> </a>, and <a
                  href="https://docs.aws.amazon.com/codeguru/latest/profiler-api/API_PostAgentProfile.html">
                  <code>PostAgentProfile</code> </a>. </p>
                tags:
                  - Removes
                  - Permission
                  - Groups
                  - Profiling
                  - Group
                  - Names
                  - Notifications
                  - Configurations
                  - Frames
                  - Metrics
                  - Configure
                  - Agent
                  - Reports
                  - Policies
                  - Profiles
                  - Recommendations
                  - Findings
                  - Times
                  - ARN
                  - Actions
            /profilingGroups/{profilingGroupName}/notificationConfiguration/{channelId}:
              DELETE:
                summary: RemoveNotificationChannel
                description: >-
                  <p>Remove one anomaly notifications channel for a profiling
                  group.</p>
                tags:
                  - Removes
                  - Notifications
                  - Channels
                  - Groups
                  - Profiling
                  - Group
                  - Names
                  - Notifications
                  - Configurations
                  - Frames
                  - Metrics
                  - Configure
                  - Agent
                  - Reports
                  - Policies
                  - Profiles
                  - Recommendations
                  - Findings
                  - Times
                  - ARN
                  - Actions
                  - Channels
                  - Identifiers
            /internal/profilingGroups/{profilingGroupName}/anomalies/{anomalyInstanceId}/feedback:
              POST:
                summary: SubmitFeedback
                description: >-
                  <p>Sends feedback to CodeGuru Profiler about whether the
                  anomaly detected by the analysis is useful o
                tags:
                  - Submit
                  - Feedback
                  - Groups
                  - Profiling
                  - Group
                  - Names
                  - Notifications
                  - Configurations
                  - Frames
                  - Metrics
                  - Configure
                  - Agent
                  - Reports
                  - Policies
                  - Profiles
                  - Recommendations
                  - Findings
                  - Times
                  - ARN
                  - Actions
                  - Channels
                  - Identifiers
                  - Anomalies
                  - Anomaly
                  - Instances
                  - Feedback
    overlays:
      - type: APIs.io Search
        url: overlays/codeguruprofiler-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/codeguruprofiler-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:codeguruprofiler
  - name: devops-guru
    description: >-
      <p> Amazon DevOps Guru is a fully managed service that helps you identify
      anomalous behavior in business critical operational applications. You
      specify the Amazon Web Services resources that you want DevOps Guru to
      cover, then the Amazon CloudWatch metrics and Amazon Web Services
      CloudTrail events related to those resources are analyzed. When anomalous
      behavior is detected, DevOps Guru creates an <i>insight</i> that includes
      recommendations, related events, and related metrics that can help you
      improve your operational applications. For more information, see <a
      href="https://docs.aws.amazon.com/devops-guru/latest/userguide/welcome.html">What
      is Amazon DevOps Guru</a>. </p> <p> You can specify 1 or 2 Amazon Simple
      Notification Service topics so you are notified every time a new insight
      is created. You can also enable DevOps Guru to generate an OpsItem in
      Amazon Web Services Systems Manager for each insight to help you manage
      and track your work addressing insights. </p> <p> To learn about the
      DevOps Guru workflow, see <a
      href="https://docs.aws.amazon.com/devops-guru/latest/userguide/welcome.html#how-it-works">How
      DevOps Guru works</a>. To learn about DevOps Guru concepts, see <a
      href="https://docs.aws.amazon.com/devops-guru/latest/userguide/concepts.html">Concepts
      in DevOps Guru</a>. </p>
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
            title: devops-guru
          paths:
            /channels:
              POST:
                summary: ListNotificationChannels
                description: >-
                  <p> Returns a list of notification channels configured for
                  DevOps Guru. Each notification channel is used to notify you
                  when DevOps Guru generates an insight that contains
                  information about how to improve your operations. The one
                  supported notification channel is Amazon Simple Notification
                  Service (Amazon SNS). </p>
                tags:
                  - Lists
                  - Notifications
                  - Channels
                  - Channels
            /insights/{Id}:
              GET:
                summary: DescribeInsight
                description: >-
                  <p> Returns details about an insight that you specify using
                  its ID. </p>
                tags:
                  - Describe
                  - Insight
                  - Channels
                  - Identifiers
            /accounts/health:
              GET:
                summary: DescribeAccountHealth
                description: >-
                  <p> Returns the number of open reactive insights, the number
                  of open proactive insights, and the number of metrics analyzed
                  in your Amazon Web Services account. Use these numbers to
                  gauge the health of operations in your Amazon Web Services
                  account. </p>
                tags:
                  - Describe
                  - Account
                  - Health
                  - Channels
                  - Identifiers
                  - Accounts
                  - Health
            /accounts/overview:
              POST:
                summary: DescribeAccountOverview
                description: >-
                  <p> For the time range passed in, returns the number of open
                  reactive insight that were created, the number of open
                  proactive insights that were created, and the Mean Time to
                  Recover (MTTR) for all closed reactive insights. </p>
                tags:
                  - Describe
                  - Account
                  - Overview
                  - Channels
                  - Identifiers
                  - Accounts
                  - Health
                  - Overview
            /anomalies/{Id}:
              GET:
                summary: DescribeAnomaly
                description: >-
                  <p> Returns details about an anomaly that you specify using
                  its ID. </p>
                tags:
                  - Describe
                  - Anomaly
                  - Channels
                  - Identifiers
                  - Accounts
                  - Health
                  - Overview
            /event-sources:
              PUT:
                summary: UpdateEventSourcesConfig
                description: >-
                  <p>Enables or disables integration with a service that can be
                  integrated with DevOps Guru. The one service that can be
                  integrated with DevOps Guru is Amazon CodeGuru Profiler, which
                  can produce proactive recommendations which can be stored and
                  viewed in DevOps Guru.</p>
                tags:
                  - Update
                  - Events
                  - Sources
                  - Configurations
                  - Channels
                  - Identifiers
                  - Accounts
                  - Health
                  - Overview
                  - Events
                  - Sources
            /feedback:
              PUT:
                summary: PutFeedback
                description: >-
                  <p> Collects customer feedback about the specified insight.
                  </p>
                tags:
                  - Put
                  - Feedback
                  - Channels
                  - Identifiers
                  - Accounts
                  - Health
                  - Overview
                  - Events
                  - Sources
                  - Feedback
            /organization/health:
              POST:
                summary: DescribeOrganizationHealth
                description: >-
                  <p>Returns active insights, predictive insights, and resource
                  hours analyzed in last hour.</p>
                tags:
                  - Describe
                  - Organizations
                  - Health
                  - Channels
                  - Identifiers
                  - Accounts
                  - Health
                  - Overview
                  - Events
                  - Sources
                  - Feedback
                  - Organizations
            /organization/overview:
              POST:
                summary: DescribeOrganizationOverview
                description: >-
                  <p>Returns an overview of your organization's history based on
                  the specified time range. The overview includes the total
                  reactive and proactive insights.</p>
                tags:
                  - Describe
                  - Organizations
                  - Overview
                  - Channels
                  - Identifiers
                  - Accounts
                  - Health
                  - Overview
                  - Events
                  - Sources
                  - Feedback
                  - Organizations
            /organization/health/resource-collection:
              POST:
                summary: DescribeOrganizationResourceCollectionHealth
                description: >-
                  <p>Provides an overview of your system's health. If additional
                  member accounts are part of your organization, you can filter
                  those accounts using the <code>AccountIds</code> field.</p>
                tags:
                  - Describe
                  - Organizations
                  - Resources
                  - Collections
                  - Health
                  - Channels
                  - Identifiers
                  - Accounts
                  - Health
                  - Overview
                  - Events
                  - Sources
                  - Feedback
                  - Organizations
                  - Resources
                  - Collections
            /accounts/health/resource-collection/{ResourceCollectionType}:
              GET:
                summary: DescribeResourceCollectionHealth
                description: >-
                  <p> Returns the number of open proactive insights, open
                  reactive insights, and the Mean Time to Recover (MTTR) for all
                  closed insights in resource collections in your account. You
                  specify the type of Amazon Web Services resources collection.
                  The two types of Amazon Web Services resource collections
                  supported are Amazon Web Services CloudFormation stacks and
                  Amazon Web Services resources that contain the same Amazon Web
                  Services tag. DevOps Guru can be configured to analyze the
                  Amazon Web Services resources that are defined in the stacks
                  or that are tagged using the same tag <i>key</i>. You can
                  specify up to 500 Amazon Web Services CloudFormation stacks.
                  </p>
                tags:
                  - Describe
                  - Resources
                  - Collections
                  - Health
                  - Channels
                  - Identifiers
                  - Accounts
                  - Health
                  - Overview
                  - Events
                  - Sources
                  - Feedback
                  - Organizations
                  - Resources
                  - Collections
                  - Types
            /service-integrations:
              PUT:
                summary: UpdateServiceIntegration
                description: >-
                  <p> Enables or disables integration with a service that can be
                  integrated with DevOps Guru. The one service that can be
                  integrated with DevOps Guru is Amazon Web Services Systems
                  Manager, which can be used to create an OpsItem for each
                  generated insight. </p>
                tags:
                  - Update
                  - Services
                  - Integrations
                  - Channels
                  - Identifiers
                  - Accounts
                  - Health
                  - Overview
                  - Events
                  - Sources
                  - Feedback
                  - Organizations
                  - Resources
                  - Collections
                  - Types
                  - Services
                  - Integrations
            /cost-estimation:
              PUT:
                summary: StartCostEstimation
                description: >-
                  <p>Starts the creation of an estimate of the monthly cost to
                  analyze your Amazon Web Services resources.</p>
                tags:
                  - Start
                  - Cost
                  - Estimation
                  - Channels
                  - Identifiers
                  - Accounts
                  - Health
                  - Overview
                  - Events
                  - Sources
                  - Feedback
                  - Organizations
                  - Resources
                  - Collections
                  - Types
                  - Services
                  - Integrations
                  - Cost
                  - Estimation
            /resource-collections/{ResourceCollectionType}:
              GET:
                summary: GetResourceCollection
                description: >-
                  <p> Returns lists Amazon Web Services resources that are of
                  the specified resource collection type. The two types of
                  Amazon Web Services resource collections supported are Amazon
                  Web Services CloudFormation stacks and Amazon Web Services
                  resources that contain the same Amazon Web Services tag.
                  DevOps Guru can be configured to analyze the Amazon Web
                  Services resources that are defined in the stacks or that are
                  tagged using the same tag <i>key</i>. You can specify up to
                  500 Amazon Web Services CloudFormation stacks. </p>
                tags:
                  - Get
                  - Resources
                  - Collections
                  - Channels
                  - Identifiers
                  - Accounts
                  - Health
                  - Overview
                  - Events
                  - Sources
                  - Feedback
                  - Organizations
                  - Resources
                  - Collections
                  - Types
                  - Services
                  - Integrations
                  - Cost
                  - Estimation
            /anomalies/insight/{InsightId}:
              POST:
                summary: ListAnomaliesForInsight
                description: >-
                  <p> Returns a list of the anomalies that belong to an insight
                  that you specify using its ID. </p>
                tags:
                  - Lists
                  - Anomalies
                  - For
                  - Insight
                  - Channels
                  - Identifiers
                  - Accounts
                  - Health
                  - Overview
                  - Events
                  - Sources
                  - Feedback
                  - Organizations
                  - Resources
                  - Collections
                  - Types
                  - Services
                  - Integrations
                  - Cost
                  - Estimation
                  - Insight
            /list-log-anomalies:
              POST:
                summary: ListAnomalousLogGroups
                description: >-
                  <p> Returns the list of log groups that contain log anomalies.
                  </p>
                tags:
                  - Lists
                  - Anomalous
                  - Logs
                  - Groups
                  - Channels
                  - Identifiers
                  - Accounts
                  - Health
                  - Overview
                  - Events
                  - Sources
                  - Feedback
                  - Organizations
                  - Resources
                  - Collections
                  - Types
                  - Services
                  - Integrations
                  - Cost
                  - Estimation
                  - Insight
                  - Lists
                  - Logs
                  - Anomalies
            /events:
              POST:
                summary: ListEvents
                description: >-
                  <p> Returns a list of the events emitted by the resources that
                  are evaluated by DevOps Guru. You can use filters to specify
                  which events are returned. </p>
                tags:
                  - Lists
                  - Events
                  - Channels
                  - Identifiers
                  - Accounts
                  - Health
                  - Overview
                  - Events
                  - Sources
                  - Feedback
                  - Organizations
                  - Resources
                  - Collections
                  - Types
                  - Services
                  - Integrations
                  - Cost
                  - Estimation
                  - Insight
                  - Lists
                  - Logs
                  - Anomalies
                  - Events
            /insights:
              POST:
                summary: ListInsights
                description: >-
                  <p> Returns a list of insights in your Amazon Web Services
                  account. You can specify which insights are returned by their
                  start time and status (<code>ONGOING</code>,
                  <code>CLOSED</code>, or <code>ANY</code>). </p>
                tags:
                  - Lists
                  - Insights
                  - Channels
                  - Identifiers
                  - Accounts
                  - Health
                  - Overview
                  - Events
                  - Sources
                  - Feedback
                  - Organizations
                  - Resources
                  - Collections
                  - Types
                  - Services
                  - Integrations
                  - Cost
                  - Estimation
                  - Insight
                  - Lists
                  - Logs
                  - Anomalies
                  - Events
                  - Insights
            /monitoredResources:
              POST:
                summary: ListMonitoredResources
                description: >-
                  <p> Returns the list of all log groups that are being
                  monitored and tagged by DevOps Guru. </p>
                tags:
                  - Lists
                  - Monitored
                  - Resources
                  - Channels
                  - Identifiers
                  - Accounts
                  - Health
                  - Overview
                  - Events
                  - Sources
                  - Feedback
                  - Organizations
                  - Resources
                  - Collections
                  - Types
                  - Services
                  - Integrations
                  - Cost
                  - Estimation
                  - Insight
                  - Lists
                  - Logs
                  - Anomalies
                  - Events
                  - Insights
                  - Resources
            /organization/insights:
              POST:
                summary: ListOrganizationInsights
                description: >-
                  <p>Returns a list of insights associated with the account or
                  OU Id.</p>
                tags:
                  - Lists
                  - Organizations
                  - Insights
                  - Channels
                  - Identifiers
                  - Accounts
                  - Health
                  - Overview
                  - Events
                  - Sources
                  - Feedback
                  - Organizations
                  - Resources
                  - Collections
                  - Types
                  - Services
                  - Integrations
                  - Cost
                  - Estimation
                  - Insight
                  - Lists
                  - Logs
                  - Anomalies
                  - Events
                  - Insights
                  - Resources
            /recommendations:
              POST:
                summary: ListRecommendations
                description: >-
                  <p> Returns a list of a specified insight's recommendations.
                  Each recommendation includes a list of related metrics and a
                  list of related events. </p>
                tags:
                  - Lists
                  - Recommendations
                  - Channels
                  - Identifiers
                  - Accounts
                  - Health
                  - Overview
                  - Events
                  - Sources
                  - Feedback
                  - Organizations
                  - Resources
                  - Collections
                  - Types
                  - Services
                  - Integrations
                  - Cost
                  - Estimation
                  - Insight
                  - Lists
                  - Logs
                  - Anomalies
                  - Events
                  - Insights
                  - Resources
                  - Recommendations
            /channels/{Id}:
              DELETE:
                summary: RemoveNotificationChannel
                description: >-
                  <p> Removes a notification channel from DevOps Guru. A
                  notification channel is used to notify you when DevOps Guru
                  generates an insight that contains information about how to
                  improve your operations. </p>
                tags:
                  - Removes
                  - Notifications
                  - Channels
                  - Channels
                  - Identifiers
                  - Accounts
                  - Health
                  - Overview
                  - Events
                  - Sources
                  - Feedback
                  - Organizations
                  - Resources
                  - Collections
                  - Types
                  - Services
                  - Integrations
                  - Cost
                  - Estimation
                  - Insight
                  - Lists
                  - Logs
                  - Anomalies
                  - Events
                  - Insights
                  - Resources
                  - Recommendations
            /insights/search:
              POST:
                summary: SearchInsights
                description: >-
                  <p> Returns a list of insights in your Amazon Web Services
                  account. You can specify which insights are returned by their
                  start time, one or more statuses (<code>ONGOING</code> or
                  <code>CLOSED</code>), one or more severities
                  (<code>LOW</code>, <code>MEDIUM</code>, and
                  <code>HIGH</code>), and type (<code>REACTIVE</code> or
                  <code>PROACTIVE</code>). </p> <p> Use the <code>Filters</code>
                  parameter to specify status and severity search parameters.
                  Use the <code>Type</code> parameter to specify
                  <code>REACTIVE</code> or <code>PROACTIVE</code> in your
                  search. </p>
                tags:
                  - Search
                  - Insights
                  - Channels
                  - Identifiers
                  - Accounts
                  - Health
                  - Overview
                  - Events
                  - Sources
                  - Feedback
                  - Organizations
                  - Resources
                  - Collections
                  - Types
                  - Services
                  - Integrations
                  - Cost
                  - Estimation
                  - Insight
                  - Lists
                  - Logs
                  - Anomalies
                  - Events
                  - Insights
                  - Resources
                  - Recommendations
                  - Search
            /organization/insights/search:
              POST:
                summary: SearchOrganizationInsights
                description: >-
                  <p> Returns a list of insights in your organization. You can
                  specify which insights are returned by their start time, one
                  or more statuses (<code>ONGOING</code>, <code>CLOSED</code>,
                  and <code>CLOSED</code>), one or more severities
                  (<code>LOW</code>, <code>MEDIUM</code>, and
                  <code>HIGH</code>), and type (<code>REACTIVE</code> or
                  <code>PROACTIVE</code>). </p> <p> Use the <code>Filters</code>
                  parameter to specify status and severity search parameters.
                  Use the <code>Type</code> parameter to specify
                  <code>REACTIVE</code> or <code>PROACTIVE</code> in your
                  search. </p>
                tags:
                  - Search
                  - Organizations
                  - Insights
                  - Channels
                  - Identifiers
                  - Accounts
                  - Health
                  - Overview
                  - Events
                  - Sources
                  - Feedback
                  - Organizations
                  - Resources
                  - Collections
                  - Types
                  - Services
                  - Integrations
                  - Cost
                  - Estimation
                  - Insight
                  - Lists
                  - Logs
                  - Anomalies
                  - Events
                  - Insights
                  - Resources
                  - Recommendations
                  - Search
            /resource-collections:
              PUT:
                summary: UpdateResourceCollection
                description: >-
                  <p> Updates the collection of resources that DevOps Guru
                  analyzes. The two types of Amazon Web Services resource
                  collections supported are Amazon Web Services CloudFormation
                  stacks and Amazon Web Services resources that contain the same
                  Amazon Web Services tag. DevOps Guru can be configured to
                  analyze the Amazon Web Services resources that are defined in
                  the stacks or that are tagged using the same tag <i>key</i>.
                  You can specify up to 500 Amazon Web Services CloudFormation
                  stacks. This method also creates the IAM role required for you
                  to use DevOps 
                tags:
                  - Update
                  - Resources
                  - Collections
                  - Channels
                  - Identifiers
                  - Accounts
                  - Health
                  - Overview
                  - Events
                  - Sources
                  - Feedback
                  - Organizations
                  - Resources
                  - Collections
                  - Types
                  - Services
                  - Integrations
                  - Cost
                  - Estimation
                  - Insight
                  - Lists
                  - Logs
                  - Anomalies
                  - Events
                  - Insights
                  - Resources
                  - Recommendations
                  - Search
                  - Collections
    overlays:
      - type: APIs.io Search
        url: overlays/devops-guru-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/devops-guru-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:devops-guru
  - name: iotanalytics
    description: >-
      <p>IoT Analytics allows you to collect large amounts of device data,
      process messages, and store them. You can then query the data and run
      sophisticated analytics on it. IoT Analytics enables advanced data
      exploration through integration with Jupyter Notebooks and data
      visualization through integration with Amazon QuickSight.</p>
      <p>Traditional analytics and business intelligence tools are designed to
      process structured data. IoT data often comes from devices that record
      noisy processes (such as temperature, motion, or sound). As a result the
      data from these devices can have significant gaps, corrupted messages, and
      false readings that must be cleaned up before analysis can occur. Also,
      IoT data is often only meaningful in the context of other data from
      external sources. </p> <p>IoT Analytics automates the steps required to
      analyze data from IoT devices. IoT Analytics filters, transforms, and
      enriches IoT data before storing it in a time-series data store for
      analysis. You can set up the service to collect only the data you need
      from your devices, apply mathematical transforms to process the data, and
      enrich the data with device-specific metadata such as device type and
      location before storing it. Then, you can analyze your data by running
      queries using the built-in SQL query engine, or perform more complex
      analytics and machine learning inference. IoT Analytics includes pre-built
      models for common IoT use cases so you can answer questions like which
      devices are about to fail or which customers are at risk of abandoning
      their wearable devices.</p>
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
            title: iotanalytics
          paths:
            /messages/batch:
              POST:
                summary: BatchPutMessage
                description: <p>Sends messages to a channel.</p>
                tags:
                  - Batches
                  - Put
                  - Messages
                  - Messages
                  - Batches
            /pipelines/{pipelineName}/reprocessing/{reprocessingId}:
              DELETE:
                summary: CancelPipelineReprocessing
                description: <p>Cancels the reprocessing of data through the pipeline.</p>
                tags:
                  - Cancel
                  - Pipelines
                  - Reprocessing
                  - Messages
                  - Batches
                  - Names
                  - Reprocessing
                  - Identifiers
            /channels:
              GET:
                summary: ListChannels
                description: <p>Retrieves a list of channels.</p>
                tags:
                  - Lists
                  - Channels
                  - Messages
                  - Batches
                  - Names
                  - Reprocessing
                  - Identifiers
                  - Channels
            /datasets:
              GET:
                summary: ListDatasets
                description: <p>Retrieves information about datasets.</p>
                tags:
                  - Lists
                  - Datasets
                  - Messages
                  - Batches
                  - Names
                  - Reprocessing
                  - Identifiers
                  - Channels
                  - Datasets
            /datasets/{datasetName}/content:
              GET:
                summary: GetDatasetContent
                description: <p>Retrieves the contents of a dataset as presigned URIs.</p>
                tags:
                  - Get
                  - Datasets
                  - Content
                  - Messages
                  - Batches
                  - Names
                  - Reprocessing
                  - Identifiers
                  - Channels
                  - Datasets
                  - Content
            /datastores:
              GET:
                summary: ListDatastores
                description: <p>Retrieves a list of data stores.</p>
                tags:
                  - Lists
                  - Data Store
                  - Messages
                  - Batches
                  - Names
                  - Reprocessing
                  - Identifiers
                  - Channels
                  - Datasets
                  - Content
                  - Data Store
            /pipelines:
              GET:
                summary: ListPipelines
                description: <p>Retrieves a list of pipelines.</p>
                tags:
                  - Lists
                  - Pipelines
                  - Messages
                  - Batches
                  - Names
                  - Reprocessing
                  - Identifiers
                  - Channels
                  - Datasets
                  - Content
                  - Data Store
                  - Pipelines
            /channels/{channelName}:
              PUT:
                summary: UpdateChannel
                description: <p>Used to update the settings of a channel.</p>
                tags:
                  - Update
                  - Channels
                  - Messages
                  - Batches
                  - Names
                  - Reprocessing
                  - Identifiers
                  - Channels
                  - Datasets
                  - Content
                  - Data Store
                  - Pipelines
            /datasets/{datasetName}:
              PUT:
                summary: UpdateDataset
                description: <p>Updates the settings of a dataset.</p>
                tags:
                  - Update
                  - Datasets
                  - Messages
                  - Batches
                  - Names
                  - Reprocessing
                  - Identifiers
                  - Channels
                  - Datasets
                  - Content
                  - Data Store
                  - Pipelines
            /datastores/{datastoreName}:
              PUT:
                summary: UpdateDatastore
                description: <p>Used to update the settings of a data store.</p>
                tags:
                  - Update
                  - Data Store
                  - Messages
                  - Batches
                  - Names
                  - Reprocessing
                  - Identifiers
                  - Channels
                  - Datasets
                  - Content
                  - Data Store
                  - Pipelines
            /pipelines/{pipelineName}:
              PUT:
                summary: UpdatePipeline
                description: >-
                  <p>Updates the settings of a pipeline. You must specify both a
                  <code>channel</code> and a <code>datastore</code> activity
                  and, optionally, as many as 23 additional activities in the
                  <code>pipelineActivities</code> array.</p>
                tags:
                  - Update
                  - Pipelines
                  - Messages
                  - Batches
                  - Names
                  - Reprocessing
                  - Identifiers
                  - Channels
                  - Datasets
                  - Content
                  - Data Store
                  - Pipelines
            /logging:
              PUT:
                summary: PutLoggingOptions
                description: >-
                  <p>Sets or updates the IoT Analytics logging options.</p>
                  <p>If you update the value of any <code>loggingOptions</code>
                  field, it takes up to one minute for the change to take
                  effect. Also, if you change the policy attached to the role
                  you specified in the <code>roleArn</code> field (for example,
                  to correct an invalid policy), it takes up to five minutes for
                  that change to take effect. </p>
                tags:
                  - Put
                  - Logging
                  - Options
                  - Messages
                  - Batches
                  - Names
                  - Reprocessing
                  - Identifiers
                  - Channels
                  - Datasets
                  - Content
                  - Data Store
                  - Pipelines
                  - Logging
            /datasets/{datasetName}/contents:
              GET:
                summary: ListDatasetContents
                description: >-
                  <p>Lists information about dataset contents that have been
                  created.</p>
                tags:
                  - Lists
                  - Datasets
                  - Contents
                  - Messages
                  - Batches
                  - Names
                  - Reprocessing
                  - Identifiers
                  - Channels
                  - Datasets
                  - Content
                  - Data Store
                  - Pipelines
                  - Logging
                  - Contents
            /tags:
              DELETE:
                summary: UntagResource
                description: <p>Removes the given tags (metadata) from the resource.</p>
                tags:
                  - Untag
                  - Resources
                  - Messages
                  - Batches
                  - Names
                  - Reprocessing
                  - Identifiers
                  - Channels
                  - Datasets
                  - Content
                  - Data Store
                  - Pipelines
                  - Logging
                  - Contents
                  - Tags
            /pipelineactivities/run:
              POST:
                summary: RunPipelineActivity
                description: >-
                  <p>Simulates the results of running a pipeline activity on a
                  message payload.</p>
                tags:
                  - Runs
                  - Pipelines
                  - Activity
                  - Messages
                  - Batches
                  - Names
                  - Reprocessing
                  - Identifiers
                  - Channels
                  - Datasets
                  - Content
                  - Data Store
                  - Pipelines
                  - Logging
                  - Contents
                  - Tags
                  - Pipeline Activities
                  - Runs
            /channels/{channelName}/sample:
              GET:
                summary: SampleChannelData
                description: >-
                  <p>Retrieves a sample of messages from the specified channel
                  ingested during the specified timeframe. Up to 10 messages can
                  be retrieved.</p>
                tags:
                  - Samples
                  - Channels
                  - Data
                  - Messages
                  - Batches
                  - Names
                  - Reprocessing
                  - Identifiers
                  - Channels
                  - Datasets
                  - Content
                  - Data Store
                  - Pipelines
                  - Logging
                  - Contents
                  - Tags
                  - Pipeline Activities
                  - Runs
                  - Samples
            /pipelines/{pipelineName}/reprocessing:
              POST:
                summary: StartPipelineReprocessing
                description: <p>Starts the reprocessing of raw message data through the pip
                tags:
                  - Start
                  - Pipelines
                  - Reprocessing
                  - Messages
                  - Batches
                  - Names
                  - Reprocessing
                  - Identifiers
                  - Channels
                  - Datasets
                  - Content
                  - Data Store
                  - Pipelines
                  - Logging
                  - Contents
                  - Tags
                  - Pipeline Activities
                  - Runs
                  - Samples
    overlays:
      - type: APIs.io Search
        url: overlays/iotanalytics-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/iotanalytics-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:iotanalytics
  - name: ivs
    description: >-
      <p> <b>Introduction</b> </p> <p>The Amazon Interactive Video Service (IVS)
      API is REST compatible, using a standard HTTP API and an Amazon Web
      Services EventBridge event stream for responses. JSON is used for both
      requests and responses, including errors.</p> <p>The API is an Amazon Web
      Services regional service. For a list of supported regions and Amazon IVS
      HTTPS service endpoints, see the <a
      href="https://docs.aws.amazon.com/general/latest/gr/ivs.html">Amazon IVS
      page</a> in the <i>Amazon Web Services General Reference</i>.</p> <p> <i>
      <b>All API request parameters and URLs are case sensitive. </b> </i> </p>
      <p>For a summary of notable documentation changes in each release, see <a
      href="https://docs.aws.amazon.com/ivs/latest/userguide/doc-history.html">
      Document History</a>.</p> <p> <b>Allowed Header Values</b> </p> <ul> <li>
      <p> <code> <b>Accept:</b> </code> application/json</p> </li> <li> <p>
      <code> <b>Accept-Encoding:</b> </code> gzip, deflate</p> </li> <li> <p>
      <code> <b>Content-Type:</b> </code>application/json</p> </li> </ul> <p>
      <b>Resources</b> </p> <p>The following resources contain information about
      your IVS live stream (see <a
      href="https://docs.aws.amazon.com/ivs/latest/userguide/getting-started.html">
      Getting Started with Amazon IVS</a>):</p> <ul> <li> <p> <b>Channel</b> —
      Stores configuration data related to your live stream. You first create a
      channel and then use the channel’s stream key to start your live stream.
      See the Channel endpoints for more information. </p> </li> <li> <p>
      <b>Stream key</b> — An identifier assigned by Amazon IVS when you create a
      channel, which is then used to authorize streaming. See the StreamKey
      endpoints for more information. <i> <b>Treat the stream key like a secret,
      since it allows anyone to stream to the channel.</b> </i> </p> </li> <li>
      <p> <b>Playback key pair</b> — Video playback may be restricted using
      playback-authorization tokens, which use public-key encryption. A playback
      key pair is the public-private pair of keys used to sign and validate the
      playback-authorization token. See the PlaybackKeyPair endpoints for more
      information.</p> </li> <li> <p> <b>Recording configuration</b> — Stores
      configuration related to recording a live stream and where to store the
      recorded content. Multiple channels can reference the same recording
      configuration. See the Recording Configuration endpoints for more
      information.</p> </li> <li> <p> <b>Playback restriction policy</b> —
      Restricts playback by countries and/or origin sites. See the Playback
      Restriction Policy endpoints for more information.</p> </li> </ul> <p>
      <b>Tagging</b> </p> <p>A <i>tag</i> is a metadata label that you assign to
      an Amazon Web Services resource. A tag comprises a <i>key</i> and a
      <i>value</i>, both set by you. For example, you might set a tag as
      <code>topic:nature</code> to label a particular video category. See <a
      href="https://docs.aws.amazon.com/general/latest/gr/aws_tagging.html">Tagging
      Amazon Web Services Resources</a> for more information, including
      restrictions that apply to tags and "Tag naming limits and requirements";
      Amazon IVS has no service-specific constraints beyond what is documented
      there.</p> <p>Tags can help you identify and organize your Amazon Web
      Services resources. For example, you can use the same tag for different
      resources to indicate that they are related. You can also use tags to
      manage access (see <a
      href="https://docs.aws.amazon.com/IAM/latest/UserGuide/access_tags.html">
      Access Tags</a>). </p> <p>The Amazon IVS API has these tag-related
      endpoints: <a>TagResource</a>, <a>UntagResource</a>, and
      <a>ListTagsForResource</a>. The following resources support tagging:
      Channels, Stream Keys, Playback Key Pairs, and Recording
      Configurations.</p> <p>At most 50 tags can be applied to a resource. </p>
      <p> <b>Authentication versus Authorization</b> </p> <p>Note the
      differences between these concepts:</p> <ul> <li> <p>
      <i>Authentication</i> is about verifying identity. You need to be
      authenticated to sign Amazon IVS API requests.</p> </li> <li> <p>
      <i>Authorization</i> is about granting permissions. Your IAM roles need to
      have permissions for Amazon IVS API requests. In addition, authorization
      is needed to view <a
      href="https://docs.aws.amazon.com/ivs/latest/userguide/private-channels.html">Amazon
      IVS private channels</a>. (Private channels are channels that are enabled
      for "playback authorization.")</p> </li> </ul> <p> <b>Authentication</b>
      </p> <p>All Amazon IVS API requests must be authenticated with a
      signature. The Amazon Web Services Command-Line Interface (CLI) and Amazon
      IVS Player SDKs take care of signing the underlying API calls for you.
      However, if your application calls the Amazon IVS API directly, it’s your
      responsibility to sign the requests.</p> <p>You generate a signature using
      valid Amazon Web Services credentials that have permission to perform the
      requested action. For example, you must sign PutMetadata requests with a
      signature generated from a user account that has the
      <code>ivs:PutMetadata</code> permission.</p> <p>For more information:</p>
      <ul> <li> <p>Authentication and generating signatures — See <a
      href="https://docs.aws.amazon.com/AmazonS3/latest/API/sig-v4-authenticating-requests.html">Authenticating
      Requests (Amazon Web Services Signature Version 4)</a> in the <i>Amazon
      Web Services General Reference</i>.</p> </li> <li> <p>Managing Amazon IVS
      permissions — See <a
      href="https://docs.aws.amazon.com/ivs/latest/userguide/security-iam.html">Identity
      and Access Management</a> on the Security page of the <i>Amazon IVS User
      Guide</i>.</p> </li> </ul> <p> <b>Amazon Resource Names (ARNs)</b> </p>
      <p>ARNs uniquely identify AWS resources. An ARN is required when you need
      to specify a resource unambiguously across all of AWS, such as in IAM
      policies and API calls. For more information, see <a
      href="https://docs.aws.amazon.com/general/latest/gr/aws-arns-and-namespaces.html">Amazon
      Resource Names</a> in the <i>AWS General Reference</i>.</p> <p> <b>Channel
      Endpoints</b> </p> <ul> <li> <p> <a>CreateChannel</a> — Creates a new
      channel and an associated stream key to start streaming.</p> </li> <li>
      <p> <a>GetChannel</a> — Gets the channel configuration for the specified
      channel ARN.</p> </li> <li> <p> <a>BatchGetChannel</a> — Performs
      <a>GetChannel</a> on multiple ARNs simultaneously.</p> </li> <li> <p>
      <a>ListChannels</a> — Gets summary information about all channels in your
      account, in the Amazon Web Services region where the API request is
      processed. This list can be filtered to match a specified name or
      recording-configuration ARN. Filters are mutually exclusive and cannot be
      used together. If you try to use both filters, you will get an error (409
      Conflict Exception).</p> </li> <li> <p> <a>UpdateChannel</a> — Updates a
      channel's configuration. This does not affect an ongoing stream of this
      channel. You must stop and restart the stream for the changes to take
      effect.</p> </li> <li> <p> <a>DeleteChannel</a> — Deletes the specified
      channel.</p> </li> </ul> <p> <b>Playback Restriction Policy Endpoints</b>
      </p> <ul> <li> <p> <a>CreatePlaybackRestrictionPolicy</a> — Creates a new
      playback restriction policy, for constraining playback by countries and/or
      origins.</p> </li> <li> <p> <a>DeletePlaybackRestrictionPolicy</a> —
      Deletes the specified playback restriction policy</p> </li> <li> <p>
      <a>GetPlaybackRestrictionPolicy</a> — Gets the specified playback
      restriction policy.</p> </li> <li> <p>
      <a>ListPlaybackRestrictionPolicies</a> — Gets summary information about
      playback restriction policies.</p> </li> <li> <p>
      <a>UpdatePlaybackRestrictionPolicy</a> — Updates a specified playback
      restriction policy.</p> </li> </ul> <p> <b>Private Channel Endpoints</b>
      </p> <p>For more information, see <a
      href="https://docs.aws.amazon.com/ivs/latest/userguide/private-channels.html">Setting
      Up Private Channels</a> in the <i>Amazon IVS User Guide</i>.</p> <ul> <li>
      <p> <a>ImportPlaybackKeyPair</a> — Imports the public portion of a new key
      pair and returns its <code>arn</code> and <code>fingerprint</code>. The
      <code>privateKey</code> can then be used to generate viewer authorization
      tokens, to grant viewers access to private channels (channels enabled for
      playback authorization).</p> </li> <li> <p> <a>GetPlaybackKeyPair</a> —
      Gets a specified playback authorization key pair and returns the
      <code>arn</code> and <code>fingerprint</code>. The <code>privateKey</code>
      held by the caller can be used to generate viewer authorization tokens, to
      grant viewers access to private channels.</p> </li> <li> <p>
      <a>ListPlaybackKeyPairs</a> — Gets summary information about playback key
      pairs.</p> </li> <li> <p> <a>DeletePlaybackKeyPair</a> — Deletes a
      specified authorization key pair. This invalidates future viewer tokens
      generated using the key pair’s <code>privateKey</code>.</p> </li> <li> <p>
      <a>StartViewerSessionRevocation</a> — Starts the process of revoking the
      viewer session associated with a specified channel ARN and viewer ID.
      Optionally, you can provide a version to revoke viewer sessions less than
      and including that version.</p> </li> <li> <p>
      <a>BatchStartViewerSessionRevocation</a> — Performs
      <a>StartViewerSessionRevocation</a> on multiple channel ARN and viewer ID
      pairs simultaneously.</p> </li> </ul> <p> <b>RecordingConfiguration
      Endpoints</b> </p> <ul> <li> <p> <a>CreateRecordingConfiguration</a> —
      Creates a new recording configuration, used to enable recording to Amazon
      S3.</p> </li> <li> <p> <a>GetRecordingConfiguration</a> — Gets the
      recording-configuration metadata for the specified ARN.</p> </li> <li> <p>
      <a>ListRecordingConfigurations</a> — Gets summary information about all
      recording configurations in your account, in the Amazon Web Services
      region where the API request is processed.</p> </li> <li> <p>
      <a>DeleteRecordingConfiguration</a> — Deletes the recording configuration
      for the specified ARN.</p> </li> </ul> <p> <b>Stream Endpoints</b> </p>
      <ul> <li> <p> <a>GetStream</a> — Gets information about the active (live)
      stream on a specified channel.</p> </li> <li> <p> <a>GetStreamSession</a>
      — Gets metadata on a specified stream.</p> </li> <li> <p>
      <a>ListStreams</a> — Gets summary information about live streams in your
      account, in the Amazon Web Services region where the API request is
      processed.</p> </li> <li> <p> <a>ListStreamSessions</a> — Gets a summary
      of current and previous streams for a specified channel in your account,
      in the AWS region where the API request is processed.</p> </li> <li> <p>
      <a>StopStream</a> — Disconnects the incoming RTMPS stream for the
      specified channel. Can be used in conjunction with <a>DeleteStreamKey</a>
      to prevent further streaming to a channel.</p> </li> <li> <p>
      <a>PutMetadata</a> — Inserts metadata into the active stream of the
      specified channel. At most 5 requests per second per channel are allowed,
      each with a maximum 1 KB payload. (If 5 TPS is not sufficient for your
      needs, we recommend batching your data into a single PutMetadata call.) At
      most 155 requests per second per account are allowed.</p> </li> </ul> <p>
      <b>StreamKey Endpoints</b> </p> <ul> <li> <p> <a>CreateStreamKey</a> —
      Creates a stream key, used to initiate a stream, for the specified channel
      ARN.</p> </li> <li> <p> <a>GetStreamKey</a> — Gets stream key information
      for the specified ARN.</p> </li> <li> <p> <a>BatchGetStreamKey</a> —
      Performs <a>GetStreamKey</a> on multiple ARNs simultaneously.</p> </li>
      <li> <p> <a>ListStreamKeys</a> — Gets summary information about stream
      keys for the specified channel.</p> </li> <li> <p> <a>DeleteStreamKey</a>
      — Deletes the stream key for the specified ARN, so it can no longer be
      used to stream.</p> </li> </ul> <p> <b>Amazon Web Services Tags
      Endpoints</b> </p> <ul> <li> <p> <a>TagResource</a> — Adds or updates tags
      for the Amazon Web Services resource with the specified ARN.</p> </li>
      <li> <p> <a>UntagResource</a> — Removes tags from the resource with the
      specified ARN.</p> </li> <li> <p> <a>ListTagsForResource</a> — Gets
      information about Amazon Web Services tags for the specified ARN.</p>
      </li> </ul>
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
            title: ivs
          paths:
            /BatchGetChannel:
              POST:
                summary: BatchGetChannel
                description: >-
                  <p>Performs <a>GetChannel</a> on multiple ARNs
                  simultaneously.</p>
                tags:
                  - Batches
                  - Get
                  - Channels
                  - Batches
                  - Get
                  - Channels
            /BatchGetStreamKey:
              POST:
                summary: BatchGetStreamKey
                description: >-
                  <p>Performs <a>GetStreamKey</a> on multiple ARNs
                  simultaneously.</p>
                tags:
                  - Batches
                  - Get
                  - Stream
                  - Keys
                  - Batches
                  - Get
                  - Channels
                  - Stream
                  - Keys
            /BatchStartViewerSessionRevocation:
              POST:
                summary: BatchStartViewerSessionRevocation
                description: >-
                  <p>Performs <a>StartViewerSessionRevocation</a> on multiple
                  channel ARN and viewer ID pairs simultaneously.</p>
                tags:
                  - Batches
                  - Start
                  - Viewers
                  - Sessions
                  - Revocations
                  - Batches
                  - Get
                  - Channels
                  - Stream
                  - Keys
                  - Start
                  - Viewers
                  - Sessions
                  - Revocations
            /CreateChannel:
              POST:
                summary: CreateChannel
                description: >-
                  <p>Creates a new channel and an associated stream key to start
                  streaming.</p>
                tags:
                  - Create
                  - Channels
                  - Batches
                  - Get
                  - Channels
                  - Stream
                  - Keys
                  - Start
                  - Viewers
                  - Sessions
                  - Revocations
                  - Create
            /CreatePlaybackRestrictionPolicy:
              POST:
                summary: CreatePlaybackRestrictionPolicy
                description: >-
                  <p>Creates a new playback restriction policy, for constraining
                  playback by countries and/or origins.</p>
                tags:
                  - Create
                  - Playback
                  - Restrictions
                  - Policies
                  - Batches
                  - Get
                  - Channels
                  - Stream
                  - Keys
                  - Start
                  - Viewers
                  - Sessions
                  - Revocations
                  - Create
                  - Playback
                  - Restrictions
                  - Policies
            /CreateRecordingConfiguration:
              POST:
                summary: CreateRecordingConfiguration
                description: >-
                  <p>Creates a new recording configuration, used to enable
                  recording to Amazon S3.</p> <p> <b>Known issue:</b> In the
                  us-east-1 region, if you use the Amazon Web Services CLI to
                  create a recording configuration, it returns success even if
                  the S3 bucket is in a different region. In this case, the
                  <code>state</code> of the recording configuration is
                  <code>CREATE_FAILED</code> (instead of <code>ACTIVE</code>).
                  (In other regions, the CLI correctly returns failure if the
                  bucket is in a different region.)</p> <p> <b>Workaround:</b>
                  Ensure that your S3 bucket is in the same region as the
                  recording configuration. If you create a recording
                  configuration in a different region as your S3 bucket, delete
                  that recording configuration and create a new one with an S3
                  bucket from the correct region.</p>
                tags:
                  - Create
                  - Recording
                  - Configurations
                  - Batches
                  - Get
                  - Channels
                  - Stream
                  - Keys
                  - Start
                  - Viewers
                  - Sessions
                  - Revocations
                  - Create
                  - Playback
                  - Restrictions
                  - Policies
                  - Recording
                  - Configurations
            /CreateStreamKey:
              POST:
                summary: CreateStreamKey
                description: >-
                  <p>Creates a stream key, used to initiate a stream, for the
                  specified channel ARN.</p> <p>Note that <a>CreateChannel</a>
                  creates a stream key. If you subsequently use CreateStreamKey
                  on the same channel, it will fail because a stream key already
                  exists and there is a limit of 1 stream key per channel. To
                  reset the stream key on a channel, use <a>DeleteStreamKey</a>
                  and then CreateStreamKey.</p>
                tags:
                  - Create
                  - Stream
                  - Keys
                  - Batches
                  - Get
                  - Channels
                  - Stream
                  - Keys
                  - Start
                  - Viewers
                  - Sessions
                  - Revocations
                  - Create
                  - Playback
                  - Restrictions
                  - Policies
                  - Recording
                  - Configurations
            /DeleteChannel:
              POST:
                summary: DeleteChannel
                description: >-
                  <p>Deletes the specified channel and its associated stream
                  keys.</p> <p>If you try to delete a live channel, you will get
                  an error (409 ConflictException). To delete a channel that is
                  live, call <a>StopStream</a>, wait for the Amazon EventBridge
                  "Stream End" event (to verify that the stream's state is no
                  longer Live), then call DeleteChannel. (See <a
                  href="https://docs.aws.amazon.com/ivs/latest/userguide/eventbridge.html">
                  Using EventBridge with Amazon IVS</a>.) </p>
                tags:
                  - Delete
                  - Channels
                  - Batches
                  - Get
                  - Channels
                  - Stream
                  - Keys
                  - Start
                  - Viewers
                  - Sessions
                  - Revocations
                  - Create
                  - Playback
                  - Restrictions
                  - Policies
                  - Recording
                  - Configurations
                  - Delete
            /DeletePlaybackKeyPair:
              POST:
                summary: DeletePlaybackKeyPair
                description: >-
                  <p>Deletes a specified authorization key pair. This
                  invalidates future viewer tokens generated using the key
                  pair’s <code>privateKey</code>. For more information, see <a
                  href="https://docs.aws.amazon.com/ivs/latest/userguide/private-channels.html">Setting
                  Up Private Channels</a> in the <i>Amazon IVS User
                  Guide</i>.</p>
                tags:
                  - Delete
                  - Playback
                  - Keys
                  - Pairs
                  - Batches
                  - Get
                  - Channels
                  - Stream
                  - Keys
                  - Start
                  - Viewers
                  - Sessions
                  - Revocations
                  - Create
                  - Playback
                  - Restrictions
                  - Policies
                  - Recording
                  - Configurations
                  - Delete
                  - Pairs
            /DeletePlaybackRestrictionPolicy:
              POST:
                summary: DeletePlaybackRestrictionPolicy
                description: <p>Deletes the specified playback restriction policy.</p>
                tags:
                  - Delete
                  - Playback
                  - Restrictions
                  - Policies
                  - Batches
                  - Get
                  - Channels
                  - Stream
                  - Keys
                  - Start
                  - Viewers
                  - Sessions
                  - Revocations
                  - Create
                  - Playback
                  - Restrictions
                  - Policies
                  - Recording
                  - Configurations
                  - Delete
                  - Pairs
            /DeleteRecordingConfiguration:
              POST:
                summary: DeleteRecordingConfiguration
                description: >-
                  <p>Deletes the recording configuration for the specified
                  ARN.</p> <p>If you try to delete a recording configuration
                  that is associated with a channel, you will get an error (409
                  ConflictException). To avoid this, for all channels that
                  reference the recording configuration, first use
                  <a>UpdateChannel</a> to set the
                  <code>recordingConfigurationArn</code> field to an empty
                  string, then use DeleteRecordingConfiguration.</p>
                tags:
                  - Delete
                  - Recording
                  - Configurations
                  - Batches
                  - Get
                  - Channels
                  - Stream
                  - Keys
                  - Start
                  - Viewers
                  - Sessions
                  - Revocations
                  - Create
                  - Playback
                  - Restrictions
                  - Policies
                  - Recording
                  - Configurations
                  - Delete
                  - Pairs
            /DeleteStreamKey:
              POST:
                summary: DeleteStreamKey
                description: >-
                  <p>Deletes the stream key for the specified ARN, so it can no
                  longer be used to stream.</p>
                tags:
                  - Delete
                  - Stream
                  - Keys
                  - Batches
                  - Get
                  - Channels
                  - Stream
                  - Keys
                  - Start
                  - Viewers
                  - Sessions
                  - Revocations
                  - Create
                  - Playback
                  - Restrictions
                  - Policies
                  - Recording
                  - Configurations
                  - Delete
                  - Pairs
            /GetChannel:
              POST:
                summary: GetChannel
                description: >-
                  <p>Gets the channel configuration for the specified channel
                  ARN. See also <a>BatchGetChannel</a>.</p>
                tags:
                  - Get
                  - Channels
                  - Batches
                  - Get
                  - Channels
                  - Stream
                  - Keys
                  - Start
                  - Viewers
                  - Sessions
                  - Revocations
                  - Create
                  - Playback
                  - Restrictions
                  - Policies
                  - Recording
                  - Configurations
                  - Delete
                  - Pairs
            /GetPlaybackKeyPair:
              POST:
                summary: GetPlaybackKeyPair
                description: >-
                  <p>Gets a specified playback authorization key pair and
                  returns the <code>arn</code> and <code>fingerprint</code>. The
                  <code>privateKey</code> held by the caller can be used to
                  generate viewer authorization tokens, to grant viewers access
                  to private channels. For more information, see <a
                  href="https://docs.aws.amazon.com/ivs/latest/userguide/private-channels.html">Setting
                  Up Private Channels</a> in the <i>Amazon IVS User
                  Guide</i>.</p>
                tags:
                  - Get
                  - Playback
                  - Keys
                  - Pairs
                  - Batches
                  - Get
                  - Channels
                  - Stream
                  - Keys
                  - Start
                  - Viewers
                  - Sessions
                  - Revocations
                  - Create
                  - Playback
                  - Restrictions
                  - Policies
                  - Recording
                  - Configurations
                  - Delete
                  - Pairs
            /GetPlaybackRestrictionPolicy:
              POST:
                summary: GetPlaybackRestrictionPolicy
                description: <p>Gets the specified playback restriction policy.</p>
                tags:
                  - Get
                  - Playback
                  - Restrictions
                  - Policies
                  - Batches
                  - Get
                  - Channels
                  - Stream
                  - Keys
                  - Start
                  - Viewers
                  - Sessions
                  - Revocations
                  - Create
                  - Playback
                  - Restrictions
                  - Policies
                  - Recording
                  - Configurations
                  - Delete
                  - Pairs
            /GetRecordingConfiguration:
              POST:
                summary: GetRecordingConfiguration
                description: <p>Gets the recording configuration for the specified ARN.</p>
                tags:
                  - Get
                  - Recording
                  - Configurations
                  - Batches
                  - Get
                  - Channels
                  - Stream
                  - Keys
                  - Start
                  - Viewers
                  - Sessions
                  - Revocations
                  - Create
                  - Playback
                  - Restrictions
                  - Policies
                  - Recording
                  - Configurations
                  - Delete
                  - Pairs
            /GetStream:
              POST:
                summary: GetStream
                description: >-
                  <p>Gets information about the active (live) stream on a
                  specified channel.</p>
                tags:
                  - Get
                  - Stream
                  - Batches
                  - Get
                  - Channels
                  - Stream
                  - Keys
                  - Start
                  - Viewers
                  - Sessions
                  - Revocations
                  - Create
                  - Playback
                  - Restrictions
                  - Policies
                  - Recording
                  - Configurations
                  - Delete
                  - Pairs
            /GetStreamKey:
              POST:
                summary: GetStreamKey
                description: <p>Gets stream-key information for a specified ARN.</p>
                tags:
                  - Get
                  - Stream
                  - Keys
                  - Batches
                  - Get
                  - Channels
                  - Stream
                  - Keys
                  - Start
                  - Viewers
                  - Sessions
                  - Revocations
                  - Create
                  - Playback
                  - Restrictions
                  - Policies
                  - Recording
                  - Configurations
                  - Delete
                  - Pairs
            /GetStreamSession:
              POST:
                summary: GetStreamSession
                description: <p>Gets metadata on a specified stream.</p>
                tags:
                  - Get
                  - Stream
                  - Sessions
                  - Batches
                  - Get
                  - Channels
                  - Stream
                  - Keys
                  - Start
                  - Viewers
                  - Sessions
                  - Revocations
                  - Create
                  - Playback
                  - Restrictions
                  - Policies
                  - Recording
                  - Configurations
                  - Delete
                  - Pairs
            /ImportPlaybackKeyPair:
              POST:
                summary: ImportPlaybackKeyPair
                description: >-
                  <p>Imports the public portion of a new key pair and returns
                  its <code>arn</code> and <code>fingerprint</code>. The
                  <code>privateKey</code> can then be used to generate viewer
                  authorization tokens, to grant viewers access to private
                  channels. For more information, see <a
                  href="https://docs.aws.amazon.com/ivs/latest/userguide/private-channels.html">Setting
                  Up Private Channels</a> in the <i>Amazon IVS User
                  Guide</i>.</p>
                tags:
                  - Import
                  - Playback
                  - Keys
                  - Pairs
                  - Batches
                  - Get
                  - Channels
                  - Stream
                  - Keys
                  - Start
                  - Viewers
                  - Sessions
                  - Revocations
                  - Create
                  - Playback
                  - Restrictions
                  - Policies
                  - Recording
                  - Configurations
                  - Delete
                  - Pairs
                  - Import
            /ListChannels:
              POST:
                summary: ListChannels
                description: >-
                  <p>Gets summary information about all channels in your
                  account, in the Amazon Web Services region where the API
                  request is processed. This list can be filtered to match a
                  specified name or recording-configuration ARN. Filters are
                  mutually exclusive and cannot be used together. If you try to
                  use both filters, you will get an error (409
                  ConflictException).</p>
                tags:
                  - Lists
                  - Channels
                  - Batches
                  - Get
                  - Channels
                  - Stream
                  - Keys
                  - Start
                  - Viewers
                  - Sessions
                  - Revocations
                  - Create
                  - Playback
                  - Restrictions
                  - Policies
                  - Recording
                  - Configurations
                  - Delete
                  - Pairs
                  - Import
                  - Lists
                  - Channels
            /ListPlaybackKeyPairs:
              POST:
                summary: ListPlaybackKeyPairs
                description: >-
                  <p>Gets summary information about playback key pairs. For more
                  information, see <a
                  href="https://docs.aws.amazon.com/ivs/latest/userguide/private-channels.html">Setting
                  Up Private Channels</a> in the <i>Amazon IVS User
                  Guide</i>.</p>
                tags:
                  - Lists
                  - Playback
                  - Keys
                  - Pairs
                  - Batches
                  - Get
                  - Channels
                  - Stream
                  - Keys
                  - Start
                  - Viewers
                  - Sessions
                  - Revocations
                  - Create
                  - Playback
                  - Restrictions
                  - Policies
                  - Recording
                  - Configurations
                  - Delete
                  - Pairs
                  - Import
                  - Lists
                  - Channels
                  - Pairs
            /ListPlaybackRestrictionPolicies:
              POST:
                summary: ListPlaybackRestrictionPolicies
                description: >-
                  <p>Gets summary information about playback restriction
                  policies.</p>
                tags:
                  - Lists
                  - Playback
                  - Restrictions
                  - Policies
                  - Batches
                  - Get
                  - Channels
                  - Stream
                  - Keys
                  - Start
                  - Viewers
                  - Sessions
                  - Revocations
                  - Create
                  - Playback
                  - Restrictions
                  - Policies
                  - Recording
                  - Configurations
                  - Delete
                  - Pairs
                  - Import
                  - Lists
                  - Channels
                  - Pairs
                  - Policies
            /ListRecordingConfigurations:
              POST:
                summary: ListRecordingConfigurations
                description: >-
                  <p>Gets summary information about all recording configurations
                  in your account, in the Amazon Web Services region where the
                  API request is processed.</p>
                tags:
                  - Lists
                  - Recording
                  - Configurations
                  - Batches
                  - Get
                  - Channels
                  - Stream
                  - Keys
                  - Start
                  - Viewers
                  - Sessions
                  - Revocations
                  - Create
                  - Playback
                  - Restrictions
                  - Policies
                  - Recording
                  - Configurations
                  - Delete
                  - Pairs
                  - Import
                  - Lists
                  - Channels
                  - Pairs
                  - Policies
                  - Configurations
            /ListStreamKeys:
              POST:
                summary: ListStreamKeys
                description: >-
                  <p>Gets summary information about stream keys for the
                  specified channel.</p>
                tags:
                  - Lists
                  - Stream
                  - Keys
                  - Batches
                  - Get
                  - Channels
                  - Stream
                  - Keys
                  - Start
                  - Viewers
                  - Sessions
                  - Revocations
                  - Create
                  - Playback
                  - Restrictions
                  - Policies
                  - Recording
                  - Configurations
                  - Delete
                  - Pairs
                  - Import
                  - Lists
                  - Channels
                  - Pairs
                  - Policies
                  - Configurations
                  - Keys
            /ListStreamSessions:
              POST:
                summary: ListStreamSessions
                description: >-
                  <p>Gets a summary of current and previous streams for a
                  specified channel in your account, in the AWS region where the
                  API request is processed.</p>
                tags:
                  - Lists
                  - Stream
                  - Sessions
                  - Batches
                  - Get
                  - Channels
                  - Stream
                  - Keys
                  - Start
                  - Viewers
                  - Sessions
                  - Revocations
                  - Create
                  - Playback
                  - Restrictions
                  - Policies
                  - Recording
                  - Configurations
                  - Delete
                  - Pairs
                  - Import
                  - Lists
                  - Channels
                  - Pairs
                  - Policies
                  - Configurations
                  - Keys
                  - Sessions
            /ListStreams:
              POST:
                summary: ListStreams
                description: >-
                  <p>Gets summary information about live streams in your
                  account, in the Amazon Web Services region where the API
                  request is processed.</p>
                tags:
                  - Lists
                  - Streams
                  - Batches
                  - Get
                  - Channels
                  - Stream
                  - Keys
                  - Start
                  - Viewers
                  - Sessions
                  - Revocations
                  - Create
                  - Playback
                  - Restrictions
                  - Policies
                  - Recording
                  - Configurations
                  - Delete
                  - Pairs
                  - Import
                  - Lists
                  - Channels
                  - Pairs
                  - Policies
                  - Configurations
                  - Keys
                  - Sessions
                  - Streams
            /tags/{resourceArn}:
              DELETE:
                summary: UntagResource
                description: <p>Removes tags from the resource with the specified ARN.</p>
                tags:
                  - Untag
                  - Resources
                  - Batches
                  - Get
                  - Channels
                  - Stream
                  - Keys
                  - Start
                  - Viewers
                  - Sessions
                  - Revocations
                  - Create
                  - Playback
                  - Restrictions
                  - Policies
                  - Recording
                  - Configurations
                  - Delete
                  - Pairs
                  - Import
                  - Lists
                  - Channels
                  - Pairs
                  - Policies
                  - Configurations
                  - Keys
                  - Sessions
                  - Streams
                  - ARN
            /PutMetadata:
              POST:
                summary: PutMetadata
                description: >-
                  <p>Inserts metadata into the active stream of the specified
                  channel. At most 5 requests per second per channel are
                  allowed, each with a maximum 1 KB payload. (If 5 TPS is not
                  sufficient for your needs, we recommend batching your data
                  into a single PutMetadata call.) At most 155 requests per
                  second per account are allowed. Also see <a
                  href="https://docs.aws.amazon.com/ivs/latest/userguide/metadata.html">Embedding
                  Metadata within a Video Stream</a> in the <i>Amazon IVS User
                  Guide</i>.</p>
                tags:
                  - Put
                  - Metadata
                  - Batches
                  - Get
                  - Channels
                  - Stream
                  - Keys
                  - Start
                  - Viewers
                  - Sessions
                  - Revocations
                  - Create
                  - Playback
                  - Restrictions
                  - Policies
                  - Recording
                  - Configurations
                  - Delete
                  - Pairs
                  - Import
                  - Lists
                  - Channels
                  - Pairs
                  - Policies
                  - Configurations
                  - Keys
                  - Sessions
                  - Streams
                  - ARN
                  - Put
                  - Metadata
            /StartViewerSessionRevocation:
              POST:
                summary: StartViewerSessionRevocation
                description: >-
                  <p>Starts the process of revoking the viewer session
                  associated with a specified channel ARN and viewer ID.
                  Optionally, you can provide a version to revoke viewer
                  sessions less than and including that version. For
                  instructions on associating a viewer ID with a viewer session,
                  see <a
                  href="https://docs.aws.amazon.com/ivs/latest/userguide/private-channels.html">Setting
                  Up Private Channels</a>.</p>
                tags:
                  - Start
                  - Viewers
                  - Sessions
                  - Revocations
                  - Batches
                  - Get
                  - Channels
                  - Stream
                  - Keys
                  - Start
                  - Viewers
                  - Sessions
                  - Revocations
                  - Create
                  - Playback
                  - Restrictions
                  - Policies
                  - Recording
                  - Configurations
                  - Delete
                  - Pairs
                  - Import
                  - Lists
                  - Channels
                  - Pairs
                  - Policies
                  - Configurations
                  - Keys
                  - Sessions
                  - Streams
                  - ARN
                  - Put
                  - Metadata
            /StopStream:
              POST:
                summary: StopStream
                description: >-
                  <p>Disconnects the incoming RTMPS stream for the specified
                  channel. Can be used in conjunction with
                  <a>DeleteStreamKey</a> to prevent further streaming to a
                  channel.</p> <note> <p>Many streaming client-software
                  libraries automatically reconnect a dropped RTMPS session, so
                  to stop the stream permanently, you may want to first revoke
                  the <code>streamKey</code> attached to the channel.</p>
                  </note>
                tags:
                  - Stop
                  - Stream
                  - Batches
                  - Get
                  - Channels
                  - Stream
                  - Keys
                  - Start
                  - Viewers
                  - Sessions
                  - Revocations
                  - Create
                  - Playback
                  - Restrictions
                  - Policies
                  - Recording
                  - Configurations
                  - Delete
                  - Pairs
                  - Import
                  - Lists
                  - Channels
                  - Pairs
                  - Policies
                  - Configurations
                  - Keys
                  - Sessions
                  - Streams
                  - ARN
                  - Put
                  - Metadata
                  - Stop
            /UpdateChannel:
              POST:
                summary: UpdateChannel
                description: >-
                  <p>Updates a channel's configuration. Live channels cannot be
                  updated. You must stop the ongoing stream, update the channel,
                  and restart the stream for the changes to take effect.</p>
                tags:
                  - Update
                  - Channels
                  - Batches
                  - Get
                  - Channels
                  - Stream
                  - Keys
                  - Start
                  - Viewers
                  - Sessions
                  - Revocations
                  - Create
                  - Playback
                  - Restrictions
                  - Policies
                  - Recording
                  - Configurations
                  - Delete
                  - Pairs
                  - Import
                  - Lists
                  - Channels
                  - Pairs
                  - Policies
                  - Configurations
                  - Keys
                  - Sessions
                  - Streams
                  - ARN
                  - Put
                  - Metadata
                  - Stop
                  - Update
            /UpdatePlaybackRestrictionPolicy:
              POST:
                summary: UpdatePlaybackRestrictionPolicy
                description: <p>Updates a specified playback restriction p
                tags:
                  - Update
                  - Playback
                  - Restrictions
                  - Policies
                  - Batches
                  - Get
                  - Channels
                  - Stream
                  - Keys
                  - Start
                  - Viewers
                  - Sessions
                  - Revocations
                  - Create
                  - Playback
                  - Restrictions
                  - Policies
                  - Recording
                  - Configurations
                  - Delete
                  - Pairs
                  - Import
                  - Lists
                  - Channels
                  - Pairs
                  - Policies
                  - Configurations
                  - Keys
                  - Sessions
                  - Streams
                  - ARN
                  - Put
                  - Metadata
                  - Stop
                  - Upda
    overlays:
      - type: APIs.io Search
        url: overlays/ivs-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/ivs-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:ivs
  - name: kinesisvideo
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
            title: kinesisvideo
          paths:
            /createSignalingChannel:
              POST:
                summary: CreateSignalingChannel
                description: >-
                  <p>Creates a signaling channel. </p> <p>
                  <code>CreateSignalingChannel</code> is an asynchronous
                  operation.</p>
                tags:
                  - Create
                  - Signaling
                  - Channels
                  - Signaling
                  - Channels
            /createStream:
              POST:
                summary: CreateStream
                description: >-
                  <p>Creates a new Kinesis video stream. </p> <p>When you create
                  a new stream, Kinesis Video Streams assigns it a version
                  number. When you change the stream's metadata, Kinesis Video
                  Streams updates the version. </p> <p>
                  <code>CreateStream</code> is an asynchronous operation.</p>
                  <p>For information about how the service works, see <a
                  href="https://docs.aws.amazon.com/kinesisvideostreams/latest/dg/how-it-works.html">How
                  it Works</a>. </p> <p>You must have permissions for the
                  <code>KinesisVideo:CreateStream</code> action.</p>
                tags:
                  - Create
                  - Stream
                  - Signaling
                  - Channels
                  - Stream
            /deleteEdgeConfiguration:
              POST:
                summary: DeleteEdgeConfiguration
                description: >-
                  <p>An asynchronous API that deletes a stream’s existing edge
                  configuration, as well as the corresponding media from the
                  Edge Agent.</p> <p>When you invoke this API, the sync status
                  is set to <code>DELETING</code>. A deletion process starts, in
                  which active edge jobs are stopped and all media is deleted
                  from the edge device. The time to delete varies, depending on
                  the total amount of stored media. If the deletion process
                  fails, the sync status changes to <code>DELETE_FAILED</code>.
                  You will need to re-try the deletion.</p> <p>When the deletion
                  process has completed successfully, the edge configuration is
                  no longer accessible.</p>
                tags:
                  - Delete
                  - Edge
                  - Configurations
                  - Signaling
                  - Channels
                  - Stream
                  - Edge
                  - Configurations
            /deleteSignalingChannel:
              POST:
                summary: DeleteSignalingChannel
                description: >-
                  <p>Deletes a specified signaling channel.
                  <code>DeleteSignalingChannel</code> is an asynchronous
                  operation. If you don't specify the channel's current version,
                  the most recent version is deleted.</p>
                tags:
                  - Delete
                  - Signaling
                  - Channels
                  - Signaling
                  - Channels
                  - Stream
                  - Edge
                  - Configurations
            /deleteStream:
              POST:
                summary: DeleteStream
                description: >-
                  <p>Deletes a Kinesis video stream and the data contained in
                  the stream. </p> <p>This method marks the stream for deletion,
                  and makes the data in the stream inaccessible immediately.</p>
                  <p> </p> <p> To ensure that you have the latest version of the
                  stream before deleting it, you can specify the stream version.
                  Kinesis Video Streams assigns a version to each stream. When
                  you update a stream, Kinesis Video Streams assigns a new
                  version number. To get the latest stream version, use the
                  <code>DescribeStream</code> API. </p> <p>This operation
                  requires permission for the
                  <code>KinesisVideo:DeleteStream</code> action.</p>
                tags:
                  - Delete
                  - Stream
                  - Signaling
                  - Channels
                  - Stream
                  - Edge
                  - Configurations
            /describeEdgeConfiguration:
              POST:
                summary: DescribeEdgeConfiguration
                description: >-
                  <p>Describes a stream’s edge configuration that was set using
                  the <code>StartEdgeConfigurationUpdate</code> API and the
                  latest status of the edge agent's recorder and uploader jobs.
                  Use this API to get the status of the configuration to
                  determine if the configuration is in sync with the Edge Agent.
                  Use this API to evaluate the health of the Edge Agent.</p>
                tags:
                  - Describe
                  - Edge
                  - Configurations
                  - Signaling
                  - Channels
                  - Stream
                  - Edge
                  - Configurations
            /describeImageGenerationConfiguration:
              POST:
                summary: DescribeImageGenerationConfiguration
                description: >-
                  <p>Gets the <code>ImageGenerationConfiguration</code> for a
                  given Kinesis video stream.</p>
                tags:
                  - Describe
                  - Images
                  - Generation
                  - Configurations
                  - Signaling
                  - Channels
                  - Stream
                  - Edge
                  - Configurations
                  - Images
                  - Generation
            /describeMappedResourceConfiguration:
              POST:
                summary: DescribeMappedResourceConfiguration
                description: >-
                  <p>Returns the most current information about the stream. The
                  <code>streamName</code> or <code>streamARN</code> should be
                  provided in the input.</p>
                tags:
                  - Describe
                  - Mapped
                  - Resources
                  - Configurations
                  - Signaling
                  - Channels
                  - Stream
                  - Edge
                  - Configurations
                  - Images
                  - Generation
                  - Mapped
                  - Resources
            /describeMediaStorageConfiguration:
              POST:
                summary: DescribeMediaStorageConfiguration
                description: >-
                  <p>Returns the most current information about the channel.
                  Specify the <code>ChannelName</code> or
                  <code>ChannelARN</code> in the input.</p>
                tags:
                  - Describe
                  - Media
                  - Storage
                  - Configurations
                  - Signaling
                  - Channels
                  - Stream
                  - Edge
                  - Configurations
                  - Images
                  - Generation
                  - Mapped
                  - Resources
                  - Media
                  - Storage
            /describeNotificationConfiguration:
              POST:
                summary: DescribeNotificationConfiguration
                description: >-
                  <p>Gets the <code>NotificationConfiguration</code> for a given
                  Kinesis video stream.</p>
                tags:
                  - Describe
                  - Notifications
                  - Configurations
                  - Signaling
                  - Channels
                  - Stream
                  - Edge
                  - Configurations
                  - Images
                  - Generation
                  - Mapped
                  - Resources
                  - Media
                  - Storage
                  - Notifications
            /describeSignalingChannel:
              POST:
                summary: DescribeSignalingChannel
                description: >-
                  <p>Returns the most current information about the signaling
                  channel. You must specify either the name or the Amazon
                  Resource Name (ARN) of the channel that you want to
                  describe.</p>
                tags:
                  - Describe
                  - Signaling
                  - Channels
                  - Signaling
                  - Channels
                  - Stream
                  - Edge
                  - Configurations
                  - Images
                  - Generation
                  - Mapped
                  - Resources
                  - Media
                  - Storage
                  - Notifications
            /describeStream:
              POST:
                summary: DescribeStream
                description: >-
                  <p>Returns the most current information about the specified
                  stream. You must specify either the <code>StreamName</code> or
                  the <code>StreamARN</code>. </p>
                tags:
                  - Describe
                  - Stream
                  - Signaling
                  - Channels
                  - Stream
                  - Edge
                  - Configurations
                  - Images
                  - Generation
                  - Mapped
                  - Resources
                  - Media
                  - Storage
                  - Notifications
            /getDataEndpoint:
              POST:
                summary: GetDataEndpoint
                description: >-
                  <p>Gets an endpoint for a specified stream for either reading
                  or writing. Use this endpoint in your application to read from
                  the specified stream (using the <code>GetMedia</code> or
                  <code>GetMediaForFragmentList</code> operations) or write to
                  it (using the <code>PutMedia</code> operation). </p> <note>
                  <p>The returned endpoint does not have the API name appended.
                  The client needs to add the API name to the returned
                  endpoint.</p> </note> <p>In the request, specify the stream
                  either by <code>StreamName</code> or
                  <code>StreamARN</code>.</p>
                tags:
                  - Get
                  - Data
                  - Endpoints
                  - Signaling
                  - Channels
                  - Stream
                  - Edge
                  - Configurations
                  - Images
                  - Generation
                  - Mapped
                  - Resources
                  - Media
                  - Storage
                  - Notifications
                  - Data
                  - Endpoints
            /getSignalingChannelEndpoint:
              POST:
                summary: GetSignalingChannelEndpoint
                description: >-
                  <p>Provides an endpoint for the specified signaling channel to
                  send and receive messages. This API uses the
                  <code>SingleMasterChannelEndpointConfiguration</code> input
                  parameter, which consists of the <code>Protocols</code> and
                  <code>Role</code> properties.</p> <p> <code>Protocols</code>
                  is used to determine the communication mechanism. For example,
                  if you specify <code>WSS</code> as the protocol, this API
                  produces a secure websocket endpoint. If you specify
                  <code>HTTPS</code> as the protocol, this API generates an
                  HTTPS endpoint. </p> <p> <code>Role</code> determines the
                  messaging permissions. A <code>MASTER</code> role results in
                  this API generating an endpoint that a client can use to
                  communicate with any of the viewers on the channel. A
                  <code>VIEWER</code> role results in this API generating an
                  endpoint that a client can use to communicate only with a
                  <code>MASTER</code>. </p>
                tags:
                  - Get
                  - Signaling
                  - Channels
                  - Endpoints
                  - Signaling
                  - Channels
                  - Stream
                  - Edge
                  - Configurations
                  - Images
                  - Generation
                  - Mapped
                  - Resources
                  - Media
                  - Storage
                  - Notifications
                  - Data
                  - Endpoints
            /listEdgeAgentConfigurations:
              POST:
                summary: ListEdgeAgentConfigurations
                description: >-
                  <p>Returns an array of edge configurations associated with the
                  specified Edge Agent.</p> <p>In the request, you must specify
                  the Edge Agent <code>HubDeviceArn</code>.</p>
                tags:
                  - Lists
                  - Edge
                  - Agent
                  - Configurations
                  - Signaling
                  - Channels
                  - Stream
                  - Edge
                  - Configurations
                  - Images
                  - Generation
                  - Mapped
                  - Resources
                  - Media
                  - Storage
                  - Notifications
                  - Data
                  - Endpoints
                  - Agent
                  - Configurations
            /listSignalingChannels:
              POST:
                summary: ListSignalingChannels
                description: >-
                  <p>Returns an array of <code>ChannelInfo</code> objects. Each
                  object describes a signaling channel. To retrieve only those
                  channels that satisfy a specific condition, you can specify a
                  <code>ChannelNameCondition</code>.</p>
                tags:
                  - Lists
                  - Signaling
                  - Channels
                  - Signaling
                  - Channels
                  - Stream
                  - Edge
                  - Configurations
                  - Images
                  - Generation
                  - Mapped
                  - Resources
                  - Media
                  - Storage
                  - Notifications
                  - Data
                  - Endpoints
                  - Agent
                  - Configurations
                  - Channels
            /listStreams:
              POST:
                summary: ListStreams
                description: >-
                  <p>Returns an array of <code>StreamInfo</code> objects. Each
                  object describes a stream. To retrieve only streams that
                  satisfy a specific condition, you can specify a
                  <code>StreamNameCondition</code>. </p>
                tags:
                  - Lists
                  - Streams
                  - Signaling
                  - Channels
                  - Stream
                  - Edge
                  - Configurations
                  - Images
                  - Generation
                  - Mapped
                  - Resources
                  - Media
                  - Storage
                  - Notifications
                  - Data
                  - Endpoints
                  - Agent
                  - Configurations
                  - Channels
                  - Streams
            /ListTagsForResource:
              POST:
                summary: ListTagsForResource
                description: >-
                  <p>Returns a list of tags associated with the specified
                  signaling channel.</p>
                tags:
                  - Lists
                  - Tags
                  - For
                  - Resources
                  - Signaling
                  - Channels
                  - Stream
                  - Edge
                  - Configurations
                  - Images
                  - Generation
                  - Mapped
                  - Resources
                  - Media
                  - Storage
                  - Notifications
                  - Data
                  - Endpoints
                  - Agent
                  - Configurations
                  - Channels
                  - Streams
                  - Lists
                  - Tags
                  - For
            /listTagsForStream:
              POST:
                summary: ListTagsForStream
                description: >-
                  <p>Returns a list of tags associated with the specified
                  stream.</p> <p>In the request, you must specify either the
                  <code>StreamName</code> or the <code>StreamARN</code>. </p>
                tags:
                  - Lists
                  - Tags
                  - For
                  - Stream
                  - Signaling
                  - Channels
                  - Stream
                  - Edge
                  - Configurations
                  - Images
                  - Generation
                  - Mapped
                  - Resources
                  - Media
                  - Storage
                  - Notifications
                  - Data
                  - Endpoints
                  - Agent
                  - Configurations
                  - Channels
                  - Streams
                  - Lists
                  - Tags
                  - For
            /startEdgeConfigurationUpdate:
              POST:
                summary: StartEdgeConfigurationUpdate
                description: >-
                  <p>An asynchronous API that updates a stream’s existing edge
                  configuration. The Kinesis Video Stream will sync the stream’s
                  edge configuration with the Edge Agent IoT Greengrass
                  component that runs on an IoT Hub Device, setup at your
                  premise. The time to sync can vary and depends on the
                  connectivity of the Hub Device. The <code>SyncStatus</code>
                  will be updated as the edge configuration is acknowledged, and
                  synced with the Edge Agent. </p> <p>If this API is invoked for
                  the first time, a new edge configuration will be created for
                  the stream, and the sync status will be set to
                  <code>SYNCING</code>. You will have to wait for the sync
                  status to reach a terminal state such as:
                  <code>IN_SYNC</code>, or <code>SYNC_FAILED</code>, before
                  using this API again. If you invoke this API during the
                  syncing process, a <code>ResourceInUseException</code> will be
                  thrown. The connectivity of the stream’s edge configuration
                  and the Edge Agent will be retried for 15 minutes. After 15
                  minutes, the status will transition into the
                  <code>SYNC_FAILED</code> state.</p> <p>To move an edge
                  configuration from one device to another, use
                  <a>DeleteEdgeConfiguration</a> to delete the current edge
                  configuration. You can then invoke
                  StartEdgeConfigurationUpdate with an updated Hub Device
                  ARN.</p>
                tags:
                  - Start
                  - Edge
                  - Configurations
                  - Update
                  - Signaling
                  - Channels
                  - Stream
                  - Edge
                  - Configurations
                  - Images
                  - Generation
                  - Mapped
                  - Resources
                  - Media
                  - Storage
                  - Notifications
                  - Data
                  - Endpoints
                  - Agent
                  - Configurations
                  - Channels
                  - Streams
                  - Lists
                  - Tags
                  - For
                  - Update
            /TagResource:
              POST:
                summary: TagResource
                description: >-
                  <p>Adds one or more tags to a signaling channel. A <i>tag</i>
                  is a key-value pair (the value is optional) that you can
                  define and assign to Amazon Web Services resources. If you
                  specify a tag that already exists, the tag value is replaced
                  with the value that you specify in the request. For more
                  information, see <a
                  href="https://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/cost-alloc-tags.html">Using
                  Cost Allocation Tags</a> in the <i>Billing and Cost Management
                  and Cost Management User Guide</i>.</p>
                tags:
                  - Tags
                  - Resources
                  - Signaling
                  - Channels
                  - Stream
                  - Edge
                  - Configurations
                  - Images
                  - Generation
                  - Mapped
                  - Resources
                  - Media
                  - Storage
                  - Notifications
                  - Data
                  - Endpoints
                  - Agent
                  - Configurations
                  - Channels
                  - Streams
                  - Lists
                  - Tags
                  - For
                  - Update
                  - Tags
            /tagStream:
              POST:
                summary: TagStream
                description: >-
                  <p>Adds one or more tags to a stream. A <i>tag</i> is a
                  key-value pair (the value is optional) that you can define and
                  assign to Amazon Web Services resources. If you specify a tag
                  that already exists, the tag value is replaced with the value
                  that you specify in the request. For more information, see <a
                  href="https://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/cost-alloc-tags.html">Using
                  Cost Allocation Tags</a> in the <i>Billing and Cost Management
                  and Cost Management User Guide</i>. </p> <p>You must provide
                  either the <code>StreamName</code> or the
                  <code>StreamARN</code>.</p> <p>This operation requires
                  permission for the <code>KinesisVideo:TagStream</code>
                  action.</p> <p>A Kinesis video stream can support up to 50
                  tags.</p>
                tags:
                  - Tags
                  - Stream
                  - Signaling
                  - Channels
                  - Stream
                  - Edge
                  - Configurations
                  - Images
                  - Generation
                  - Mapped
                  - Resources
                  - Media
                  - Storage
                  - Notifications
                  - Data
                  - Endpoints
                  - Agent
                  - Configurations
                  - Channels
                  - Streams
                  - Lists
                  - Tags
                  - For
                  - Update
                  - Tags
            /UntagResource:
              POST:
                summary: UntagResource
                description: >-
                  <p>Removes one or more tags from a signaling channel. In the
                  request, specify only a tag key or keys; don't specify the
                  value. If you specify a tag key that does not exist, it's
                  ignored.</p>
                tags:
                  - Untag
                  - Resources
                  - Signaling
                  - Channels
                  - Stream
                  - Edge
                  - Configurations
                  - Images
                  - Generation
                  - Mapped
                  - Resources
                  - Media
                  - Storage
                  - Notifications
                  - Data
                  - Endpoints
                  - Agent
                  - Configurations
                  - Channels
                  - Streams
                  - Lists
                  - Tags
                  - For
                  - Update
                  - Tags
                  - Untag
            /untagStream:
              POST:
                summary: UntagStream
                description: >-
                  <p>Removes one or more tags from a stream. In the request,
                  specify only a tag key or keys; don't specify the value. If
                  you specify a tag key that does not exist, it's ignored.</p>
                  <p>In the request, you must provide the
                  <code>StreamName</code> or <code>StreamARN</code>.</p>
                tags:
                  - Untag
                  - Stream
                  - Signaling
                  - Channels
                  - Stream
                  - Edge
                  - Configurations
                  - Images
                  - Generation
                  - Mapped
                  - Resources
                  - Media
                  - Storage
                  - Notifications
                  - Data
                  - Endpoints
                  - Agent
                  - Configurations
                  - Channels
                  - Streams
                  - Lists
                  - Tags
                  - For
                  - Update
                  - Tags
                  - Untag
            /updateDataRetention:
              POST:
                summary: UpdateDataRetention
                description: >-
                  <p>Increases or decreases the stream's data retention period
                  by the value that you specify. To indicate whether you want to
                  increase or decrease the data retention period, specify the
                  <code>Operation</code> parameter in the request body. In the
                  request, you must specify either the <code>StreamName</code>
                  or the <code>StreamARN</code>. </p> <p>This operation requires
                  permission for the
                  <code>KinesisVideo:UpdateDataRetention</code> action.</p>
                  <p>Changing the data retention period affects the data in the
                  stream as follows:</p> <ul> <li> <p>If the data retention
                  period is increased, existing data is retained for the new
                  retention period. For example, if the data retention period is
                  increased from one hour to seven hours, all existing data is
                  retained for seven hours.</p> </li> <li> <p>If the data
                  retention period is decreased, existing data is retained for
                  the new retention period. For example, if the data retention
                  period is decreased from seven hours to one hour, all existing
                  data is retained for one hour, and any data older than one
                  hour is deleted immediately.</p> </li> </ul>
                tags:
                  - Update
                  - Data
                  - Retention
                  - Signaling
                  - Channels
                  - Stream
                  - Edge
                  - Configurations
                  - Images
                  - Generation
                  - Mapped
                  - Resources
                  - Media
                  - Storage
                  - Notifications
                  - Data
                  - Endpoints
                  - Agent
                  - Configurations
                  - Channels
                  - Streams
                  - Lists
                  - Tags
                  - For
                  - Update
                  - Tags
                  - Untag
                  - Retention
            /updateImageGenerationConfiguration:
              POST:
                summary: UpdateImageGenerationConfiguration
                description: >-
                  <p>Updates the <code>StreamInfo</code> and
                  <code>ImageProcessingConfiguration</code> fields.</p>
                tags:
                  - Update
                  - Images
                  - Generation
                  - Configurations
                  - Signaling
                  - Channels
                  - Stream
                  - Edge
                  - Configurations
                  - Images
                  - Generation
                  - Mapped
                  - Resources
                  - Media
                  - Storage
                  - Notifications
                  - Data
                  - Endpoints
                  - Agent
                  - Configurations
                  - Channels
                  - Streams
                  - Lists
                  - Tags
                  - For
                  - Update
                  - Tags
                  - Untag
                  - Retention
            /updateMediaStorageConfiguration:
              POST:
                summary: UpdateMediaStorageConfiguration
                description: >-
                  <p>Associates a <code>SignalingChannel</code> to a stream to
                  store the media. There are two signaling modes that you can
                  specify :</p> <ul> <li> <p>If <code>StorageStatus</code> is
                  enabled, the data will be stored in the <code>StreamARN</code>
                  provided. In order for WebRTC Ingestion to work, the stream
                  must have data retention enabled.</p> </li> <li> <p>If
                  <code>StorageStatus</code> is disabled, no data will be
                  stored, and the <code>StreamARN</code> parameter will not be
                  needed. </p> </li> </ul> <important> <p>If
                  <code>StorageStatus</code> is enabled, direct peer-to-peer
                  (master-viewer) connections no longer occur. Peers connect
                  directly to the storage session. You must call the
                  <code>JoinStorageSession</code> API to trigger an SDP offer
                  send and establish a connection between a peer and the storage
                  session. </p> </important>
                tags:
                  - Update
                  - Media
                  - Storage
                  - Configurations
                  - Signaling
                  - Channels
                  - Stream
                  - Edge
                  - Configurations
                  - Images
                  - Generation
                  - Mapped
                  - Resources
                  - Media
                  - Storage
                  - Notifications
                  - Data
                  - Endpoints
                  - Agent
                  - Configurations
                  - Channels
                  - Streams
                  - Lists
                  - Tags
                  - For
                  - Update
                  - Tags
                  - Untag
                  - Retention
            /updateNotificationConfiguration:
              POST:
                summary: UpdateNotificationConfiguration
                description: <p>Updates the notification information for a stream.</p>
                tags:
                  - Update
                  - Notifications
                  - Configurations
                  - Signaling
                  - Channels
                  - Stream
                  - Edge
                  - Configurations
                  - Images
                  - Generation
                  - Mapped
                  - Resources
                  - Media
                  - Storage
                  - Notifications
                  - Data
                  - Endpoints
                  - Agent
                  - Configurations
                  - Channels
                  - Streams
                  - Lists
                  - Tags
                  - For
                  - Update
                  - Tags
                  - Untag
                  - Retention
            /updateSignalingChannel:
              POST:
                summary: UpdateSignalingChannel
                description: >-
                  <p>Updates the existing signaling channel. This is an
                  asynchronous operation and takes time to complete. </p> <p>If
                  the <code>MessageTtlSeconds</code> value is updated (either
                  increased or reduced), it only applies to new messages sent
                  via this channel after it's been updated. Existing messages
                  are still expired as per the previous
                  <code>MessageTtlSeconds</code> value.</p>
                tags:
                  - Update
                  - Signaling
                  - Channels
                  - Signaling
                  - Channels
                  - Stream
                  - Edge
                  - Configurations
                  - Images
                  - Generation
                  - Mapped
                  - Resources
                  - Media
                  - Storage
                  - Notifications
                  - Data
                  - Endpoints
                  - Agent
                  - Configurations
                  - Channels
                  - Streams
                  - Lists
                  - Tags
                  - For
                  - Update
                  - Tags
                  - Untag
                  - Retention
            /updateStream:
              POST:
                summary: UpdateStream
                description: >-
                  <p>Updates stream metadata, such as the device name and media
                  type.</p> <p>You must provide the stream name or the Amazon
                  Resource Name (ARN) of the stream.</p> <p>To make sure that
                  you have the latest version of the stream before updating it,
                  you can specify the stream version. Kinesis Video Streams
                  assigns a version to each stream. When you update a stream,
                  Kinesis Video Streams assigns a new version number. To get the
                  latest stream version, use the <code>DescribeStream</code>
                  API. </p> <p> <code>UpdateStream</code> is an asynchronous
                  operation, and takes time to com
                tags:
                  - Update
                  - Stream
                  - Signaling
                  - Channels
                  - Stream
                  - Edge
                  - Configurations
                  - Images
                  - Generation
                  - Mapped
                  - Resources
                  - Media
                  - Storage
                  - Notifications
                  - Data
                  - Endpoints
                  - Agent
                  - Configurations
                  - Channels
                  - Streams
                  - Lists
                  - Tags
                  - For
                  - Update
                  - Tags
                  - Untag
                  - Retention
    overlays:
      - type: APIs.io Search
        url: overlays/kinesisvideo-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/kinesisvideo-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:kinesisvideo
  - name: lex-models
    description: >-
      <fullname>Amazon Lex Build-Time Actions</fullname> <p> Amazon Lex is an
      AWS service for building conversational voice and text interfaces. Use
      these actions to create, update, and delete conversational bots for new
      and existing client applications. </p>
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
            title: lex-models
          paths:
            /bots/{name}/versions:
              POST:
                summary: CreateBotVersion
                description: >-
                  <p>Creates a new version of the bot based on the
                  <code>$LATEST</code> version. If the <code>$LATEST</code>
                  version of this resource hasn't changed since you created the
                  last version, Amazon Lex doesn't create a new version. It
                  returns the last created version.</p> <note> <p>You can update
                  only the <code>$LATEST</code> version of the bot. You can't
                  update the numbered versions that you create with the
                  <code>CreateBotVersion</code> operation.</p> </note> <p> When
                  you create the first version of a bot, Amazon Lex sets the
                  version to 1. Subsequent versions increment by 1. For more
                  information, see <a>versioning-intro</a>. </p> <p> This
                  operation requires permission for the
                  <code>lex:CreateBotVersion</code> action. </p>
                tags:
                  - Create
                  - Bot
                  - Versions
                  - Bots
                  - Names
                  - Versions
            /intents/{name}/versions:
              POST:
                summary: CreateIntentVersion
                description: >-
                  <p>Creates a new version of an intent based on the
                  <code>$LATEST</code> version of the intent. If the
                  <code>$LATEST</code> version of this intent hasn't changed
                  since you last updated it, Amazon Lex doesn't create a new
                  version. It returns the last version you created.</p> <note>
                  <p>You can update only the <code>$LATEST</code> version of the
                  intent. You can't update the numbered versions that you create
                  with the <code>CreateIntentVersion</code> operation.</p>
                  </note> <p> When you create a version of an intent, Amazon Lex
                  sets the version to 1. Subsequent versions increment by 1. For
                  more information, see <a>versioning-intro</a>. </p> <p>This
                  operation requires permissions to perform the
                  <code>lex:CreateIntentVersion</code> action. </p>
                tags:
                  - Create
                  - Intent
                  - Versions
                  - Bots
                  - Names
                  - Versions
                  - Intents
            /slottypes/{name}/versions:
              POST:
                summary: CreateSlotTypeVersion
                description: >-
                  <p>Creates a new version of a slot type based on the
                  <code>$LATEST</code> version of the specified slot type. If
                  the <code>$LATEST</code> version of this resource has not
                  changed since the last version that you created, Amazon Lex
                  doesn't create a new version. It returns the last version that
                  you created. </p> <note> <p>You can update only the
                  <code>$LATEST</code> version of a slot type. You can't update
                  the numbered versions that you create with the
                  <code>CreateSlotTypeVersion</code> operation.</p> </note>
                  <p>When you create a version of a slot type, Amazon Lex sets
                  the version to 1. Subsequent versions increment by 1. For more
                  information, see <a>versioning-intro</a>. </p> <p>This
                  operation requires permissions for the
                  <code>lex:CreateSlotTypeVersion</code> action.</p>
                tags:
                  - Create
                  - Slots
                  - Types
                  - Versions
                  - Bots
                  - Names
                  - Versions
                  - Intents
                  - Slot Types
            /bots/{name}:
              DELETE:
                summary: DeleteBot
                description: >-
                  <p>Deletes all versions of the bot, including the
                  <code>$LATEST</code> version. To delete a specific version of
                  the bot, use the <a>DeleteBotVersion</a> operation. The
                  <code>DeleteBot</code> operation doesn't immediately remove
                  the bot schema. Instead, it is marked for deletion and removed
                  later.</p> <p>Amazon Lex stores utterances indefinitely for
                  improving the ability of your bot to respond to user inputs.
                  These utterances are not removed when the bot is deleted. To
                  remove the utterances, use the <a>DeleteUtterances</a>
                  operation.</p> <p>If a bot has an alias, you can't delete it.
                  Instead, the <code>DeleteBot</code> operation returns a
                  <code>ResourceInUseException</code> exception that includes a
                  reference to the alias that refers to the bot. To remove the
                  reference to the bot, delete the alias. If you get the same
                  exception again, delete the referring alias until the
                  <code>DeleteBot</code> operation is successful.</p> <p>This
                  operation requires permissions for the
                  <code>lex:DeleteBot</code> action.</p>
                tags:
                  - Delete
                  - Bot
                  - Bots
                  - Names
                  - Versions
                  - Intents
                  - Slot Types
            /bots/{botName}/aliases/{name}:
              PUT:
                summary: PutBotAlias
                description: >-
                  <p>Creates an alias for the specified version of the bot or
                  replaces an alias for the specified bot. To change the version
                  of the bot that the alias points to, replace the alias. For
                  more information about aliases, see
                  <a>versioning-aliases</a>.</p> <p>This operation requires
                  permissions for the <code>lex:PutBotAlias</code> action. </p>
                tags:
                  - Put
                  - Bot
                  - Alias
                  - Bots
                  - Names
                  - Versions
                  - Intents
                  - Slot Types
                  - Aliases
            /bots/{botName}/aliases/{aliasName}/channels/{name}:
              GET:
                summary: GetBotChannelAssociation
                description: >-
                  <p>Returns information about the association between an Amazon
                  Lex bot and a messaging platform.</p> <p>This operation
                  requires permissions for the
                  <code>lex:GetBotChannelAssociation</code> action.</p>
                tags:
                  - Get
                  - Bot
                  - Channels
                  - Association
                  - Bots
                  - Names
                  - Versions
                  - Intents
                  - Slot Types
                  - Aliases
                  - Alias
                  - Channels
            /bots/{name}/versions/{version}:
              DELETE:
                summary: DeleteBotVersion
                description: >-
                  <p>Deletes a specific version of a bot. To delete all versions
                  of a bot, use the <a>DeleteBot</a> operation. </p> <p>This
                  operation requires permissions for the
                  <code>lex:DeleteBotVersion</code> action.</p>
                tags:
                  - Delete
                  - Bot
                  - Versions
                  - Bots
                  - Names
                  - Versions
                  - Intents
                  - Slot Types
                  - Aliases
                  - Alias
                  - Channels
                  - Versions
            /intents/{name}:
              DELETE:
                summary: DeleteIntent
                description: >-
                  <p>Deletes all versions of the intent, including the
                  <code>$LATEST</code> version. To delete a specific version of
                  the intent, use the <a>DeleteIntentVersion</a> operation.</p>
                  <p> You can delete a version of an intent only if it is not
                  referenced. To delete an intent that is referred to in one or
                  more bots (see <a>how-it-works</a>), you must remove those
                  references first. </p> <note> <p> If you get the
                  <code>ResourceInUseException</code> exception, it provides an
                  example reference that shows where the intent is referenced.
                  To remove the reference to the intent, either update the bot
                  or delete it. If you get the same exception when you attempt
                  to delete the intent again, repeat until the intent has no
                  references and the call to <code>DeleteIntent</code> is
                  successful. </p> </note> <p> This operation requires
                  permission for the <code>lex:DeleteIntent</code> action. </p>
                tags:
                  - Delete
                  - Intent
                  - Bots
                  - Names
                  - Versions
                  - Intents
                  - Slot Types
                  - Aliases
                  - Alias
                  - Channels
                  - Versions
            /intents/{name}/versions/{version}:
              GET:
                summary: GetIntent
                description: >-
                  <p> Returns information about an intent. In addition to the
                  intent name, you must specify the intent version. </p> <p>
                  This operation requires permissions to perform the
                  <code>lex:GetIntent</code> action. </p>
                tags:
                  - Get
                  - Intent
                  - Bots
                  - Names
                  - Versions
                  - Intents
                  - Slot Types
                  - Aliases
                  - Alias
                  - Channels
                  - Versions
            /slottypes/{name}:
              DELETE:
                summary: DeleteSlotType
                description: >-
                  <p>Deletes all versions of the slot type, including the
                  <code>$LATEST</code> version. To delete a specific version of
                  the slot type, use the <a>DeleteSlotTypeVersion</a>
                  operation.</p> <p> You can delete a version of a slot type
                  only if it is not referenced. To delete a slot type that is
                  referred to in one or more intents, you must remove those
                  references first. </p> <note> <p> If you get the
                  <code>ResourceInUseException</code> exception, the exception
                  provides an example reference that shows the intent where the
                  slot type is referenced. To remove the reference to the slot
                  type, either update the intent or delete it. If you get the
                  same exception when you attempt to delete the slot type again,
                  repeat until the slot type has no references and the
                  <code>DeleteSlotType</code> call is successful. </p> </note>
                  <p>This operation requires permission for the
                  <code>lex:DeleteSlotType</code> action.</p>
                tags:
                  - Delete
                  - Slots
                  - Types
                  - Bots
                  - Names
                  - Versions
                  - Intents
                  - Slot Types
                  - Aliases
                  - Alias
                  - Channels
                  - Versions
            /slottypes/{name}/version/{version}:
              DELETE:
                summary: DeleteSlotTypeVersion
                description: >-
                  <p>Deletes a specific version of a slot type. To delete all
                  versions of a slot type, use the <a>DeleteSlotType</a>
                  operation. </p> <p>This operation requires permissions for the
                  <code>lex:DeleteSlotTypeVersion</code> action.</p>
                tags:
                  - Delete
                  - Slots
                  - Types
                  - Versions
                  - Bots
                  - Names
                  - Versions
                  - Intents
                  - Slot Types
                  - Aliases
                  - Alias
                  - Channels
                  - Versions
            /bots/{botName}/utterances/{userId}:
              DELETE:
                summary: DeleteUtterances
                description: >-
                  <p>Deletes stored utterances.</p> <p>Amazon Lex stores the
                  utterances that users send to your bot. Utterances are stored
                  for 15 days for use with the <a>GetUtterancesView</a>
                  operation, and then stored indefinitely for use in improving
                  the ability of your bot to respond to user input.</p> <p>Use
                  the <code>DeleteUtterances</code> operation to manually delete
                  stored utterances for a specific user. When you use the
                  <code>DeleteUtterances</code> operation, utterances stored for
                  improving your bot's ability to respond to user input are
                  deleted immediately. Utterances stored for use with the
                  <code>GetUtterancesView</code> operation are deleted after 15
                  days.</p> <p>This operation requires permissions for the
                  <code>lex:DeleteUtterances</code> action.</p>
                tags:
                  - Delete
                  - Utterances
                  - Bots
                  - Names
                  - Versions
                  - Intents
                  - Slot Types
                  - Aliases
                  - Alias
                  - Channels
                  - Versions
                  - Utterances
                  - Users
                  - Identifiers
            /bots/{name}/versions/{versionoralias}:
              GET:
                summary: GetBot
                description: >-
                  <p>Returns metadata information for a specific bot. You must
                  provide the bot name and the bot version or alias. </p> <p>
                  This operation requires permissions for the
                  <code>lex:GetBot</code> action. </p>
                tags:
                  - Get
                  - Bot
                  - Bots
                  - Names
                  - Versions
                  - Intents
                  - Slot Types
                  - Aliases
                  - Alias
                  - Channels
                  - Versions
                  - Utterances
                  - Users
                  - Identifiers
                  - Versionoralias
            /bots/{botName}/aliases/:
              GET:
                summary: GetBotAliases
                description: >-
                  <p>Returns a list of aliases for a specified Amazon Lex
                  bot.</p> <p>This operation requires permissions for the
                  <code>lex:GetBotAliases</code> action.</p>
                tags:
                  - Get
                  - Bot
                  - Aliases
                  - Bots
                  - Names
                  - Versions
                  - Intents
                  - Slot Types
                  - Aliases
                  - Alias
                  - Channels
                  - Versions
                  - Utterances
                  - Users
                  - Identifiers
                  - Versionoralias
            /bots/{botName}/aliases/{aliasName}/channels/:
              GET:
                summary: GetBotChannelAssociations
                description: >-
                  <p> Returns a list of all of the channels associated with the
                  specified bot. </p> <p>The
                  <code>GetBotChannelAssociations</code> operation requires
                  permissions for the <code>lex:GetBotChannelAssociations</code>
                  action.</p>
                tags:
                  - Get
                  - Bot
                  - Channels
                  - Associations
                  - Bots
                  - Names
                  - Versions
                  - Intents
                  - Slot Types
                  - Aliases
                  - Alias
                  - Channels
                  - Versions
                  - Utterances
                  - Users
                  - Identifiers
                  - Versionoralias
            /bots/{name}/versions/:
              GET:
                summary: GetBotVersions
                description: >-
                  <p>Gets information about all of the versions of a bot.</p>
                  <p>The <code>GetBotVersions</code> operation returns a
                  <code>BotMetadata</code> object for each version of a bot. For
                  example, if a bot has three numbered versions, the
                  <code>GetBotVersions</code> operation returns four
                  <code>BotMetadata</code> objects in the response, one for each
                  numbered version and one for the <code>$LATEST</code> version.
                  </p> <p>The <code>GetBotVersions</code> operation always
                  returns at least one version, the <code>$LATEST</code>
                  version.</p> <p>This operation requires permissions for the
                  <code>lex:GetBotVersions</code> action.</p>
                tags:
                  - Get
                  - Bot
                  - Versions
                  - Bots
                  - Names
                  - Versions
                  - Intents
                  - Slot Types
                  - Aliases
                  - Alias
                  - Channels
                  - Versions
                  - Utterances
                  - Users
                  - Identifiers
                  - Versionoralias
            /bots/:
              GET:
                summary: GetBots
                description: >-
                  <p>Returns bot information as follows: </p> <ul> <li> <p>If
                  you provide the <code>nameContains</code> field, the response
                  includes information for the <code>$LATEST</code> version of
                  all bots whose name contains the specified string.</p> </li>
                  <li> <p>If you don't specify the <code>nameContains</code>
                  field, the operation returns information about the
                  <code>$LATEST</code> version of all of your bots.</p> </li>
                  </ul> <p>This operation requires permission for the
                  <code>lex:GetBots</code> action.</p>
                tags:
                  - Get
                  - Bots
                  - Bots
                  - Names
                  - Versions
                  - Intents
                  - Slot Types
                  - Aliases
                  - Alias
                  - Channels
                  - Versions
                  - Utterances
                  - Users
                  - Identifiers
                  - Versionoralias
            /builtins/intents/{signature}:
              GET:
                summary: GetBuiltinIntent
                description: >-
                  <p>Returns information about a built-in intent.</p> <p>This
                  operation requires permission for the
                  <code>lex:GetBuiltinIntent</code> action.</p>
                tags:
                  - Get
                  - Built In
                  - Intent
                  - Bots
                  - Names
                  - Versions
                  - Intents
                  - Slot Types
                  - Aliases
                  - Alias
                  - Channels
                  - Versions
                  - Utterances
                  - Users
                  - Identifiers
                  - Versionoralias
                  - Built In
                  - Signatures
            /builtins/intents/:
              GET:
                summary: GetBuiltinIntents
                description: >-
                  <p>Gets a list of built-in intents that meet the specified
                  criteria.</p> <p>This operation requires permission for the
                  <code>lex:GetBuiltinIntents</code> action.</p>
                tags:
                  - Get
                  - Built In
                  - Intents
                  - Bots
                  - Names
                  - Versions
                  - Intents
                  - Slot Types
                  - Aliases
                  - Alias
                  - Channels
                  - Versions
                  - Utterances
                  - Users
                  - Identifiers
                  - Versionoralias
                  - Built In
                  - Signatures
            /builtins/slottypes/:
              GET:
                summary: GetBuiltinSlotTypes
                description: >-
                  <p>Gets a list of built-in slot types that meet the specified
                  criteria.</p> <p>For a list of built-in slot types, see <a
                  href="https://developer.amazon.com/public/solutions/alexa/alexa-skills-kit/docs/built-in-intent-ref/slot-type-reference">Slot
                  Type Reference</a> in the <i>Alexa Skills Kit</i>.</p> <p>This
                  operation requires permission for the
                  <code>lex:GetBuiltInSlotTypes</code> action.</p>
                tags:
                  - Get
                  - Built In
                  - Slots
                  - Types
                  - Bots
                  - Names
                  - Versions
                  - Intents
                  - Slot Types
                  - Aliases
                  - Alias
                  - Channels
                  - Versions
                  - Utterances
                  - Users
                  - Identifiers
                  - Versionoralias
                  - Built In
                  - Signatures
            /exports/:
              GET:
                summary: GetExport
                description: >-
                  <p>Exports the contents of a Amazon Lex resource in a
                  specified format. </p>
                tags:
                  - Get
                  - Export
                  - Bots
                  - Names
                  - Versions
                  - Intents
                  - Slot Types
                  - Aliases
                  - Alias
                  - Channels
                  - Versions
                  - Utterances
                  - Users
                  - Identifiers
                  - Versionoralias
                  - Built In
                  - Signatures
                  - Exports
            /imports/{importId}:
              GET:
                summary: GetImport
                description: >-
                  <p>Gets information about an import job started with the
                  <code>StartImport</code> operation.</p>
                tags:
                  - Get
                  - Import
                  - Bots
                  - Names
                  - Versions
                  - Intents
                  - Slot Types
                  - Aliases
                  - Alias
                  - Channels
                  - Versions
                  - Utterances
                  - Users
                  - Identifiers
                  - Versionoralias
                  - Built In
                  - Signatures
                  - Exports
            /intents/{name}/versions/:
              GET:
                summary: GetIntentVersions
                description: >-
                  <p>Gets information about all of the versions of an
                  intent.</p> <p>The <code>GetIntentVersions</code> operation
                  returns an <code>IntentMetadata</code> object for each version
                  of an intent. For example, if an intent has three numbered
                  versions, the <code>GetIntentVersions</code> operation returns
                  four <code>IntentMetadata</code> objects in the response, one
                  for each numbered version and one for the <code>$LATEST</code>
                  version. </p> <p>The <code>GetIntentVersions</code> operation
                  always returns at least one version, the <code>$LATEST</code>
                  version.</p> <p>This operation requires permissions for the
                  <code>lex:GetIntentVersions</code> action.</p>
                tags:
                  - Get
                  - Intent
                  - Versions
                  - Bots
                  - Names
                  - Versions
                  - Intents
                  - Slot Types
                  - Aliases
                  - Alias
                  - Channels
                  - Versions
                  - Utterances
                  - Users
                  - Identifiers
                  - Versionoralias
                  - Built In
                  - Signatures
                  - Exports
            /intents/:
              GET:
                summary: GetIntents
                description: >-
                  <p>Returns intent information as follows: </p> <ul> <li> <p>If
                  you specify the <code>nameContains</code> field, returns the
                  <code>$LATEST</code> version of all intents that contain the
                  specified string.</p> </li> <li> <p> If you don't specify the
                  <code>nameContains</code> field, returns information about the
                  <code>$LATEST</code> version of all intents. </p> </li> </ul>
                  <p> The operation requires permission for the
                  <code>lex:GetIntents</code> action. </p>
                tags:
                  - Get
                  - Intents
                  - Bots
                  - Names
                  - Versions
                  - Intents
                  - Slot Types
                  - Aliases
                  - Alias
                  - Channels
                  - Versions
                  - Utterances
                  - Users
                  - Identifiers
                  - Versionoralias
                  - Built In
                  - Signatures
                  - Exports
            /migrations/{migrationId}:
              GET:
                summary: GetMigration
                description: >-
                  <p>Provides details about an ongoing or complete migration
                  from an Amazon Lex V1 bot to an Amazon Lex V2 bot. Use this
                  operation to view the migration alerts and warnings related to
                  the migration.</p>
                tags:
                  - Get
                  - Migrations
                  - Bots
                  - Names
                  - Versions
                  - Intents
                  - Slot Types
                  - Aliases
                  - Alias
                  - Channels
                  - Versions
                  - Utterances
                  - Users
                  - Identifiers
                  - Versionoralias
                  - Built In
                  - Signatures
                  - Exports
            /migrations:
              POST:
                summary: StartMigration
                description: >-
                  <p>Starts migrating a bot from Amazon Lex V1 to Amazon Lex V2.
                  Migrate your bot when you want to take advantage of the new
                  features of Amazon Lex V2.</p> <p>For more information, see <a
                  href="https://docs.aws.amazon.com/lex/latest/dg/migrate.html">Migrating
                  a bot</a> in the <i>Amazon Lex developer guide</i>.</p>
                tags:
                  - Start
                  - Migrations
                  - Bots
                  - Names
                  - Versions
                  - Intents
                  - Slot Types
                  - Aliases
                  - Alias
                  - Channels
                  - Versions
                  - Utterances
                  - Users
                  - Identifiers
                  - Versionoralias
                  - Built In
                  - Signatures
                  - Exports
                  - Migrations
            /slottypes/{name}/versions/{version}:
              GET:
                summary: GetSlotType
                description: >-
                  <p>Returns information about a specific version of a slot
                  type. In addition to specifying the slot type name, you must
                  specify the slot type version.</p> <p>This operation requires
                  permissions for the <code>lex:GetSlotType</code> action.</p>
                tags:
                  - Get
                  - Slots
                  - Types
                  - Bots
                  - Names
                  - Versions
                  - Intents
                  - Slot Types
                  - Aliases
                  - Alias
                  - Channels
                  - Versions
                  - Utterances
                  - Users
                  - Identifiers
                  - Versionoralias
                  - Built In
                  - Signatures
                  - Exports
                  - Migrations
            /slottypes/{name}/versions/:
              GET:
                summary: GetSlotTypeVersions
                description: >-
                  <p>Gets information about all versions of a slot type.</p>
                  <p>The <code>GetSlotTypeVersions</code> operation returns a
                  <code>SlotTypeMetadata</code> object for each version of a
                  slot type. For example, if a slot type has three numbered
                  versions, the <code>GetSlotTypeVersions</code> operation
                  returns four <code>SlotTypeMetadata</code> objects in the
                  response, one for each numbered version and one for the
                  <code>$LATEST</code> version. </p> <p>The
                  <code>GetSlotTypeVersions</code> operation always returns at
                  least one version, the <code>$LATEST</code> version.</p>
                  <p>This operation requires permissions for the
                  <code>lex:GetSlotTypeVersions</code> action.</p>
                tags:
                  - Get
                  - Slots
                  - Types
                  - Versions
                  - Bots
                  - Names
                  - Versions
                  - Intents
                  - Slot Types
                  - Aliases
                  - Alias
                  - Channels
                  - Versions
                  - Utterances
                  - Users
                  - Identifiers
                  - Versionoralias
                  - Built In
                  - Signatures
                  - Exports
                  - Migrations
            /slottypes/:
              GET:
                summary: GetSlotTypes
                description: >-
                  <p>Returns slot type information as follows: </p> <ul> <li>
                  <p>If you specify the <code>nameContains</code> field, returns
                  the <code>$LATEST</code> version of all slot types that
                  contain the specified string.</p> </li> <li> <p> If you don't
                  specify the <code>nameContains</code> field, returns
                  information about the <code>$LATEST</code> version of all slot
                  types. </p> </li> </ul> <p> The operation requires permission
                  for the <code>lex:GetSlotTypes</code> action. </p>
                tags:
                  - Get
                  - Slots
                  - Types
                  - Bots
                  - Names
                  - Versions
                  - Intents
                  - Slot Types
                  - Aliases
                  - Alias
                  - Channels
                  - Versions
                  - Utterances
                  - Users
                  - Identifiers
                  - Versionoralias
                  - Built In
                  - Signatures
                  - Exports
                  - Migrations
            /bots/{botname}/utterances?view=aggregation:
              GET:
                summary: GetUtterancesView
                description: >-
                  <p>Use the <code>GetUtterancesView</code> operation to get
                  information about the utterances that your users have made to
                  your bot. You can use this list to tune the utterances that
                  your bot responds to.</p> <p>For example, say that you have
                  created a bot to order flowers. After your users have used
                  your bot for a while, use the <code>GetUtterancesView</code>
                  operation to see the requests that they have made and whether
                  they have been successful. You might find that the utterance
                  "I want flowers" is not being recognized. You could add this
                  utterance to the <code>OrderFlowers</code> intent so that your
                  bot recognizes that utterance.</p> <p>After you publish a new
                  version of a bot, you can get information about the old
                  version and the new so that you can compare the performance
                  across the two versions. </p> <p>Utterance statistics are
                  generated once a day. Data is available for the last 15 days.
                  You can request information for up to 5 versions of your bot
                  in each request. Amazon Lex returns the most frequent
                  utterances received by the bot in the last 15 days. The
                  response contains information about a maximum of 100
                  utterances for each version.</p> <p>If you set
                  <code>childDirected</code> field to true when you created your
                  bot, if you are using slot obfuscation with one or more slots,
                  or if you opted out of participating in improving Amazon Lex,
                  utterances are not available.</p> <p>This operation requires
                  permissions for the <code>lex:GetUtterancesView</code>
                  action.</p>
                tags:
                  - Get
                  - Utterances
                  - View
                  - Bots
                  - Names
                  - Versions
                  - Intents
                  - Slot Types
                  - Aliases
                  - Alias
                  - Channels
                  - Versions
                  - Utterances
                  - Users
                  - Identifiers
                  - Versionoralias
                  - Built In
                  - Signatures
                  - Exports
                  - Migrations
                  - Bot Name
                  - Utterances
            /tags/{resourceArn}:
              DELETE:
                summary: UntagResource
                description: <p>Removes tags from a bot, bot alias or bot channel.</p>
                tags:
                  - Untag
                  - Resources
                  - Bots
                  - Names
                  - Versions
                  - Intents
                  - Slot Types
                  - Aliases
                  - Alias
                  - Channels
                  - Versions
                  - Utterances
                  - Users
                  - Identifiers
                  - Versionoralias
                  - Built In
                  - Signatures
                  - Exports
                  - Migrations
                  - Bot Name
                  - Utterances
                  - ARN
            /bots/{name}/versions/$LATEST:
              PUT:
                summary: PutBot
                description: >-
                  <p>Creates an Amazon Lex conversational bot or replaces an
                  existing bot. When you create or update a bot you are only
                  required to specify a name, a locale, and whether the bot is
                  directed toward children under age 13. You can use this to add
                  intents later, or to remove intents from an existing bot. When
                  you create a bot with the minimum information, the bot is
                  created or updated but Amazon Lex returns the <code/> response
                  <code>FAILED</code>. You can build the bot after you add one
                  or more intents. For more information about Amazon Lex bots,
                  see <a>how-it-works</a>. </p> <p>If you specify the name of an
                  existing bot, the fields in the request replace the existing
                  values in the <code>$LATEST</code> version of the bot. Amazon
                  Lex removes any fields that you don't provide values for in
                  the request, except for the <code>idleTTLInSeconds</code> and
                  <code>privacySettings</code> fields, which are set to their
                  default values. If you don't specify values for required
                  fields, Amazon Lex throws an exception.</p> <p>This operation
                  requires permissions for the <code>lex:PutBot</code> action.
                  For more information, see <a>security-iam</a>.</p>
                tags:
                  - Put
                  - Bot
                  - Bots
                  - Names
                  - Versions
                  - Intents
                  - Slot Types
                  - Aliases
                  - Alias
                  - Channels
                  - Versions
                  - Utterances
                  - Users
                  - Identifiers
                  - Versionoralias
                  - Built In
                  - Signatures
                  - Exports
                  - Migrations
                  - Bot Name
                  - Utterances
                  - ARN
                  - $LATEST
            /intents/{name}/versions/$LATEST:
              PUT:
                summary: PutIntent
                description: >-
                  <p>Creates an intent or replaces an existing intent.</p> <p>To
                  define the interaction between the user and your bot, you use
                  one or more intents. For a pizza ordering bot, for example,
                  you would create an <code>OrderPizza</code> intent. </p> <p>To
                  create an intent or replace an existing intent, you must
                  provide the following:</p> <ul> <li> <p>Intent name. For
                  example, <code>OrderPizza</code>.</p> </li> <li> <p>Sample
                  utterances. For example, "Can I order a pizza, please." and "I
                  want to order a pizza."</p> </li> <li> <p>Information to be
                  gathered. You specify slot types for the information that your
                  bot will request from the user. You can specify standard slot
                  types, such as a date or a time, or custom slot types such as
                  the size and crust of a pizza.</p> </li> <li> <p>How the
                  intent will be fulfilled. You can provide a Lambda function or
                  configure the intent to return the intent information to the
                  client application. If you use a Lambda function, when all of
                  the intent information is available, Amazon Lex invokes your
                  Lambda function. If you configure your intent to return the
                  intent information to the client application. </p> </li> </ul>
                  <p>You can specify other optional information in the request,
                  such as:</p> <ul> <li> <p>A confirmation prompt to ask the
                  user to confirm an intent. For example, "Shall I order your
                  pizza?"</p> </li> <li> <p>A conclusion statement to send to
                  the user after the intent has been fulfilled. For example, "I
                  placed your pizza order."</p> </li> <li> <p>A follow-up prompt
                  that asks the user for additional activity. For example,
                  asking "Do you want to order a drink with your pizza?"</p>
                  </li> </ul> <p>If you specify an existing intent name to
                  update the intent, Amazon Lex replaces the values in the
                  <code>$LATEST</code> version of the intent with the values in
                  the request. Amazon Lex removes fields that you don't provide
                  in the request. If you don't specify the required fields,
                  Amazon Lex throws an exception. When you update the
                  <code>$LATEST</code> version of an intent, the
                  <code>status</code> field of any bot that uses the
                  <code>$LATEST</code> version of the intent is set to
                  <code>NOT_BUILT</code>.</p> <p>For more information, see
                  <a>how-it-works</a>.</p> <p>This operation requires
                  permissions for the <code>lex:PutIntent</code> action.</p>
                tags:
                  - Put
                  - Intent
                  - Bots
                  - Names
                  - Versions
                  - Intents
                  - Slot Types
                  - Aliases
                  - Alias
                  - Channels
                  - Versions
                  - Utterances
                  - Users
                  - Identifiers
                  - Versionoralias
                  - Built In
                  - Signatures
                  - Exports
                  - Migrations
                  - Bot Name
                  - Utterances
                  - ARN
                  - $LATEST
            /slottypes/{name}/versions/$LATEST:
              PUT:
                summary: PutSlotType
                description: >-
                  <p>Creates a custom slot type or replaces an existing custom
                  slot type.</p> <p>To create a custom slot type, specify a name
                  for the slot type and a set of enumeration values, which are
                  the values that a slot of this type can assume. For more
                  information, see <a>how-it-works</a>.</p> <p>If you specify
                  the name of an existing slot type, the fields in the request
                  replace the existing values in the <code>$LATEST</code>
                  version of the slot type. Amazon Lex removes the fields that
                  you don't provide in the request. If you don't specify
                  required fields, Amazon Lex throws an exception. When you
                  update the <code>$LATEST</code> version of a slot type, if a
                  bot uses the <code>$LATEST</code> version of an intent that
                  contains the slot type, the bot's <code>status</code> field is
                  set to <code>NOT_BUILT</code>.</p> <p>This operation requires
                  permissions for the <code>lex:PutSlotType</code> action.</p>
                tags:
                  - Put
                  - Slots
                  - Types
                  - Bots
                  - Names
                  - Versions
                  - Intents
                  - Slot Types
                  - Aliases
                  - Alias
                  - Channels
                  - Versions
                  - Utterances
                  - Users
                  - Identifiers
                  - Versionoralias
                  - Built In
                  - Signatures
                  - Exports
                  - Migrations
                  - Bot Name
                  - Utterances
                  - ARN
                  - $LATEST
            /imports/:
              POST:
                summary: StartImport
                description: <p>Starts a job to import a resource to Amaz
                tags:
                  - Start
                  - Import
                  - Bots
                  - Names
                  - Versions
                  - Intents
                  - Slot Types
                  - Aliases
                  - Alias
                  - Channels
                  - Versions
                  - Utterances
                  - Users
                  - Identifiers
                  - Versionoralias
                  - Built In
                  - Signatures
                  - Exports
                  - Migrations
                  - Bot Name
                  - Utterances
                  - ARN
                  - $LATEST
                  - Import
    overlays:
      - type: APIs.io Search
        url: overlays/lex-models-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/lex-models-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:lex-models
  - name: medialive
    description: API for AWS Elemental MediaLive
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
            title: medialive
          paths:
            /prod/inputDevices/{inputDeviceId}/accept:
              POST:
                summary: AcceptInputDeviceTransfer
                description: >-
                  Accept an incoming input device transfer. The ownership of the
                  device will transfer to your AWS account.
                tags:
                  - Accept
                  - Inputs
                  - Device
                  - Transfers
                  - Devices
                  - Inputs
                  - Device
                  - Identifiers
                  - Accept
            /prod/batch/delete:
              POST:
                summary: BatchDelete
                description: Starts delete of resources.
                tags:
                  - Batches
                  - Delete
                  - Devices
                  - Inputs
                  - Device
                  - Identifiers
                  - Accept
                  - Prod
                  - Batches
                  - Delete
            /prod/batch/start:
              POST:
                summary: BatchStart
                description: Starts existing resources
                tags:
                  - Batches
                  - Start
                  - Devices
                  - Inputs
                  - Device
                  - Identifiers
                  - Accept
                  - Prod
                  - Batches
                  - Delete
                  - Start
            /prod/batch/stop:
              POST:
                summary: BatchStop
                description: Stops running resources
                tags:
                  - Batches
                  - Stop
                  - Devices
                  - Inputs
                  - Device
                  - Identifiers
                  - Accept
                  - Prod
                  - Batches
                  - Delete
                  - Start
                  - Stop
            /prod/channels/{channelId}/schedule:
              GET:
                summary: DescribeSchedule
                description: Get a channel schedule
                tags:
                  - Describe
                  - Schedules
                  - Devices
                  - Inputs
                  - Device
                  - Identifiers
                  - Accept
                  - Prod
                  - Batches
                  - Delete
                  - Start
                  - Stop
                  - Schedules
            /prod/inputDevices/{inputDeviceId}/cancel:
              POST:
                summary: CancelInputDeviceTransfer
                description: Cancel an input device transfer that you have requested.
                tags:
                  - Cancel
                  - Inputs
                  - Device
                  - Transfers
                  - Devices
                  - Inputs
                  - Device
                  - Identifiers
                  - Accept
                  - Prod
                  - Batches
                  - Delete
                  - Start
                  - Stop
                  - Schedules
                  - Cancel
            /prod/claimDevice:
              POST:
                summary: ClaimDevice
                description: >-
                  Send a request to claim an AWS Elemental device that you have
                  purchased from a third-party vendor. After the request
                  succeeds, you will own the device.
                tags:
                  - Claim
                  - Device
                  - Devices
                  - Inputs
                  - Device
                  - Identifiers
                  - Accept
                  - Prod
                  - Batches
                  - Delete
                  - Start
                  - Stop
                  - Schedules
                  - Cancel
            /prod/channels:
              GET:
                summary: ListChannels
                description: Produces list of channels that have been created
                tags:
                  - Lists
                  - Channels
                  - Devices
                  - Inputs
                  - Device
                  - Identifiers
                  - Accept
                  - Prod
                  - Batches
                  - Delete
                  - Start
                  - Stop
                  - Schedules
                  - Cancel
                  - Channels
            /prod/inputs:
              GET:
                summary: ListInputs
                description: Produces list of inputs that have been created
                tags:
                  - Lists
                  - Inputs
                  - Devices
                  - Inputs
                  - Device
                  - Identifiers
                  - Accept
                  - Prod
                  - Batches
                  - Delete
                  - Start
                  - Stop
                  - Schedules
                  - Cancel
                  - Channels
                  - Inputs
            /prod/inputSecurityGroups:
              GET:
                summary: ListInputSecurityGroups
                description: Produces a list of Input Security Groups for an account
                tags:
                  - Lists
                  - Inputs
                  - Security
                  - Groups
                  - Devices
                  - Inputs
                  - Device
                  - Identifiers
                  - Accept
                  - Prod
                  - Batches
                  - Delete
                  - Start
                  - Stop
                  - Schedules
                  - Cancel
                  - Channels
                  - Inputs
                  - Security
                  - Groups
            /prod/multiplexes:
              GET:
                summary: ListMultiplexes
                description: Retrieve a list of the existing multiplexes.
                tags:
                  - Lists
                  - Multiplexes
                  - Devices
                  - Inputs
                  - Device
                  - Identifiers
                  - Accept
                  - Prod
                  - Batches
                  - Delete
                  - Start
                  - Stop
                  - Schedules
                  - Cancel
                  - Channels
                  - Inputs
                  - Security
                  - Groups
                  - Multiplexes
            /prod/multiplexes/{multiplexId}/programs:
              GET:
                summary: ListMultiplexPrograms
                description: >-
                  List the programs that currently exist for a specific
                  multiplex.
                tags:
                  - Lists
                  - Multiplex
                  - Programs
                  - Devices
                  - Inputs
                  - Device
                  - Identifiers
                  - Accept
                  - Prod
                  - Batches
                  - Delete
                  - Start
                  - Stop
                  - Schedules
                  - Cancel
                  - Channels
                  - Inputs
                  - Security
                  - Groups
                  - Multiplexes
                  - Programs
            /prod/inputs/{inputId}/partners:
              POST:
                summary: CreatePartnerInput
                description: Create a partner input
                tags:
                  - Create
                  - Partners
                  - Inputs
                  - Devices
                  - Inputs
                  - Device
                  - Identifiers
                  - Accept
                  - Prod
                  - Batches
                  - Delete
                  - Start
                  - Stop
                  - Schedules
                  - Cancel
                  - Channels
                  - Inputs
                  - Security
                  - Groups
                  - Multiplexes
                  - Programs
                  - Partners
            /prod/tags/{resource-arn}:
              GET:
                summary: ListTagsForResource
                description: Produces list of tags that have been created for a resource
                tags:
                  - Lists
                  - Tags
                  - For
                  - Resources
                  - Devices
                  - Inputs
                  - Device
                  - Identifiers
                  - Accept
                  - Prod
                  - Batches
                  - Delete
                  - Start
                  - Stop
                  - Schedules
                  - Cancel
                  - Channels
                  - Inputs
                  - Security
                  - Groups
                  - Multiplexes
                  - Programs
                  - Partners
                  - Tags
                  - Resources
                  - ARN
            /prod/channels/{channelId}:
              PUT:
                summary: UpdateChannel
                description: Updates a channel.
                tags:
                  - Update
                  - Channels
                  - Devices
                  - Inputs
                  - Device
                  - Identifiers
                  - Accept
                  - Prod
                  - Batches
                  - Delete
                  - Start
                  - Stop
                  - Schedules
                  - Cancel
                  - Channels
                  - Inputs
                  - Security
                  - Groups
                  - Multiplexes
                  - Programs
                  - Partners
                  - Tags
                  - Resources
                  - ARN
            /prod/inputs/{inputId}:
              PUT:
                summary: UpdateInput
                description: Updates an input.
                tags:
                  - Update
                  - Inputs
                  - Devices
                  - Inputs
                  - Device
                  - Identifiers
                  - Accept
                  - Prod
                  - Batches
                  - Delete
                  - Start
                  - Stop
                  - Schedules
                  - Cancel
                  - Channels
                  - Inputs
                  - Security
                  - Groups
                  - Multiplexes
                  - Programs
                  - Partners
                  - Tags
                  - Resources
                  - ARN
            /prod/inputSecurityGroups/{inputSecurityGroupId}:
              PUT:
                summary: UpdateInputSecurityGroup
                description: Update an Input Security Group's Whilelists.
                tags:
                  - Update
                  - Inputs
                  - Security
                  - Group
                  - Devices
                  - Inputs
                  - Device
                  - Identifiers
                  - Accept
                  - Prod
                  - Batches
                  - Delete
                  - Start
                  - Stop
                  - Schedules
                  - Cancel
                  - Channels
                  - Inputs
                  - Security
                  - Groups
                  - Multiplexes
                  - Programs
                  - Partners
                  - Tags
                  - Resources
                  - ARN
                  - Group
            /prod/multiplexes/{multiplexId}:
              PUT:
                summary: UpdateMultiplex
                description: Updates a multiplex.
                tags:
                  - Update
                  - Multiplex
                  - Devices
                  - Inputs
                  - Device
                  - Identifiers
                  - Accept
                  - Prod
                  - Batches
                  - Delete
                  - Start
                  - Stop
                  - Schedules
                  - Cancel
                  - Channels
                  - Inputs
                  - Security
                  - Groups
                  - Multiplexes
                  - Programs
                  - Partners
                  - Tags
                  - Resources
                  - ARN
                  - Group
            /prod/multiplexes/{multiplexId}/programs/{programName}:
              PUT:
                summary: UpdateMultiplexProgram
                description: Update a program in a multiplex.
                tags:
                  - Update
                  - Multiplex
                  - Program
                  - Devices
                  - Inputs
                  - Device
                  - Identifiers
                  - Accept
                  - Prod
                  - Batches
                  - Delete
                  - Start
                  - Stop
                  - Schedules
                  - Cancel
                  - Channels
                  - Inputs
                  - Security
                  - Groups
                  - Multiplexes
                  - Programs
                  - Partners
                  - Tags
                  - Resources
                  - ARN
                  - Group
                  - Program
                  - Names
            /prod/reservations/{reservationId}:
              PUT:
                summary: UpdateReservation
                description: Update reservation.
                tags:
                  - Update
                  - Reservations
                  - Devices
                  - Inputs
                  - Device
                  - Identifiers
                  - Accept
                  - Prod
                  - Batches
                  - Delete
                  - Start
                  - Stop
                  - Schedules
                  - Cancel
                  - Channels
                  - Inputs
                  - Security
                  - Groups
                  - Multiplexes
                  - Programs
                  - Partners
                  - Tags
                  - Resources
                  - ARN
                  - Group
                  - Program
                  - Names
            /prod/accountConfiguration:
              PUT:
                summary: UpdateAccountConfiguration
                description: Update account configuration
                tags:
                  - Update
                  - Account
                  - Configurations
                  - Devices
                  - Inputs
                  - Device
                  - Identifiers
                  - Accept
                  - Prod
                  - Batches
                  - Delete
                  - Start
                  - Stop
                  - Schedules
                  - Cancel
                  - Channels
                  - Inputs
                  - Security
                  - Groups
                  - Multiplexes
                  - Programs
                  - Partners
                  - Tags
                  - Resources
                  - ARN
                  - Group
                  - Program
                  - Names
                  - Configurations
            /prod/inputDevices/{inputDeviceId}:
              PUT:
                summary: UpdateInputDevice
                description: Updates the parameters for the input device.
                tags:
                  - Update
                  - Inputs
                  - Device
                  - Devices
                  - Inputs
                  - Device
                  - Identifiers
                  - Accept
                  - Prod
                  - Batches
                  - Delete
                  - Start
                  - Stop
                  - Schedules
                  - Cancel
                  - Channels
                  - Inputs
                  - Security
                  - Groups
                  - Multiplexes
                  - Programs
                  - Partners
                  - Tags
                  - Resources
                  - ARN
                  - Group
                  - Program
                  - Names
                  - Configurations
            /prod/inputDevices/{inputDeviceId}/thumbnailData:
              GET:
                summary: DescribeInputDeviceThumbnail
                description: Get the latest thumbnail data for the input device.
                tags:
                  - Describe
                  - Inputs
                  - Device
                  - Thumbnails
                  - Devices
                  - Inputs
                  - Device
                  - Identifiers
                  - Accept
                  - Prod
                  - Batches
                  - Delete
                  - Start
                  - Stop
                  - Schedules
                  - Cancel
                  - Channels
                  - Inputs
                  - Security
                  - Groups
                  - Multiplexes
                  - Programs
                  - Partners
                  - Tags
                  - Resources
                  - ARN
                  - Group
                  - Program
                  - Names
                  - Configurations
                  - Thumbnails
                  - Data
            /prod/offerings/{offeringId}:
              GET:
                summary: DescribeOffering
                description: Get details for an offering.
                tags:
                  - Describe
                  - Offerings
                  - Devices
                  - Inputs
                  - Device
                  - Identifiers
                  - Accept
                  - Prod
                  - Batches
                  - Delete
                  - Start
                  - Stop
                  - Schedules
                  - Cancel
                  - Channels
                  - Inputs
                  - Security
                  - Groups
                  - Multiplexes
                  - Programs
                  - Partners
                  - Tags
                  - Resources
                  - ARN
                  - Group
                  - Program
                  - Names
                  - Configurations
                  - Thumbnails
                  - Data
            /prod/channels/{channelId}/thumbnails:
              GET:
                summary: DescribeThumbnails
                description: Describe the latest thumbnails data.
                tags:
                  - Describe
                  - Thumbnails
                  - Devices
                  - Inputs
                  - Device
                  - Identifiers
                  - Accept
                  - Prod
                  - Batches
                  - Delete
                  - Start
                  - Stop
                  - Schedules
                  - Cancel
                  - Channels
                  - Inputs
                  - Security
                  - Groups
                  - Multiplexes
                  - Programs
                  - Partners
                  - Tags
                  - Resources
                  - ARN
                  - Group
                  - Program
                  - Names
                  - Configurations
                  - Thumbnails
                  - Data
                  - Thumbnails
            /prod/inputDeviceTransfers:
              GET:
                summary: ListInputDeviceTransfers
                description: >-
                  List input devices that are currently being transferred. List
                  input devices that you are transferring from your AWS account
                  or input devices that another AWS account is transferring to
                  you.
                tags:
                  - Lists
                  - Inputs
                  - Device
                  - Transfers
                  - Devices
                  - Inputs
                  - Device
                  - Identifiers
                  - Accept
                  - Prod
                  - Batches
                  - Delete
                  - Start
                  - Stop
                  - Schedules
                  - Cancel
                  - Channels
                  - Inputs
                  - Security
                  - Groups
                  - Multiplexes
                  - Programs
                  - Partners
                  - Tags
                  - Resources
                  - ARN
                  - Group
                  - Program
                  - Names
                  - Configurations
                  - Thumbnails
                  - Data
                  - Thumbnails
                  - Transfers
            /prod/inputDevices:
              GET:
                summary: ListInputDevices
                description: List input devices
                tags:
                  - Lists
                  - Inputs
                  - Devices
                  - Devices
                  - Inputs
                  - Device
                  - Identifiers
                  - Accept
                  - Prod
                  - Batches
                  - Delete
                  - Start
                  - Stop
                  - Schedules
                  - Cancel
                  - Channels
                  - Inputs
                  - Security
                  - Groups
                  - Multiplexes
                  - Programs
                  - Partners
                  - Tags
                  - Resources
                  - ARN
                  - Group
                  - Program
                  - Names
                  - Configurations
                  - Thumbnails
                  - Data
                  - Thumbnails
                  - Transfers
            /prod/offerings:
              GET:
                summary: ListOfferings
                description: List offerings available for purchase.
                tags:
                  - Lists
                  - Offerings
                  - Devices
                  - Inputs
                  - Device
                  - Identifiers
                  - Accept
                  - Prod
                  - Batches
                  - Delete
                  - Start
                  - Stop
                  - Schedules
                  - Cancel
                  - Channels
                  - Inputs
                  - Security
                  - Groups
                  - Multiplexes
                  - Programs
                  - Partners
                  - Tags
                  - Resources
                  - ARN
                  - Group
                  - Program
                  - Names
                  - Configurations
                  - Thumbnails
                  - Data
                  - Thumbnails
                  - Transfers
                  - Offerings
            /prod/reservations:
              GET:
                summary: ListReservations
                description: List purchased reservations.
                tags:
                  - Lists
                  - Reservations
                  - Devices
                  - Inputs
                  - Device
                  - Identifiers
                  - Accept
                  - Prod
                  - Batches
                  - Delete
                  - Start
                  - Stop
                  - Schedules
                  - Cancel
                  - Channels
                  - Inputs
                  - Security
                  - Groups
                  - Multiplexes
                  - Programs
                  - Partners
                  - Tags
                  - Resources
                  - ARN
                  - Group
                  - Program
                  - Names
                  - Configurations
                  - Thumbnails
                  - Data
                  - Thumbnails
                  - Transfers
                  - Offerings
                  - Reservations
            /prod/offerings/{offeringId}/purchase:
              POST:
                summary: PurchaseOffering
                description: Purchase an offering and create a reservation.
                tags:
                  - Purchase
                  - Offerings
                  - Devices
                  - Inputs
                  - Device
                  - Identifiers
                  - Accept
                  - Prod
                  - Batches
                  - Delete
                  - Start
                  - Stop
                  - Schedules
                  - Cancel
                  - Channels
                  - Inputs
                  - Security
                  - Groups
                  - Multiplexes
                  - Programs
                  - Partners
                  - Tags
                  - Resources
                  - ARN
                  - Group
                  - Program
                  - Names
                  - Configurations
                  - Thumbnails
                  - Data
                  - Thumbnails
                  - Transfers
                  - Offerings
                  - Reservations
                  - Purchase
            /prod/inputDevices/{inputDeviceId}/reboot:
              POST:
                summary: RebootInputDevice
                description: >-
                  Send a reboot command to the specified input device. The
                  device will begin rebooting within a few seconds of sending
                  the command. When the reboot is complete, the device’s
                  connection status will change to connected.
                tags:
                  - Reboot
                  - Inputs
                  - Device
                  - Devices
                  - Inputs
                  - Device
                  - Identifiers
                  - Accept
                  - Prod
                  - Batches
                  - Delete
                  - Start
                  - Stop
                  - Schedules
                  - Cancel
                  - Channels
                  - Inputs
                  - Security
                  - Groups
                  - Multiplexes
                  - Programs
                  - Partners
                  - Tags
                  - Resources
                  - ARN
                  - Group
                  - Program
                  - Names
                  - Configurations
                  - Thumbnails
                  - Data
                  - Thumbnails
                  - Transfers
                  - Offerings
                  - Reservations
                  - Purchase
                  - Reboot
            /prod/inputDevices/{inputDeviceId}/reject:
              POST:
                summary: RejectInputDeviceTransfer
                description: >-
                  Reject the transfer of the specified input device to your AWS
                  account.
                tags:
                  - Reject
                  - Inputs
                  - Device
                  - Transfers
                  - Devices
                  - Inputs
                  - Device
                  - Identifiers
                  - Accept
                  - Prod
                  - Batches
                  - Delete
                  - Start
                  - Stop
                  - Schedules
                  - Cancel
                  - Channels
                  - Inputs
                  - Security
                  - Groups
                  - Multiplexes
                  - Programs
                  - Partners
                  - Tags
                  - Resources
                  - ARN
                  - Group
                  - Program
                  - Names
                  - Configurations
                  - Thumbnails
                  - Data
                  - Thumbnails
                  - Transfers
                  - Offerings
                  - Reservations
                  - Purchase
                  - Reboot
                  - Reject
            /prod/channels/{channelId}/start:
              POST:
                summary: StartChannel
                description: Starts an existing channel
                tags:
                  - Start
                  - Channels
                  - Devices
                  - Inputs
                  - Device
                  - Identifiers
                  - Accept
                  - Prod
                  - Batches
                  - Delete
                  - Start
                  - Stop
                  - Schedules
                  - Cancel
                  - Channels
                  - Inputs
                  - Security
                  - Groups
                  - Multiplexes
                  - Programs
                  - Partners
                  - Tags
                  - Resources
                  - ARN
                  - Group
                  - Program
                  - Names
                  - Configurations
                  - Thumbnails
                  - Data
                  - Thumbnails
                  - Transfers
                  - Offerings
                  - Reservations
                  - Purchase
                  - Reboot
                  - Reject
            /prod/inputDevices/{inputDeviceId}/start:
              POST:
                summary: StartInputDevice
                description: >-
                  Start an input device that is attached to a MediaConnect flow.
                  (There is no need to start a device that is attached to a
                  MediaLive input; MediaLive starts the device when the channel
                  starts.)
                tags:
                  - Start
                  - Inputs
                  - Device
                  - Devices
                  - Inputs
                  - Device
                  - Identifiers
                  - Accept
                  - Prod
                  - Batches
                  - Delete
                  - Start
                  - Stop
                  - Schedules
                  - Cancel
                  - Channels
                  - Inputs
                  - Security
                  - Groups
                  - Multiplexes
                  - Programs
                  - Partners
                  - Tags
                  - Resources
                  - ARN
                  - Group
                  - Program
                  - Names
                  - Configurations
                  - Thumbnails
                  - Data
                  - Thumbnails
                  - Transfers
                  - Offerings
                  - Reservations
                  - Purchase
                  - Reboot
                  - Reject
            /prod/inputDevices/{inputDeviceId}/startInputDeviceMaintenanceWindow:
              POST:
                summary: StartInputDeviceMaintenanceWindow
                description: >-
                  Start a maintenance window for the specified input device.
                  Starting a maintenance window will give the device up to two
                  hours to install software. If the device was streaming prior
                  to the maintenance, it will resume streaming when the software
                  is fully installed. Devices automatically install updates
                  while they are powered on and their MediaLive channels are
                  stopped. A maintenance window allows you to update a device
                  without having to stop MediaLive channels that use the device.
                  The device must remain powered on and connected to the
                  internet for the duration of the maintenance.
                tags:
                  - Start
                  - Inputs
                  - Device
                  - Maintenance
                  - Window
                  - Devices
                  - Inputs
                  - Device
                  - Identifiers
                  - Accept
                  - Prod
                  - Batches
                  - Delete
                  - Start
                  - Stop
                  - Schedules
                  - Cancel
                  - Channels
                  - Inputs
                  - Security
                  - Groups
                  - Multiplexes
                  - Programs
                  - Partners
                  - Tags
                  - Resources
                  - ARN
                  - Group
                  - Program
                  - Names
                  - Configurations
                  - Thumbnails
                  - Data
                  - Thumbnails
                  - Transfers
                  - Offerings
                  - Reservations
                  - Purchase
                  - Reboot
                  - Reject
                  - Maintenance
                  - Window
            /prod/multiplexes/{multiplexId}/start:
              POST:
                summary: StartMultiplex
                description: >-
                  Start (run) the multiplex. Starting the multiplex does not
                  start the channels. You must explicitly start each channel.
                tags:
                  - Start
                  - Multiplex
                  - Devices
                  - Inputs
                  - Device
                  - Identifiers
                  - Accept
                  - Prod
                  - Batches
                  - Delete
                  - Start
                  - Stop
                  - Schedules
                  - Cancel
                  - Channels
                  - Inputs
                  - Security
                  - Groups
                  - Multiplexes
                  - Programs
                  - Partners
                  - Tags
                  - Resources
                  - ARN
                  - Group
                  - Program
                  - Names
                  - Configurations
                  - Thumbnails
                  - Data
                  - Thumbnails
                  - Transfers
                  - Offerings
                  - Reservations
                  - Purchase
                  - Reboot
                  - Reject
                  - Maintenance
                  - Window
            /prod/channels/{channelId}/stop:
              POST:
                summary: StopChannel
                description: Stops a running channel
                tags:
                  - Stop
                  - Channels
                  - Devices
                  - Inputs
                  - Device
                  - Identifiers
                  - Accept
                  - Prod
                  - Batches
                  - Delete
                  - Start
                  - Stop
                  - Schedules
                  - Cancel
                  - Channels
                  - Inputs
                  - Security
                  - Groups
                  - Multiplexes
                  - Programs
                  - Partners
                  - Tags
                  - Resources
                  - ARN
                  - Group
                  - Program
                  - Names
                  - Configurations
                  - Thumbnails
                  - Data
                  - Thumbnails
                  - Transfers
                  - Offerings
                  - Reservations
                  - Purchase
                  - Reboot
                  - Reject
                  - Maintenance
                  - Window
            /prod/inputDevices/{inputDeviceId}/stop:
              POST:
                summary: StopInputDevice
                description: >-
                  Stop an input device that is attached to a MediaConnect flow.
                  (There is no need to stop a device that is attached to a
                  MediaLive input; MediaLive automatically stops the device when
                  the channel stops.)
                tags:
                  - Stop
                  - Inputs
                  - Device
                  - Devices
                  - Inputs
                  - Device
                  - Identifiers
                  - Accept
                  - Prod
                  - Batches
                  - Delete
                  - Start
                  - Stop
                  - Schedules
                  - Cancel
                  - Channels
                  - Inputs
                  - Security
                  - Groups
                  - Multiplexes
                  - Programs
                  - Partners
                  - Tags
                  - Resources
                  - ARN
                  - Group
                  - Program
                  - Names
                  - Configurations
                  - Thumbnails
                  - Data
                  - Thumbnails
                  - Transfers
                  - Offerings
                  - Reservations
                  - Purchase
                  - Reboot
                  - Reject
                  - Maintenance
                  - Window
            /prod/multiplexes/{multiplexId}/stop:
              POST:
                summary: StopMultiplex
                description: >-
                  Stops a running multiplex. If the multiplex isn't running,
                  this action has no effect.
                tags:
                  - Stop
                  - Multiplex
                  - Devices
                  - Inputs
                  - Device
                  - Identifiers
                  - Accept
                  - Prod
                  - Batches
                  - Delete
                  - Start
                  - Stop
                  - Schedules
                  - Cancel
                  - Channels
                  - Inputs
                  - Security
                  - Groups
                  - Multiplexes
                  - Programs
                  - Partners
                  - Tags
                  - Resources
                  - ARN
                  - Group
                  - Program
                  - Names
                  - Configurations
                  - Thumbnails
                  - Data
                  - Thumbnails
                  - Transfers
                  - Offerings
                  - Reservations
                  - Purchase
                  - Reboot
                  - Reject
                  - Maintenance
                  - Window
            /prod/inputDevices/{inputDeviceId}/transfer:
              POST:
                summary: TransferInputDevice
                description: >-
                  Start an input device transfer to another AWS account. After
                  you make the request, the other account must accept or reject
                  the transfer.
                tags:
                  - Transfers
                  - Inputs
                  - Device
                  - Devices
                  - Inputs
                  - Device
                  - Identifiers
                  - Accept
                  - Prod
                  - Batches
                  - Delete
                  - Start
                  - Stop
                  - Schedules
                  - Cancel
                  - Channels
                  - Inputs
                  - Security
                  - Groups
                  - Multiplexes
                  - Programs
                  - Partners
                  - Tags
                  - Resources
                  - ARN
                  - Group
                  - Program
                  - Names
                  - Configurations
                  - Thumbnails
                  - Data
                  - Thumbnails
                  - Transfers
                  - Offerings
                  - Reservations
                  - Purchase
                  - Reboot
                  - Reject
                  - Maintenance
                  - Window
                  - Transfers
            /prod/channels/{channelId}/channelClass:
              PUT:
                summary: UpdateChannelClass
                description: Changes the class of t
                tags:
                  - Update
                  - Channels
                  - Classes
                  - Devices
                  - Inputs
                  - Device
                  - Identifiers
                  - Accept
                  - Prod
                  - Batches
                  - Delete
                  - Start
                  - Stop
                  - Schedules
                  - Cancel
                  - Channels
                  - Inputs
                  - Security
                  - Groups
                  - Multiplexes
                  - Programs
                  - Partners
                  - Tags
                  - Resources
                  - ARN
                  - Group
                  - Program
                  - Names
                  - Configurations
                  - Thumbnails
                  - Data
                  - Thumbnails
                  - Transfers
                  - Offerings
                  - Reservations
                  - Purchase
                  - Reboot
                  - Reject
                  - Maintenance
                  - Window
                  - Transfers
                  - Channels
                  - Cla
    overlays:
      - type: APIs.io Search
        url: overlays/medialive-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/medialive-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:medialive
  - name: mediapackage
    description: AWS Elemental MediaPackage
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
            title: mediapackage
          paths:
            /channels/{id}/configure_logs:
              PUT:
                summary: ConfigureLogs
                description: >-
                  Changes the Channel's properities to configure log
                  subscription
                tags:
                  - Configure
                  - Logs
                  - Channels
                  - Identifiers
                  - Configure_logs
            /channels:
              GET:
                summary: ListChannels
                description: Returns a collection of Channels.
                tags:
                  - Lists
                  - Channels
                  - Channels
                  - Identifiers
                  - Configure_logs
            /harvest_jobs:
              GET:
                summary: ListHarvestJobs
                description: Returns a collection of HarvestJob records.
                tags:
                  - Lists
                  - Harvest
                  - Jobs
                  - Channels
                  - Identifiers
                  - Configure_logs
                  - Harvest_jobs
            /origin_endpoints:
              GET:
                summary: ListOriginEndpoints
                description: Returns a collection of OriginEndpoint records.
                tags:
                  - Lists
                  - Origin
                  - Endpoints
                  - Channels
                  - Identifiers
                  - Configure_logs
                  - Harvest_jobs
                  - Origin_endpoints
            /channels/{id}:
              PUT:
                summary: UpdateChannel
                description: Updates an existing Channel.
                tags:
                  - Update
                  - Channels
                  - Channels
                  - Identifiers
                  - Configure_logs
                  - Harvest_jobs
                  - Origin_endpoints
            /origin_endpoints/{id}:
              PUT:
                summary: UpdateOriginEndpoint
                description: Updates an existing OriginEndpoint.
                tags:
                  - Update
                  - Origin
                  - Endpoints
                  - Channels
                  - Identifiers
                  - Configure_logs
                  - Harvest_jobs
                  - Origin_endpoints
            /harvest_jobs/{id}:
              GET:
                summary: DescribeHarvestJob
                description: Gets details about an existing HarvestJob.
                tags:
                  - Describe
                  - Harvest
                  - Jobs
                  - Channels
                  - Identifiers
                  - Configure_logs
                  - Harvest_jobs
                  - Origin_endpoints
            /tags/{resource-arn}:
              DELETE:
                summary: UntagResource
                description: null
                tags:
                  - Untag
                  - Resources
                  - Channels
                  - Identifiers
                  - Configure_logs
                  - Harvest_jobs
                  - Origin_endpoints
                  - Tags
                  - Resources
                  - ARN
            /channels/{id}/credentials:
              PUT:
                summary: RotateChannelCredentials
                description: >-
                  Changes the Channel's first IngestEndpoint's username and
                  password. WARNING - This API is deprecated. Please use
                  RotateIngestEndpointCredentials instead
                tags:
                  - Rotate
                  - Channels
                  - Credentials
                  - Channels
                  - Identifiers
                  - Configure_logs
                  - Harvest_jobs
                  - Origin_endpoints
                  - Tags
                  - Resources
                  - ARN
                  - Credentials
            /channels/{id}/ingest_endpoints/{ingest_endpoint_id}/credentials:
              PUT:
                summary: RotateIngestEndpointCredentials
                description: >-
                  Rotate the IngestEndpoint's username and password, as
                  specified by the IngestEndp
                tags:
                  - Rotate
                  - Ingest
                  - Endpoints
                  - Credentials
                  - Channels
                  - Identifiers
                  - Configure_logs
                  - Harvest_jobs
                  - Origin_endpoints
                  - Tags
                  - Resources
                  - ARN
                  - Credentials
                  - Ingest_endpoints
                  - Ingest_endpoint_
    overlays:
      - type: APIs.io Search
        url: overlays/mediapackage-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/mediapackage-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:mediapackage
  - name: mediapackagev2
    description: >-
      <note> <p>This guide is intended for creating AWS Elemental MediaPackage
      resources in MediaPackage Version 2 (v2) starting from May 2023. To get
      started with MediaPackage v2, create your MediaPackage resources. There
      isn't an automated process to migrate your resources from MediaPackage v1
      to MediaPackage v2. </p> <p>The names of the entities that you use to
      access this API, like URLs and ARNs, all have the versioning information
      added, like "v2", to distinguish from the prior version. If you used
      MediaPackage prior to this release, you can't use the MediaPackage v2 CLI
      or the MediaPackage v2 API to access any MediaPackage v1 resources.</p>
      <p>If you created resources in MediaPackage v1, use video on demand (VOD)
      workflows, and aren't looking to migrate to MediaPackage v2 yet, see the
      <a
      href="https://docs.aws.amazon.com/mediapackage/latest/apireference/what-is.html">MediaPackage
      v1 Live API Reference</a>.</p> </note> <p>This is the AWS Elemental
      MediaPackage v2 Live REST API Reference. It describes all the MediaPackage
      API operations for live content in detail, and provides sample requests,
      responses, and errors for the supported web services protocols.</p> <p>We
      assume that you have the IAM permissions that you need to use MediaPackage
      via the REST API. We also assume that you are familiar with the features
      and operations of MediaPackage, as described in the AWS Elemental
      MediaPackage User Guide.</p>
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
            title: mediapackagev2
          paths:
            /channelGroup/{ChannelGroupName}/channel:
              GET:
                summary: ListChannels
                description: >-
                  <p>Retrieves all channels in a specific channel group that are
                  configured in AWS Elemental MediaPackage, including the origin
                  endpoints that are associated with it.</p>
                tags:
                  - Lists
                  - Channels
                  - Group
                  - Channels
                  - Names
            /channelGroup:
              GET:
                summary: ListChannelGroups
                description: >-
                  <p>Retrieves all channel groups that are configured in AWS
                  Elemental MediaPackage, including the channels and origin
                  endpoints that are associated with it.</p>
                tags:
                  - Lists
                  - Channels
                  - Groups
                  - Group
                  - Channels
                  - Names
            /channelGroup/{ChannelGroupName}/channel/{ChannelName}/originEndpoint:
              GET:
                summary: ListOriginEndpoints
                description: >-
                  <p>Retrieves all origin endpoints in a specific channel that
                  are configured in AWS Elemental MediaPackage.</p>
                tags:
                  - Lists
                  - Origin
                  - Endpoints
                  - Group
                  - Channels
                  - Names
                  - Origin
                  - Endpoints
            /channelGroup/{ChannelGroupName}/channel/{ChannelName}/:
              PUT:
                summary: UpdateChannel
                description: >-
                  <p>Update the specified channel. You can edit if MediaPackage
                  sends ingest or egress access logs to the CloudWatch log
                  group, if content will be encrypted, the description on a
                  channel, and your channel's policy settings. You can't edit
                  the name of the channel or CloudFront distribution
                  details.</p> <p>Any edits you make that impact the video
                  output may not be reflected for a few minutes.</p>
                tags:
                  - Update
                  - Channels
                  - Group
                  - Channels
                  - Names
                  - Origin
                  - Endpoints
            /channelGroup/{ChannelGroupName}:
              PUT:
                summary: UpdateChannelGroup
                description: >-
                  <p>Update the specified channel group. You can edit the
                  description on a channel group for easier identification later
                  from the AWS Elemental MediaPackage console. You can't edit
                  the name of the channel group.</p> <p>Any edits you make that
                  impact the video output may not be reflected for a few
                  minutes.</p>
                tags:
                  - Update
                  - Channels
                  - Group
                  - Group
                  - Channels
                  - Names
                  - Origin
                  - Endpoints
            /channelGroup/{ChannelGroupName}/channel/{ChannelName}/policy:
              PUT:
                summary: PutChannelPolicy
                description: >-
                  <p>Attaches an IAM policy to the specified channel. With
                  policies, you can specify who has access to AWS resources and
                  what actions they can perform on those resources. You can
                  attach only one policy with each request.</p>
                tags:
                  - Put
                  - Channels
                  - Policies
                  - Group
                  - Channels
                  - Names
                  - Origin
                  - Endpoints
                  - Policies
            /channelGroup/{ChannelGroupName}/channel/{ChannelName}/originEndpoint/{OriginEndpointName}:
              PUT:
                summary: UpdateOriginEndpoint
                description: >-
                  <p>Update the specified origin endpoint. Edit the packaging
                  preferences on an endpoint to optimize the viewing experience.
                  You can't edit the name of the endpoint.</p> <p>Any edits you
                  make that impact the video output may not be reflected for a
                  few minutes.</p>
                tags:
                  - Update
                  - Origin
                  - Endpoints
                  - Group
                  - Channels
                  - Names
                  - Origin
                  - Endpoints
                  - Policies
            /channelGroup/{ChannelGroupName}/channel/{ChannelName}/originEndpoint/{OriginEndpointName}/policy:
              POST:
                summary: PutOriginEndpointPolicy
                description: >-
                  <p>Attaches an IAM policy to the specified origin endpoint.
                  You can attach only one policy with each request.</p>
                tags:
                  - Put
                  - Origin
                  - Endpoints
                  - Policies
                  - Group
                  - Channels
                  - Names
                  - Origin
                  - Endpoints
                  - Policies
            /tags/{ResourceArn}:
              DELETE:
                summary: UntagResource
                description: <p>Removes one or more tags from the specified res
                tags:
                  - Untag
                  - Resources
                  - Group
                  - Channels
                  - Names
                  - Origin
                  - Endpoints
                  - Policies
                  - Resources
                  - A
    overlays:
      - type: APIs.io Search
        url: overlays/mediapackagev2-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/mediapackagev2-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:mediapackagev2
  - name: mediatailor
    description: >-
      <p>Use the AWS Elemental MediaTailor SDKs and CLI to configure scalable ad
      insertion and linear channels. With MediaTailor, you can assemble existing
      content into a linear stream and serve targeted ads to viewers while
      maintaining broadcast quality in over-the-top (OTT) video applications.
      For information about using the service, including detailed information
      about the settings covered in this guide, see the <a
      href="https://docs.aws.amazon.com/mediatailor/latest/ug/">AWS Elemental
      MediaTailor User Guide</a>.</p> <p>Through the SDKs and the CLI you manage
      AWS Elemental MediaTailor configurations and channels the same as you do
      through the console. For example, you specify ad insertion behavior and
      mapping information for the origin server and the ad decision server
      (ADS).</p>
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
            title: mediatailor
          paths:
            /configureLogs/channel:
              PUT:
                summary: ConfigureLogsForChannel
                description: >-
                  <p>Configures Amazon CloudWatch log settings for a
                  channel.</p>
                tags:
                  - Configure
                  - Logs
                  - For
                  - Channels
                  - Logs
                  - Channels
            /configureLogs/playbackConfiguration:
              PUT:
                summary: ConfigureLogsForPlaybackConfiguration
                description: >-
                  <p>Amazon CloudWatch log settings for a playback
                  configuration.</p>
                tags:
                  - Configure
                  - Logs
                  - For
                  - Playback
                  - Configurations
                  - Logs
                  - Channels
                  - Playback
                  - Configurations
            /channel/{ChannelName}:
              PUT:
                summary: UpdateChannel
                description: >-
                  <p>Updates a channel. For information about MediaTailor
                  channels, see <a
                  href="https://docs.aws.amazon.com/mediatailor/latest/ug/channel-assembly-channels.html">Working
                  with channels</a> in the <i>MediaTailor User Guide</i>.</p>
                tags:
                  - Update
                  - Channels
                  - Logs
                  - Channels
                  - Playback
                  - Configurations
                  - Names
            /sourceLocation/{SourceLocationName}/liveSource/{LiveSourceName}:
              PUT:
                summary: UpdateLiveSource
                description: <p>Updates a live source's configuration.</p>
                tags:
                  - Update
                  - Live
                  - Source
                  - Logs
                  - Channels
                  - Playback
                  - Configurations
                  - Names
                  - Locations
                  - Source
                  - Live
            /prefetchSchedule/{PlaybackConfigurationName}/{Name}:
              GET:
                summary: GetPrefetchSchedule
                description: >-
                  <p>Retrieves a prefetch schedule for a playback configuration.
                  A prefetch schedule allows you to tell MediaTailor to fetch
                  and prepare certain ads before an ad break happens. For more
                  information about ad prefetching, see <a
                  href="https://docs.aws.amazon.com/mediatailor/latest/ug/prefetching-ads.html">Using
                  ad prefetching</a> in the <i>MediaTailor User Guide</i>.</p>
                tags:
                  - Get
                  - Prefetch
                  - Schedules
                  - Logs
                  - Channels
                  - Playback
                  - Configurations
                  - Names
                  - Locations
                  - Source
                  - Live
                  - Schedules
            /channel/{ChannelName}/program/{ProgramName}:
              PUT:
                summary: UpdateProgram
                description: <p>Updates a program within a channel.</p>
                tags:
                  - Update
                  - Program
                  - Logs
                  - Channels
                  - Playback
                  - Configurations
                  - Names
                  - Locations
                  - Source
                  - Live
                  - Schedules
                  - Program
            /sourceLocation/{SourceLocationName}:
              PUT:
                summary: UpdateSourceLocation
                description: >-
                  <p>Updates a source location. A source location is a container
                  for sources. For more information about source locations, see
                  <a
                  href="https://docs.aws.amazon.com/mediatailor/latest/ug/channel-assembly-source-locations.html">Working
                  with source locations</a> in the <i>MediaTailor User
                  Guide</i>.</p>
                tags:
                  - Update
                  - Source
                  - Locations
                  - Logs
                  - Channels
                  - Playback
                  - Configurations
                  - Names
                  - Locations
                  - Source
                  - Live
                  - Schedules
                  - Program
            /sourceLocation/{SourceLocationName}/vodSource/{VodSourceName}:
              PUT:
                summary: UpdateVodSource
                description: <p>Updates a VOD source's configuration.</p>
                tags:
                  - Update
                  - Vod
                  - Source
                  - Logs
                  - Channels
                  - Playback
                  - Configurations
                  - Names
                  - Locations
                  - Source
                  - Live
                  - Schedules
                  - Program
                  - Vod
            /channel/{ChannelName}/policy:
              PUT:
                summary: PutChannelPolicy
                description: >-
                  <p>Creates an IAM policy for the channel. IAM policies are
                  used to control access to your channel.</p>
                tags:
                  - Put
                  - Channels
                  - Policies
                  - Logs
                  - Channels
                  - Playback
                  - Configurations
                  - Names
                  - Locations
                  - Source
                  - Live
                  - Schedules
                  - Program
                  - Vod
                  - Policies
            /playbackConfiguration/{Name}:
              GET:
                summary: GetPlaybackConfiguration
                description: >-
                  <p>Retrieves a playback configuration. For information about
                  MediaTailor configurations, see <a
                  href="https://docs.aws.amazon.com/mediatailor/latest/ug/configurations.html">Working
                  with configurations in AWS Elemental MediaTailor</a>.</p>
                tags:
                  - Get
                  - Playback
                  - Configurations
                  - Logs
                  - Channels
                  - Playback
                  - Configurations
                  - Names
                  - Locations
                  - Source
                  - Live
                  - Schedules
                  - Program
                  - Vod
                  - Policies
            /channel/{ChannelName}/schedule:
              GET:
                summary: GetChannelSchedule
                description: <p>Retrieves information about your channel's schedule.</p>
                tags:
                  - Get
                  - Channels
                  - Schedules
                  - Logs
                  - Channels
                  - Playback
                  - Configurations
                  - Names
                  - Locations
                  - Source
                  - Live
                  - Schedules
                  - Program
                  - Vod
                  - Policies
            /alerts:
              GET:
                summary: ListAlerts
                description: >-
                  <p>Lists the alerts that are associated with a MediaTailor
                  channel assembly resource.</p>
                tags:
                  - Lists
                  - Alerts
                  - Logs
                  - Channels
                  - Playback
                  - Configurations
                  - Names
                  - Locations
                  - Source
                  - Live
                  - Schedules
                  - Program
                  - Vod
                  - Policies
                  - Alerts
            /channels:
              GET:
                summary: ListChannels
                description: >-
                  <p>Retrieves information about the channels that are
                  associated with the current AWS account.</p>
                tags:
                  - Lists
                  - Channels
                  - Logs
                  - Channels
                  - Playback
                  - Configurations
                  - Names
                  - Locations
                  - Source
                  - Live
                  - Schedules
                  - Program
                  - Vod
                  - Policies
                  - Alerts
                  - Channels
            /sourceLocation/{SourceLocationName}/liveSources:
              GET:
                summary: ListLiveSources
                description: >-
                  <p>Lists the live sources contained in a source location. A
                  source represents a piece of content.</p>
                tags:
                  - Lists
                  - Live
                  - Sources
                  - Logs
                  - Channels
                  - Playback
                  - Configurations
                  - Names
                  - Locations
                  - Source
                  - Live
                  - Schedules
                  - Program
                  - Vod
                  - Policies
                  - Alerts
                  - Channels
                  - Sources
            /playbackConfigurations:
              GET:
                summary: ListPlaybackConfigurations
                description: >-
                  <p>Retrieves existing playback configurations. For information
                  about MediaTailor configurations, see <a
                  href="https://docs.aws.amazon.com/mediatailor/latest/ug/configurations.html">Working
                  with Configurations in AWS Elemental MediaTailor</a>.</p>
                tags:
                  - Lists
                  - Playback
                  - Configurations
                  - Logs
                  - Channels
                  - Playback
                  - Configurations
                  - Names
                  - Locations
                  - Source
                  - Live
                  - Schedules
                  - Program
                  - Vod
                  - Policies
                  - Alerts
                  - Channels
                  - Sources
                  - Configurations
            /prefetchSchedule/{PlaybackConfigurationName}:
              POST:
                summary: ListPrefetchSchedules
                description: >-
                  <p>Lists the prefetch schedules for a playback
                  configuration.</p>
                tags:
                  - Lists
                  - Prefetch
                  - Schedules
                  - Logs
                  - Channels
                  - Playback
                  - Configurations
                  - Names
                  - Locations
                  - Source
                  - Live
                  - Schedules
                  - Program
                  - Vod
                  - Policies
                  - Alerts
                  - Channels
                  - Sources
                  - Configurations
            /sourceLocations:
              GET:
                summary: ListSourceLocations
                description: >-
                  <p>Lists the source locations for a channel. A source location
                  defines the host server URL, and contains a list of
                  sources.</p>
                tags:
                  - Lists
                  - Source
                  - Locations
                  - Logs
                  - Channels
                  - Playback
                  - Configurations
                  - Names
                  - Locations
                  - Source
                  - Live
                  - Schedules
                  - Program
                  - Vod
                  - Policies
                  - Alerts
                  - Channels
                  - Sources
                  - Configurations
                  - Locations
            /tags/{ResourceArn}:
              DELETE:
                summary: UntagResource
                description: <p>The resource to untag.</p>
                tags:
                  - Untag
                  - Resources
                  - Logs
                  - Channels
                  - Playback
                  - Configurations
                  - Names
                  - Locations
                  - Source
                  - Live
                  - Schedules
                  - Program
                  - Vod
                  - Policies
                  - Alerts
                  - Channels
                  - Sources
                  - Configurations
                  - Locations
                  - Resources
                  - ARN
            /sourceLocation/{SourceLocationName}/vodSources:
              GET:
                summary: ListVodSources
                description: >-
                  <p>Lists the VOD sources contained in a source location. A
                  source represents a piece of content.</p>
                tags:
                  - Lists
                  - Vod
                  - Sources
                  - Logs
                  - Channels
                  - Playback
                  - Configurations
                  - Names
                  - Locations
                  - Source
                  - Live
                  - Schedules
                  - Program
                  - Vod
                  - Policies
                  - Alerts
                  - Channels
                  - Sources
                  - Configurations
                  - Locations
                  - Resources
                  - ARN
            /playbackConfiguration:
              PUT:
                summary: PutPlaybackConfiguration
                description: >-
                  <p>Creates a playback configuration. For information about
                  MediaTailor configurations, see <a
                  href="https://docs.aws.amazon.com/mediatailor/latest/ug/configurations.html">Working
                  with configurations in AWS Elemental MediaTailor</a>.</p>
                tags:
                  - Put
                  - Playback
                  - Configurations
                  - Logs
                  - Channels
                  - Playback
                  - Configurations
                  - Names
                  - Locations
                  - Source
                  - Live
                  - Schedules
                  - Program
                  - Vod
                  - Policies
                  - Alerts
                  - Channels
                  - Sources
                  - Configurations
                  - Locations
                  - Resources
                  - ARN
            /channel/{ChannelName}/start:
              PUT:
                summary: StartChannel
                description: >-
                  <p>Starts a channel. For information about MediaTailor
                  channels, see <a
                  href="https://docs.aws.amazon.com/mediatailor/latest/ug/channel-assembly-channels.html">Working
                  with channels</a> in the <i>MediaTailor User Guide</i>.</p>
                tags:
                  - Start
                  - Channels
                  - Logs
                  - Channels
                  - Playback
                  - Configurations
                  - Names
                  - Locations
                  - Source
                  - Live
                  - Schedules
                  - Program
                  - Vod
                  - Policies
                  - Alerts
                  - Channels
                  - Sources
                  - Configurations
                  - Locations
                  - Resources
                  - ARN
                  - Start
            /channel/{ChannelName}/stop:
              PUT:
                summary: StopChannel
                description: >-
                  <p>Stops a channel. For information about MediaTailor
                  channels, see <a
                  href="https://docs.aws.amazon.com/mediatailor/latest/ug/channel-assembly-channels.html">Working
                  with channels</a> in the <i>MediaTailor User Guid
                tags:
                  - Stop
                  - Channels
                  - Logs
                  - Channels
                  - Playback
                  - Configurations
                  - Names
                  - Locations
                  - Source
                  - Live
                  - Schedules
                  - Program
                  - Vod
                  - Policies
                  - Alerts
                  - Channels
                  - Sources
                  - Configurations
                  - Locations
                  - Resources
                  - ARN
                  - Start
                  - St
    overlays:
      - type: APIs.io Search
        url: overlays/mediatailor-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/mediatailor-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:mediatailor
  - name: pinpoint
    description: <p>Doc Engage API - Amazon Pinpoint API</p>
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
            title: pinpoint
          paths:
            /v1/apps:
              GET:
                summary: GetApps
                description: >-
                  <p>Retrieves information about all the applications that are
                  associated with your Amazon Pinpoint account.</p>
                tags:
                  - Get
                  - Applications
                  - V1
                  - Applications
            /v1/apps/{application-id}/campaigns:
              GET:
                summary: GetCampaigns
                description: >-
                  <p>Retrieves information about the status, configuration, and
                  other settings for all the campaigns that are associated with
                  an application.</p>
                tags:
                  - Get
                  - Campaigns
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
            /v1/templates/{template-name}/email:
              PUT:
                summary: UpdateEmailTemplate
                description: >-
                  <p>Updates an existing message template for messages that are
                  sent through the email channel.</p>
                tags:
                  - Update
                  - Email
                  - Templates
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
            /v1/apps/{application-id}/jobs/export:
              GET:
                summary: GetExportJobs
                description: >-
                  <p>Retrieves information about the status and settings of all
                  the export jobs for an application.</p>
                tags:
                  - Get
                  - Export
                  - Jobs
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
            /v1/apps/{application-id}/jobs/import:
              GET:
                summary: GetImportJobs
                description: >-
                  <p>Retrieves information about the status and settings of all
                  the import jobs for an application.</p>
                tags:
                  - Get
                  - Import
                  - Jobs
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
            /v1/templates/{template-name}/inapp:
              PUT:
                summary: UpdateInAppTemplate
                description: >-
                  <p>Updates an existing message template for messages sent
                  through the in-app message channel.</p>
                tags:
                  - Update
                  - In
                  - Applications
                  - Templates
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
            /v1/apps/{application-id}/journeys:
              GET:
                summary: ListJourneys
                description: >-
                  <p>Retrieves information about the status, configuration, and
                  other settings for all the journeys that are associated with
                  an application.</p>
                tags:
                  - Lists
                  - Journeys
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
            /v1/templates/{template-name}/push:
              PUT:
                summary: UpdatePushTemplate
                description: >-
                  <p>Updates an existing message template for messages that are
                  sent through a push notification channel.</p>
                tags:
                  - Update
                  - Push
                  - Templates
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
            /v1/recommenders:
              GET:
                summary: GetRecommenderConfigurations
                description: >-
                  <p>Retrieves information about all the recommender model
                  configurations that are associated with your Amazon Pinpoint
                  account.</p>
                tags:
                  - Get
                  - Recommenders
                  - Configurations
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
            /v1/apps/{application-id}/segments:
              GET:
                summary: GetSegments
                description: >-
                  <p>Retrieves information about the configuration, dimension,
                  and other settings for all the segments that are associated
                  with an application.</p>
                tags:
                  - Get
                  - Segments
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
            /v1/templates/{template-name}/sms:
              PUT:
                summary: UpdateSmsTemplate
                description: >-
                  <p>Updates an existing message template for messages that are
                  sent through the SMS channel.</p>
                tags:
                  - Update
                  - SMS
                  - Templates
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
            /v1/templates/{template-name}/voice:
              PUT:
                summary: UpdateVoiceTemplate
                description: >-
                  <p>Updates an existing message template for messages that are
                  sent through the voice channel.</p>
                tags:
                  - Update
                  - Voice
                  - Templates
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
            /v1/apps/{application-id}/channels/adm:
              PUT:
                summary: UpdateAdmChannel
                description: >-
                  <p>Enables the ADM channel for an application or updates the
                  status and settings of the ADM channel for an application.</p>
                tags:
                  - Update
                  - ADM
                  - Channels
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
            /v1/apps/{application-id}/channels/apns:
              PUT:
                summary: UpdateApnsChannel
                description: >-
                  <p>Enables the APNs channel for an application or updates the
                  status and settings of the APNs channel for an
                  application.</p>
                tags:
                  - Update
                  - Apns
                  - Channels
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
            /v1/apps/{application-id}/channels/apns_sandbox:
              PUT:
                summary: UpdateApnsSandboxChannel
                description: >-
                  <p>Enables the APNs sandbox channel for an application or
                  updates the status and settings of the APNs sandbox channel
                  for an application.</p>
                tags:
                  - Update
                  - Apns
                  - Sandbox
                  - Channels
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
            /v1/apps/{application-id}/channels/apns_voip:
              PUT:
                summary: UpdateApnsVoipChannel
                description: >-
                  <p>Enables the APNs VoIP channel for an application or updates
                  the status and settings of the APNs VoIP channel for an
                  application.</p>
                tags:
                  - Update
                  - Apns
                  - Voice Over IP
                  - Channels
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
            /v1/apps/{application-id}/channels/apns_voip_sandbox:
              PUT:
                summary: UpdateApnsVoipSandboxChannel
                description: >-
                  <p>Enables the APNs VoIP sandbox channel for an application or
                  updates the status and settings of the APNs VoIP sandbox
                  channel for an application.</p>
                tags:
                  - Update
                  - Apns
                  - Voice Over IP
                  - Sandbox
                  - Channels
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
            /v1/apps/{application-id}:
              GET:
                summary: GetApp
                description: <p>Retrieves information about an application.</p>
                tags:
                  - Get
                  - Applications
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
            /v1/apps/{application-id}/channels/baidu:
              PUT:
                summary: UpdateBaiduChannel
                description: >-
                  <p>Enables the Baidu channel for an application or updates the
                  status and settings of the Baidu channel for an
                  application.</p>
                tags:
                  - Update
                  - Baidu
                  - Channels
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
                  - Baidu
            /v1/apps/{application-id}/campaigns/{campaign-id}:
              PUT:
                summary: UpdateCampaign
                description: >-
                  <p>Updates the configuration and other settings for a
                  campaign.</p>
                tags:
                  - Update
                  - Campaigns
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
                  - Baidu
                  - Campaigns
            /v1/apps/{application-id}/channels/email:
              PUT:
                summary: UpdateEmailChannel
                description: >-
                  <p>Enables the email channel for an application or updates the
                  status and settings of the email channel for an
                  application.</p>
                tags:
                  - Update
                  - Email
                  - Channels
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
                  - Baidu
                  - Campaigns
            /v1/apps/{application-id}/endpoints/{endpoint-id}:
              PUT:
                summary: UpdateEndpoint
                description: >-
                  <p>Creates a new endpoint for an application or updates the
                  settings and attributes of an existing endpoint for an
                  application. You can also use this operation to define custom
                  attributes for an endpoint. If an update includes one or more
                  values for a custom attribute, Amazon Pinpoint replaces
                  (overwrites) any existing values with the new values.</p>
                tags:
                  - Update
                  - Endpoints
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
                  - Baidu
                  - Campaigns
                  - Endpoints
                  - Endpoints
            /v1/apps/{application-id}/eventstream:
              POST:
                summary: PutEventStream
                description: >-
                  <p>Creates a new event stream for an application or updates
                  the settings of an existing event stream for an
                  application.</p>
                tags:
                  - Put
                  - Events
                  - Stream
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
                  - Baidu
                  - Campaigns
                  - Endpoints
                  - Endpoints
                  - Event Stream
            /v1/apps/{application-id}/channels/gcm:
              PUT:
                summary: UpdateGcmChannel
                description: >-
                  <p>Enables the GCM channel for an application or updates the
                  status and settings of the GCM channel for an application.</p>
                tags:
                  - Update
                  - Gcm
                  - Channels
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
                  - Baidu
                  - Campaigns
                  - Endpoints
                  - Endpoints
                  - Event Stream
                  - Gcm
            /v1/apps/{application-id}/journeys/{journey-id}:
              PUT:
                summary: UpdateJourney
                description: >-
                  <p>Updates the configuration and other settings for a
                  journey.</p>
                tags:
                  - Update
                  - Journeys
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
                  - Baidu
                  - Campaigns
                  - Endpoints
                  - Endpoints
                  - Event Stream
                  - Gcm
                  - Journeys
            /v1/recommenders/{recommender-id}:
              PUT:
                summary: UpdateRecommenderConfiguration
                description: >-
                  <p>Updates an Amazon Pinpoint configuration for a recommender
                  model.</p>
                tags:
                  - Update
                  - Recommenders
                  - Configurations
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
                  - Baidu
                  - Campaigns
                  - Endpoints
                  - Endpoints
                  - Event Stream
                  - Gcm
                  - Journeys
                  - Recommenders
            /v1/apps/{application-id}/segments/{segment-id}:
              PUT:
                summary: UpdateSegment
                description: >-
                  <p>Creates a new segment for an application or updates the
                  configuration, dimension, and other settings for an existing
                  segment that's associated with an application.</p>
                tags:
                  - Update
                  - Segments
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
                  - Baidu
                  - Campaigns
                  - Endpoints
                  - Endpoints
                  - Event Stream
                  - Gcm
                  - Journeys
                  - Recommenders
                  - Segments
            /v1/apps/{application-id}/channels/sms:
              PUT:
                summary: UpdateSmsChannel
                description: >-
                  <p>Enables the SMS channel for an application or updates the
                  status and settings of the SMS channel for an application.</p>
                tags:
                  - Update
                  - SMS
                  - Channels
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
                  - Baidu
                  - Campaigns
                  - Endpoints
                  - Endpoints
                  - Event Stream
                  - Gcm
                  - Journeys
                  - Recommenders
                  - Segments
            /v1/apps/{application-id}/users/{user-id}:
              GET:
                summary: GetUserEndpoints
                description: >-
                  <p>Retrieves information about all the endpoints that are
                  associated with a specific user ID.</p>
                tags:
                  - Get
                  - Users
                  - Endpoints
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
                  - Baidu
                  - Campaigns
                  - Endpoints
                  - Endpoints
                  - Event Stream
                  - Gcm
                  - Journeys
                  - Recommenders
                  - Segments
                  - Users
                  - Users
            /v1/apps/{application-id}/channels/voice:
              PUT:
                summary: UpdateVoiceChannel
                description: >-
                  <p>Enables the voice channel for an application or updates the
                  status and settings of the voice channel for an
                  application.</p>
                tags:
                  - Update
                  - Voice
                  - Channels
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
                  - Baidu
                  - Campaigns
                  - Endpoints
                  - Endpoints
                  - Event Stream
                  - Gcm
                  - Journeys
                  - Recommenders
                  - Segments
                  - Users
                  - Users
            /v1/apps/{application-id}/kpis/daterange/{kpi-name}:
              GET:
                summary: GetApplicationDateRangeKpi
                description: >-
                  <p>Retrieves (queries) pre-aggregated data for a standard
                  metric that applies to an application.</p>
                tags:
                  - Get
                  - Applications
                  - Dates
                  - Ranges
                  - KPI
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
                  - Baidu
                  - Campaigns
                  - Endpoints
                  - Endpoints
                  - Event Stream
                  - Gcm
                  - Journeys
                  - Recommenders
                  - Segments
                  - Users
                  - Users
                  - KPI
                  - Date Range
                  - KPI
            /v1/apps/{application-id}/settings:
              PUT:
                summary: UpdateApplicationSettings
                description: <p>Updates the settings for an application.</p>
                tags:
                  - Update
                  - Applications
                  - Settings
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
                  - Baidu
                  - Campaigns
                  - Endpoints
                  - Endpoints
                  - Event Stream
                  - Gcm
                  - Journeys
                  - Recommenders
                  - Segments
                  - Users
                  - Users
                  - KPI
                  - Date Range
                  - KPI
                  - Settings
            /v1/apps/{application-id}/campaigns/{campaign-id}/activities:
              GET:
                summary: GetCampaignActivities
                description: >-
                  <p>Retrieves information about all the activities for a
                  campaign.</p>
                tags:
                  - Get
                  - Campaigns
                  - Activities
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
                  - Baidu
                  - Campaigns
                  - Endpoints
                  - Endpoints
                  - Event Stream
                  - Gcm
                  - Journeys
                  - Recommenders
                  - Segments
                  - Users
                  - Users
                  - KPI
                  - Date Range
                  - KPI
                  - Settings
                  - Activities
            /v1/apps/{application-id}/campaigns/{campaign-id}/kpis/daterange/{kpi-name}:
              GET:
                summary: GetCampaignDateRangeKpi
                description: >-
                  <p>Retrieves (queries) pre-aggregated data for a standard
                  metric that applies to a campaign.</p>
                tags:
                  - Get
                  - Campaigns
                  - Dates
                  - Ranges
                  - KPI
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
                  - Baidu
                  - Campaigns
                  - Endpoints
                  - Endpoints
                  - Event Stream
                  - Gcm
                  - Journeys
                  - Recommenders
                  - Segments
                  - Users
                  - Users
                  - KPI
                  - Date Range
                  - KPI
                  - Settings
                  - Activities
            /v1/apps/{application-id}/campaigns/{campaign-id}/versions/{version}:
              GET:
                summary: GetCampaignVersion
                description: >-
                  <p>Retrieves information about the status, configuration, and
                  other settings for a specific version of a campaign.</p>
                tags:
                  - Get
                  - Campaigns
                  - Versions
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
                  - Baidu
                  - Campaigns
                  - Endpoints
                  - Endpoints
                  - Event Stream
                  - Gcm
                  - Journeys
                  - Recommenders
                  - Segments
                  - Users
                  - Users
                  - KPI
                  - Date Range
                  - KPI
                  - Settings
                  - Activities
                  - Versions
                  - Versions
            /v1/apps/{application-id}/campaigns/{campaign-id}/versions:
              GET:
                summary: GetCampaignVersions
                description: >-
                  <p>Retrieves information about the status, configuration, and
                  other settings for all versions of a campaign.</p>
                tags:
                  - Get
                  - Campaigns
                  - Versions
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
                  - Baidu
                  - Campaigns
                  - Endpoints
                  - Endpoints
                  - Event Stream
                  - Gcm
                  - Journeys
                  - Recommenders
                  - Segments
                  - Users
                  - Users
                  - KPI
                  - Date Range
                  - KPI
                  - Settings
                  - Activities
                  - Versions
                  - Versions
            /v1/apps/{application-id}/channels:
              GET:
                summary: GetChannels
                description: >-
                  <p>Retrieves information about the history and status of each
                  channel for an application.</p>
                tags:
                  - Get
                  - Channels
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
                  - Baidu
                  - Campaigns
                  - Endpoints
                  - Endpoints
                  - Event Stream
                  - Gcm
                  - Journeys
                  - Recommenders
                  - Segments
                  - Users
                  - Users
                  - KPI
                  - Date Range
                  - KPI
                  - Settings
                  - Activities
                  - Versions
                  - Versions
            /v1/apps/{application-id}/jobs/export/{job-id}:
              GET:
                summary: GetExportJob
                description: >-
                  <p>Retrieves information about the status and settings of a
                  specific export job for an application.</p>
                tags:
                  - Get
                  - Export
                  - Jobs
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
                  - Baidu
                  - Campaigns
                  - Endpoints
                  - Endpoints
                  - Event Stream
                  - Gcm
                  - Journeys
                  - Recommenders
                  - Segments
                  - Users
                  - Users
                  - KPI
                  - Date Range
                  - KPI
                  - Settings
                  - Activities
                  - Versions
                  - Versions
                  - Jobs
            /v1/apps/{application-id}/jobs/import/{job-id}:
              GET:
                summary: GetImportJob
                description: >-
                  <p>Retrieves information about the status and settings of a
                  specific import job for an application.</p>
                tags:
                  - Get
                  - Import
                  - Jobs
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
                  - Baidu
                  - Campaigns
                  - Endpoints
                  - Endpoints
                  - Event Stream
                  - Gcm
                  - Journeys
                  - Recommenders
                  - Segments
                  - Users
                  - Users
                  - KPI
                  - Date Range
                  - KPI
                  - Settings
                  - Activities
                  - Versions
                  - Versions
                  - Jobs
            /v1/apps/{application-id}/endpoints/{endpoint-id}/inappmessages:
              GET:
                summary: GetInAppMessages
                description: >-
                  <p>Retrieves the in-app messages targeted for the provided
                  endpoint ID.</p>
                tags:
                  - Get
                  - In
                  - Applications
                  - Messages
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
                  - Baidu
                  - Campaigns
                  - Endpoints
                  - Endpoints
                  - Event Stream
                  - Gcm
                  - Journeys
                  - Recommenders
                  - Segments
                  - Users
                  - Users
                  - KPI
                  - Date Range
                  - KPI
                  - Settings
                  - Activities
                  - Versions
                  - Versions
                  - Jobs
                  - Inappmessages
            /v1/apps/{application-id}/journeys/{journey-id}/kpis/daterange/{kpi-name}:
              GET:
                summary: GetJourneyDateRangeKpi
                description: >-
                  <p>Retrieves (queries) pre-aggregated data for a standard
                  engagement metric that applies to a journey.</p>
                tags:
                  - Get
                  - Journeys
                  - Dates
                  - Ranges
                  - KPI
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
                  - Baidu
                  - Campaigns
                  - Endpoints
                  - Endpoints
                  - Event Stream
                  - Gcm
                  - Journeys
                  - Recommenders
                  - Segments
                  - Users
                  - Users
                  - KPI
                  - Date Range
                  - KPI
                  - Settings
                  - Activities
                  - Versions
                  - Versions
                  - Jobs
                  - Inappmessages
            /v1/apps/{application-id}/journeys/{journey-id}/activities/{journey-activity-id}/execution-metrics:
              GET:
                summary: GetJourneyExecutionActivityMetrics
                description: >-
                  <p>Retrieves (queries) pre-aggregated data for a standard
                  execution metric that applies to a journey activity.</p>
                tags:
                  - Get
                  - Journeys
                  - Execution
                  - Activity
                  - Metrics
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
                  - Baidu
                  - Campaigns
                  - Endpoints
                  - Endpoints
                  - Event Stream
                  - Gcm
                  - Journeys
                  - Recommenders
                  - Segments
                  - Users
                  - Users
                  - KPI
                  - Date Range
                  - KPI
                  - Settings
                  - Activities
                  - Versions
                  - Versions
                  - Jobs
                  - Inappmessages
                  - Activity
                  - Execution
                  - Metrics
            /v1/apps/{application-id}/journeys/{journey-id}/execution-metrics:
              GET:
                summary: GetJourneyExecutionMetrics
                description: >-
                  <p>Retrieves (queries) pre-aggregated data for a standard
                  execution metric that applies to a journey.</p>
                tags:
                  - Get
                  - Journeys
                  - Execution
                  - Metrics
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
                  - Baidu
                  - Campaigns
                  - Endpoints
                  - Endpoints
                  - Event Stream
                  - Gcm
                  - Journeys
                  - Recommenders
                  - Segments
                  - Users
                  - Users
                  - KPI
                  - Date Range
                  - KPI
                  - Settings
                  - Activities
                  - Versions
                  - Versions
                  - Jobs
                  - Inappmessages
                  - Activity
                  - Execution
                  - Metrics
            /v1/apps/{application-id}/journeys/{journey-id}/runs/{run-id}/activities/{journey-activity-id}/execution-metrics:
              GET:
                summary: GetJourneyRunExecutionActivityMetrics
                description: >-
                  <p>Retrieves (queries) pre-aggregated data for a standard run
                  execution metric that applies to a journey activity.</p>
                tags:
                  - Get
                  - Journeys
                  - Runs
                  - Execution
                  - Activity
                  - Metrics
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
                  - Baidu
                  - Campaigns
                  - Endpoints
                  - Endpoints
                  - Event Stream
                  - Gcm
                  - Journeys
                  - Recommenders
                  - Segments
                  - Users
                  - Users
                  - KPI
                  - Date Range
                  - KPI
                  - Settings
                  - Activities
                  - Versions
                  - Versions
                  - Jobs
                  - Inappmessages
                  - Activity
                  - Execution
                  - Metrics
                  - Runs
                  - Runs
            /v1/apps/{application-id}/journeys/{journey-id}/runs/{run-id}/execution-metrics:
              GET:
                summary: GetJourneyRunExecutionMetrics
                description: >-
                  <p>Retrieves (queries) pre-aggregated data for a standard run
                  execution metric that applies to a journey.</p>
                tags:
                  - Get
                  - Journeys
                  - Runs
                  - Execution
                  - Metrics
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
                  - Baidu
                  - Campaigns
                  - Endpoints
                  - Endpoints
                  - Event Stream
                  - Gcm
                  - Journeys
                  - Recommenders
                  - Segments
                  - Users
                  - Users
                  - KPI
                  - Date Range
                  - KPI
                  - Settings
                  - Activities
                  - Versions
                  - Versions
                  - Jobs
                  - Inappmessages
                  - Activity
                  - Execution
                  - Metrics
                  - Runs
                  - Runs
            /v1/apps/{application-id}/journeys/{journey-id}/runs:
              GET:
                summary: GetJourneyRuns
                description: <p>Provides information about the runs of a journey.</p>
                tags:
                  - Get
                  - Journeys
                  - Runs
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
                  - Baidu
                  - Campaigns
                  - Endpoints
                  - Endpoints
                  - Event Stream
                  - Gcm
                  - Journeys
                  - Recommenders
                  - Segments
                  - Users
                  - Users
                  - KPI
                  - Date Range
                  - KPI
                  - Settings
                  - Activities
                  - Versions
                  - Versions
                  - Jobs
                  - Inappmessages
                  - Activity
                  - Execution
                  - Metrics
                  - Runs
                  - Runs
            /v1/apps/{application-id}/segments/{segment-id}/jobs/export:
              GET:
                summary: GetSegmentExportJobs
                description: >-
                  <p>Retrieves information about the status and settings of the
                  export jobs for a segment.</p>
                tags:
                  - Get
                  - Segments
                  - Export
                  - Jobs
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
                  - Baidu
                  - Campaigns
                  - Endpoints
                  - Endpoints
                  - Event Stream
                  - Gcm
                  - Journeys
                  - Recommenders
                  - Segments
                  - Users
                  - Users
                  - KPI
                  - Date Range
                  - KPI
                  - Settings
                  - Activities
                  - Versions
                  - Versions
                  - Jobs
                  - Inappmessages
                  - Activity
                  - Execution
                  - Metrics
                  - Runs
                  - Runs
            /v1/apps/{application-id}/segments/{segment-id}/jobs/import:
              GET:
                summary: GetSegmentImportJobs
                description: >-
                  <p>Retrieves information about the status and settings of the
                  import jobs for a segment.</p>
                tags:
                  - Get
                  - Segments
                  - Import
                  - Jobs
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
                  - Baidu
                  - Campaigns
                  - Endpoints
                  - Endpoints
                  - Event Stream
                  - Gcm
                  - Journeys
                  - Recommenders
                  - Segments
                  - Users
                  - Users
                  - KPI
                  - Date Range
                  - KPI
                  - Settings
                  - Activities
                  - Versions
                  - Versions
                  - Jobs
                  - Inappmessages
                  - Activity
                  - Execution
                  - Metrics
                  - Runs
                  - Runs
            /v1/apps/{application-id}/segments/{segment-id}/versions/{version}:
              GET:
                summary: GetSegmentVersion
                description: >-
                  <p>Retrieves information about the configuration, dimension,
                  and other settings for a specific version of a segment that's
                  associated with an application.</p>
                tags:
                  - Get
                  - Segments
                  - Versions
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
                  - Baidu
                  - Campaigns
                  - Endpoints
                  - Endpoints
                  - Event Stream
                  - Gcm
                  - Journeys
                  - Recommenders
                  - Segments
                  - Users
                  - Users
                  - KPI
                  - Date Range
                  - KPI
                  - Settings
                  - Activities
                  - Versions
                  - Versions
                  - Jobs
                  - Inappmessages
                  - Activity
                  - Execution
                  - Metrics
                  - Runs
                  - Runs
            /v1/apps/{application-id}/segments/{segment-id}/versions:
              GET:
                summary: GetSegmentVersions
                description: >-
                  <p>Retrieves information about the configuration, dimension,
                  and other settings for all the versions of a specific segment
                  that's associated with an application.</p>
                tags:
                  - Get
                  - Segments
                  - Versions
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
                  - Baidu
                  - Campaigns
                  - Endpoints
                  - Endpoints
                  - Event Stream
                  - Gcm
                  - Journeys
                  - Recommenders
                  - Segments
                  - Users
                  - Users
                  - KPI
                  - Date Range
                  - KPI
                  - Settings
                  - Activities
                  - Versions
                  - Versions
                  - Jobs
                  - Inappmessages
                  - Activity
                  - Execution
                  - Metrics
                  - Runs
                  - Runs
            /v1/tags/{resource-arn}:
              DELETE:
                summary: UntagResource
                description: >-
                  <p>Removes one or more tags (keys and values) from an
                  application, campaign, message template, or segment.</p>
                tags:
                  - Untag
                  - Resources
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
                  - Baidu
                  - Campaigns
                  - Endpoints
                  - Endpoints
                  - Event Stream
                  - Gcm
                  - Journeys
                  - Recommenders
                  - Segments
                  - Users
                  - Users
                  - KPI
                  - Date Range
                  - KPI
                  - Settings
                  - Activities
                  - Versions
                  - Versions
                  - Jobs
                  - Inappmessages
                  - Activity
                  - Execution
                  - Metrics
                  - Runs
                  - Runs
                  - Tags
                  - Resources
                  - ARN
            /v1/templates/{template-name}/{template-type}/versions:
              GET:
                summary: ListTemplateVersions
                description: >-
                  <p>Retrieves information about all the versions of a specific
                  message template.</p>
                tags:
                  - Lists
                  - Templates
                  - Versions
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
                  - Baidu
                  - Campaigns
                  - Endpoints
                  - Endpoints
                  - Event Stream
                  - Gcm
                  - Journeys
                  - Recommenders
                  - Segments
                  - Users
                  - Users
                  - KPI
                  - Date Range
                  - KPI
                  - Settings
                  - Activities
                  - Versions
                  - Versions
                  - Jobs
                  - Inappmessages
                  - Activity
                  - Execution
                  - Metrics
                  - Runs
                  - Runs
                  - Tags
                  - Resources
                  - ARN
                  - Types
            /v1/templates:
              GET:
                summary: ListTemplates
                description: >-
                  <p>Retrieves information about all the message templates that
                  are associated with your Amazon Pinpoint account.</p>
                tags:
                  - Lists
                  - Templates
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
                  - Baidu
                  - Campaigns
                  - Endpoints
                  - Endpoints
                  - Event Stream
                  - Gcm
                  - Journeys
                  - Recommenders
                  - Segments
                  - Users
                  - Users
                  - KPI
                  - Date Range
                  - KPI
                  - Settings
                  - Activities
                  - Versions
                  - Versions
                  - Jobs
                  - Inappmessages
                  - Activity
                  - Execution
                  - Metrics
                  - Runs
                  - Runs
                  - Tags
                  - Resources
                  - ARN
                  - Types
            /v1/phone/number/validate:
              POST:
                summary: PhoneNumberValidate
                description: <p>Retrieves information about a phone number.</p>
                tags:
                  - Phone
                  - Numbers
                  - Validate
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
                  - Baidu
                  - Campaigns
                  - Endpoints
                  - Endpoints
                  - Event Stream
                  - Gcm
                  - Journeys
                  - Recommenders
                  - Segments
                  - Users
                  - Users
                  - KPI
                  - Date Range
                  - KPI
                  - Settings
                  - Activities
                  - Versions
                  - Versions
                  - Jobs
                  - Inappmessages
                  - Activity
                  - Execution
                  - Metrics
                  - Runs
                  - Runs
                  - Tags
                  - Resources
                  - ARN
                  - Types
                  - Phone
                  - Numbers
                  - Validate
            /v1/apps/{application-id}/events:
              POST:
                summary: PutEvents
                description: >-
                  <p>Creates a new event to record for endpoints, or creates or
                  updates endpoint data that existing events are associated
                  with.</p>
                tags:
                  - Put
                  - Events
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
                  - Baidu
                  - Campaigns
                  - Endpoints
                  - Endpoints
                  - Event Stream
                  - Gcm
                  - Journeys
                  - Recommenders
                  - Segments
                  - Users
                  - Users
                  - KPI
                  - Date Range
                  - KPI
                  - Settings
                  - Activities
                  - Versions
                  - Versions
                  - Jobs
                  - Inappmessages
                  - Activity
                  - Execution
                  - Metrics
                  - Runs
                  - Runs
                  - Tags
                  - Resources
                  - ARN
                  - Types
                  - Phone
                  - Numbers
                  - Validate
                  - Events
            /v1/apps/{application-id}/attributes/{attribute-type}:
              PUT:
                summary: RemoveAttributes
                description: >-
                  <p>Removes one or more custom attributes, of the same
                  attribute type, from the application. Existing endpoints still
                  have the attributes but Amazon Pinpoint will stop capturing
                  new or changed values for these attributes.</p>
                tags:
                  - Removes
                  - Attributes
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
                  - Baidu
                  - Campaigns
                  - Endpoints
                  - Endpoints
                  - Event Stream
                  - Gcm
                  - Journeys
                  - Recommenders
                  - Segments
                  - Users
                  - Users
                  - KPI
                  - Date Range
                  - KPI
                  - Settings
                  - Activities
                  - Versions
                  - Versions
                  - Jobs
                  - Inappmessages
                  - Activity
                  - Execution
                  - Metrics
                  - Runs
                  - Runs
                  - Tags
                  - Resources
                  - ARN
                  - Types
                  - Phone
                  - Numbers
                  - Validate
                  - Events
                  - Attributes
                  - Attributes
            /v1/apps/{application-id}/messages:
              POST:
                summary: SendMessages
                description: <p>Creates and sends a direct message.</p>
                tags:
                  - Send
                  - Messages
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
                  - Baidu
                  - Campaigns
                  - Endpoints
                  - Endpoints
                  - Event Stream
                  - Gcm
                  - Journeys
                  - Recommenders
                  - Segments
                  - Users
                  - Users
                  - KPI
                  - Date Range
                  - KPI
                  - Settings
                  - Activities
                  - Versions
                  - Versions
                  - Jobs
                  - Inappmessages
                  - Activity
                  - Execution
                  - Metrics
                  - Runs
                  - Runs
                  - Tags
                  - Resources
                  - ARN
                  - Types
                  - Phone
                  - Numbers
                  - Validate
                  - Events
                  - Attributes
                  - Attributes
                  - Messages
            /v1/apps/{application-id}/otp:
              POST:
                summary: SendOTPMessage
                description: <p>Send an OTP message</p>
                tags:
                  - Send
                  - Messages
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
                  - Baidu
                  - Campaigns
                  - Endpoints
                  - Endpoints
                  - Event Stream
                  - Gcm
                  - Journeys
                  - Recommenders
                  - Segments
                  - Users
                  - Users
                  - KPI
                  - Date Range
                  - KPI
                  - Settings
                  - Activities
                  - Versions
                  - Versions
                  - Jobs
                  - Inappmessages
                  - Activity
                  - Execution
                  - Metrics
                  - Runs
                  - Runs
                  - Tags
                  - Resources
                  - ARN
                  - Types
                  - Phone
                  - Numbers
                  - Validate
                  - Events
                  - Attributes
                  - Attributes
                  - Messages
                  - Otp
            /v1/apps/{application-id}/users-messages:
              POST:
                summary: SendUsersMessages
                description: <p>Creates and sends a message to a list of users.</p>
                tags:
                  - Send
                  - Users
                  - Messages
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
                  - Baidu
                  - Campaigns
                  - Endpoints
                  - Endpoints
                  - Event Stream
                  - Gcm
                  - Journeys
                  - Recommenders
                  - Segments
                  - Users
                  - Users
                  - KPI
                  - Date Range
                  - KPI
                  - Settings
                  - Activities
                  - Versions
                  - Versions
                  - Jobs
                  - Inappmessages
                  - Activity
                  - Execution
                  - Metrics
                  - Runs
                  - Runs
                  - Tags
                  - Resources
                  - ARN
                  - Types
                  - Phone
                  - Numbers
                  - Validate
                  - Events
                  - Attributes
                  - Attributes
                  - Messages
                  - Otp
            /v1/apps/{application-id}/endpoints:
              PUT:
                summary: UpdateEndpointsBatch
                description: >-
                  <p>Creates a new batch of endpoints for an application or
                  updates the settings and attributes of a batch of existing
                  endpoints for an application. You can also use this operation
                  to define custom attributes for a batch of endpoints. If an
                  update includes one or more values for a custom attribute,
                  Amazon Pinpoint replaces (overwrites) any existing values with
                  the new values.</p>
                tags:
                  - Update
                  - Endpoints
                  - Batches
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
                  - Baidu
                  - Campaigns
                  - Endpoints
                  - Endpoints
                  - Event Stream
                  - Gcm
                  - Journeys
                  - Recommenders
                  - Segments
                  - Users
                  - Users
                  - KPI
                  - Date Range
                  - KPI
                  - Settings
                  - Activities
                  - Versions
                  - Versions
                  - Jobs
                  - Inappmessages
                  - Activity
                  - Execution
                  - Metrics
                  - Runs
                  - Runs
                  - Tags
                  - Resources
                  - ARN
                  - Types
                  - Phone
                  - Numbers
                  - Validate
                  - Events
                  - Attributes
                  - Attributes
                  - Messages
                  - Otp
            /v1/apps/{application-id}/journeys/{journey-id}/state:
              PUT:
                summary: UpdateJourneyState
                description: <p>Pause, resume or cancels (stops) a journey.</p>
                tags:
                  - Update
                  - Journeys
                  - States
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
                  - Baidu
                  - Campaigns
                  - Endpoints
                  - Endpoints
                  - Event Stream
                  - Gcm
                  - Journeys
                  - Recommenders
                  - Segments
                  - Users
                  - Users
                  - KPI
                  - Date Range
                  - KPI
                  - Settings
                  - Activities
                  - Versions
                  - Versions
                  - Jobs
                  - Inappmessages
                  - Activity
                  - Execution
                  - Metrics
                  - Runs
                  - Runs
                  - Tags
                  - Resources
                  - ARN
                  - Types
                  - Phone
                  - Numbers
                  - Validate
                  - Events
                  - Attributes
                  - Attributes
                  - Messages
                  - Otp
                  - States
            /v1/templates/{template-name}/{template-type}/active-version:
              PUT:
                summary: UpdateTemplateActiveVersion
                description: >-
                  <p>Changes the status of a specific version of a message
                  template to <i>active</i>.</p>
                tags:
                  - Update
                  - Templates
                  - Active
                  - Versions
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
                  - Baidu
                  - Campaigns
                  - Endpoints
                  - Endpoints
                  - Event Stream
                  - Gcm
                  - Journeys
                  - Recommenders
                  - Segments
                  - Users
                  - Users
                  - KPI
                  - Date Range
                  - KPI
                  - Settings
                  - Activities
                  - Versions
                  - Versions
                  - Jobs
                  - Inappmessages
                  - Activity
                  - Execution
                  - Metrics
                  - Runs
                  - Runs
                  - Tags
                  - Resources
                  - ARN
                  - Types
                  - Phone
                  - Numbers
                  - Validate
                  - Events
                  - Attributes
                  - Attributes
                  - Messages
                  - Otp
                  - States
                  - Active
            /v1/apps/{application-id}/verify-otp:
              POST:
                summary: VerifyOTPMessage
                description: <p>Verify
                tags:
                  - Verify
                  - Messages
                  - V1
                  - Applications
                  - Applications
                  - Identifiers
                  - Campaigns
                  - Templates
                  - Templates
                  - Names
                  - Email
                  - Jobs
                  - Export
                  - Import
                  - Inapp
                  - Journeys
                  - Push
                  - Recommenders
                  - Segments
                  - SMS
                  - Voice
                  - Channels
                  - ADM
                  - Apns
                  - Apns_sandbox
                  - Apns_voip
                  - Apns_voip_sandbox
                  - Baidu
                  - Campaigns
                  - Endpoints
                  - Endpoints
                  - Event Stream
                  - Gcm
                  - Journeys
                  - Recommenders
                  - Segments
                  - Users
                  - Users
                  - KPI
                  - Date Range
                  - KPI
                  - Settings
                  - Activities
                  - Versions
                  - Versions
                  - Jobs
                  - Inappmessages
                  - Activity
                  - Execution
                  - Metrics
                  - Runs
                  - Runs
                  - Tags
                  - Resources
                  - ARN
                  - Types
                  - Phone
                  - Numbers
                  - Validate
                  - Events
                  - Attributes
                  - Attributes
                  - Messages
                  - Otp
                  - States
                  - Active
                  - Veri
    overlays:
      - type: APIs.io Search
        url: overlays/pinpoint-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/pinpoint-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:pinpoint
  - name: support-app
    description: >-
      <p><fullname>Amazon Web Services Support App in Slack</fullname> <p>You
      can use the Amazon Web Services Support App in Slack API to manage your
      support cases in Slack for your Amazon Web Services account. After you
      configure your Slack workspace and channel with the Amazon Web Services
      Support App, you can perform the following tasks directly in your Slack
      channel:</p> <ul> <li> <p>Create, search, update, and resolve your support
      cases</p> </li> <li> <p>Request service quota increases for your
      account</p> </li> <li> <p>Invite Amazon Web Services Support agents to
      your channel so that you can chat directly about your support cases</p>
      </li> </ul> <p>For more information about how to perform these actions in
      Slack, see the following documentation in the <i>Amazon Web Services
      Support User Guide</i>:</p> <ul> <li> <p> <a
      href="https://docs.aws.amazon.com/awssupport/latest/user/aws-support-app-for-slack.html">Amazon
      Web Services Support App in Slack</a> </p> </li> <li> <p> <a
      href="https://docs.aws.amazon.com/awssupport/latest/user/joining-a-live-chat-session.html">Joining
      a live chat session with Amazon Web Services Support</a> </p> </li> <li>
      <p> <a
      href="https://docs.aws.amazon.com/awssupport/latest/user/service-quota-increase.html">Requesting
      service quota increases</a> </p> </li> <li> <p> <a
      href="https://docs.aws.amazon.com/awssupport/latest/user/support-app-commands.html">Amazon
      Web Services Support App commands in Slack</a> </p> </li> </ul> <p>You can
      also use the Amazon Web Services Management Console instead of the Amazon
      Web Services Support App API to manage your Slack configurations. For more
      information, see <a
      href="https://docs.aws.amazon.com/awssupport/latest/user/authorize-slack-workspace.html">Authorize
      a Slack workspace to enable the Amazon Web Services Support App</a>.</p>
      <note> <ul> <li> <p>You must have a Business or Enterprise Support plan to
      use the Amazon Web Services Support App API. </p> </li> <li> <p>For more
      information about the Amazon Web Services Support App endpoints, see the
      <a
      href="https://docs.aws.amazon.com/general/latest/gr/awssupport.html#awssupport_app_region">Amazon
      Web Services Support App in Slack endpoints</a> in the <i>Amazon Web
      Services General Reference</i>.</p> </li> </ul> </note></p>
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
            title: support-app
          paths:
            /control/create-slack-channel-configuration:
              POST:
                summary: CreateSlackChannelConfiguration
                description: >-
                  <p>Creates a Slack channel configuration for your Amazon Web
                  Services account.</p> <note> <ul> <li> <p>You can add up to 5
                  Slack workspaces for your account.</p> </li> <li> <p>You can
                  add up to 20 Slack channels for your account.</p> </li> </ul>
                  </note> <p>A Slack channel can have up to 100 Amazon Web
                  Services accounts. This means that only 100 accounts can add
                  the same Slack channel to the Amazon Web Services Support App.
                  We recommend that you only add the accounts that you need to
                  manage support cases for your organization. This can reduce
                  the notifications about case updates that you receive in the
                  Slack channel.</p> <note> <p>We recommend that you choose a
                  private Slack channel so that only members in that channel
                  have read and write access to your support cases. Anyone in
                  your Slack channel can create, update, or resolve support
                  cases for your account. Users require an invitation to join
                  private channels. </p> </note>
                tags:
                  - Create
                  - Slack
                  - Channels
                  - Configurations
                  - Control
                  - Create
                  - Slack
                  - Channels
                  - Configurations
            /control/delete-account-alias:
              POST:
                summary: DeleteAccountAlias
                description: >-
                  <p>Deletes an alias for an Amazon Web Services account ID. The
                  alias appears in the Amazon Web Services Support App page of
                  the Amazon Web Services Support Center. The alias also appears
                  in Slack messages from the Amazon Web Services Support
                  App.</p>
                tags:
                  - Delete
                  - Account
                  - Alias
                  - Control
                  - Create
                  - Slack
                  - Channels
                  - Configurations
                  - Delete
                  - Account
                  - Alias
            /control/delete-slack-channel-configuration:
              POST:
                summary: DeleteSlackChannelConfiguration
                description: >-
                  <p>Deletes a Slack channel configuration from your Amazon Web
                  Services account. This operation doesn't delete your Slack
                  channel.</p>
                tags:
                  - Delete
                  - Slack
                  - Channels
                  - Configurations
                  - Control
                  - Create
                  - Slack
                  - Channels
                  - Configurations
                  - Delete
                  - Account
                  - Alias
            /control/delete-slack-workspace-configuration:
              POST:
                summary: DeleteSlackWorkspaceConfiguration
                description: >-
                  <p>Deletes a Slack workspace configuration from your Amazon
                  Web Services account. This operation doesn't delete your Slack
                  workspace.</p>
                tags:
                  - Delete
                  - Slack
                  - Workspaces
                  - Configurations
                  - Control
                  - Create
                  - Slack
                  - Channels
                  - Configurations
                  - Delete
                  - Account
                  - Alias
                  - Workspaces
            /control/get-account-alias:
              POST:
                summary: GetAccountAlias
                description: >-
                  <p>Retrieves the alias from an Amazon Web Services account ID.
                  The alias appears in the Amazon Web Services Support App page
                  of the Amazon Web Services Support Center. The alias also
                  appears in Slack messages from the Amazon Web Services Support
                  App.</p>
                tags:
                  - Get
                  - Account
                  - Alias
                  - Control
                  - Create
                  - Slack
                  - Channels
                  - Configurations
                  - Delete
                  - Account
                  - Alias
                  - Workspaces
                  - Get
            /control/list-slack-channel-configurations:
              POST:
                summary: ListSlackChannelConfigurations
                description: >-
                  <p>Lists the Slack channel configurations for an Amazon Web
                  Services account.</p>
                tags:
                  - Lists
                  - Slack
                  - Channels
                  - Configurations
                  - Control
                  - Create
                  - Slack
                  - Channels
                  - Configurations
                  - Delete
                  - Account
                  - Alias
                  - Workspaces
                  - Get
                  - Lists
                  - Configurations
            /control/list-slack-workspace-configurations:
              POST:
                summary: ListSlackWorkspaceConfigurations
                description: >-
                  <p>Lists the Slack workspace configurations for an Amazon Web
                  Services account.</p>
                tags:
                  - Lists
                  - Slack
                  - Workspaces
                  - Configurations
                  - Control
                  - Create
                  - Slack
                  - Channels
                  - Configurations
                  - Delete
                  - Account
                  - Alias
                  - Workspaces
                  - Get
                  - Lists
                  - Configurations
            /control/put-account-alias:
              POST:
                summary: PutAccountAlias
                description: >-
                  <p>Creates or updates an individual alias for each Amazon Web
                  Services account ID. The alias appears in the Amazon Web
                  Services Support App page of the Amazon Web Services Support
                  Center. The alias also appears in Slack messages from the
                  Amazon Web Services Support App.</p>
                tags:
                  - Put
                  - Account
                  - Alias
                  - Control
                  - Create
                  - Slack
                  - Channels
                  - Configurations
                  - Delete
                  - Account
                  - Alias
                  - Workspaces
                  - Get
                  - Lists
                  - Configurations
                  - Put
            /control/register-slack-workspace-for-organization:
              POST:
                summary: RegisterSlackWorkspaceForOrganization
                description: >-
                  <p>Registers a Slack workspace for your Amazon Web Services
                  account. To call this API, your account must be part of an
                  organization in Organizations.</p> <p>If you're the
                  <i>management account</i> and you want to register Slack
                  workspaces for your organization, you must complete the
                  following tasks:</p> <ol> <li> <p>Sign in to the <a
                  href="https://console.aws.amazon.com/support/app">Amazon Web
                  Services Support Center</a> and authorize the Slack workspaces
                  where you want your organization to have access to. See <a
                  href="https://docs.aws.amazon.com/awssupport/latest/user/authorize-slack-workspace.html">Authorize
                  a Slack workspace</a> in the <i>Amazon Web Services Support
                  User Guide</i>.</p> </li> <li> <p>Call the
                  <code>RegisterSlackWorkspaceForOrganization</code> API to
                  authorize each Slack workspace for the organization.</p> </li>
                  </ol> <p>After the management account authorizes the Slack
                  workspace, member accounts can call this API to authorize the
                  same Slack workspace for their individual accounts. Member
                  accounts don't need to authorize the Slack workspace manually
                  through the <a
                  href="https://console.aws.amazon.com/support/app">Amazon Web
                  Services Support Center</a>.</p> <p>To use the Amazon Web
                  Services Support App, each account must then complete the
                  following tasks:</p> <ul> <li> <p>Create an Identity and
                  Access Management (IAM) role with the required permission. For
                  more information, see <a
                  href="https://docs.aws.amazon.com/awssupport/latest/user/support-app-permissions.html">Managing
                  access to the Amazon Web Services Support App</a>.</p> </li>
                  <li> <p>Configure a Slack channel to use the Amazon Web
                  Services Support App for support cases for that account. For
                  more information, see <a
                  href="https://docs.aws.amazon.com/awssupport/latest/user/add-your-slack-channel.html">Configuring
                  a Slack channel</a>.</p> </li> </ul>
                tags:
                  - Register
                  - Slack
                  - Workspaces
                  - For
                  - Organizations
                  - Control
                  - Create
                  - Slack
                  - Channels
                  - Configurations
                  - Delete
                  - Account
                  - Alias
                  - Workspaces
                  - Get
                  - Lists
                  - Configurations
                  - Put
                  - Register
                  - For
                  - Organizations
            /control/update-slack-channel-configuration:
              POST:
                summary: UpdateSlackChannelConfiguration
                description: >-
                  <p>Updates the configuration for a Slack channel, such as case
                  update notifica
                tags:
                  - Update
                  - Slack
                  - Channels
                  - Configurations
                  - Control
                  - Create
                  - Slack
                  - Channels
                  - Configurations
                  - Delete
                  - Account
                  - Alias
                  - Workspaces
                  - Get
                  - Lists
                  - Configurations
                  - Put
                  - Register
                  - For
                  - Organizations
                  - Upda
    overlays:
      - type: APIs.io Search
        url: overlays/support-app-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/support-app-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:support-app
  - aid: bigcommerce:abandoned-carts
    name: Abandoned Carts
    description: Needs a description
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.bigcommerce.com/
    baseURL: https://api.example.com
    tags: []
    properties:
      - type: Documentation
        url: https://developer.bigcommerce.com/
      - type: OpenAPI
        data:
          openapi: 3.0.0
          info:
            version: ''
            title: Abandoned Carts
          tags:
            - name: Abandoned Carts
            - name: Abandoned Cart Settings
            - name: Abandoned Carts Settings
          paths:
            /abandoned-carts/settings:
              get:
                summary: Get Global Abandoned Cart Settings
                description: Returns the global abandoned cart settings of a store.
                tags:
                  - Get
                  - Global
                  - Abandoned
                  - Cart
                  - Settings
                  - Abandoned
                  - Carts
                  - Settings
              put:
                summary: Update Global Abandoned Cart Settings
                description: Updates the global abandoned cart settings of a store.
                tags:
                  - Update
                  - Global
                  - Abandoned
                  - Cart
                  - Settings
                  - Abandoned
                  - Carts
                  - Settings
              parameters:
                - null
            /abandoned-carts/settings/channels/{channel_id}:
              get:
                summary: Get Channel Abandoned Cart Settings
                description: >-
                  Returns the per-channel overrides for the abandoned cart
                  settings of a store.
                tags:
                  - Get
                  - Channel
                  - Abandoned
                  - Cart
                  - Settings
                  - Abandoned
                  - Carts
                  - Settings
                  - Channels
                  - Channel_id
              put:
                summary: Update Channel Abandoned Cart Settings
                description: >-
                  Updates the per-channel overrides for the abandoned cart
                  settings of a store.


                  #### OAuth Scopes

                  | UI Name                                      | Permission |
                  Parameter                                     |

                  |-||--|     

                  | Information & Settings                       | modify     |
                  `store_v2_information`                        |
                tags:
                  - Update
                  - Channel
                  - Abandoned
                  - Cart
                  - Settings
                  - Abandoned
                  - Carts
                  - Settings
                  - Channels
                  - Channel_id
              parameters:
                - null
                - null
            /abandoned-carts/{token}:
              get:
                summary: Get an Abandoned Cart
                description: >-
                  Returns the `cart_id` corresponding to the abandoned cart
                  `{token}` passed in.


                  **Usage Notes**:

                  * `{token}` is the token in the query string of the abandoned
                  cart link found in abandoned cart email notifications to
                  shoppers
                tags:
                  - Get
                  - An
                  - Abandoned
                  - Cart
                  - Abandoned
                  - Carts
                  - Settings
                  - Channels
                  - Channel_id
                  - Token
              parameters:
                - null
                - null
    overlays:
      - type: APIs.io Search
        url: overlays/abandoned-carts-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/abandoned-carts-openapi-api-evangelist-ratings.yml
  - aid: bigcommerce:carts
    name: Carts
    description: Needs a description
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.bigcommerce.com/
    baseURL: https://api.example.com
    tags: []
    properties:
      - type: Documentation
        url: https://developer.bigcommerce.com/
      - type: OpenAPI
        data:
          openapi: 3.0.3
          info:
            title: Carts
            version: ''
          tags:
            - name: Carts (Single)
            - name: Items
            - name: Redirects
            - name: Settings
            - name: Metafields
            - name: Batch metafields
          paths:
            /carts:
              parameters:
                - null
              post:
                description: >-
                  Creates a **Cart**. 


                  **Required Fields**


                  |Field|Details|

                  |-|-|

                  |`line_item`|Specifies a line item.| 

                  |`custom_items`|Specifies a custom item. Only required if
                  adding a custom item to the cart.|

                  |`gift_certificates`|Specifies a gift certificate. Only
                  required if adding a gift certificate to the cart.|


                  **Usage Notes**


                  * A **cart** `id` (UUID) is returned in the response.

                  * A **cart** `id` is the same as a **checkout** `id`.

                  * A cart can be created by adding an existing **catalog item**
                  or a **custom item**.

                  * Carts are valid for **30 days** from the **last
                  modification** (this includes creating the cart or editing the
                  cart).

                  * If a product has modifiers, use the `option_selections`
                  array to describe the **modifier** selection(s).

                  * The format and data type of a cart’s `option_value` are
                  defined by the `value_data` object of a product’s [variant
                  option
                  value](/docs/rest-catalog/product-variant-options/values),
                  [modifier value](/docs/rest-catalog/product-modifiers/values),
                  or a combination of both.

                  * Redirect URLs can only be generated from carts that were
                  created using the **REST Management API**. 

                  * To get cart `redirect_urls` in the response, append the
                  following query parameter to the request URL:
                  `include=redirect_urls`. Redirect URLs point to either a
                  shared checkout domain or a channel-specific domain, depending
                  on the storefront configuration.

                  * To restore a cart that was created by a shopper or through a
                  Storefront API, first recreate the cart using the **REST
                  Management API**.

                  * To get cart `promotions` in the response, append the
                  following query parameter to the request URL:
                  `include=promotions.banners`.
                tags:
                  - Create
                  - Cart
                  - Carts
                summary: Create a Cart
            /carts/{cartId}/items:
              parameters:
                - null
                - null
                - null
              post:
                description: >-
                  Adds line item to the *Cart*.


                  **Usage Notes**


                  To add a custom item use `custom_items`. 


                  Overriding a product’s `list_price` will make that item
                  ineligible for V3 product level promotions.


                  If a product has modifiers, omit the `variant_id` and instead
                  use the `option_selections` array to describe both the
                  **variant** and the **modifier** selections.


                  Please note that this API endpoint is not concurrent safe,
                  meaning multiple simultaneous requests could result in
                  unexpected and inconsistent results.
                tags:
                  - Add
                  - Cart
                  - Line
                  - Items
                  - Carts
                  - Id
                  - Items
                summary: Add Cart Line Items
            /carts/{cartId}/redirect_urls:
              parameters:
                - null
                - null
                - null
              post:
                description: >-
                  Creates a **Cart** redirect URL for redirecting a shopper to
                  an already created cart using the `cartId`.


                  **Usage Notes**


                  * Redirect URLs can also be created with **Create a Cart**
                  requests by appending `include=redirect_urls`.

                  * A **Carts** redirect URL may only be used once.

                  * Redirect URLs point to either a shared checkout domain or a
                  channel-specific domain, depending on the storefront
                  configuration.

                  * Once a redirect URL has been visited, it will be invalidated
                  and cannot be used again. 

                  * If your application requires URLs to be visited more than
                  once, consider generating a fresh one each time you need to
                  restore a cart, and redirecting to the URL from your own
                  application.

                  * Redirect URLs can be generated only from carts that were
                  created using the **REST Management API**. 

                  * To restore a cart that was created on the storefront, either
                  by a shopper or a Storefront API, first recreate the cart
                  using the **REST Management API**.

                  * When redirecting the shopper, you can add a set of
                  `query_params` to the URL. The `query_params` feature allows
                  passing additional information to the redirect URL.
                tags:
                  - Create
                  - Cart
                  - Redirect
                  - Carts
                  - Id
                  - Items
                  - Redirect_urls
                summary: Create Cart Redirect URL
            /carts/{cartId}/items/{itemId}:
              parameters:
                - null
                - null
                - null
              put:
                description: >-
                  Updates an existing, single line item in the *Cart*. 


                  **Notes**


                  Currently, only updating `list_price` and `quantity` are
                  supported. Updating a product’s `list_price` will make that
                  item ineligible for V3 product-level promotions. 


                  If the product has modifiers, omit the `variant_id` and
                  instead use the `option_selections` array to describe both the
                  **variant** and the **modifier** selections.


                  If a variant needs to be changed or updated, the product will
                  need to be removed and re-added to the cart with the correct
                  variants using the **Add Cart Line Items** endpoint.


                  `custom_items` cannot be updated via the API at this time. To
                  update your cart, add a new updated custom item and delete the
                  outdated one. If your cart contains only one line item,
                  perform the add operation before the delete operation.


                  Deleting all line items from the cart will invalidate the
                  cart. 


                  Please note that this API endpoint is not concurrent safe,
                  meaning multiple simultaneous requests could result in
                  unexpected and inconsistent results.
                tags:
                  - Update
                  - Cart
                  - Line
                  - Item
                  - Carts
                  - Id
                  - Items
                  - Redirect_urls
                  - Item
                summary: Update Cart Line Item
              delete:
                description: >-
                  Deletes a *Cart* line item. 


                  **Notes**


                  Removing the last `line_item` in the *Cart* deletes the
                  *Cart*.
                tags:
                  - Delete
                  - Cart
                  - Line
                  - Item
                  - Carts
                  - Id
                  - Items
                  - Redirect_urls
                  - Item
                summary: Delete Cart Line Item
            /carts/{cartId}:
              parameters:
                - null
                - null
              get:
                description: Returns a storeʼs *Cart*.
                tags:
                  - Get
                  - Cart
                  - Carts
                  - Id
                  - Items
                  - Redirect_urls
                  - Item
                summary: Get a Cart
              put:
                description: >-
                  Updates a *Cartʼs* `customer_id`.


                  **Notes**


                  Changing the *Cart* `customer_id` will remove any promotions
                  or shipping calculations on the *Cart*. These are tied to the
                  customer depending on cart conditions and any customer
                  groups. 
                tags:
                  - Update
                  - Customer
                  - Carts
                  - Id
                  - Items
                  - Redirect_urls
                  - Item
                summary: Update Customer ID
              delete:
                description: >-
                  Deletes a *Cart*. Once a *Cart* has been deleted it can’t be
                  recovered.
                tags:
                  - Delete
                  - Cart
                  - Carts
                  - Id
                  - Items
                  - Redirect_urls
                  - Item
                summary: Delete a Cart
            /carts/settings:
              parameters:
                - null
              get:
                summary: Get Global Cart Settings
                description: Returns the global cart settings of a store.
                tags:
                  - Get
                  - Global
                  - Cart
                  - Settings
                  - Carts
                  - Id
                  - Items
                  - Redirect_urls
                  - Item
                  - Settings
              put:
                summary: Update Global Cart Settings
                description: Update the global cart settings of a store.
                tags:
                  - Update
                  - Global
                  - Cart
                  - Settings
                  - Carts
                  - Id
                  - Items
                  - Redirect_urls
                  - Item
                  - Settings
            /carts/settings/channels/{channel_id}:
              parameters:
                - null
                - null
              get:
                summary: Get Channel Cart Settings
                description: >-
                  Returns the per-channel overrides for the cart settings of a
                  store.
                tags:
                  - Get
                  - Channel
                  - Cart
                  - Settings
                  - Carts
                  - Id
                  - Items
                  - Redirect_urls
                  - Item
                  - Settings
                  - Channels
                  - Channel_id
              put:
                summary: Update Channel Cart Settings
                description: >-
                  Update the per-channel overrides for the cart settings of a
                  store.
                tags:
                  - Update
                  - Channel
                  - Cart
                  - Settings
                  - Carts
                  - Id
                  - Items
                  - Redirect_urls
                  - Item
                  - Settings
                  - Channels
                  - Channel_id
            /carts/{cart_id}/metafields:
              parameters:
                - null
                - null
              get:
                summary: Get Cart Metafields
                tags:
                  - Get
                  - Cart
                  - Metafields
                  - Carts
                  - Id
                  - Items
                  - Redirect_urls
                  - Item
                  - Settings
                  - Channels
                  - Channel_id
                  - Cart_id
                  - Metafields
                description: Get a cart's metafields.
              post:
                summary: Create a Cart Metafield
                tags:
                  - Create
                  - Cart
                  - Metafield
                  - Carts
                  - Id
                  - Items
                  - Redirect_urls
                  - Item
                  - Settings
                  - Channels
                  - Channel_id
                  - Cart_id
                  - Metafields
                description: >
                  Create a cart `Metafield`. 


                  If you create an order from a Cart, you can continue
                  referencing the Cart Metafields even if you delete the
                  original Cart. Use the `cart_id` field on the Order to
                  construct the Cart Metafield endpoint. 
            /carts/{cart_id}/metafields/{metafield_id}:
              get:
                summary: Get a Cart Metafield
                tags:
                  - Get
                  - Cart
                  - Metafield
                  - Carts
                  - Id
                  - Items
                  - Redirect_urls
                  - Item
                  - Settings
                  - Channels
                  - Channel_id
                  - Cart_id
                  - Metafields
                  - Metafield_id
                description: Gets a cart metafield.
              put:
                summary: Update a Cart Metafield
                tags:
                  - Update
                  - Cart
                  - Metafield
                  - Carts
                  - Id
                  - Items
                  - Redirect_urls
                  - Item
                  - Settings
                  - Channels
                  - Channel_id
                  - Cart_id
                  - Metafields
                  - Metafield_id
                description: |
                  Update a `Metafield`, by `cart_id`.
              delete:
                summary: Delete a Metafield
                tags:
                  - Delete
                  - Metafield
                  - Carts
                  - Id
                  - Items
                  - Redirect_urls
                  - Item
                  - Settings
                  - Channels
                  - Channel_id
                  - Cart_id
                  - Metafields
                  - Metafield_id
                description: |
                  Deletes a `Metafield`.
              parameters:
                - null
                - null
                - null
            /carts/metafields:
              get:
                summary: Get All Cart Metafields
                tags:
                  - Get
                  - All
                  - Cart
                  - Metafields
                  - Carts
                  - Id
                  - Items
                  - Redirect_urls
                  - Item
                  - Settings
                  - Channels
                  - Channel_id
                  - Cart_id
                  - Metafields
                  - Metafield_id
                description: Get all cart metafields.
              post:
                summary: Create multiple Metafields
                tags:
                  - Create
                  - Multiple
                  - Metafields
                  - Carts
                  - Id
                  - Items
                  - Redirect_urls
                  - Item
                  - Settings
                  - Channels
                  - Channel_id
                  - Cart_id
                  - Metafields
                  - Metafield_id
                description: Create multiple metafields.
              put:
                summary: Update multiple Metafields
                tags:
                  - Update
                  - Multiple
                  - Metafields
                  - Carts
                  - Id
                  - Items
                  - Redirect_urls
                  - Item
                  - Settings
                  - Channels
                  - Channel_id
                  - Cart_id
                  - Metafields
                  - Metafield_id
                description: Create multiple metafields.
              delete:
                summary: Delete All Metafields
                tags:
                  - Delete
                  - All
                  - Metafields
                  - Carts
                  - Id
                  - Items
                  - Redirect_urls
                  - Item
                  - Settings
                  - Channels
                  - Channel_id
                  - Cart_id
                  - Metafields
                  - Metafield_id
                description: Delete all cart
    overlays:
      - type: APIs.io Search
        url: overlays/carts-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/carts-openapi-api-evangelist-ratings.yml
  - aid: bigcommerce:channels
    name: Channels
    description: Needs a description
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.bigcommerce.com/
    baseURL: https://api.example.com
    tags: []
    properties:
      - type: Documentation
        url: https://developer.bigcommerce.com/
      - type: OpenAPI
        data:
          openapi: 3.0.0
          info:
            version: ''
            title: Channels
          tags:
            - name: Batch metafields
            - name: Channels
            - name: Metafields
            - name: Menus
            - name: Active Theme
            - name: Currency Assignments
            - name: Listings
            - name: Site
            - name: Site Checkout URL
          paths:
            /channels:
              parameters:
                - null
              get:
                tags:
                  - Get
                  - All
                  - Channels
                  - Channels
                summary: Get All Channels
                description: >-
                  Returns a list of *Channels*.


                  Will always return the default BigCommerce storefront with an
                  ID of `1`. This storefront is created by default when you
                  provision a BigCommerce store.
              post:
                tags:
                  - Create
                  - Channel
                  - Channels
                summary: Create a Channel
                description: Creates a *Channel*.
            /channels/{channel_id}:
              parameters:
                - null
                - null
              get:
                tags:
                  - Get
                  - Channel
                  - Channels
                  - Channel_id
                summary: Get a Channel
                description: >-
                  Returns a *Channel*. Channel ID `1` returns the default
                  BigCommerce storefront.
              put:
                tags:
                  - Update
                  - Channel
                  - Channels
                  - Channel_id
                summary: Update a Channel
                description: >-
                  Updates a *Channel*.


                  ## Updatable Fields


                  The following fields can be updated.

                  * `name`

                  * `external_id`

                  * `status`

                  * `is_listable_from_ui`

                  * `is_visible`

                  * `config_meta`



                  > #### Note

                  > * Partial updates are supported. In most cases, if a field
                  that *cannot* be updated is passed in, the API **will not**
                  respond with an error. It returns a 200 response with the
                  object, in which you will see the field(s) were not updated.

                  > * `platform` and `type` cannot be updated after a channel is
                  created.

                  > * A channel with status `deleted` or `terminated` cannot be
                  updated.
            /channels/{channel_id}/active-theme:
              parameters:
                - null
                - null
              get:
                tags:
                  - Get
                  - Channel
                  - Active
                  - Theme
                  - Channels
                  - Channel_id
                  - Active
                  - Theme
                summary: Get a Channel Active Theme
                description: |-
                  Returns details of the theme active on the specified channel.
                  Does not support active Blueprint (legacy) themes.
            /channels/currency-assignments:
              parameters:
                - null
              get:
                tags:
                  - Get
                  - All
                  - Channels
                  - Currency
                  - Assignments
                  - Channels
                  - Channel_id
                  - Active
                  - Theme
                  - Currency
                  - Assignments
                summary: Get All Channels Currency Assignments
                description: Returns a list of currency assignments for all channels.
              post:
                tags:
                  - Create
                  - Multiple
                  - Channels
                  - Currency
                  - Assignments
                  - Channels
                  - Channel_id
                  - Active
                  - Theme
                  - Currency
                  - Assignments
                summary: Create Multiple Channels Currency Assignments
                description: >-
                  Sets enabled currencies and default currency for multiple
                  channels. Note that currencies must be added first in the
                  **Settings > Setup > Currencies** settings from an active
                  MSF-enabled BigCommerce store control panel before the
                  currencies can be assigned to a channel.
              put:
                tags:
                  - Update
                  - Multiple
                  - Channels
                  - Currency
                  - Assignments
                  - Channels
                  - Channel_id
                  - Active
                  - Theme
                  - Currency
                  - Assignments
                summary: Update Multiple Channels Currency Assignments
                description: >-
                  Updates enabled currencies and default currency for multiple
                  channels. Note that currencies must be added first in the
                  **Settings > Setup > Currencies** settings from an active
                  MSF-enabled BigCommerce store control panel before the
                  currencies can be assigned to a channel.
            /channels/{channel_id}/currency-assignments:
              parameters:
                - null
                - null
              get:
                tags:
                  - Get
                  - Channel
                  - Currency
                  - Assignments
                  - Channels
                  - Channel_id
                  - Active
                  - Theme
                  - Currency
                  - Assignments
                summary: Get Channel Currency Assignments
                description: Returns a list of currency assignments for a specific channel.
              post:
                tags:
                  - Create
                  - Channel
                  - Currency
                  - Assignments
                  - Channels
                  - Channel_id
                  - Active
                  - Theme
                  - Currency
                  - Assignments
                summary: Create Channel Currency Assignments
                description: >-
                  Sets enabled currencies and default currency for a specific
                  channel. Note that currencies must be added first in the
                  **Settings > Setup > Currencies** settings from an active
                  MSF-enabled BigCommerce store control panel before the
                  currencies can be assigned to a channel.
              put:
                tags:
                  - Update
                  - Channel
                  - Currency
                  - Assignments
                  - Channels
                  - Channel_id
                  - Active
                  - Theme
                  - Currency
                  - Assignments
                summary: Update Channel Currency Assignments
                description: >-
                  Updates enabled currencies and default currency for a specific
                  channel. Note that currencies must be added first in the
                  **Settings > Setup > Currencies** settings from an active
                  MSF-enabled BigCommerce store control panel before the
                  currencies can be assigned to a channel.
              delete:
                tags:
                  - Delete
                  - Channel
                  - Currency
                  - Assignments
                  - Channels
                  - Channel_id
                  - Active
                  - Theme
                  - Currency
                  - Assignments
                summary: Delete Channel Currency Assignments
                description: >-
                  Deletes currency assignments for a specific channel. Once
                  done, this channel will inherit the store’s currency settings.
            /channels/{channel_id}/listings:
              parameters:
                - null
                - null
              get:
                tags:
                  - Get
                  - Channel
                  - Listings
                  - Channels
                  - Channel_id
                  - Active
                  - Theme
                  - Currency
                  - Assignments
                  - Listings
                summary: Get Channel Listings
                description: >-
                  Returns a list of all *Channel Listings* for a specific
                  channel. Note that if the *Channel* is not found or there is
                  no listing associated to the *Channel*, it will return a 200
                  response with empty data.
              post:
                tags:
                  - Create
                  - Channel
                  - Listings
                  - Channels
                  - Channel_id
                  - Active
                  - Theme
                  - Currency
                  - Assignments
                  - Listings
                summary: Create Channel Listings
                description: Creates one or more *Channel Listings* for a specific channel.
              put:
                tags:
                  - Update
                  - Channel
                  - Listings
                  - Channels
                  - Channel_id
                  - Active
                  - Theme
                  - Currency
                  - Assignments
                  - Listings
                summary: Update Channel Listings
                description: >-
                  Updates one or more *Channel Listings* for a specific channel.


                  > #### Note

                  > * Partial updates are supported. In most cases, if a field
                  that *cannot* be updated is passed in, the API **will not**
                  respond with an error. It returns a 200 response with the
                  object, in which you will see the field(s) were not updated.

                  > * If a new variant is provided, the API will append the
                  variant to the list. If a variant already exists, the API will
                  update the existing variant. Other variants that are not
                  provided in the payload remains unchanged.

                  > * If `listing_id` does not exist, the API will return a 200
                  response with empty data.

                  > * `listing_id` is required and cannot be less than or equal
                  to zero.

                  > * `product_id` cannot be updated after a channel listing is
                  created.

                  > * `product_id` of a variant must match the `product_id` of
                  the channel listing.
            /channels/{channel_id}/listings/{listing_id}:
              parameters:
                - null
                - null
                - null
              get:
                tags:
                  - Get
                  - Channel
                  - Listing
                  - Channels
                  - Channel_id
                  - Active
                  - Theme
                  - Currency
                  - Assignments
                  - Listings
                  - Listing_id
                summary: Get a Channel Listing
                description: Returns a *Channel Listing* for a specific channel.
            /channels/{channel_id}/site/checkout-url:
              parameters:
                - null
                - null
              put:
                summary: Upsert a Siteʼs Checkout URL
                tags:
                  - Upsert
                  - Siteʼs
                  - Checkout
                  - Channels
                  - Channel_id
                  - Active
                  - Theme
                  - Currency
                  - Assignments
                  - Listings
                  - Listing_id
                  - Site
                  - Checkout
                  - Url
                description: Creates or updates (upserts) a siteʼs checkout URL
              delete:
                summary: Delete a Siteʼs Checkout URL
                description: >-
                  Deletes a siteʼs checkout URL. After deletion, a shared
                  checkout URL is used.
                tags:
                  - Delete
                  - Siteʼs
                  - Checkout
                  - Channels
                  - Channel_id
                  - Active
                  - Theme
                  - Currency
                  - Assignments
                  - Listings
                  - Listing_id
                  - Site
                  - Checkout
                  - Url
            /channels/{channel_id}/site:
              parameters:
                - null
                - null
              get:
                summary: Get a Channel Site
                description: |
                  Alias of `GET /sites?channel_id=channel_id`

                  Returns site data for the specified channel.
                tags:
                  - Get
                  - Channel
                  - Site
                  - Channels
                  - Channel_id
                  - Active
                  - Theme
                  - Currency
                  - Assignments
                  - Listings
                  - Listing_id
                  - Site
                  - Checkout
                  - Url
              put:
                summary: Update a Channel Site
                tags:
                  - Update
                  - Channel
                  - Site
                  - Channels
                  - Channel_id
                  - Active
                  - Theme
                  - Currency
                  - Assignments
                  - Listings
                  - Listing_id
                  - Site
                  - Checkout
                  - Url
                description: Updates a site for provided channel.
              post:
                summary: Create a Channel Site
                tags:
                  - Create
                  - Channel
                  - Site
                  - Channels
                  - Channel_id
                  - Active
                  - Theme
                  - Currency
                  - Assignments
                  - Listings
                  - Listing_id
                  - Site
                  - Checkout
                  - Url
                description: Alias of POST `/sites`. Creates a site for provided channel.
              delete:
                description: Deletes the Channelʼs site.
                tags:
                  - Delete
                  - Channel
                  - Site
                  - Channels
                  - Channel_id
                  - Active
                  - Theme
                  - Currency
                  - Assignments
                  - Listings
                  - Listing_id
                  - Site
                  - Checkout
                  - Url
                summary: Delete a Channel Site
            /channels/{channel_id}/channel-menus:
              parameters:
                - null
                - null
              get:
                summary: Get Channel Menus
                description: >
                  Returns list of Control Panel side navigation menus for a
                  channel.
                tags:
                  - Get
                  - Channel
                  - Menus
                  - Channels
                  - Channel_id
                  - Active
                  - Theme
                  - Currency
                  - Assignments
                  - Listings
                  - Listing_id
                  - Site
                  - Checkout
                  - Url
                  - Channel
                  - Menus
              post:
                summary: Create Channel Menus
                tags:
                  - Create
                  - Channel
                  - Menus
                  - Channels
                  - Channel_id
                  - Active
                  - Theme
                  - Currency
                  - Assignments
                  - Listings
                  - Listing_id
                  - Site
                  - Checkout
                  - Url
                  - Channel
                  - Menus
                description: >-
                  Creates or replaces list of control panel side navigation
                  menus for a channel.
              delete:
                description: Deletes control panel side navigation menus for a channel.
                tags:
                  - Delete
                  - Channel
                  - Menus
                  - Channels
                  - Channel_id
                  - Active
                  - Theme
                  - Currency
                  - Assignments
                  - Listings
                  - Listing_id
                  - Site
                  - Checkout
                  - Url
                  - Channel
                  - Menus
                summary: Delete Channel Menus
            /channels/{channel_id}/metafields:
              parameters:
                - null
                - null
              get:
                summary: Get Channel Metafields
                tags:
                  - Get
                  - Channel
                  - Metafields
                  - Channels
                  - Channel_id
                  - Active
                  - Theme
                  - Currency
                  - Assignments
                  - Listings
                  - Listing_id
                  - Site
                  - Checkout
                  - Url
                  - Channel
                  - Menus
                  - Metafields
                description: >-
                  Returns a list of metafields on a channel. Optional filter
                  parameters can be passed in.
              post:
                summary: Create a Channel Metafield
                tags:
                  - Create
                  - Channel
                  - Metafield
                  - Channels
                  - Channel_id
                  - Active
                  - Theme
                  - Currency
                  - Assignments
                  - Listings
                  - Listing_id
                  - Site
                  - Checkout
                  - Url
                  - Channel
                  - Menus
                  - Metafields
                description: >-
                  Creates a channel metafield.


                  **Note:** The maxiumum number of metafields allowed on each
                  order, product, category, variant, channel, or brand is 250
                  per client ID. For more information, see [Platform
                  Limits](https://support.bigcommerce.com/s/article/Platform-Limits)
                  in the Help Center.
            /channels/{channel_id}/metafields/{metafield_id}:
              parameters:
                - null
                - null
                - null
              get:
                summary: Get a Channel Metafield
                tags:
                  - Get
                  - Channel
                  - Metafield
                  - Channels
                  - Channel_id
                  - Active
                  - Theme
                  - Currency
                  - Assignments
                  - Listings
                  - Listing_id
                  - Site
                  - Checkout
                  - Url
                  - Channel
                  - Menus
                  - Metafields
                  - Metafield_id
                description: Returns a single channel metafield.
              put:
                summary: Update a Channel Metafield
                tags:
                  - Update
                  - Channel
                  - Metafield
                  - Channels
                  - Channel_id
                  - Active
                  - Theme
                  - Currency
                  - Assignments
                  - Listings
                  - Listing_id
                  - Site
                  - Checkout
                  - Url
                  - Channel
                  - Menus
                  - Metafields
                  - Metafield_id
                description: >-
                  Updates a single channel metafield.


                  **Usage Notes**

                  * Attempting to modify `namespace`, `key`, and
                  `permission_set` fields using a client ID different from the
                  one used to create those metafields will result in a `403`
                  error message. 
              delete:
                summary: Delete a Channel Metafield
                tags:
                  - Delete
                  - Channel
                  - Metafield
                  - Channels
                  - Channel_id
                  - Active
                  - Theme
                  - Currency
                  - Assignments
                  - Listings
                  - Listing_id
                  - Site
                  - Checkout
                  - Url
                  - Channel
                  - Menus
                  - Metafields
                  - Metafield_id
                description: Deletes a single channel metafield.
            /channels/metafields:
              get:
                summary: Get All Channel Metafields
                tags:
                  - Get
                  - All
                  - Channel
                  - Metafields
                  - Channels
                  - Channel_id
                  - Active
                  - Theme
                  - Currency
                  - Assignments
                  - Listings
                  - Listing_id
                  - Site
                  - Checkout
                  - Url
                  - Channel
                  - Menus
                  - Metafields
                  - Metafield_id
                description: Get all channel metafields.
              post:
                summary: Create multiple Metafields
                tags:
                  - Create
                  - Multiple
                  - Metafields
                  - Channels
                  - Channel_id
                  - Active
                  - Theme
                  - Currency
                  - Assignments
                  - Listings
                  - Listing_id
                  - Site
                  - Checkout
                  - Url
                  - Channel
                  - Menus
                  - Metafields
                  - Metafield_id
                description: Create multiple metafields.
              put:
                summary: Update multiple Metafields
                tags:
                  - Update
                  - Multiple
                  - Metafields
                  - Channels
                  - Channel_id
                  - Active
                  - Theme
                  - Currency
                  - Assignments
                  - Listings
                  - Listing_id
                  - Site
                  - Checkout
                  - Url
                  - Channel
                  - Menus
                  - Metafields
                  - Metafield_id
                description: Update multiple metafields.
              delete:
                summary: Delete All Metafields
                tags:
                  - Delete
                  - All
                  - Metafields
                  - Channels
                  - Channel_id
                  - Active
                  - Theme
                  - Currency
                  - Assignments
                  - Listings
                  - Listing_id
                  - Site
                  - Checkout
                  - Url
                  - Channel
                  - Menus
                  - Metafields
                  - Metafield_id
                description: Delete all channel
    overlays:
      - type: APIs.io Search
        url: overlays/channels-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/channels-openapi-api-evangelist-ratings.yml
  - aid: bigcommerce:customers
    name: Customers
    description: Needs a description
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.bigcommerce.com/
    baseURL: https://api.example.com
    tags: []
    properties:
      - type: Documentation
        url: https://developer.bigcommerce.com/
      - type: OpenAPI
        data:
          openapi: 3.0.0
          info:
            version: ''
            title: Customers V3
          tags:
            - name: Customers
            - name: Consent
            - name: Validate Credentials
            - name: Metafields
            - name: Customer Metafields
            - name: Customer Batch Metafields
            - name: Addresses
            - name: Attributes
            - name: Attribute Values
            - name: Form Fields
            - name: Form Field Values
            - name: Stored Instruments
            - name: Global Settings
            - name: Channel Settings
          paths:
            /customers:
              get:
                description: >-
                  Returns a list of Customers. Optional filter parameters can be
                  passed in.


                  **Notes**


                  Attribute names are not available on the customer object.
                summary: Get All Customers
                tags:
                  - Get
                  - All
                  - Customers
                  - Customers
              post:
                description: >-
                  Creates Customers. Create up to 10 customers in one call.


                  **Required Fields**

                  * last_name

                  * first_name

                  * email


                  **Required Fields Customer Address**

                  * first_name

                  * city

                  * country_code

                  * last_name

                  * address1


                  **Required Fields Attributes**

                  * Attributes must be
                  [created](/docs/rest-management/customers/customer-attributes#create-a-customer-attribute)
                  **BEFORE** creating a customer.

                  * attribute_id

                  * attribute_value -- This is input as a string, regardless of
                  the
                  [Type](/docs/rest-management/customers/customer-attributes#create-a-customer-attribute).


                  **Notes**


                  A customer can be created with global access or
                  channel-specific access.

                  * **Global access:**
                    * Make sure the channel has `allow_global_logins` enabled. This is on by default only for the default storefront. Find more info at [Customer Settings > Channel](/docs/rest-management/customers/customer-settings-channel).
                    * Omit `channel_ids` field, or provide `channel_ids: null`.
                  * **Channel-specific access:**
                    * Provide a `channel_ids` array containing the channels accessible by the customer. This array cannot be empty.
                summary: Create Customers
                tags:
                  - Create
                  - Customers
                  - Customers
              put:
                description: >-
                  Updates Customers. Subresource updates are not supported. Up
                  to 10 customers can be updated in one call.


                  **Required Fields**

                  * id -- ID of the *Customer* This must be included in the
                  request body


                  **Read Only Fields**

                  * id

                  * registration_ip_address

                  * date_created

                  * date_modified



                  **Notes**


                  * Attributes Values can not be updated using Update a
                  Customer. Use the [Update customer attribute
                  values](/docs/rest-management/customers/customer-attribute-values#upsert-customer-attribute-values)
                  endpoint.

                  * channel_ids -- Updating the list of channels a customer can
                  access may create some side effects in a multi-storefront
                  situation. This list determines which customer account we will
                  use to authenticate a shopper given a channel.
                summary: Update Customers
                tags:
                  - Update
                  - Customers
                  - Customers
              delete:
                description: >-
                  Deletes Customers.


                  **Required Query**

                  * id:in -- ID of the customer


                  **Notes**


                  A query is required to delete customers. If not provided, a
                  204 is returned, with no changes to the data.
                summary: Delete Customers
                tags:
                  - Delete
                  - Customers
                  - Customers
            /customers/addresses:
              get:
                description: >-
                  Returns a list of Customer Addresses. Optional filter
                  parameters can be passed in.
                summary: Get All Customer Addresses
                tags:
                  - Get
                  - All
                  - Customer
                  - Addresses
                  - Customers
                  - Addresses
              post:
                description: >-
                  Creates a Customer Address. Multiple customer addresses can be
                  created in one call.


                  **Required Fields**

                  * **customer_id**

                  * **first_name**

                  * **last_name**

                  * **city**

                  * **country_code**

                  * **address1**


                  **Notes**

                  * A unique customer address is a combination of the following
                  core address fields:
                    * **customer_id**
                    * **first_name**
                    * **last_name**
                    * **company**
                    * **phone**
                    * **address_type**
                    * **address1**
                    * **address2**
                    * **city**
                    * **country_code**
                    * **state_or_province**
                    * **postal_code**
                  * An attempt to create an address that already exists will
                  result in no change to the address or custom form field
                  values, an HTTP 200 return code, and the address will be
                  absent from the response body.

                  * The default rate limit for this endpoint is 10 concurrent
                  requests.
                summary: Create a Customer Address
                tags:
                  - Create
                  - Customer
                  - Address
                  - Customers
                  - Addresses
              put:
                description: >-
                  Updates a Customer Address. Multiple customer addresses can be
                  updated in one call.


                  **Required Fields**

                  * **id** -- ID of the *Customer Address*


                  **Limits**

                  * Limit of **3** concurrent requests.


                  **Notes**

                  * A unique customer address is a combination of the following
                  core address fields:
                    * **first_name**
                    * **last_name**
                    * **company**
                    * **phone**
                    * **address_type**
                    * **address1**
                    * **address2**
                    * **city**
                    * **country_code**
                    * **state_or_province**
                    * **postal_code**
                  * An attempt to update an address such that it becomes
                  identical to another address that already exists will result
                  in no change to the target address or custom form field
                  values. The response will have an HTTP 200 return code, and
                  the address will be absent from the response body.
                summary: Update a Customer Address
                tags:
                  - Update
                  - Customer
                  - Address
                  - Customers
                  - Addresses
              delete:
                description: |-
                  Deletes a Customer Address.

                  **Required Query**
                  * id:in -- ID of the *Customer Address*
                summary: Delete a Customer Address
                tags:
                  - Delete
                  - Customer
                  - Address
                  - Customers
                  - Addresses
            /customers/validate-credentials:
              post:
                tags:
                  - Validate
                  - Customer
                  - Credentials
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                description: >-
                  Validate a customer credentials - This endpoint has special
                  rate limiting protections to protect against abuse.
                summary: Validate a customer credentials
            /customers/settings:
              get:
                tags:
                  - Get
                  - Customer
                  - Settings
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                description: Returns the global-level customer settings.
                summary: Get Customer Settings
              put:
                tags:
                  - Update
                  - Customer
                  - Settings
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                description: Updates the customer settings on the global level.
                summary: Update Customer Settings
            /customers/settings/channels/{channel_id}:
              get:
                tags:
                  - Get
                  - Customer
                  - Settings
                  - Per
                  - Channel
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                description: |-
                  Returns the customer settings per channel.

                  **Notes**

                   * `null` indicates that there is no override per given channel and values are inherited from the global level.
                summary: Get Customer Settings per Channel
              put:
                tags:
                  - Update
                  - Customer
                  - Settings
                  - Per
                  - Channel
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                description: >-
                  Update the customer settings per channel


                  **Required Fields**


                  * `channel_id`: Provide a `channel_id` array containing one or
                  more channel IDs. Customers will have access to these channels
                  and no others. This array cannot be empty.


                  **Notes**


                  * Setting `null` will delete override per given channel, and
                  values will be inherited from the global level. Make sure the
                  channel has `allow_global_logins` enabled.
                summary: Update Customer Settings per Channel
              parameters:
                - null
            /customers/attributes:
              get:
                description: >-
                  Returns a list of Customer Attributes. You can pass in
                  optional filter parameters.
                summary: Get All Customer Attributes
                tags:
                  - Get
                  - All
                  - Customer
                  - Attributes
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                  - Attributes
              post:
                description: >-
                  Creates a Customer Attribute. Multiple customer attributes can
                  be created in one call.


                  **Required Fields**

                  * name

                  * type


                  **Limits**

                  * Limit of 3 concurrent requests.


                  **Notes**


                  Once the data type is set, it cannot be changed. The attribute
                  will need to be deleted then created again with the new data
                  type. This will also delete it from the customer.


                  Customer attributes are created separately from the customer.
                  After the name and type are created, then the attributes can
                  be added to the customer.


                  A store cannot have more than 50 customer attributes.
                summary: Create a Customer Attribute
                tags:
                  - Create
                  - Customer
                  - Attribute
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                  - Attributes
              put:
                description: >-
                  Updates a Customer Attribute. Multiple customer attributes can
                  be updated in one call.


                  **Required Fields**

                  * id -- ID of the *Customer Attribute*


                  Once the data type is set, it can not be changed. The
                  attribute will need to be deleted then created again with the
                  new data type. This will also delete it from the customer.


                  **Limits**

                  * Limit of 3 concurrent requests.
                summary: Update a Customer Attribute
                tags:
                  - Update
                  - Customer
                  - Attribute
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                  - Attributes
              delete:
                description: |-
                  Deletes Customer Attributes from the store.

                  **Required Query**
                  * id:in -- ID of the *Customer Attribute*
                summary: Delete Customer Attributes
                tags:
                  - Delete
                  - Customer
                  - Attributes
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                  - Attributes
            /customers/attribute-values:
              get:
                description: >-
                  Returns a list of Customer Attribute Values. Optional filter
                  parameters can be passed in.
                summary: Get All Customer Attribute Values
                tags:
                  - Get
                  - All
                  - Customer
                  - Attribute
                  - Values
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                  - Attributes
                  - Attribute
                  - Values
              put:
                description: >-
                  Upserts Customer Attribute Values. Updates the attribute
                  values on the Customer. Multiple customer attribute values can
                  be updated in one call.


                  Upsert checks for an existing record. If there is none, it
                  creates the record, if there is a matching record, it updates
                  that record.


                  **Limits**

                  * 10 per call limit.
                summary: Upsert Customer Attribute Values
                tags:
                  - Upsert
                  - Customer
                  - Attribute
                  - Values
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                  - Attributes
                  - Attribute
                  - Values
              delete:
                description: >-
                  Deletes Customer Attribute Values. Deletes the attribute value
                  from the customer.


                  **Required Query**

                  * id:in - ID of the *Customer Attribute Value*
                summary: Delete Customer Attribute Values
                tags:
                  - Delete
                  - Customer
                  - Attribute
                  - Values
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                  - Attributes
                  - Attribute
                  - Values
            /customers/form-field-values:
              get:
                summary: Get Customer Form Field Values
                description: >-
                  Returns a list of form field values for the Customer or
                  Customer Address object.


                  To learn about adding and managing form fields, see [Adding
                  and Editing Fields in the Account Signup
                  Form](https://support.bigcommerce.com/s/article/Editing-Form-Fields).
                tags:
                  - Get
                  - Customer
                  - Form
                  - Field
                  - Values
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                  - Attributes
                  - Attribute
                  - Values
                  - Form
                  - Field
              put:
                summary: Upsert Customer Form Field Values
                description: >-
                  Updates form field values on the Customer or Customer Address
                  objects. Multiple form field values can be updated in one
                  call.


                  Upsert checks for an existing record, if there is none it
                  creates the record, if there is a matching record it updates
                  that record.


                  To learn more about editing form fields, see [Adding and
                  Editing Fields in the Account Signup
                  Form](https://support.bigcommerce.com/s/article/Editing-Form-Fields).


                  **Limits**

                  * Limit of 10 concurrent requests.
                tags:
                  - Upsert
                  - Customer
                  - Form
                  - Field
                  - Values
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                  - Attributes
                  - Attribute
                  - Values
                  - Form
                  - Field
            /customers/{customerId}/consent:
              get:
                description: >-
                  Gets the status of a customerʼs consent to allow data
                  collection by cookies and scripts while shopping on a
                  storefront.
                summary: Get Customer Consent
                tags:
                  - Get
                  - Customer
                  - Consent
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                  - Attributes
                  - Attribute
                  - Values
                  - Form
                  - Field
                  - Id
                  - Consent
              put:
                description: >-
                  Updates the status of a customerʼs consent to allow data
                  collection by cookies and scripts while shopping on a
                  storefront.
                summary: Update Customer Consent
                tags:
                  - Update
                  - Customer
                  - Consent
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                  - Attributes
                  - Attribute
                  - Values
                  - Form
                  - Field
                  - Id
                  - Consent
              parameters:
                - null
            /customers/{customerId}/stored-instruments:
              get:
                summary: Get Stored Instruments
                tags:
                  - Get
                  - Stored
                  - Instruments
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                  - Attributes
                  - Attribute
                  - Values
                  - Form
                  - Field
                  - Id
                  - Consent
                  - Stored
                  - Instruments
                description: >-
                  Lists all available stored instruments for a customer. This
                  list will include all types of stored instruments namely card,
                  account and bank_account instruments
              parameters:
                - null
            /customers/{customerId}/metafields:
              get:
                summary: Get Customer Metafields
                tags:
                  - Get
                  - Customer
                  - Metafields
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                  - Attributes
                  - Attribute
                  - Values
                  - Form
                  - Field
                  - Id
                  - Consent
                  - Stored
                  - Instruments
                  - Metafields
                description: >-
                  Gets customer metafields by passing the `customerId` in the
                  query parameters.
              post:
                summary: Create Customer Metafields
                tags:
                  - Create
                  - Customer
                  - Metafields
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                  - Attributes
                  - Attribute
                  - Values
                  - Form
                  - Field
                  - Id
                  - Consent
                  - Stored
                  - Instruments
                  - Metafields
                description: >-
                  Creates Customer metafields by passing the `customerId` in the
                  query parameters.
            /customers/{customerId}/metafields/{metafieldId}:
              get:
                summary: Get Customer Metafields List
                description: >
                  Lists available metafields for a customer. To retrieve the
                  list, use `customerId` and `metafieldId` in the query
                  parameters.
                tags:
                  - Get
                  - Customer
                  - Metafields
                  - List
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                  - Attributes
                  - Attribute
                  - Values
                  - Form
                  - Field
                  - Id
                  - Consent
                  - Stored
                  - Instruments
                  - Metafields
                  - Metafield
              put:
                summary: Update a Metafield
                tags:
                  - Update
                  - Metafield
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                  - Attributes
                  - Attribute
                  - Values
                  - Form
                  - Field
                  - Id
                  - Consent
                  - Stored
                  - Instruments
                  - Metafields
                  - Metafield
                description: >-
                  Updates customer metafields. To update the customer
                  metafields, use 'customerId' and 'metafield' in the query
                  parameters.
              delete:
                summary: Delete Customer Metafields
                tags:
                  - Delete
                  - Customer
                  - Metafields
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                  - Attributes
                  - Attribute
                  - Values
                  - Form
                  - Field
                  - Id
                  - Consent
                  - Stored
                  - Instruments
                  - Metafields
                  - Metafield
                description: >
                  Deletes customer metafields. To delete customer metafields,
                  use 'customerId' and 'metafieldId' in the query parameters.
            /customers/metafields:
              get:
                summary: Get All Customer Metafields
                tags:
                  - Get
                  - All
                  - Customer
                  - Metafields
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                  - Attributes
                  - Attribute
                  - Values
                  - Form
                  - Field
                  - Id
                  - Consent
                  - Stored
                  - Instruments
                  - Metafields
                  - Metafield
                description: Get all customer metafields.
              post:
                summary: Create Multiple Metafields
                tags:
                  - Create
                  - Multiple
                  - Metafields
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                  - Attributes
                  - Attribute
                  - Values
                  - Form
                  - Field
                  - Id
                  - Consent
                  - Stored
                  - Instruments
                  - Metafields
                  - Metafield
                description: Create multiple metafields.
              put:
                summary: Update Multiple Metafields
                tags:
                  - Update
                  - Multiple
                  - Metafields
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                  - Attributes
                  - Attribute
                  - Values
                  - Form
                  - Field
                  - Id
                  - Consent
                  - Stored
                  - Instruments
                  - Metafields
                  - Metafield
                description: Create multiple metafields.
              delete:
                summary: Delete All Metafields
                tags:
                  - Delete
                  - All
                  - Metafields
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                  - Attributes
                  - Attribute
                  - Values
                  - Form
                  - Field
                  - Id
                  - Consent
                  - Stored
                  - Instruments
                  - Metafields
                  - Metafield
                description: Delete all customer
    overlays:
      - type: APIs.io Search
        url: overlays/customers-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/customers-openapi-api-evangelist-ratings.yml
  - aid: bigcommerce:customers
    name: Customers
    description: Needs a description
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.bigcommerce.com/
    baseURL: https://api.example.com
    tags: []
    properties:
      - type: Documentation
        url: https://developer.bigcommerce.com/
      - type: OpenAPI
        data:
          openapi: 3.0.0
          info:
            version: ''
            title: Customers V3
          tags:
            - name: Customers
            - name: Consent
            - name: Validate Credentials
            - name: Metafields
            - name: Customer Metafields
            - name: Customer Batch Metafields
            - name: Addresses
            - name: Attributes
            - name: Attribute Values
            - name: Form Fields
            - name: Form Field Values
            - name: Stored Instruments
            - name: Global Settings
            - name: Channel Settings
          paths:
            /customers:
              get:
                description: >-
                  Returns a list of Customers. Optional filter parameters can be
                  passed in.


                  **Notes**


                  Attribute names are not available on the customer object.
                summary: Get All Customers
                tags:
                  - Get
                  - All
                  - Customers
                  - Customers
              post:
                description: >-
                  Creates Customers. Create up to 10 customers in one call.


                  **Required Fields**

                  * last_name

                  * first_name

                  * email


                  **Required Fields Customer Address**

                  * first_name

                  * city

                  * country_code

                  * last_name

                  * address1


                  **Required Fields Attributes**

                  * Attributes must be
                  [created](/docs/rest-management/customers/customer-attributes#create-a-customer-attribute)
                  **BEFORE** creating a customer.

                  * attribute_id

                  * attribute_value -- This is input as a string, regardless of
                  the
                  [Type](/docs/rest-management/customers/customer-attributes#create-a-customer-attribute).


                  **Notes**


                  A customer can be created with global access or
                  channel-specific access.

                  * **Global access:**
                    * Make sure the channel has `allow_global_logins` enabled. This is on by default only for the default storefront. Find more info at [Customer Settings > Channel](/docs/rest-management/customers/customer-settings-channel).
                    * Omit `channel_ids` field, or provide `channel_ids: null`.
                  * **Channel-specific access:**
                    * Provide a `channel_ids` array containing the channels accessible by the customer. This array cannot be empty.
                summary: Create Customers
                tags:
                  - Create
                  - Customers
                  - Customers
              put:
                description: >-
                  Updates Customers. Subresource updates are not supported. Up
                  to 10 customers can be updated in one call.


                  **Required Fields**

                  * id -- ID of the *Customer* This must be included in the
                  request body


                  **Read Only Fields**

                  * id

                  * registration_ip_address

                  * date_created

                  * date_modified



                  **Notes**


                  * Attributes Values can not be updated using Update a
                  Customer. Use the [Update customer attribute
                  values](/docs/rest-management/customers/customer-attribute-values#upsert-customer-attribute-values)
                  endpoint.

                  * channel_ids -- Updating the list of channels a customer can
                  access may create some side effects in a multi-storefront
                  situation. This list determines which customer account we will
                  use to authenticate a shopper given a channel.
                summary: Update Customers
                tags:
                  - Update
                  - Customers
                  - Customers
              delete:
                description: >-
                  Deletes Customers.


                  **Required Query**

                  * id:in -- ID of the customer


                  **Notes**


                  A query is required to delete customers. If not provided, a
                  204 is returned, with no changes to the data.
                summary: Delete Customers
                tags:
                  - Delete
                  - Customers
                  - Customers
            /customers/addresses:
              get:
                description: >-
                  Returns a list of Customer Addresses. Optional filter
                  parameters can be passed in.
                summary: Get All Customer Addresses
                tags:
                  - Get
                  - All
                  - Customer
                  - Addresses
                  - Customers
                  - Addresses
              post:
                description: >-
                  Creates a Customer Address. Multiple customer addresses can be
                  created in one call.


                  **Required Fields**

                  * **customer_id**

                  * **first_name**

                  * **last_name**

                  * **city**

                  * **country_code**

                  * **address1**


                  **Notes**

                  * A unique customer address is a combination of the following
                  core address fields:
                    * **customer_id**
                    * **first_name**
                    * **last_name**
                    * **company**
                    * **phone**
                    * **address_type**
                    * **address1**
                    * **address2**
                    * **city**
                    * **country_code**
                    * **state_or_province**
                    * **postal_code**
                  * An attempt to create an address that already exists will
                  result in no change to the address or custom form field
                  values, an HTTP 200 return code, and the address will be
                  absent from the response body.

                  * The default rate limit for this endpoint is 10 concurrent
                  requests.
                summary: Create a Customer Address
                tags:
                  - Create
                  - Customer
                  - Address
                  - Customers
                  - Addresses
              put:
                description: >-
                  Updates a Customer Address. Multiple customer addresses can be
                  updated in one call.


                  **Required Fields**

                  * **id** -- ID of the *Customer Address*


                  **Limits**

                  * Limit of **3** concurrent requests.


                  **Notes**

                  * A unique customer address is a combination of the following
                  core address fields:
                    * **first_name**
                    * **last_name**
                    * **company**
                    * **phone**
                    * **address_type**
                    * **address1**
                    * **address2**
                    * **city**
                    * **country_code**
                    * **state_or_province**
                    * **postal_code**
                  * An attempt to update an address such that it becomes
                  identical to another address that already exists will result
                  in no change to the target address or custom form field
                  values. The response will have an HTTP 200 return code, and
                  the address will be absent from the response body.
                summary: Update a Customer Address
                tags:
                  - Update
                  - Customer
                  - Address
                  - Customers
                  - Addresses
              delete:
                description: |-
                  Deletes a Customer Address.

                  **Required Query**
                  * id:in -- ID of the *Customer Address*
                summary: Delete a Customer Address
                tags:
                  - Delete
                  - Customer
                  - Address
                  - Customers
                  - Addresses
            /customers/validate-credentials:
              post:
                tags:
                  - Validate
                  - Customer
                  - Credentials
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                description: >-
                  Validate a customer credentials - This endpoint has special
                  rate limiting protections to protect against abuse.
                summary: Validate a customer credentials
            /customers/settings:
              get:
                tags:
                  - Get
                  - Customer
                  - Settings
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                description: Returns the global-level customer settings.
                summary: Get Customer Settings
              put:
                tags:
                  - Update
                  - Customer
                  - Settings
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                description: Updates the customer settings on the global level.
                summary: Update Customer Settings
            /customers/settings/channels/{channel_id}:
              get:
                tags:
                  - Get
                  - Customer
                  - Settings
                  - Per
                  - Channel
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                description: |-
                  Returns the customer settings per channel.

                  **Notes**

                   * `null` indicates that there is no override per given channel and values are inherited from the global level.
                summary: Get Customer Settings per Channel
              put:
                tags:
                  - Update
                  - Customer
                  - Settings
                  - Per
                  - Channel
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                description: >-
                  Update the customer settings per channel


                  **Required Fields**


                  * `channel_id`: Provide a `channel_id` array containing one or
                  more channel IDs. Customers will have access to these channels
                  and no others. This array cannot be empty.


                  **Notes**


                  * Setting `null` will delete override per given channel, and
                  values will be inherited from the global level. Make sure the
                  channel has `allow_global_logins` enabled.
                summary: Update Customer Settings per Channel
              parameters:
                - null
            /customers/attributes:
              get:
                description: >-
                  Returns a list of Customer Attributes. You can pass in
                  optional filter parameters.
                summary: Get All Customer Attributes
                tags:
                  - Get
                  - All
                  - Customer
                  - Attributes
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                  - Attributes
              post:
                description: >-
                  Creates a Customer Attribute. Multiple customer attributes can
                  be created in one call.


                  **Required Fields**

                  * name

                  * type


                  **Limits**

                  * Limit of 3 concurrent requests.


                  **Notes**


                  Once the data type is set, it cannot be changed. The attribute
                  will need to be deleted then created again with the new data
                  type. This will also delete it from the customer.


                  Customer attributes are created separately from the customer.
                  After the name and type are created, then the attributes can
                  be added to the customer.


                  A store cannot have more than 50 customer attributes.
                summary: Create a Customer Attribute
                tags:
                  - Create
                  - Customer
                  - Attribute
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                  - Attributes
              put:
                description: >-
                  Updates a Customer Attribute. Multiple customer attributes can
                  be updated in one call.


                  **Required Fields**

                  * id -- ID of the *Customer Attribute*


                  Once the data type is set, it can not be changed. The
                  attribute will need to be deleted then created again with the
                  new data type. This will also delete it from the customer.


                  **Limits**

                  * Limit of 3 concurrent requests.
                summary: Update a Customer Attribute
                tags:
                  - Update
                  - Customer
                  - Attribute
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                  - Attributes
              delete:
                description: |-
                  Deletes Customer Attributes from the store.

                  **Required Query**
                  * id:in -- ID of the *Customer Attribute*
                summary: Delete Customer Attributes
                tags:
                  - Delete
                  - Customer
                  - Attributes
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                  - Attributes
            /customers/attribute-values:
              get:
                description: >-
                  Returns a list of Customer Attribute Values. Optional filter
                  parameters can be passed in.
                summary: Get All Customer Attribute Values
                tags:
                  - Get
                  - All
                  - Customer
                  - Attribute
                  - Values
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                  - Attributes
                  - Attribute
                  - Values
              put:
                description: >-
                  Upserts Customer Attribute Values. Updates the attribute
                  values on the Customer. Multiple customer attribute values can
                  be updated in one call.


                  Upsert checks for an existing record. If there is none, it
                  creates the record, if there is a matching record, it updates
                  that record.


                  **Limits**

                  * 10 per call limit.
                summary: Upsert Customer Attribute Values
                tags:
                  - Upsert
                  - Customer
                  - Attribute
                  - Values
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                  - Attributes
                  - Attribute
                  - Values
              delete:
                description: >-
                  Deletes Customer Attribute Values. Deletes the attribute value
                  from the customer.


                  **Required Query**

                  * id:in - ID of the *Customer Attribute Value*
                summary: Delete Customer Attribute Values
                tags:
                  - Delete
                  - Customer
                  - Attribute
                  - Values
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                  - Attributes
                  - Attribute
                  - Values
            /customers/form-field-values:
              get:
                summary: Get Customer Form Field Values
                description: >-
                  Returns a list of form field values for the Customer or
                  Customer Address object.


                  To learn about adding and managing form fields, see [Adding
                  and Editing Fields in the Account Signup
                  Form](https://support.bigcommerce.com/s/article/Editing-Form-Fields).
                tags:
                  - Get
                  - Customer
                  - Form
                  - Field
                  - Values
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                  - Attributes
                  - Attribute
                  - Values
                  - Form
                  - Field
              put:
                summary: Upsert Customer Form Field Values
                description: >-
                  Updates form field values on the Customer or Customer Address
                  objects. Multiple form field values can be updated in one
                  call.


                  Upsert checks for an existing record, if there is none it
                  creates the record, if there is a matching record it updates
                  that record.


                  To learn more about editing form fields, see [Adding and
                  Editing Fields in the Account Signup
                  Form](https://support.bigcommerce.com/s/article/Editing-Form-Fields).


                  **Limits**

                  * Limit of 10 concurrent requests.
                tags:
                  - Upsert
                  - Customer
                  - Form
                  - Field
                  - Values
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                  - Attributes
                  - Attribute
                  - Values
                  - Form
                  - Field
            /customers/{customerId}/consent:
              get:
                description: >-
                  Gets the status of a customerʼs consent to allow data
                  collection by cookies and scripts while shopping on a
                  storefront.
                summary: Get Customer Consent
                tags:
                  - Get
                  - Customer
                  - Consent
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                  - Attributes
                  - Attribute
                  - Values
                  - Form
                  - Field
                  - Id
                  - Consent
              put:
                description: >-
                  Updates the status of a customerʼs consent to allow data
                  collection by cookies and scripts while shopping on a
                  storefront.
                summary: Update Customer Consent
                tags:
                  - Update
                  - Customer
                  - Consent
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                  - Attributes
                  - Attribute
                  - Values
                  - Form
                  - Field
                  - Id
                  - Consent
              parameters:
                - null
            /customers/{customerId}/stored-instruments:
              get:
                summary: Get Stored Instruments
                tags:
                  - Get
                  - Stored
                  - Instruments
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                  - Attributes
                  - Attribute
                  - Values
                  - Form
                  - Field
                  - Id
                  - Consent
                  - Stored
                  - Instruments
                description: >-
                  Lists all available stored instruments for a customer. This
                  list will include all types of stored instruments namely card,
                  account and bank_account instruments
              parameters:
                - null
            /customers/{customerId}/metafields:
              get:
                summary: Get Customer Metafields
                tags:
                  - Get
                  - Customer
                  - Metafields
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                  - Attributes
                  - Attribute
                  - Values
                  - Form
                  - Field
                  - Id
                  - Consent
                  - Stored
                  - Instruments
                  - Metafields
                description: >-
                  Gets customer metafields by passing the `customerId` in the
                  query parameters.
              post:
                summary: Create Customer Metafields
                tags:
                  - Create
                  - Customer
                  - Metafields
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                  - Attributes
                  - Attribute
                  - Values
                  - Form
                  - Field
                  - Id
                  - Consent
                  - Stored
                  - Instruments
                  - Metafields
                description: >-
                  Creates Customer metafields by passing the `customerId` in the
                  query parameters.
            /customers/{customerId}/metafields/{metafieldId}:
              get:
                summary: Get Customer Metafields List
                description: >
                  Lists available metafields for a customer. To retrieve the
                  list, use `customerId` and `metafieldId` in the query
                  parameters.
                tags:
                  - Get
                  - Customer
                  - Metafields
                  - List
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                  - Attributes
                  - Attribute
                  - Values
                  - Form
                  - Field
                  - Id
                  - Consent
                  - Stored
                  - Instruments
                  - Metafields
                  - Metafield
              put:
                summary: Update a Metafield
                tags:
                  - Update
                  - Metafield
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                  - Attributes
                  - Attribute
                  - Values
                  - Form
                  - Field
                  - Id
                  - Consent
                  - Stored
                  - Instruments
                  - Metafields
                  - Metafield
                description: >-
                  Updates customer metafields. To update the customer
                  metafields, use 'customerId' and 'metafield' in the query
                  parameters.
              delete:
                summary: Delete Customer Metafields
                tags:
                  - Delete
                  - Customer
                  - Metafields
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                  - Attributes
                  - Attribute
                  - Values
                  - Form
                  - Field
                  - Id
                  - Consent
                  - Stored
                  - Instruments
                  - Metafields
                  - Metafield
                description: >
                  Deletes customer metafields. To delete customer metafields,
                  use 'customerId' and 'metafieldId' in the query parameters.
            /customers/metafields:
              get:
                summary: Get All Customer Metafields
                tags:
                  - Get
                  - All
                  - Customer
                  - Metafields
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                  - Attributes
                  - Attribute
                  - Values
                  - Form
                  - Field
                  - Id
                  - Consent
                  - Stored
                  - Instruments
                  - Metafields
                  - Metafield
                description: Get all customer metafields.
              post:
                summary: Create Multiple Metafields
                tags:
                  - Create
                  - Multiple
                  - Metafields
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                  - Attributes
                  - Attribute
                  - Values
                  - Form
                  - Field
                  - Id
                  - Consent
                  - Stored
                  - Instruments
                  - Metafields
                  - Metafield
                description: Create multiple metafields.
              put:
                summary: Update Multiple Metafields
                tags:
                  - Update
                  - Multiple
                  - Metafields
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                  - Attributes
                  - Attribute
                  - Values
                  - Form
                  - Field
                  - Id
                  - Consent
                  - Stored
                  - Instruments
                  - Metafields
                  - Metafield
                description: Create multiple metafields.
              delete:
                summary: Delete All Metafields
                tags:
                  - Delete
                  - All
                  - Metafields
                  - Customers
                  - Addresses
                  - Validate
                  - Credentials
                  - Settings
                  - Channels
                  - Channel_id
                  - Attributes
                  - Attribute
                  - Values
                  - Form
                  - Field
                  - Id
                  - Consent
                  - Stored
                  - Instruments
                  - Metafields
                  - Metafield
                description: Delete all customer
    overlays:
      - type: APIs.io Search
        url: overlays/customers-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/customers-openapi-api-evangelist-ratings.yml
  - aid: bigcommerce:orders
    name: Orders
    description: Needs a description
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.bigcommerce.com/
    baseURL: https://api.example.com
    tags: []
    properties:
      - type: Documentation
        url: https://developer.bigcommerce.com/
      - type: OpenAPI
        data:
          openapi: 3.0.3
          info:
            title: Orders V3
            version: ''
            license:
              name: ''
          tags:
            - name: Metafields
            - name: Payment Actions
            - name: Transactions
            - name: Order Settings
            - name: Batch metafields
          paths:
            /orders/{order_id}/payment_actions/capture:
              post:
                summary: Capture order payment
                description: >-
                  Capture the payment for an order. When there are no payment
                  method validation issues, the capture process is successful,
                  the `payment_status` updates to `capture pending`, and the
                  payment request is scheduled. The payment request itself
                  occurs asynchronously.

                  Requires at least one of the following scopes:

                  * `store_v2_orders`

                  * `store_v2_transactions`
                tags:
                  - Capture
                  - Order
                  - Payment
                  - Orders
                  - Order_id
                  - Payment_actions
                  - Capture
              parameters:
                - null
                - null
            /orders/{order_id}/payment_actions/void:
              post:
                summary: Void
                description: >-
                  Void the payment for an order. When there are no payment
                  method validation issues, the void process is successful, the
                  `payment_status` updates to `void pending`, and the void
                  payment request is scheduled. The payment request itself
                  occurs asynchronously.


                  Requires at least one of the following scopes:

                  * `store_v2_orders`

                  * `store_v2_transactions`
                tags:
                  - Void
                  - Orders
                  - Order_id
                  - Payment_actions
                  - Capture
                  - Void
              parameters:
                - null
                - null
            /orders/{order_id}/transactions:
              parameters:
                - null
                - null
              get:
                tags:
                  - Get
                  - Transactions
                  - Orders
                  - Order_id
                  - Payment_actions
                  - Capture
                  - Void
                  - Transactions
                description: >-
                  Returns an **orderʼs** transactions.


                  **Usage Notes**

                  * Depending on the payment method, different information will
                  be available (not all payment gateways return full card or
                  fraud detail).



                  Requires at least one of the following scopes:

                  * `store_v2_transactions_read_only`

                  * `store_v2_transactions`
                summary: Get Transactions
            /orders/{order_id}/payment_actions/refund_quotes:
              post:
                summary: Create a Refund Quote
                description: >-
                  Calculate the tax amount, total refund amount and get
                  available payment options for an order refund by providing
                  items and costs or quantities to refund.


                  Requires at least one of the following scopes:

                  * `store_v2_orders`

                  * `store_v2_transactions`


                  **Note:**

                  Order refunds are processed consecutively. Processing
                  synchronous refunds on an order are not yet supported.
                tags:
                  - Create
                  - Refund
                  - Quote
                  - Orders
                  - Order_id
                  - Payment_actions
                  - Capture
                  - Void
                  - Transactions
                  - Refund_quotes
              parameters:
                - null
                - null
            /orders/{order_id}/payment_actions/refunds:
              post:
                summary: Create a Refund
                description: >-
                  Creates a refund. When there are no payment method validation
                  issues, the refund process is successful and the refund
                  payment request is scheduled. The payment request itself
                  occurs asynchronously.


                  Requires at least one of the following scopes:

                  * `store_v2_orders`

                  * `store_v2_transactions`


                  **Note:**

                  Order refunds are processed consecutively. Processing
                  synchronous refunds on an order are not yet supported.
                tags:
                  - Create
                  - Refund
                  - Orders
                  - Order_id
                  - Payment_actions
                  - Capture
                  - Void
                  - Transactions
                  - Refund_quotes
                  - Refunds
              get:
                summary: Get Refunds for Order
                description: >-
                  Returns a list of refunds ordered by refund ID in ascending
                  order for the given order.


                  Requires at least one of the following scopes:

                  * `store_v2_transactions_read_only`

                  * `store_v2_transactions`

                  * `store_v2_orders_read_only`

                  * `store_v2_orders`
                tags:
                  - Get
                  - Refunds
                  - For
                  - Order
                  - Orders
                  - Order_id
                  - Payment_actions
                  - Capture
                  - Void
                  - Transactions
                  - Refund_quotes
                  - Refunds
              parameters:
                - null
                - null
            /orders/payment_actions/refunds/{refund_id}:
              parameters:
                - null
                - null
              get:
                summary: Get a Refund
                description: Returns a refund by refund ID.
                tags:
                  - Get
                  - Refund
                  - Orders
                  - Order_id
                  - Payment_actions
                  - Capture
                  - Void
                  - Transactions
                  - Refund_quotes
                  - Refunds
                  - Refund_id
            /orders/payment_actions/refunds:
              parameters:
                - null
              get:
                summary: Get All Refunds
                description: >-
                  Returns a list of refunds ordered by refund ID in ascending
                  order.


                  Requires at least one of the following scopes:

                  * `store_v2_transactions_read_only`

                  * `store_v2_transactions`

                  * `store_v2_orders_read_only`

                  * `store_v2_orders`
                tags:
                  - Get
                  - All
                  - Refunds
                  - Orders
                  - Order_id
                  - Payment_actions
                  - Capture
                  - Void
                  - Transactions
                  - Refund_quotes
                  - Refunds
                  - Refund_id
            /orders/payment_actions/refund_quotes:
              post:
                summary: Create Refund Quotes - BATCH
                description: >-
                  Calculate the tax amount, total refund amount and get
                  available payment options for an order refund by providing
                  items and costs or quantities to refund.


                  This endpoint will accept a batch of one or more.


                  Requires at least one of the following scopes:

                  * `store_v2_orders`

                  * `store_v2_transactions`
                tags:
                  - Create
                  - Refund
                  - Quotes
                  - Orders
                  - Order_id
                  - Payment_actions
                  - Capture
                  - Void
                  - Transactions
                  - Refund_quotes
                  - Refunds
                  - Refund_id
            /orders/{order_id}/metafields:
              parameters:
                - null
                - null
              get:
                summary: Get Order Metafields
                tags:
                  - Get
                  - Order
                  - Metafields
                  - Orders
                  - Order_id
                  - Payment_actions
                  - Capture
                  - Void
                  - Transactions
                  - Refund_quotes
                  - Refunds
                  - Refund_id
                  - Metafields
                description: >
                  Gets a `Metafield` object list, by `order_id`.


                  The maximum number of metafields allowed on each order,
                  product, category, variant, or brand is 250 per client ID.
              post:
                summary: Create Metafields
                tags:
                  - Create
                  - Metafields
                  - Orders
                  - Order_id
                  - Payment_actions
                  - Capture
                  - Void
                  - Transactions
                  - Refund_quotes
                  - Refunds
                  - Refund_id
                  - Metafields
                description: >-
                  Creates an order `Metafield`.


                  The maximum number of metafields allowed on each order,
                  product, category, variant, or brand is 250 per client ID.
            /orders/{order_id}/metafields/{metafield_id}:
              parameters:
                - null
                - null
                - null
              get:
                summary: Get a Metafield
                tags:
                  - Get
                  - Metafield
                  - Orders
                  - Order_id
                  - Payment_actions
                  - Capture
                  - Void
                  - Transactions
                  - Refund_quotes
                  - Refunds
                  - Refund_id
                  - Metafields
                  - Metafield_id
                description: |
                  Gets a `Metafield`, by `order_id`.
              put:
                summary: Update a Metafield
                tags:
                  - Update
                  - Metafield
                  - Orders
                  - Order_id
                  - Payment_actions
                  - Capture
                  - Void
                  - Transactions
                  - Refund_quotes
                  - Refunds
                  - Refund_id
                  - Metafields
                  - Metafield_id
                description: >-
                  Updates a `Metafield` object.


                  The maxiumum number of metafields allowed on each order,
                  product, category, variant, or brand is 250 per client ID.
              delete:
                summary: Delete a Metafield
                tags:
                  - Delete
                  - Metafield
                  - Orders
                  - Order_id
                  - Payment_actions
                  - Capture
                  - Void
                  - Transactions
                  - Refund_quotes
                  - Refunds
                  - Refund_id
                  - Metafields
                  - Metafield_id
                description: |
                  Deletes a `Metafield`.
            /orders/settings:
              get:
                summary: Get Global Order Settings
                description: Returns global order settings.
                tags:
                  - Get
                  - Global
                  - Order
                  - Settings
                  - Orders
                  - Order_id
                  - Payment_actions
                  - Capture
                  - Void
                  - Transactions
                  - Refund_quotes
                  - Refunds
                  - Refund_id
                  - Metafields
                  - Metafield_id
                  - Settings
              put:
                summary: Update Global Order Settings
                description: Updates global order settings.
                tags:
                  - Update
                  - Global
                  - Order
                  - Settings
                  - Orders
                  - Order_id
                  - Payment_actions
                  - Capture
                  - Void
                  - Transactions
                  - Refund_quotes
                  - Refunds
                  - Refund_id
                  - Metafields
                  - Metafield_id
                  - Settings
              parameters:
                - null
            /orders/settings/channels/{channel_id}:
              get:
                summary: Get Channel Order Settings
                description: Returns order settings for a specific channel.
                tags:
                  - Get
                  - Channel
                  - Order
                  - Settings
                  - Orders
                  - Order_id
                  - Payment_actions
                  - Capture
                  - Void
                  - Transactions
                  - Refund_quotes
                  - Refunds
                  - Refund_id
                  - Metafields
                  - Metafield_id
                  - Settings
                  - Channels
                  - Channel_id
              put:
                summary: Update Channel Order Settings
                description: |-
                  Updates order settings for a specific channel.

                   **Note:** You must override both notifications `email_addresses` or neither, i.e. either both notification `email_addresses` are an array of valid email addresses, or both `email_addresses` must be null. You may not have one set to an array of addresses and the other set to `null`.
                tags:
                  - Update
                  - Channel
                  - Order
                  - Settings
                  - Orders
                  - Order_id
                  - Payment_actions
                  - Capture
                  - Void
                  - Transactions
                  - Refund_quotes
                  - Refunds
                  - Refund_id
                  - Metafields
                  - Metafield_id
                  - Settings
                  - Channels
                  - Channel_id
              parameters:
                - null
                - null
            /orders/metafields:
              get:
                summary: Get All Order Metafields
                tags:
                  - Get
                  - All
                  - Order
                  - Metafields
                  - Orders
                  - Order_id
                  - Payment_actions
                  - Capture
                  - Void
                  - Transactions
                  - Refund_quotes
                  - Refunds
                  - Refund_id
                  - Metafields
                  - Metafield_id
                  - Settings
                  - Channels
                  - Channel_id
                description: Get all order metafields.
              post:
                summary: Create multiple Metafields
                tags:
                  - Create
                  - Multiple
                  - Metafields
                  - Orders
                  - Order_id
                  - Payment_actions
                  - Capture
                  - Void
                  - Transactions
                  - Refund_quotes
                  - Refunds
                  - Refund_id
                  - Metafields
                  - Metafield_id
                  - Settings
                  - Channels
                  - Channel_id
                description: Create multiple metafields.
              put:
                summary: Update multiple Metafields
                tags:
                  - Update
                  - Multiple
                  - Metafields
                  - Orders
                  - Order_id
                  - Payment_actions
                  - Capture
                  - Void
                  - Transactions
                  - Refund_quotes
                  - Refunds
                  - Refund_id
                  - Metafields
                  - Metafield_id
                  - Settings
                  - Channels
                  - Channel_id
                description: Create multiple metafields.
              delete:
                summary: Delete All Metafields
                tags:
                  - Delete
                  - All
                  - Metafields
                  - Orders
                  - Order_id
                  - Payment_actions
                  - Capture
                  - Void
                  - Transactions
                  - Refund_quotes
                  - Refunds
                  - Refund_id
                  - Metafields
                  - Metafield_id
                  - Settings
                  - Channels
                  - Channel_id
                description: Delete all order
    overlays:
      - type: APIs.io Search
        url: overlays/orders-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/orders-openapi-api-evangelist-ratings.yml
  - aid: bigcommerce:orders
    name: Orders
    description: Needs a description
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.bigcommerce.com/
    baseURL: https://api.example.com
    tags: []
    properties:
      - type: Documentation
        url: https://developer.bigcommerce.com/
      - type: OpenAPI
        data:
          openapi: 3.0.3
          info:
            title: Orders V3
            version: ''
            license:
              name: ''
          tags:
            - name: Metafields
            - name: Payment Actions
            - name: Transactions
            - name: Order Settings
            - name: Batch metafields
          paths:
            /orders/{order_id}/payment_actions/capture:
              post:
                summary: Capture order payment
                description: >-
                  Capture the payment for an order. When there are no payment
                  method validation issues, the capture process is successful,
                  the `payment_status` updates to `capture pending`, and the
                  payment request is scheduled. The payment request itself
                  occurs asynchronously.

                  Requires at least one of the following scopes:

                  * `store_v2_orders`

                  * `store_v2_transactions`
                tags:
                  - Capture
                  - Order
                  - Payment
                  - Orders
                  - Order_id
                  - Payment_actions
                  - Capture
              parameters:
                - null
                - null
            /orders/{order_id}/payment_actions/void:
              post:
                summary: Void
                description: >-
                  Void the payment for an order. When there are no payment
                  method validation issues, the void process is successful, the
                  `payment_status` updates to `void pending`, and the void
                  payment request is scheduled. The payment request itself
                  occurs asynchronously.


                  Requires at least one of the following scopes:

                  * `store_v2_orders`

                  * `store_v2_transactions`
                tags:
                  - Void
                  - Orders
                  - Order_id
                  - Payment_actions
                  - Capture
                  - Void
              parameters:
                - null
                - null
            /orders/{order_id}/transactions:
              parameters:
                - null
                - null
              get:
                tags:
                  - Get
                  - Transactions
                  - Orders
                  - Order_id
                  - Payment_actions
                  - Capture
                  - Void
                  - Transactions
                description: >-
                  Returns an **orderʼs** transactions.


                  **Usage Notes**

                  * Depending on the payment method, different information will
                  be available (not all payment gateways return full card or
                  fraud detail).



                  Requires at least one of the following scopes:

                  * `store_v2_transactions_read_only`

                  * `store_v2_transactions`
                summary: Get Transactions
            /orders/{order_id}/payment_actions/refund_quotes:
              post:
                summary: Create a Refund Quote
                description: >-
                  Calculate the tax amount, total refund amount and get
                  available payment options for an order refund by providing
                  items and costs or quantities to refund.


                  Requires at least one of the following scopes:

                  * `store_v2_orders`

                  * `store_v2_transactions`


                  **Note:**

                  Order refunds are processed consecutively. Processing
                  synchronous refunds on an order are not yet supported.
                tags:
                  - Create
                  - Refund
                  - Quote
                  - Orders
                  - Order_id
                  - Payment_actions
                  - Capture
                  - Void
                  - Transactions
                  - Refund_quotes
              parameters:
                - null
                - null
            /orders/{order_id}/payment_actions/refunds:
              post:
                summary: Create a Refund
                description: >-
                  Creates a refund. When there are no payment method validation
                  issues, the refund process is successful and the refund
                  payment request is scheduled. The payment request itself
                  occurs asynchronously.


                  Requires at least one of the following scopes:

                  * `store_v2_orders`

                  * `store_v2_transactions`


                  **Note:**

                  Order refunds are processed consecutively. Processing
                  synchronous refunds on an order are not yet supported.
                tags:
                  - Create
                  - Refund
                  - Orders
                  - Order_id
                  - Payment_actions
                  - Capture
                  - Void
                  - Transactions
                  - Refund_quotes
                  - Refunds
              get:
                summary: Get Refunds for Order
                description: >-
                  Returns a list of refunds ordered by refund ID in ascending
                  order for the given order.


                  Requires at least one of the following scopes:

                  * `store_v2_transactions_read_only`

                  * `store_v2_transactions`

                  * `store_v2_orders_read_only`

                  * `store_v2_orders`
                tags:
                  - Get
                  - Refunds
                  - For
                  - Order
                  - Orders
                  - Order_id
                  - Payment_actions
                  - Capture
                  - Void
                  - Transactions
                  - Refund_quotes
                  - Refunds
              parameters:
                - null
                - null
            /orders/payment_actions/refunds/{refund_id}:
              parameters:
                - null
                - null
              get:
                summary: Get a Refund
                description: Returns a refund by refund ID.
                tags:
                  - Get
                  - Refund
                  - Orders
                  - Order_id
                  - Payment_actions
                  - Capture
                  - Void
                  - Transactions
                  - Refund_quotes
                  - Refunds
                  - Refund_id
            /orders/payment_actions/refunds:
              parameters:
                - null
              get:
                summary: Get All Refunds
                description: >-
                  Returns a list of refunds ordered by refund ID in ascending
                  order.


                  Requires at least one of the following scopes:

                  * `store_v2_transactions_read_only`

                  * `store_v2_transactions`

                  * `store_v2_orders_read_only`

                  * `store_v2_orders`
                tags:
                  - Get
                  - All
                  - Refunds
                  - Orders
                  - Order_id
                  - Payment_actions
                  - Capture
                  - Void
                  - Transactions
                  - Refund_quotes
                  - Refunds
                  - Refund_id
            /orders/payment_actions/refund_quotes:
              post:
                summary: Create Refund Quotes - BATCH
                description: >-
                  Calculate the tax amount, total refund amount and get
                  available payment options for an order refund by providing
                  items and costs or quantities to refund.


                  This endpoint will accept a batch of one or more.


                  Requires at least one of the following scopes:

                  * `store_v2_orders`

                  * `store_v2_transactions`
                tags:
                  - Create
                  - Refund
                  - Quotes
                  - Orders
                  - Order_id
                  - Payment_actions
                  - Capture
                  - Void
                  - Transactions
                  - Refund_quotes
                  - Refunds
                  - Refund_id
            /orders/{order_id}/metafields:
              parameters:
                - null
                - null
              get:
                summary: Get Order Metafields
                tags:
                  - Get
                  - Order
                  - Metafields
                  - Orders
                  - Order_id
                  - Payment_actions
                  - Capture
                  - Void
                  - Transactions
                  - Refund_quotes
                  - Refunds
                  - Refund_id
                  - Metafields
                description: >
                  Gets a `Metafield` object list, by `order_id`.


                  The maximum number of metafields allowed on each order,
                  product, category, variant, or brand is 250 per client ID.
              post:
                summary: Create Metafields
                tags:
                  - Create
                  - Metafields
                  - Orders
                  - Order_id
                  - Payment_actions
                  - Capture
                  - Void
                  - Transactions
                  - Refund_quotes
                  - Refunds
                  - Refund_id
                  - Metafields
                description: >-
                  Creates an order `Metafield`.


                  The maximum number of metafields allowed on each order,
                  product, category, variant, or brand is 250 per client ID.
            /orders/{order_id}/metafields/{metafield_id}:
              parameters:
                - null
                - null
                - null
              get:
                summary: Get a Metafield
                tags:
                  - Get
                  - Metafield
                  - Orders
                  - Order_id
                  - Payment_actions
                  - Capture
                  - Void
                  - Transactions
                  - Refund_quotes
                  - Refunds
                  - Refund_id
                  - Metafields
                  - Metafield_id
                description: |
                  Gets a `Metafield`, by `order_id`.
              put:
                summary: Update a Metafield
                tags:
                  - Update
                  - Metafield
                  - Orders
                  - Order_id
                  - Payment_actions
                  - Capture
                  - Void
                  - Transactions
                  - Refund_quotes
                  - Refunds
                  - Refund_id
                  - Metafields
                  - Metafield_id
                description: >-
                  Updates a `Metafield` object.


                  The maxiumum number of metafields allowed on each order,
                  product, category, variant, or brand is 250 per client ID.
              delete:
                summary: Delete a Metafield
                tags:
                  - Delete
                  - Metafield
                  - Orders
                  - Order_id
                  - Payment_actions
                  - Capture
                  - Void
                  - Transactions
                  - Refund_quotes
                  - Refunds
                  - Refund_id
                  - Metafields
                  - Metafield_id
                description: |
                  Deletes a `Metafield`.
            /orders/settings:
              get:
                summary: Get Global Order Settings
                description: Returns global order settings.
                tags:
                  - Get
                  - Global
                  - Order
                  - Settings
                  - Orders
                  - Order_id
                  - Payment_actions
                  - Capture
                  - Void
                  - Transactions
                  - Refund_quotes
                  - Refunds
                  - Refund_id
                  - Metafields
                  - Metafield_id
                  - Settings
              put:
                summary: Update Global Order Settings
                description: Updates global order settings.
                tags:
                  - Update
                  - Global
                  - Order
                  - Settings
                  - Orders
                  - Order_id
                  - Payment_actions
                  - Capture
                  - Void
                  - Transactions
                  - Refund_quotes
                  - Refunds
                  - Refund_id
                  - Metafields
                  - Metafield_id
                  - Settings
              parameters:
                - null
            /orders/settings/channels/{channel_id}:
              get:
                summary: Get Channel Order Settings
                description: Returns order settings for a specific channel.
                tags:
                  - Get
                  - Channel
                  - Order
                  - Settings
                  - Orders
                  - Order_id
                  - Payment_actions
                  - Capture
                  - Void
                  - Transactions
                  - Refund_quotes
                  - Refunds
                  - Refund_id
                  - Metafields
                  - Metafield_id
                  - Settings
                  - Channels
                  - Channel_id
              put:
                summary: Update Channel Order Settings
                description: |-
                  Updates order settings for a specific channel.

                   **Note:** You must override both notifications `email_addresses` or neither, i.e. either both notification `email_addresses` are an array of valid email addresses, or both `email_addresses` must be null. You may not have one set to an array of addresses and the other set to `null`.
                tags:
                  - Update
                  - Channel
                  - Order
                  - Settings
                  - Orders
                  - Order_id
                  - Payment_actions
                  - Capture
                  - Void
                  - Transactions
                  - Refund_quotes
                  - Refunds
                  - Refund_id
                  - Metafields
                  - Metafield_id
                  - Settings
                  - Channels
                  - Channel_id
              parameters:
                - null
                - null
            /orders/metafields:
              get:
                summary: Get All Order Metafields
                tags:
                  - Get
                  - All
                  - Order
                  - Metafields
                  - Orders
                  - Order_id
                  - Payment_actions
                  - Capture
                  - Void
                  - Transactions
                  - Refund_quotes
                  - Refunds
                  - Refund_id
                  - Metafields
                  - Metafield_id
                  - Settings
                  - Channels
                  - Channel_id
                description: Get all order metafields.
              post:
                summary: Create multiple Metafields
                tags:
                  - Create
                  - Multiple
                  - Metafields
                  - Orders
                  - Order_id
                  - Payment_actions
                  - Capture
                  - Void
                  - Transactions
                  - Refund_quotes
                  - Refunds
                  - Refund_id
                  - Metafields
                  - Metafield_id
                  - Settings
                  - Channels
                  - Channel_id
                description: Create multiple metafields.
              put:
                summary: Update multiple Metafields
                tags:
                  - Update
                  - Multiple
                  - Metafields
                  - Orders
                  - Order_id
                  - Payment_actions
                  - Capture
                  - Void
                  - Transactions
                  - Refund_quotes
                  - Refunds
                  - Refund_id
                  - Metafields
                  - Metafield_id
                  - Settings
                  - Channels
                  - Channel_id
                description: Create multiple metafields.
              delete:
                summary: Delete All Metafields
                tags:
                  - Delete
                  - All
                  - Metafields
                  - Orders
                  - Order_id
                  - Payment_actions
                  - Capture
                  - Void
                  - Transactions
                  - Refund_quotes
                  - Refunds
                  - Refund_id
                  - Metafields
                  - Metafield_id
                  - Settings
                  - Channels
                  - Channel_id
                description: Delete all order
    overlays:
      - type: APIs.io Search
        url: overlays/orders-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/orders-openapi-api-evangelist-ratings.yml
  - aid: twilio:twilio-ip-messaging-api
    name: Twilio IP Messaging API
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
            title: Twilio - Ip_messaging
            license:
              name: Apache 2.0
              url: https://www.apache.org/licenses/LICENSE-2.0.html
          openapi: 3.0.1
          paths:
            /v2/Services/{ServiceSid}/Bindings:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Bindings
            /v2/Services/{ServiceSid}/Bindings/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Bindings
              delete:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Bindings
            /v2/Services/{ServiceSid}/Channels/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Bindings
                  - Channels
              delete:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Bindings
                  - Channels
              post:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Bindings
                  - Channels
            /v2/Services/{ServiceSid}/Channels:
              description: 'TODO: Resource-level docs'
              post:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Bindings
                  - Channels
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Bindings
                  - Channels
            /v2/Services/{ServiceSid}/Channels/{ChannelSid}/Webhooks:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Bindings
                  - Channels
                  - Channel
                  - Webhooks
              post:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Bindings
                  - Channels
                  - Channel
                  - Webhooks
            /v2/Services/{ServiceSid}/Channels/{ChannelSid}/Webhooks/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Bindings
                  - Channels
                  - Channel
                  - Webhooks
              post:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Bindings
                  - Channels
                  - Channel
                  - Webhooks
              delete:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Bindings
                  - Channels
                  - Channel
                  - Webhooks
            /v2/Credentials:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Bindings
                  - Channels
                  - Channel
                  - Webhooks
                  - Credentials
              post:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Bindings
                  - Channels
                  - Channel
                  - Webhooks
                  - Credentials
            /v2/Credentials/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Bindings
                  - Channels
                  - Channel
                  - Webhooks
                  - Credentials
              post:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Bindings
                  - Channels
                  - Channel
                  - Webhooks
                  - Credentials
              delete:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Bindings
                  - Channels
                  - Channel
                  - Webhooks
                  - Credentials
            /v2/Services/{ServiceSid}/Channels/{ChannelSid}/Invites/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Bindings
                  - Channels
                  - Channel
                  - Webhooks
                  - Credentials
                  - Invites
              delete:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Bindings
                  - Channels
                  - Channel
                  - Webhooks
                  - Credentials
                  - Invites
            /v2/Services/{ServiceSid}/Channels/{ChannelSid}/Invites:
              description: 'TODO: Resource-level docs'
              post:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Bindings
                  - Channels
                  - Channel
                  - Webhooks
                  - Credentials
                  - Invites
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Bindings
                  - Channels
                  - Channel
                  - Webhooks
                  - Credentials
                  - Invites
            /v2/Services/{ServiceSid}/Channels/{ChannelSid}/Members/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Bindings
                  - Channels
                  - Channel
                  - Webhooks
                  - Credentials
                  - Invites
                  - Members
              delete:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Bindings
                  - Channels
                  - Channel
                  - Webhooks
                  - Credentials
                  - Invites
                  - Members
              post:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Bindings
                  - Channels
                  - Channel
                  - Webhooks
                  - Credentials
                  - Invites
                  - Members
            /v2/Services/{ServiceSid}/Channels/{ChannelSid}/Members:
              description: 'TODO: Resource-level docs'
              post:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Bindings
                  - Channels
                  - Channel
                  - Webhooks
                  - Credentials
                  - Invites
                  - Members
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Bindings
                  - Channels
                  - Channel
                  - Webhooks
                  - Credentials
                  - Invites
                  - Members
            /v2/Services/{ServiceSid}/Channels/{ChannelSid}/Messages/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Bindings
                  - Channels
                  - Channel
                  - Webhooks
                  - Credentials
                  - Invites
                  - Members
                  - Messages
              delete:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Bindings
                  - Channels
                  - Channel
                  - Webhooks
                  - Credentials
                  - Invites
                  - Members
                  - Messages
              post:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Bindings
                  - Channels
                  - Channel
                  - Webhooks
                  - Credentials
                  - Invites
                  - Members
                  - Messages
            /v2/Services/{ServiceSid}/Channels/{ChannelSid}/Messages:
              description: 'TODO: Resource-level docs'
              post:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Bindings
                  - Channels
                  - Channel
                  - Webhooks
                  - Credentials
                  - Invites
                  - Members
                  - Messages
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Bindings
                  - Channels
                  - Channel
                  - Webhooks
                  - Credentials
                  - Invites
                  - Members
                  - Messages
            /v2/Services/{ServiceSid}/Roles/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Bindings
                  - Channels
                  - Channel
                  - Webhooks
                  - Credentials
                  - Invites
                  - Members
                  - Messages
                  - Roles
              delete:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Bindings
                  - Channels
                  - Channel
                  - Webhooks
                  - Credentials
                  - Invites
                  - Members
                  - Messages
                  - Roles
              post:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Bindings
                  - Channels
                  - Channel
                  - Webhooks
                  - Credentials
                  - Invites
                  - Members
                  - Messages
                  - Roles
            /v2/Services/{ServiceSid}/Roles:
              description: 'TODO: Resource-level docs'
              post:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Bindings
                  - Channels
                  - Channel
                  - Webhooks
                  - Credentials
                  - Invites
                  - Members
                  - Messages
                  - Roles
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Bindings
                  - Channels
                  - Channel
                  - Webhooks
                  - Credentials
                  - Invites
                  - Members
                  - Messages
                  - Roles
            /v2/Services/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Bindings
                  - Channels
                  - Channel
                  - Webhooks
                  - Credentials
                  - Invites
                  - Members
                  - Messages
                  - Roles
              delete:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Bindings
                  - Channels
                  - Channel
                  - Webhooks
                  - Credentials
                  - Invites
                  - Members
                  - Messages
                  - Roles
              post:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Bindings
                  - Channels
                  - Channel
                  - Webhooks
                  - Credentials
                  - Invites
                  - Members
                  - Messages
                  - Roles
            /v2/Services:
              description: 'TODO: Resource-level docs'
              post:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Bindings
                  - Channels
                  - Channel
                  - Webhooks
                  - Credentials
                  - Invites
                  - Members
                  - Messages
                  - Roles
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Bindings
                  - Channels
                  - Channel
                  - Webhooks
                  - Credentials
                  - Invites
                  - Members
                  - Messages
                  - Roles
            /v2/Services/{ServiceSid}/Users/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Bindings
                  - Channels
                  - Channel
                  - Webhooks
                  - Credentials
                  - Invites
                  - Members
                  - Messages
                  - Roles
                  - Users
              delete:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Bindings
                  - Channels
                  - Channel
                  - Webhooks
                  - Credentials
                  - Invites
                  - Members
                  - Messages
                  - Roles
                  - Users
              post:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Bindings
                  - Channels
                  - Channel
                  - Webhooks
                  - Credentials
                  - Invites
                  - Members
                  - Messages
                  - Roles
                  - Users
            /v2/Services/{ServiceSid}/Users:
              description: 'TODO: Resource-level docs'
              post:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Bindings
                  - Channels
                  - Channel
                  - Webhooks
                  - Credentials
                  - Invites
                  - Members
                  - Messages
                  - Roles
                  - Users
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Bindings
                  - Channels
                  - Channel
                  - Webhooks
                  - Credentials
                  - Invites
                  - Members
                  - Messages
                  - Roles
                  - Users
            /v2/Services/{ServiceSid}/Users/{UserSid}/Bindings:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Bindings
                  - Channels
                  - Channel
                  - Webhooks
                  - Credentials
                  - Invites
                  - Members
                  - Messages
                  - Roles
                  - Users
                  - User
            /v2/Services/{ServiceSid}/Users/{UserSid}/Bindings/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Bindings
                  - Channels
                  - Channel
                  - Webhooks
                  - Credentials
                  - Invites
                  - Members
                  - Messages
                  - Roles
                  - Users
                  - User
              delete:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Bindings
                  - Channels
                  - Channel
                  - Webhooks
                  - Credentials
                  - Invites
                  - Members
                  - Messages
                  - Roles
                  - Users
                  - User
            /v2/Services/{ServiceSid}/Users/{UserSid}/Channels:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Bindings
                  - Channels
                  - Channel
                  - Webhooks
                  - Credentials
                  - Invites
                  - Members
                  - Messages
                  - Roles
                  - Users
                  - User
            /v2/Services/{ServiceSid}/Users/{UserSid}/Channels/{ChannelSid}:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Bindings
                  - Channels
                  - Channel
                  - Webhooks
                  - Credentials
                  - Invites
                  - Members
                  - Messages
                  - Roles
                  - Users
                  - User
              delete:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Bindings
                  - Channels
                  - Channel
                  - Webhooks
                  - Credentials
                  - Invites
                  - Members
                  - Messages
                  - Roles
                  - Users
                  - User
              post:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Bindings
                  - Channels
                  - Channel
                  - Webhooks
                  - Credentials
                  - Invites
                  - Members
                  - Messages
                  - Roles
                  - Users
                  - User
          tags:
            - name: IpMessagingV2Binding
            - name: IpMessagingV2Channel
            - name: IpMessagingV2Credential
            - name: IpMessagingV2Invite
            - name: IpMessagingV2Member
            - name: IpMessagingV2Message
            - name: IpMessagingV2Role
            - name: IpMessagingV2Service
            - name: IpMessagingV2User
            - name: IpMessagingV2UserBinding
            - name: IpMessagingV2UserChannel
            - name: IpMessagingV2Webhook
          x-maturity:
            - name: GA
              description: This product is G
    overlays:
      - type: APIs.io Search
        url: overlays/ip-message-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/ip-message-openapi-api-evangelist-ratings.yml
  - aid: twilio:twilio-task-router-api
    name: Twilio Task Router API
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
            title: Twilio - Taskrouter
            license:
              name: Apache 2.0
              url: https://www.apache.org/licenses/LICENSE-2.0.html
          openapi: 3.0.1
          paths:
            /v1/Workspaces/{WorkspaceSid}/Activities/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Workspaces
                  - Workspace
                  - Sid
                  - Activities
              post:
                description: ''
                tags:
                  - Workspaces
                  - Workspace
                  - Sid
                  - Activities
              delete:
                description: ''
                tags:
                  - Workspaces
                  - Workspace
                  - Sid
                  - Activities
            /v1/Workspaces/{WorkspaceSid}/Activities:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Workspaces
                  - Workspace
                  - Sid
                  - Activities
              post:
                description: ''
                tags:
                  - Workspaces
                  - Workspace
                  - Sid
                  - Activities
            /v1/Workspaces/{WorkspaceSid}/Events/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Workspaces
                  - Workspace
                  - Sid
                  - Activities
                  - Events
            /v1/Workspaces/{WorkspaceSid}/Events:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Workspaces
                  - Workspace
                  - Sid
                  - Activities
                  - Events
            /v1/Workspaces/{WorkspaceSid}/Tasks/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Workspaces
                  - Workspace
                  - Sid
                  - Activities
                  - Events
                  - Tasks
              post:
                description: ''
                tags:
                  - Workspaces
                  - Workspace
                  - Sid
                  - Activities
                  - Events
                  - Tasks
              delete:
                description: ''
                tags:
                  - Workspaces
                  - Workspace
                  - Sid
                  - Activities
                  - Events
                  - Tasks
            /v1/Workspaces/{WorkspaceSid}/Tasks:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Workspaces
                  - Workspace
                  - Sid
                  - Activities
                  - Events
                  - Tasks
              post:
                description: ''
                tags:
                  - Workspaces
                  - Workspace
                  - Sid
                  - Activities
                  - Events
                  - Tasks
            /v1/Workspaces/{WorkspaceSid}/TaskChannels/{Sid}:
              description: Types of tasks
              get:
                description: ''
                tags:
                  - Workspaces
                  - Workspace
                  - Sid
                  - Activities
                  - Events
                  - Tasks
                  - Task
                  - Channels
              post:
                description: ''
                tags:
                  - Workspaces
                  - Workspace
                  - Sid
                  - Activities
                  - Events
                  - Tasks
                  - Task
                  - Channels
              delete:
                description: ''
                tags:
                  - Workspaces
                  - Workspace
                  - Sid
                  - Activities
                  - Events
                  - Tasks
                  - Task
                  - Channels
            /v1/Workspaces/{WorkspaceSid}/TaskChannels:
              description: Types of tasks
              get:
                description: ''
                tags:
                  - Workspaces
                  - Workspace
                  - Sid
                  - Activities
                  - Events
                  - Tasks
                  - Task
                  - Channels
              post:
                description: ''
                tags:
                  - Workspaces
                  - Workspace
                  - Sid
                  - Activities
                  - Events
                  - Tasks
                  - Task
                  - Channels
            /v1/Workspaces/{WorkspaceSid}/TaskQueues/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Workspaces
                  - Workspace
                  - Sid
                  - Activities
                  - Events
                  - Tasks
                  - Task
                  - Channels
                  - Queues
              post:
                description: ''
                tags:
                  - Workspaces
                  - Workspace
                  - Sid
                  - Activities
                  - Events
                  - Tasks
                  - Task
                  - Channels
                  - Queues
              delete:
                description: ''
                tags:
                  - Workspaces
                  - Workspace
                  - Sid
                  - Activities
                  - Events
                  - Tasks
                  - Task
                  - Channels
                  - Queues
            /v1/Workspaces/{WorkspaceSid}/TaskQueues:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Workspaces
                  - Workspace
                  - Sid
                  - Activities
                  - Events
                  - Tasks
                  - Task
                  - Channels
                  - Queues
              post:
                description: ''
                tags:
                  - Workspaces
                  - Workspace
                  - Sid
                  - Activities
                  - Events
                  - Tasks
                  - Task
                  - Channels
                  - Queues
            /v1/Workspaces/{WorkspaceSid}/TaskQueues/RealTimeStatistics:
              description: 'TODO: Resource-level docs'
            /v1/Workspaces/{WorkspaceSid}/TaskQueues/{TaskQueueSid}/CumulativeStatistics:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Workspaces
                  - Workspace
                  - Sid
                  - Activities
                  - Events
                  - Tasks
                  - Task
                  - Channels
                  - Queues
                  - Real
                  - Time
                  - Statistics
                  - Queue
                  - Cumulative
            /v1/Workspaces/{WorkspaceSid}/TaskQueues/{TaskQueueSid}/RealTimeStatistics:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Workspaces
                  - Workspace
                  - Sid
                  - Activities
                  - Events
                  - Tasks
                  - Task
                  - Channels
                  - Queues
                  - Real
                  - Time
                  - Statistics
                  - Queue
                  - Cumulative
            /v1/Workspaces/{WorkspaceSid}/TaskQueues/{TaskQueueSid}/Statistics:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Workspaces
                  - Workspace
                  - Sid
                  - Activities
                  - Events
                  - Tasks
                  - Task
                  - Channels
                  - Queues
                  - Real
                  - Time
                  - Statistics
                  - Queue
                  - Cumulative
            /v1/Workspaces/{WorkspaceSid}/TaskQueues/Statistics:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Workspaces
                  - Workspace
                  - Sid
                  - Activities
                  - Events
                  - Tasks
                  - Task
                  - Channels
                  - Queues
                  - Real
                  - Time
                  - Statistics
                  - Queue
                  - Cumulative
            /v1/Workspaces/{WorkspaceSid}/Tasks/{TaskSid}/Reservations:
              description: Tasks reserved for workers
              get:
                description: ''
                tags:
                  - Workspaces
                  - Workspace
                  - Sid
                  - Activities
                  - Events
                  - Tasks
                  - Task
                  - Channels
                  - Queues
                  - Real
                  - Time
                  - Statistics
                  - Queue
                  - Cumulative
                  - Reservations
            /v1/Workspaces/{WorkspaceSid}/Tasks/{TaskSid}/Reservations/{Sid}:
              description: Tasks reserved for workers
              get:
                description: ''
                tags:
                  - Workspaces
                  - Workspace
                  - Sid
                  - Activities
                  - Events
                  - Tasks
                  - Task
                  - Channels
                  - Queues
                  - Real
                  - Time
                  - Statistics
                  - Queue
                  - Cumulative
                  - Reservations
              post:
                description: ''
                tags:
                  - Workspaces
                  - Workspace
                  - Sid
                  - Activities
                  - Events
                  - Tasks
                  - Task
                  - Channels
                  - Queues
                  - Real
                  - Time
                  - Statistics
                  - Queue
                  - Cumulative
                  - Reservations
            /v1/Workspaces/{WorkspaceSid}/Workers:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Workspaces
                  - Workspace
                  - Sid
                  - Activities
                  - Events
                  - Tasks
                  - Task
                  - Channels
                  - Queues
                  - Real
                  - Time
                  - Statistics
                  - Queue
                  - Cumulative
                  - Reservations
                  - Workers
              post:
                description: ''
                tags:
                  - Workspaces
                  - Workspace
                  - Sid
                  - Activities
                  - Events
                  - Tasks
                  - Task
                  - Channels
                  - Queues
                  - Real
                  - Time
                  - Statistics
                  - Queue
                  - Cumulative
                  - Reservations
                  - Workers
            /v1/Workspaces/{WorkspaceSid}/Workers/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Workspaces
                  - Workspace
                  - Sid
                  - Activities
                  - Events
                  - Tasks
                  - Task
                  - Channels
                  - Queues
                  - Real
                  - Time
                  - Statistics
                  - Queue
                  - Cumulative
                  - Reservations
                  - Workers
              post:
                description: ''
                tags:
                  - Workspaces
                  - Workspace
                  - Sid
                  - Activities
                  - Events
                  - Tasks
                  - Task
                  - Channels
                  - Queues
                  - Real
                  - Time
                  - Statistics
                  - Queue
                  - Cumulative
                  - Reservations
                  - Workers
              delete:
                description: ''
                tags:
                  - Workspaces
                  - Workspace
                  - Sid
                  - Activities
                  - Events
                  - Tasks
                  - Task
                  - Channels
                  - Queues
                  - Real
                  - Time
                  - Statistics
                  - Queue
                  - Cumulative
                  - Reservations
                  - Workers
            /v1/Workspaces/{WorkspaceSid}/Workers/{WorkerSid}/Channels:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Workspaces
                  - Workspace
                  - Sid
                  - Activities
                  - Events
                  - Tasks
                  - Task
                  - Channels
                  - Queues
                  - Real
                  - Time
                  - Statistics
                  - Queue
                  - Cumulative
                  - Reservations
                  - Workers
                  - Worker
            /v1/Workspaces/{WorkspaceSid}/Workers/{WorkerSid}/Channels/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Workspaces
                  - Workspace
                  - Sid
                  - Activities
                  - Events
                  - Tasks
                  - Task
                  - Channels
                  - Queues
                  - Real
                  - Time
                  - Statistics
                  - Queue
                  - Cumulative
                  - Reservations
                  - Workers
                  - Worker
              post:
                description: ''
                tags:
                  - Workspaces
                  - Workspace
                  - Sid
                  - Activities
                  - Events
                  - Tasks
                  - Task
                  - Channels
                  - Queues
                  - Real
                  - Time
                  - Statistics
                  - Queue
                  - Cumulative
                  - Reservations
                  - Workers
                  - Worker
            /v1/Workspaces/{WorkspaceSid}/Workers/{WorkerSid}/Statistics:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Workspaces
                  - Workspace
                  - Sid
                  - Activities
                  - Events
                  - Tasks
                  - Task
                  - Channels
                  - Queues
                  - Real
                  - Time
                  - Statistics
                  - Queue
                  - Cumulative
                  - Reservations
                  - Workers
                  - Worker
            /v1/Workspaces/{WorkspaceSid}/Workers/{WorkerSid}/Reservations:
              description: Current and past reservations for a worker
              get:
                description: ''
                tags:
                  - Workspaces
                  - Workspace
                  - Sid
                  - Activities
                  - Events
                  - Tasks
                  - Task
                  - Channels
                  - Queues
                  - Real
                  - Time
                  - Statistics
                  - Queue
                  - Cumulative
                  - Reservations
                  - Workers
                  - Worker
            /v1/Workspaces/{WorkspaceSid}/Workers/{WorkerSid}/Reservations/{Sid}:
              description: Current and past reservations for a worker
              get:
                description: ''
                tags:
                  - Workspaces
                  - Workspace
                  - Sid
                  - Activities
                  - Events
                  - Tasks
                  - Task
                  - Channels
                  - Queues
                  - Real
                  - Time
                  - Statistics
                  - Queue
                  - Cumulative
                  - Reservations
                  - Workers
                  - Worker
              post:
                description: ''
                tags:
                  - Workspaces
                  - Workspace
                  - Sid
                  - Activities
                  - Events
                  - Tasks
                  - Task
                  - Channels
                  - Queues
                  - Real
                  - Time
                  - Statistics
                  - Queue
                  - Cumulative
                  - Reservations
                  - Workers
                  - Worker
            /v1/Workspaces/{WorkspaceSid}/Workers/Statistics:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Workspaces
                  - Workspace
                  - Sid
                  - Activities
                  - Events
                  - Tasks
                  - Task
                  - Channels
                  - Queues
                  - Real
                  - Time
                  - Statistics
                  - Queue
                  - Cumulative
                  - Reservations
                  - Workers
                  - Worker
            /v1/Workspaces/{WorkspaceSid}/Workers/CumulativeStatistics:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Workspaces
                  - Workspace
                  - Sid
                  - Activities
                  - Events
                  - Tasks
                  - Task
                  - Channels
                  - Queues
                  - Real
                  - Time
                  - Statistics
                  - Queue
                  - Cumulative
                  - Reservations
                  - Workers
                  - Worker
            /v1/Workspaces/{WorkspaceSid}/Workers/RealTimeStatistics:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Workspaces
                  - Workspace
                  - Sid
                  - Activities
                  - Events
                  - Tasks
                  - Task
                  - Channels
                  - Queues
                  - Real
                  - Time
                  - Statistics
                  - Queue
                  - Cumulative
                  - Reservations
                  - Workers
                  - Worker
            /v1/Workspaces/{WorkspaceSid}/Workflows/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Workspaces
                  - Workspace
                  - Sid
                  - Activities
                  - Events
                  - Tasks
                  - Task
                  - Channels
                  - Queues
                  - Real
                  - Time
                  - Statistics
                  - Queue
                  - Cumulative
                  - Reservations
                  - Workers
                  - Worker
                  - Workflows
              post:
                description: ''
                tags:
                  - Workspaces
                  - Workspace
                  - Sid
                  - Activities
                  - Events
                  - Tasks
                  - Task
                  - Channels
                  - Queues
                  - Real
                  - Time
                  - Statistics
                  - Queue
                  - Cumulative
                  - Reservations
                  - Workers
                  - Worker
                  - Workflows
              delete:
                description: ''
                tags:
                  - Workspaces
                  - Workspace
                  - Sid
                  - Activities
                  - Events
                  - Tasks
                  - Task
                  - Channels
                  - Queues
                  - Real
                  - Time
                  - Statistics
                  - Queue
                  - Cumulative
                  - Reservations
                  - Workers
                  - Worker
                  - Workflows
            /v1/Workspaces/{WorkspaceSid}/Workflows:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Workspaces
                  - Workspace
                  - Sid
                  - Activities
                  - Events
                  - Tasks
                  - Task
                  - Channels
                  - Queues
                  - Real
                  - Time
                  - Statistics
                  - Queue
                  - Cumulative
                  - Reservations
                  - Workers
                  - Worker
                  - Workflows
              post:
                description: ''
                tags:
                  - Workspaces
                  - Workspace
                  - Sid
                  - Activities
                  - Events
                  - Tasks
                  - Task
                  - Channels
                  - Queues
                  - Real
                  - Time
                  - Statistics
                  - Queue
                  - Cumulative
                  - Reservations
                  - Workers
                  - Worker
                  - Workflows
            /v1/Workspaces/{WorkspaceSid}/Workflows/{WorkflowSid}/CumulativeStatistics:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Workspaces
                  - Workspace
                  - Sid
                  - Activities
                  - Events
                  - Tasks
                  - Task
                  - Channels
                  - Queues
                  - Real
                  - Time
                  - Statistics
                  - Queue
                  - Cumulative
                  - Reservations
                  - Workers
                  - Worker
                  - Workflows
                  - Workflow
            /v1/Workspaces/{WorkspaceSid}/Workflows/{WorkflowSid}/RealTimeStatistics:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Workspaces
                  - Workspace
                  - Sid
                  - Activities
                  - Events
                  - Tasks
                  - Task
                  - Channels
                  - Queues
                  - Real
                  - Time
                  - Statistics
                  - Queue
                  - Cumulative
                  - Reservations
                  - Workers
                  - Worker
                  - Workflows
                  - Workflow
            /v1/Workspaces/{WorkspaceSid}/Workflows/{WorkflowSid}/Statistics:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Workspaces
                  - Workspace
                  - Sid
                  - Activities
                  - Events
                  - Tasks
                  - Task
                  - Channels
                  - Queues
                  - Real
                  - Time
                  - Statistics
                  - Queue
                  - Cumulative
                  - Reservations
                  - Workers
                  - Worker
                  - Workflows
                  - Workflow
            /v1/Workspaces/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Workspaces
                  - Workspace
                  - Sid
                  - Activities
                  - Events
                  - Tasks
                  - Task
                  - Channels
                  - Queues
                  - Real
                  - Time
                  - Statistics
                  - Queue
                  - Cumulative
                  - Reservations
                  - Workers
                  - Worker
                  - Workflows
                  - Workflow
              post:
                description: ''
                tags:
                  - Workspaces
                  - Workspace
                  - Sid
                  - Activities
                  - Events
                  - Tasks
                  - Task
                  - Channels
                  - Queues
                  - Real
                  - Time
                  - Statistics
                  - Queue
                  - Cumulative
                  - Reservations
                  - Workers
                  - Worker
                  - Workflows
                  - Workflow
              delete:
                description: ''
                tags:
                  - Workspaces
                  - Workspace
                  - Sid
                  - Activities
                  - Events
                  - Tasks
                  - Task
                  - Channels
                  - Queues
                  - Real
                  - Time
                  - Statistics
                  - Queue
                  - Cumulative
                  - Reservations
                  - Workers
                  - Worker
                  - Workflows
                  - Workflow
            /v1/Workspaces:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Workspaces
                  - Workspace
                  - Sid
                  - Activities
                  - Events
                  - Tasks
                  - Task
                  - Channels
                  - Queues
                  - Real
                  - Time
                  - Statistics
                  - Queue
                  - Cumulative
                  - Reservations
                  - Workers
                  - Worker
                  - Workflows
                  - Workflow
              post:
                description: ''
                tags:
                  - Workspaces
                  - Workspace
                  - Sid
                  - Activities
                  - Events
                  - Tasks
                  - Task
                  - Channels
                  - Queues
                  - Real
                  - Time
                  - Statistics
                  - Queue
                  - Cumulative
                  - Reservations
                  - Workers
                  - Worker
                  - Workflows
                  - Workflow
            /v1/Workspaces/{WorkspaceSid}/CumulativeStatistics:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Workspaces
                  - Workspace
                  - Sid
                  - Activities
                  - Events
                  - Tasks
                  - Task
                  - Channels
                  - Queues
                  - Real
                  - Time
                  - Statistics
                  - Queue
                  - Cumulative
                  - Reservations
                  - Workers
                  - Worker
                  - Workflows
                  - Workflow
            /v1/Workspaces/{WorkspaceSid}/RealTimeStatistics:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Workspaces
                  - Workspace
                  - Sid
                  - Activities
                  - Events
                  - Tasks
                  - Task
                  - Channels
                  - Queues
                  - Real
                  - Time
                  - Statistics
                  - Queue
                  - Cumulative
                  - Reservations
                  - Workers
                  - Worker
                  - Workflows
                  - Workflow
            /v1/Workspaces/{WorkspaceSid}/Statistics:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Workspaces
                  - Workspace
                  - Sid
                  - Activities
                  - Events
                  - Tasks
                  - Task
                  - Channels
                  - Queues
                  - Real
                  - Time
                  - Statistics
                  - Queue
                  - Cumulative
                  - Reservations
                  - Workers
                  - Worker
                  - Workflows
                  - Workflow
          tags:
            - name: TaskrouterV1Activity
            - name: TaskrouterV1Event
            - name: TaskrouterV1Reservation
            - name: TaskrouterV1Task
            - name: TaskrouterV1TaskChannel
            - name: TaskrouterV1TaskQueue
            - name: TaskrouterV1TaskQueueCumulativeStatistics
            - name: TaskrouterV1TaskQueueRealTimeStatistics
            - name: TaskrouterV1TaskQueueStatistics
            - name: TaskrouterV1TaskQueuesStatistics
            - name: TaskrouterV1Worker
            - name: TaskrouterV1WorkerChannel
            - name: TaskrouterV1WorkerStatistics
            - name: TaskrouterV1WorkersCumulativeStatistics
            - name: TaskrouterV1WorkersRealTimeStatistics
            - name: TaskrouterV1WorkersStatistics
            - name: TaskrouterV1Workflow
            - name: TaskrouterV1WorkflowCumulativeStatistics
            - name: TaskrouterV1WorkflowRealTimeStatistics
            - name: TaskrouterV1WorkflowStatistics
            - name: TaskrouterV1Workspace
            - name: TaskrouterV1WorkspaceCumulativeStatistics
            - name: TaskrouterV1WorkspaceRealTimeStatistics
            - name: TaskrouterV1WorkspaceStatistics
          x-maturity:
            - name: GA
              description: This product is G
    overlays:
      - type: APIs.io Search
        url: overlays/task-router-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/task-router-openapi-api-evangelist-ratings.yml
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---