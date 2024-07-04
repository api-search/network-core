---
name: Bots
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/bots.png
url: https://example.com/apis/bots.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Bots
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
  - name: chime-sdk-identity
    description: >-
      <p>The Amazon Chime SDK Identity APIs in this section allow software
      developers to create and manage unique instances of their messaging
      applications. These APIs provide the overarching framework for creating
      and sending messages. For more information about the identity APIs, refer
      to <a
      href="https://docs.aws.amazon.com/chime/latest/APIReference/API_Operations_Amazon_Chime_SDK_Identity.html">Amazon
      Chime SDK identity</a>.</p>
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
            title: chime-sdk-identity
          paths:
            /app-instances:
              GET:
                summary: ListAppInstances
                description: >-
                  <p>Lists all Amazon Chime <code>AppInstance</code>s created
                  under a single AWS account.</p>
                tags:
                  - Lists
                  - Applications
                  - Instances
                  - Applications
                  - Instances
            /app-instances/{appInstanceArn}/admins:
              GET:
                summary: ListAppInstanceAdmins
                description: >-
                  <p>Returns a list of the administrators in the
                  <code>AppInstance</code>.</p>
                tags:
                  - Lists
                  - Applications
                  - Instances
                  - Administrator
                  - Applications
                  - Instances
                  - Instances
                  - ARN
                  - Administrator
            /app-instance-bots:
              GET:
                summary: ListAppInstanceBots
                description: >-
                  <p>Lists all <code>AppInstanceBots</code> created under a
                  single <code>AppInstance</code>.</p>
                tags:
                  - Lists
                  - Applications
                  - Instances
                  - Bots
                  - Applications
                  - Instances
                  - Instances
                  - ARN
                  - Administrator
                  - Bots
            /app-instance-users:
              GET:
                summary: ListAppInstanceUsers
                description: >-
                  <p>List all <code>AppInstanceUsers</code> created under a
                  single <code>AppInstance</code>.</p>
                tags:
                  - Lists
                  - Applications
                  - Instances
                  - Users
                  - Applications
                  - Instances
                  - Instances
                  - ARN
                  - Administrator
                  - Bots
                  - Users
            /app-instances/{appInstanceArn}:
              PUT:
                summary: UpdateAppInstance
                description: <p>Updates <code>AppInstance</code> metadata.</p>
                tags:
                  - Update
                  - Applications
                  - Instances
                  - Applications
                  - Instances
                  - Instances
                  - ARN
                  - Administrator
                  - Bots
                  - Users
            /app-instances/{appInstanceArn}/admins/{appInstanceAdminArn}:
              GET:
                summary: DescribeAppInstanceAdmin
                description: >-
                  <p>Returns the full details of an
                  <code>AppInstanceAdmin</code>.</p>
                tags:
                  - Describe
                  - Applications
                  - Instances
                  - Administrative
                  - Applications
                  - Instances
                  - Instances
                  - ARN
                  - Administrator
                  - Bots
                  - Users
                  - Administrative
            /app-instance-bots/{appInstanceBotArn}:
              PUT:
                summary: UpdateAppInstanceBot
                description: >-
                  <p>Updates the name and metadata of an
                  <code>AppInstanceBot</code>.</p>
                tags:
                  - Update
                  - Applications
                  - Instances
                  - Bot
                  - Applications
                  - Instances
                  - Instances
                  - ARN
                  - Administrator
                  - Bots
                  - Users
                  - Administrative
                  - Bot
            /app-instance-users/{appInstanceUserArn}:
              PUT:
                summary: UpdateAppInstanceUser
                description: >-
                  <p>Updates the details of an <code>AppInstanceUser</code>. You
                  can update names and metadata.</p>
                tags:
                  - Update
                  - Applications
                  - Instances
                  - Users
                  - Applications
                  - Instances
                  - Instances
                  - ARN
                  - Administrator
                  - Bots
                  - Users
                  - Administrative
                  - Bot
                  - Users
            /app-instance-users/{appInstanceUserArn}/endpoints/{endpointId}:
              PUT:
                summary: UpdateAppInstanceUserEndpoint
                description: >-
                  <p>Updates the details of an
                  <code>AppInstanceUserEndpoint</code>. You can update the name
                  and <code>AllowMessage</code> values.</p>
                tags:
                  - Update
                  - Applications
                  - Instances
                  - Users
                  - Endpoints
                  - Applications
                  - Instances
                  - Instances
                  - ARN
                  - Administrator
                  - Bots
                  - Users
                  - Administrative
                  - Bot
                  - Users
                  - Endpoints
                  - Endpoints
                  - Identifiers
            /app-instances/{appInstanceArn}/retention-settings:
              PUT:
                summary: PutAppInstanceRetentionSettings
                description: >-
                  <p>Sets the amount of time in days that a given
                  <code>AppInstance</code> retains data.</p>
                tags:
                  - Put
                  - Applications
                  - Instances
                  - Retention
                  - Settings
                  - Applications
                  - Instances
                  - Instances
                  - ARN
                  - Administrator
                  - Bots
                  - Users
                  - Administrative
                  - Bot
                  - Users
                  - Endpoints
                  - Endpoints
                  - Identifiers
                  - Retention
                  - Settings
            /app-instance-users/{appInstanceUserArn}/endpoints:
              POST:
                summary: RegisterAppInstanceUserEndpoint
                description: >-
                  <p>Registers an endpoint under an Amazon Chime
                  <code>AppInstanceUser</code>. The endpoint receives messages
                  for a user. For push notifications, the endpoint is a mobile
                  device used to receive mobile push notifications for a
                  user.</p>
                tags:
                  - Register
                  - Applications
                  - Instances
                  - Users
                  - Endpoints
                  - Applications
                  - Instances
                  - Instances
                  - ARN
                  - Administrator
                  - Bots
                  - Users
                  - Administrative
                  - Bot
                  - Users
                  - Endpoints
                  - Endpoints
                  - Identifiers
                  - Retention
                  - Settings
            /tags:
              GET:
                summary: ListTagsForResource
                description: >-
                  <p>Lists the tags applied to an Amazon Chime SDK identity
                  resource.</p>
                tags:
                  - Lists
                  - Tags
                  - For
                  - Resources
                  - Applications
                  - Instances
                  - Instances
                  - ARN
                  - Administrator
                  - Bots
                  - Users
                  - Administrative
                  - Bot
                  - Users
                  - Endpoints
                  - Endpoints
                  - Identifiers
                  - Retention
                  - Settings
                  - Tags
            /app-instance-users/{appInstanceUserArn}/expiration-settings:
              PUT:
                summary: PutAppInstanceUserExpirationSettings
                description: >-
                  <p>Sets the number of days before the
                  <code>AppInstanceUser</code> is automatically deleted.</p>
                  <note> <p>A background process deletes expired
                  <code>AppInstanceUsers</code> within 6 hours of expiration.
                  Actual deletion times may vary.</p> <p>Expired
                  <code>AppInstanceUsers</code> that have not yet been deleted
                  appear as active, and you can update their expiration
                  settings. The system honors the new settings.</p> </note>
                tags:
                  - Put
                  - Applications
                  - Instances
                  - Users
                  - Expiration
                  - Settings
                  - Applications
                  - Instances
                  - Instances
                  - ARN
                  - Administrator
                  - Bots
                  - Users
                  - Administrative
                  - Bot
                  - Users
                  - Endpoints
                  - Endpoints
                  - Identifiers
                  - Retention
                  - Settings
                  - Tags
                  - Expiration
            /tags?operation=tag-resource:
              POST:
                summary: TagResource
                description: >-
                  <p>Applies the specified tags to the specified Amazon Chime
                  SDK identity resource.</p>
                tags:
                  - Tags
                  - Resources
                  - Applications
                  - Instances
                  - Instances
                  - ARN
                  - Administrator
                  - Bots
                  - Users
                  - Administrative
                  - Bot
                  - Users
                  - Endpoints
                  - Endpoints
                  - Identifiers
                  - Retention
                  - Settings
                  - Tags
                  - Expiration
                  - Tags
                  - Resources
            /tags?operation=untag-resource:
              POST:
                summary: UntagResource
                description: >-
                  <p>Removes the specified tags from the specified Amazon Chime
                  SDK identity res
                tags:
                  - Untag
                  - Resources
                  - Applications
                  - Instances
                  - Instances
                  - ARN
                  - Administrator
                  - Bots
                  - Users
                  - Administrative
                  - Bot
                  - Users
                  - Endpoints
                  - Endpoints
                  - Identifiers
                  - Retention
                  - Settings
                  - Tags
                  - Expiration
                  - Tags
                  - Resources
                  - Tags
    overlays:
      - type: APIs.io Search
        url: overlays/chime-sdk-identity-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/chime-sdk-identity-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:chime-sdk-identity
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
  - name: models.lex.v2
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
            title: models.lex.v2
          paths:
            /bots/{botId}/botversions/{botVersion}/botlocales/{localeId}/customvocabulary/DEFAULT/batchcreate:
              PUT:
                summary: BatchCreateCustomVocabularyItem
                description: >-
                  <p>Create a batch of custom vocabulary items for a given bot
                  locale's custom vocabulary.</p>
                tags:
                  - Batches
                  - Create
                  - Custom
                  - Vocabularies
                  - Items
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
            /bots/{botId}/botversions/{botVersion}/botlocales/{localeId}/customvocabulary/DEFAULT/batchdelete:
              POST:
                summary: BatchDeleteCustomVocabularyItem
                description: >-
                  <p>Delete a batch of custom vocabulary items for a given bot
                  locale's custom vocabulary.</p>
                tags:
                  - Batches
                  - Delete
                  - Custom
                  - Vocabularies
                  - Items
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
            /bots/{botId}/botversions/{botVersion}/botlocales/{localeId}/customvocabulary/DEFAULT/batchupdate:
              PUT:
                summary: BatchUpdateCustomVocabularyItem
                description: >-
                  <p>Update a batch of custom vocabulary items for a given bot
                  locale's custom vocabulary.</p>
                tags:
                  - Batches
                  - Update
                  - Custom
                  - Vocabularies
                  - Items
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
            /bots/{botId}/botversions/{botVersion}/botlocales/{localeId}/:
              PUT:
                summary: UpdateBotLocale
                description: >-
                  <p>Updates the settings that a bot has for a specific
                  locale.</p>
                tags:
                  - Update
                  - Bot
                  - Locales
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
            /bots/:
              POST:
                summary: ListBots
                description: <p>Gets a list of available bots.</p>
                tags:
                  - Lists
                  - Bots
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
            /bots/{botId}/botaliases/:
              POST:
                summary: ListBotAliases
                description: <p>Gets a list of aliases for the specified bot.</p>
                tags:
                  - Lists
                  - Bot
                  - Aliases
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
            /bots/{botId}/botversions/{botVersion}/botlocales/:
              POST:
                summary: ListBotLocales
                description: <p>Gets a list of locales for the specified bot.</p>
                tags:
                  - Lists
                  - Bot
                  - Locales
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
            /bots/{botId}/replicas/:
              POST:
                summary: ListBotReplicas
                description: <p>The action to list the replicated bots.</p>
                tags:
                  - Lists
                  - Bot
                  - Replicas
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
            /bots/{botId}/botversions/:
              POST:
                summary: ListBotVersions
                description: >-
                  <p>Gets information about all of the versions of a bot.</p>
                  <p>The <code>ListBotVersions</code> operation returns a
                  summary of each version of a bot. For example, if a bot has
                  three numbered versions, the <code>ListBotVersions</code>
                  operation returns for summaries, one for each numbered version
                  and one for the <code>DRAFT</code> version.</p> <p>The
                  <code>ListBotVersions</code> operation always returns at least
                  one version, the <code>DRAFT</code> version.</p>
                tags:
                  - Lists
                  - Bot
                  - Versions
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
            /exports/:
              POST:
                summary: ListExports
                description: >-
                  <p>Lists the exports for a bot, bot locale, or custom
                  vocabulary. Exports are kept in the list for 7 days.</p>
                tags:
                  - Lists
                  - Exports
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
            /bots/{botId}/botversions/{botVersion}/botlocales/{localeId}/intents/:
              POST:
                summary: ListIntents
                description: <p>Get a list of intents that meet the specified criteria.</p>
                tags:
                  - Lists
                  - Intents
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
            /policy/{resourceArn}/:
              PUT:
                summary: UpdateResourcePolicy
                description: >-
                  <p>Replaces the existing resource policy for a bot or bot
                  alias with a new one. If the policy doesn't exist, Amazon Lex
                  returns an exception.</p>
                tags:
                  - Update
                  - Resources
                  - Policies
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
            /policy/{resourceArn}/statements/:
              POST:
                summary: CreateResourcePolicyStatement
                description: >-
                  <p>Adds a new resource policy statement to a bot or bot alias.
                  If a resource policy exists, the statement is added to the
                  current resource policy. If a policy doesn't exist, a new
                  policy is created.</p> <p>You can't create a resource policy
                  statement that allows cross-account access.</p>
                tags:
                  - Create
                  - Resources
                  - Policies
                  - Statements
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
            /bots/{botId}/botversions/{botVersion}/botlocales/{localeId}/intents/{intentId}/slots/:
              POST:
                summary: ListSlots
                description: <p>Gets a list of slots that match the specified criteria.</p>
                tags:
                  - Lists
                  - Slots
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
            /bots/{botId}/botversions/{botVersion}/botlocales/{localeId}/slottypes/:
              POST:
                summary: ListSlotTypes
                description: >-
                  <p>Gets a list of slot types that match the specified
                  criteria.</p>
                tags:
                  - Lists
                  - Slots
                  - Types
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
            /testsets/{testSetId}/testsetdiscrepancy:
              POST:
                summary: CreateTestSetDiscrepancyReport
                description: >-
                  <p>Create a report that describes the differences between the
                  bot and the test set.</p>
                tags:
                  - Create
                  - Tests
                  - Sets
                  - Discrepancy
                  - Reports
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
            /createuploadurl/:
              POST:
                summary: CreateUploadUrl
                description: >-
                  <p>Gets a pre-signed S3 write URL that you use to upload the
                  zip archive when importing a bot or a bot locale. </p>
                tags:
                  - Create
                  - Uploads
                  - URL
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
            /bots/{botId}/:
              PUT:
                summary: UpdateBot
                description: <p>Updates the configuration of an existing bot. </p>
                tags:
                  - Update
                  - Bot
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
            /bots/{botId}/botaliases/{botAliasId}/:
              PUT:
                summary: UpdateBotAlias
                description: <p>Updates the configuration of an existing bot alias.</p>
                tags:
                  - Update
                  - Bot
                  - Alias
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
            /bots/{botId}/replicas/{replicaRegion}/:
              GET:
                summary: DescribeBotReplica
                description: >-
                  <p>Monitors the bot replication status through the UI
                  console.</p>
                tags:
                  - Describe
                  - Bot
                  - Replicas
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
            /bots/{botId}/botversions/{botVersion}/:
              GET:
                summary: DescribeBotVersion
                description: <p>Provides metadata about a version of a bot.</p>
                tags:
                  - Describe
                  - Bot
                  - Versions
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
            /bots/{botId}/botversions/{botVersion}/botlocales/{localeId}/customvocabulary:
              DELETE:
                summary: DeleteCustomVocabulary
                description: >-
                  <p>Removes a custom vocabulary from the specified locale in
                  the specified bot.</p>
                tags:
                  - Delete
                  - Custom
                  - Vocabularies
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
            /exports/{exportId}/:
              PUT:
                summary: UpdateExport
                description: >-
                  <p>Updates the password used to protect an export zip
                  archive.</p> <p>The password is not required. If you don't
                  supply a password, Amazon Lex generates a zip file that is not
                  protected by a password. This is the archive that is available
                  at the pre-signed S3 URL provided by the <a
                  href="https://docs.aws.amazon.com/lexv2/latest/APIReference/API_DescribeExport.html">DescribeExport</a>
                  operation.</p>
                tags:
                  - Update
                  - Export
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
            /imports/{importId}/:
              GET:
                summary: DescribeImport
                description: <p>Gets information about a specific import.</p>
                tags:
                  - Describe
                  - Import
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
            /bots/{botId}/botversions/{botVersion}/botlocales/{localeId}/intents/{intentId}/:
              PUT:
                summary: UpdateIntent
                description: <p>Updates the settings for an intent.</p>
                tags:
                  - Update
                  - Intent
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
            /policy/{resourceArn}/statements/{statementId}/:
              DELETE:
                summary: DeleteResourcePolicyStatement
                description: >-
                  <p>Deletes a policy statement from a resource policy. If you
                  delete the last statement from a policy, the policy is
                  deleted. If you specify a statement ID that doesn't exist in
                  the policy, or if the bot or bot alias doesn't have a policy
                  attached, Amazon Lex returns an exception.</p>
                tags:
                  - Delete
                  - Resources
                  - Policies
                  - Statements
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
            /bots/{botId}/botversions/{botVersion}/botlocales/{localeId}/intents/{intentId}/slots/{slotId}/:
              PUT:
                summary: UpdateSlot
                description: <p>Updates the settings for a slot.</p>
                tags:
                  - Update
                  - Slots
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
            /bots/{botId}/botversions/{botVersion}/botlocales/{localeId}/slottypes/{slotTypeId}/:
              PUT:
                summary: UpdateSlotType
                description: <p>Updates the configuration of an existing slot type.</p>
                tags:
                  - Update
                  - Slots
                  - Types
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
            /testsets/{testSetId}:
              PUT:
                summary: UpdateTestSet
                description: <p>The action to update the test set.</p>
                tags:
                  - Update
                  - Tests
                  - Sets
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
            /bots/{botId}/utterances/:
              DELETE:
                summary: DeleteUtterances
                description: >-
                  <p>Deletes stored utterances.</p> <p>Amazon Lex stores the
                  utterances that users send to your bot. Utterances are stored
                  for 15 days for use with the <a
                  href="https://docs.aws.amazon.com/lexv2/latest/APIReference/API_ListAggregatedUtterances.html">ListAggregatedUtterances</a>
                  operation, and then stored indefinitely for use in improving
                  the ability of your bot to respond to user input..</p> <p>Use
                  the <code>DeleteUtterances</code> operation to manually delete
                  utterances for a specific session. When you use the
                  <code>DeleteUtterances</code> operation, utterances stored for
                  improving your bot's ability to respond to user input are
                  deleted immediately. Utterances stored for use with the
                  <code>ListAggregatedUtterances</code> operation are deleted
                  after 15 days.</p>
                tags:
                  - Delete
                  - Utterances
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
            /bots/{botId}/botversions/{botVersion}/botlocales/{localeId}/botrecommendations/{botRecommendationId}/:
              PUT:
                summary: UpdateBotRecommendation
                description: <p>Updates an existing bot recommendation request.</p>
                tags:
                  - Update
                  - Bot
                  - Recommendations
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
            /bots/{botId}/botversions/{botVersion}/botlocales/{localeId}/generations/{generationId}:
              GET:
                summary: DescribeBotResourceGeneration
                description: >-
                  <p>Returns information about a request to generate a bot
                  through natural language description, made through the
                  <code>StartBotResource</code> API. Use the
                  <code>generatedBotLocaleUrl</code> to retrieve the Amazon S3
                  object containing the bot locale configuration. You can then
                  modify and import this configuration.</p>
                tags:
                  - Describe
                  - Bot
                  - Resources
                  - Generation
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
            /bots/{botId}/botversions/{botVersion}/botlocales/{localeId}/customvocabulary/DEFAULT/metadata:
              GET:
                summary: DescribeCustomVocabularyMetadata
                description: >-
                  <p>Provides metadata information about a custom
                  vocabulary.</p>
                tags:
                  - Describe
                  - Custom
                  - Vocabularies
                  - Metadata
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
            /testexecutions/{testExecutionId}:
              GET:
                summary: DescribeTestExecution
                description: <p>Gets metadata information about the test execution.</p>
                tags:
                  - Describe
                  - Tests
                  - Execution
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
            /testsetdiscrepancy/{testSetDiscrepancyReportId}:
              GET:
                summary: DescribeTestSetDiscrepancyReport
                description: >-
                  <p>Gets metadata information about the test set discrepancy
                  report.</p>
                tags:
                  - Describe
                  - Tests
                  - Sets
                  - Discrepancy
                  - Reports
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
            /testsetgenerations/{testSetGenerationId}:
              GET:
                summary: DescribeTestSetGeneration
                description: >-
                  <p>Gets metadata information about the test set
                  generation.</p>
                tags:
                  - Describe
                  - Tests
                  - Sets
                  - Generation
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
            /bots/{botId}/botversions/{botVersion}/botlocales/{localeId}/generate:
              POST:
                summary: GenerateBotElement
                description: <p>Generates sample utterances for an intent.</p>
                tags:
                  - Generate
                  - Bot
                  - Elements
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
                  - Generate
            /testexecutions/{testExecutionId}/artifacturl:
              GET:
                summary: GetTestExecutionArtifactsUrl
                description: >-
                  <p>The pre-signed Amazon S3 URL to download the test execution
                  result artifacts.</p>
                tags:
                  - Get
                  - Tests
                  - Execution
                  - Artifacts
                  - URL
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
                  - Generate
                  - Artifact URL
            /bots/{botId}/aggregatedutterances/:
              POST:
                summary: ListAggregatedUtterances
                description: >-
                  <p>Provides a list of utterances that users have sent to the
                  bot.</p> <p>Utterances are aggregated by the text of the
                  utterance. For example, all instances where customers used the
                  phrase "I want to order pizza" are aggregated into the same
                  line in the response.</p> <p>You can see both detected
                  utterances and missed utterances. A detected utterance is
                  where the bot properly recognized the utterance and activated
                  the associated intent. A missed utterance was not recognized
                  by the bot and didn't activate an intent.</p> <p>Utterances
                  can be aggregated for a bot alias or for a bot version, but
                  not both at the same time.</p> <p>Utterances statistics are
                  not generated under the following conditions:</p> <ul> <li>
                  <p>The <code>childDirected</code> field was set to true when
                  the bot was created.</p> </li> <li> <p>You are using slot
                  obfuscation with one or more slots.</p> </li> <li> <p>You
                  opted out of participating in improving Amazon Lex.</p> </li>
                  </ul>
                tags:
                  - Lists
                  - Aggregated
                  - Utterances
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
                  - Generate
                  - Artifact URL
                  - Aggregated Utterances
            /bots/{botId}/replicas/{replicaRegion}/botaliases/:
              POST:
                summary: ListBotAliasReplicas
                description: >-
                  <p>The action to list the replicated bots created from the
                  source bot alias.</p>
                tags:
                  - Lists
                  - Bot
                  - Alias
                  - Replicas
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
                  - Generate
                  - Artifact URL
                  - Aggregated Utterances
            /bots/{botId}/botversions/{botVersion}/botlocales/{localeId}/botrecommendations/:
              PUT:
                summary: StartBotRecommendation
                description: >-
                  <p>Use this to provide your transcript data, and to start the
                  bot recommendation process.</p>
                tags:
                  - Start
                  - Bot
                  - Recommendations
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
                  - Generate
                  - Artifact URL
                  - Aggregated Utterances
            /bots/{botId}/botversions/{botVersion}/botlocales/{localeId}/generations:
              POST:
                summary: ListBotResourceGenerations
                description: <p>Lists the generation requests made for a bot locale.</p>
                tags:
                  - Lists
                  - Bot
                  - Resources
                  - Generations
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
                  - Generate
                  - Artifact URL
                  - Aggregated Utterances
            /bots/{botId}/replicas/{replicaRegion}/botversions/:
              POST:
                summary: ListBotVersionReplicas
                description: >-
                  <p>Contains information about all the versions replication
                  statuses applicable for Global Resiliency.</p>
                tags:
                  - Lists
                  - Bot
                  - Versions
                  - Replicas
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
                  - Generate
                  - Artifact URL
                  - Aggregated Utterances
            /builtins/locales/{localeId}/intents/:
              POST:
                summary: ListBuiltInIntents
                description: >-
                  <p>Gets a list of built-in intents provided by Amazon Lex that
                  you can use in your bot. </p> <p>To use a built-in intent as a
                  the base for your own intent, include the built-in intent
                  signature in the <code>parentIntentSignature</code> parameter
                  when you call the <code>CreateIntent</code> operation. For
                  more information, see <a
                  href="https://docs.aws.amazon.com/lexv2/latest/APIReference/API_CreateIntent.html">CreateIntent</a>.</p>
                tags:
                  - Lists
                  - Built
                  - In
                  - Intents
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
                  - Generate
                  - Artifact URL
                  - Aggregated Utterances
            /builtins/locales/{localeId}/slottypes/:
              POST:
                summary: ListBuiltInSlotTypes
                description: >-
                  <p>Gets a list of built-in slot types that meet the specified
                  criteria.</p>
                tags:
                  - Lists
                  - Built
                  - In
                  - Slots
                  - Types
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
                  - Generate
                  - Artifact URL
                  - Aggregated Utterances
            /bots/{botId}/botversions/{botVersion}/botlocales/{localeId}/customvocabulary/DEFAULT/list:
              POST:
                summary: ListCustomVocabularyItems
                description: >-
                  <p>Paginated list of custom vocabulary items for a given bot
                  locale's custom vocabulary.</p>
                tags:
                  - Lists
                  - Custom
                  - Vocabularies
                  - Items
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
                  - Generate
                  - Artifact URL
                  - Aggregated Utterances
                  - Lists
            /imports/:
              PUT:
                summary: StartImport
                description: >-
                  <p>Starts importing a bot, bot locale, or custom vocabulary
                  from a zip archive that you uploaded to an S3 bucket.</p>
                tags:
                  - Start
                  - Import
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
                  - Generate
                  - Artifact URL
                  - Aggregated Utterances
                  - Lists
                  - Imports
            /bots/{botId}/analytics/intentmetrics:
              POST:
                summary: ListIntentMetrics
                description: >-
                  <p>Retrieves summary metrics for the intents in your bot. The
                  following fields are required:</p> <ul> <li> <p>
                  <code>metrics</code> – A list of <a
                  href="https://docs.aws.amazon.com/lexv2/latest/APIReference/API_AnalyticsIntentMetric.html">AnalyticsIntentMetric</a>
                  objects. In each object, use the <code>name</code> field to
                  specify the metric to calculate, the <code>statistic</code>
                  field to specify whether to calculate the <code>Sum</code>,
                  <code>Average</code>, or <code>Max</code> number, and the
                  <code>order</code> field to specify whether to sort the
                  results in <code>Ascending</code> or <code>Descending</code>
                  order.</p> </li> <li> <p> <code>startDateTime</code> and
                  <code>endDateTime</code> – Define a time range for which you
                  want to retrieve results.</p> </li> </ul> <p>Of the optional
                  fields, you can organize the results in the following
                  ways:</p> <ul> <li> <p>Use the <code>filters</code> field to
                  filter the results, the <code>groupBy</code> field to specify
                  categories by which to group the results, and the
                  <code>binBy</code> field to specify time intervals by which to
                  group the results.</p> </li> <li> <p>Use the
                  <code>maxResults</code> field to limit the number of results
                  to return in a single response and the <code>nextToken</code>
                  field to return the next batch of results if the response does
                  not return the full set of results.</p> </li> </ul> <p>Note
                  that an <code>order</code> field exists in both
                  <code>binBy</code> and <code>metrics</code>. You can specify
                  only one <code>order</code> in a given request.</p>
                tags:
                  - Lists
                  - Intent
                  - Metrics
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
                  - Generate
                  - Artifact URL
                  - Aggregated Utterances
                  - Lists
                  - Imports
                  - Analytics
                  - Intent Metrics
            /bots/{botId}/analytics/intentpaths:
              POST:
                summary: ListIntentPaths
                description: >-
                  <p>Retrieves summary statistics for a path of intents that
                  users take over sessions with your bot. The following fields
                  are required:</p> <ul> <li> <p> <code>startDateTime</code> and
                  <code>endDateTime</code> – Define a time range for which you
                  want to retrieve results.</p> </li> <li> <p>
                  <code>intentPath</code> – Define an order of intents for which
                  you want to retrieve metrics. Separate intents in the path
                  with a forward slash. For example, populate the
                  <code>intentPath</code> field with
                  <code>/BookCar/BookHotel</code> to see details about how many
                  times users invoked the <code>BookCar</code> and
                  <code>BookHotel</code> intents in that order.</p> </li> </ul>
                  <p>Use the optional <code>filters</code> field to filter the
                  results.</p>
                tags:
                  - Lists
                  - Intent
                  - Paths
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
                  - Generate
                  - Artifact URL
                  - Aggregated Utterances
                  - Lists
                  - Imports
                  - Analytics
                  - Intent Metrics
                  - Intent Paths
            /bots/{botId}/analytics/intentstagemetrics:
              POST:
                summary: ListIntentStageMetrics
                description: >-
                  <p>Retrieves summary metrics for the stages within intents in
                  your bot. The following fields are required:</p> <ul> <li> <p>
                  <code>metrics</code> – A list of <a
                  href="https://docs.aws.amazon.com/lexv2/latest/APIReference/API_AnalyticsIntentStageMetric.html">AnalyticsIntentStageMetric</a>
                  objects. In each object, use the <code>name</code> field to
                  specify the metric to calculate, the <code>statistic</code>
                  field to specify whether to calculate the <code>Sum</code>,
                  <code>Average</code>, or <code>Max</code> number, and the
                  <code>order</code> field to specify whether to sort the
                  results in <code>Ascending</code> or <code>Descending</code>
                  order.</p> </li> <li> <p> <code>startDateTime</code> and
                  <code>endDateTime</code> – Define a time range for which you
                  want to retrieve results.</p> </li> </ul> <p>Of the optional
                  fields, you can organize the results in the following
                  ways:</p> <ul> <li> <p>Use the <code>filters</code> field to
                  filter the results, the <code>groupBy</code> field to specify
                  categories by which to group the results, and the
                  <code>binBy</code> field to specify time intervals by which to
                  group the results.</p> </li> <li> <p>Use the
                  <code>maxResults</code> field to limit the number of results
                  to return in a single response and the <code>nextToken</code>
                  field to return the next batch of results if the response does
                  not return the full set of results.</p> </li> </ul> <p>Note
                  that an <code>order</code> field exists in both
                  <code>binBy</code> and <code>metrics</code>. You can only
                  specify one <code>order</code> in a given request.</p>
                tags:
                  - Lists
                  - Intent
                  - Stage
                  - Metrics
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
                  - Generate
                  - Artifact URL
                  - Aggregated Utterances
                  - Lists
                  - Imports
                  - Analytics
                  - Intent Metrics
                  - Intent Paths
                  - Intent Stage Metrics
            /bots/{botId}/botversions/{botVersion}/botlocales/{localeId}/botrecommendations/{botRecommendationId}/intents:
              POST:
                summary: ListRecommendedIntents
                description: >-
                  <p>Gets a list of recommended intents provided by the bot
                  recommendation that you can use in your bot. Intents in the
                  response are ordered by relevance.</p>
                tags:
                  - Lists
                  - Recommended
                  - Intents
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
                  - Generate
                  - Artifact URL
                  - Aggregated Utterances
                  - Lists
                  - Imports
                  - Analytics
                  - Intent Metrics
                  - Intent Paths
                  - Intent Stage Metrics
            /bots/{botId}/analytics/sessions:
              POST:
                summary: ListSessionAnalyticsData
                description: >-
                  <p>Retrieves a list of metadata for individual user sessions
                  with your bot. The <code>startDateTime</code> and
                  <code>endDateTime</code> fields are required. These fields
                  define a time range for which you want to retrieve results. Of
                  the optional fields, you can organize the results in the
                  following ways:</p> <ul> <li> <p>Use the <code>filters</code>
                  field to filter the results and the <code>sortBy</code> field
                  to specify the values by which to sort the results.</p> </li>
                  <li> <p>Use the <code>maxResults</code> field to limit the
                  number of results to return in a single response and the
                  <code>nextToken</code> field to return the next batch of
                  results if the response does not return the full set of
                  results.</p> </li> </ul>
                tags:
                  - Lists
                  - Sessions
                  - Analytics
                  - Data
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
                  - Generate
                  - Artifact URL
                  - Aggregated Utterances
                  - Lists
                  - Imports
                  - Analytics
                  - Intent Metrics
                  - Intent Paths
                  - Intent Stage Metrics
                  - Sessions
            /bots/{botId}/analytics/sessionmetrics:
              POST:
                summary: ListSessionMetrics
                description: >-
                  <p>Retrieves summary metrics for the user sessions with your
                  bot. The following fields are required:</p> <ul> <li> <p>
                  <code>metrics</code> – A list of <a
                  href="https://docs.aws.amazon.com/lexv2/latest/APIReference/API_AnalyticsSessionMetric.html">AnalyticsSessionMetric</a>
                  objects. In each object, use the <code>name</code> field to
                  specify the metric to calculate, the <code>statistic</code>
                  field to specify whether to calculate the <code>Sum</code>,
                  <code>Average</code>, or <code>Max</code> number, and the
                  <code>order</code> field to specify whether to sort the
                  results in <code>Ascending</code> or <code>Descending</code>
                  order.</p> </li> <li> <p> <code>startDateTime</code> and
                  <code>endDateTime</code> – Define a time range for which you
                  want to retrieve results.</p> </li> </ul> <p>Of the optional
                  fields, you can organize the results in the following
                  ways:</p> <ul> <li> <p>Use the <code>filters</code> field to
                  filter the results, the <code>groupBy</code> field to specify
                  categories by which to group the results, and the
                  <code>binBy</code> field to specify time intervals by which to
                  group the results.</p> </li> <li> <p>Use the
                  <code>maxResults</code> field to limit the number of results
                  to return in a single response and the <code>nextToken</code>
                  field to return the next batch of results if the response does
                  not return the full set of results.</p> </li> </ul> <p>Note
                  that an <code>order</code> field exists in both
                  <code>binBy</code> and <code>metrics</code>. Currently, you
                  can specify it in either field, but not in both.</p>
                tags:
                  - Lists
                  - Sessions
                  - Metrics
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
                  - Generate
                  - Artifact URL
                  - Aggregated Utterances
                  - Lists
                  - Imports
                  - Analytics
                  - Intent Metrics
                  - Intent Paths
                  - Intent Stage Metrics
                  - Sessions
                  - Session Metrics
            /tags/{resourceARN}:
              DELETE:
                summary: UntagResource
                description: <p>Removes tags from a bot, bot alias, or bot channel.</p>
                tags:
                  - Untag
                  - Resources
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
                  - Generate
                  - Artifact URL
                  - Aggregated Utterances
                  - Lists
                  - Imports
                  - Analytics
                  - Intent Metrics
                  - Intent Paths
                  - Intent Stage Metrics
                  - Sessions
                  - Session Metrics
                  - Tags
                  - ResourceARN
            /testexecutions/{testExecutionId}/results:
              POST:
                summary: ListTestExecutionResultItems
                description: <p>Gets a list of test execution result items.</p>
                tags:
                  - Lists
                  - Tests
                  - Execution
                  - Results
                  - Items
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
                  - Generate
                  - Artifact URL
                  - Aggregated Utterances
                  - Lists
                  - Imports
                  - Analytics
                  - Intent Metrics
                  - Intent Paths
                  - Intent Stage Metrics
                  - Sessions
                  - Session Metrics
                  - Tags
                  - ResourceARN
                  - Results
            /testexecutions:
              POST:
                summary: ListTestExecutions
                description: <p>The list of test set executions.</p>
                tags:
                  - Lists
                  - Tests
                  - Executions
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
                  - Generate
                  - Artifact URL
                  - Aggregated Utterances
                  - Lists
                  - Imports
                  - Analytics
                  - Intent Metrics
                  - Intent Paths
                  - Intent Stage Metrics
                  - Sessions
                  - Session Metrics
                  - Tags
                  - ResourceARN
                  - Results
                  - Test Executions
            /testsets/{testSetId}/records:
              POST:
                summary: ListTestSetRecords
                description: <p>The list of test set records.</p>
                tags:
                  - Lists
                  - Tests
                  - Sets
                  - Records
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
                  - Generate
                  - Artifact URL
                  - Aggregated Utterances
                  - Lists
                  - Imports
                  - Analytics
                  - Intent Metrics
                  - Intent Paths
                  - Intent Stage Metrics
                  - Sessions
                  - Session Metrics
                  - Tags
                  - ResourceARN
                  - Results
                  - Test Executions
                  - Records
            /testsets:
              POST:
                summary: ListTestSets
                description: <p>The list of the test sets</p>
                tags:
                  - Lists
                  - Tests
                  - Sets
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
                  - Generate
                  - Artifact URL
                  - Aggregated Utterances
                  - Lists
                  - Imports
                  - Analytics
                  - Intent Metrics
                  - Intent Paths
                  - Intent Stage Metrics
                  - Sessions
                  - Session Metrics
                  - Tags
                  - ResourceARN
                  - Results
                  - Test Executions
                  - Records
                  - Test Sets
            /bots/{botId}/analytics/utterances:
              POST:
                summary: ListUtteranceAnalyticsData
                description: >-
                  <note> <p>To use this API operation, your IAM role must have
                  permissions to perform the <a
                  href="https://docs.aws.amazon.com/lexv2/latest/APIReference/API_ListAggregatedUtterances.html">ListAggregatedUtterances</a>
                  operation, which provides access to utterance-related
                  analytics. See <a
                  href="https://docs.aws.amazon.com/lexv2/latest/dg/monitoring-utterances.html">Viewing
                  utterance statistics</a> for the IAM policy to apply to the
                  IAM role.</p> </note> <p>Retrieves a list of metadata for
                  individual user utterances to your bot. The following fields
                  are required:</p> <ul> <li> <p> <code>startDateTime</code> and
                  <code>endDateTime</code> – Define a time range for which you
                  want to retrieve results.</p> </li> </ul> <p>Of the optional
                  fields, you can organize the results in the following
                  ways:</p> <ul> <li> <p>Use the <code>filters</code> field to
                  filter the results and the <code>sortBy</code> field to
                  specify the values by which to sort the results.</p> </li>
                  <li> <p>Use the <code>maxResults</code> field to limit the
                  number of results to return in a single response and the
                  <code>nextToken</code> field to return the next batch of
                  results if the response does not return the full set of
                  results.</p> </li> </ul>
                tags:
                  - Lists
                  - Utterances
                  - Analytics
                  - Data
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
                  - Generate
                  - Artifact URL
                  - Aggregated Utterances
                  - Lists
                  - Imports
                  - Analytics
                  - Intent Metrics
                  - Intent Paths
                  - Intent Stage Metrics
                  - Sessions
                  - Session Metrics
                  - Tags
                  - ResourceARN
                  - Results
                  - Test Executions
                  - Records
                  - Test Sets
            /bots/{botId}/analytics/utterancemetrics:
              POST:
                summary: ListUtteranceMetrics
                description: >-
                  <note> <p>To use this API operation, your IAM role must have
                  permissions to perform the <a
                  href="https://docs.aws.amazon.com/lexv2/latest/APIReference/API_ListAggregatedUtterances.html">ListAggregatedUtterances</a>
                  operation, which provides access to utterance-related
                  analytics. See <a
                  href="https://docs.aws.amazon.com/lexv2/latest/dg/monitoring-utterances.html">Viewing
                  utterance statistics</a> for the IAM policy to apply to the
                  IAM role.</p> </note> <p>Retrieves summary metrics for the
                  utterances in your bot. The following fields are required:</p>
                  <ul> <li> <p> <code>metrics</code> – A list of <a
                  href="https://docs.aws.amazon.com/lexv2/latest/APIReference/API_AnalyticsUtteranceMetric.html">AnalyticsUtteranceMetric</a>
                  objects. In each object, use the <code>name</code> field to
                  specify the metric to calculate, the <code>statistic</code>
                  field to specify whether to calculate the <code>Sum</code>,
                  <code>Average</code>, or <code>Max</code> number, and the
                  <code>order</code> field to specify whether to sort the
                  results in <code>Ascending</code> or <code>Descending</code>
                  order.</p> </li> <li> <p> <code>startDateTime</code> and
                  <code>endDateTime</code> – Define a time range for which you
                  want to retrieve results.</p> </li> </ul> <p>Of the optional
                  fields, you can organize the results in the following
                  ways:</p> <ul> <li> <p>Use the <code>filters</code> field to
                  filter the results, the <code>groupBy</code> field to specify
                  categories by which to group the results, and the
                  <code>binBy</code> field to specify time intervals by which to
                  group the results.</p> </li> <li> <p>Use the
                  <code>maxResults</code> field to limit the number of results
                  to return in a single response and the <code>nextToken</code>
                  field to return the next batch of results if the response does
                  not return the full set of results.</p> </li> </ul> <p>Note
                  that an <code>order</code> field exists in both
                  <code>binBy</code> and <code>metrics</code>. Currently, you
                  can specify it in either field, but not in both.</p>
                tags:
                  - Lists
                  - Utterances
                  - Metrics
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
                  - Generate
                  - Artifact URL
                  - Aggregated Utterances
                  - Lists
                  - Imports
                  - Analytics
                  - Intent Metrics
                  - Intent Paths
                  - Intent Stage Metrics
                  - Sessions
                  - Session Metrics
                  - Tags
                  - ResourceARN
                  - Results
                  - Test Executions
                  - Records
                  - Test Sets
                  - Utterance Metrics
            /bots/{botId}/botversions/{botVersion}/botlocales/{localeId}/botrecommendations/{botRecommendationId}/associatedtranscripts:
              POST:
                summary: SearchAssociatedTranscripts
                description: >-
                  <p>Search for associated transcripts that meet the specified
                  criteria.</p>
                tags:
                  - Search
                  - Associated
                  - Transcripts
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
                  - Generate
                  - Artifact URL
                  - Aggregated Utterances
                  - Lists
                  - Imports
                  - Analytics
                  - Intent Metrics
                  - Intent Paths
                  - Intent Stage Metrics
                  - Sessions
                  - Session Metrics
                  - Tags
                  - ResourceARN
                  - Results
                  - Test Executions
                  - Records
                  - Test Sets
                  - Utterance Metrics
                  - Associated Transcripts
            /bots/{botId}/botversions/{botVersion}/botlocales/{localeId}/startgeneration:
              PUT:
                summary: StartBotResourceGeneration
                description: >-
                  <p>Starts a request for the descriptive bot builder to
                  generate a bot locale configuration based on the prompt you
                  provide it. After you make this call, use the
                  <code>DescribeBotResourceGeneration</code> operation to check
                  on the status of the generation and for the
                  <code>generatedBotLocaleUrl</code> when the generation is
                  complete. Use that value to retrieve the Amazon S3 object
                  containing the bot locale configuration. You can then modify
                  and import this configuration.</p>
                tags:
                  - Start
                  - Bot
                  - Resources
                  - Generation
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
                  - Generate
                  - Artifact URL
                  - Aggregated Utterances
                  - Lists
                  - Imports
                  - Analytics
                  - Intent Metrics
                  - Intent Paths
                  - Intent Stage Metrics
                  - Sessions
                  - Session Metrics
                  - Tags
                  - ResourceARN
                  - Results
                  - Test Executions
                  - Records
                  - Test Sets
                  - Utterance Metrics
                  - Associated Transcripts
                  - Start Generation
            /testsets/{testSetId}/testexecutions:
              POST:
                summary: StartTestExecution
                description: <p>The action to start test set execution.</p>
                tags:
                  - Start
                  - Tests
                  - Execution
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
                  - Generate
                  - Artifact URL
                  - Aggregated Utterances
                  - Lists
                  - Imports
                  - Analytics
                  - Intent Metrics
                  - Intent Paths
                  - Intent Stage Metrics
                  - Sessions
                  - Session Metrics
                  - Tags
                  - ResourceARN
                  - Results
                  - Test Executions
                  - Records
                  - Test Sets
                  - Utterance Metrics
                  - Associated Transcripts
                  - Start Generation
            /testsetgenerations:
              PUT:
                summary: StartTestSetGeneration
                description: <p>The action to start the generation of test set.</p>
                tags:
                  - Start
                  - Tests
                  - Sets
                  - Generation
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
                  - Generate
                  - Artifact URL
                  - Aggregated Utterances
                  - Lists
                  - Imports
                  - Analytics
                  - Intent Metrics
                  - Intent Paths
                  - Intent Stage Metrics
                  - Sessions
                  - Session Metrics
                  - Tags
                  - ResourceARN
                  - Results
                  - Test Executions
                  - Records
                  - Test Sets
                  - Utterance Metrics
                  - Associated Transcripts
                  - Start Generation
                  - Test Set Generations
            /bots/{botId}/botversions/{botVersion}/botlocales/{localeId}/botrecommendations/{botRecommendationId}/stopbotrecommendation:
              PUT:
                summary: StopBotRecommendation
                description: <p>Stop an already running Bot Recommendation re
                tags:
                  - Stop
                  - Bot
                  - Recommendations
                  - Identifiers
                  - Bot Versions
                  - Bot
                  - Versions
                  - Bot Locales
                  - Locales
                  - Custom Vocabulary
                  - Batches
                  - Batches
                  - Batches
                  - Bots
                  - Bot Aliases
                  - Replicas
                  - Exports
                  - Intents
                  - ARN
                  - Statements
                  - Intent
                  - Slots
                  - Slot Types
                  - Sets
                  - Test Set Discrepancy
                  - Upload URLs
                  - Alias
                  - Replicas
                  - Regions
                  - Statements
                  - Slots
                  - Types
                  - Utterances
                  - Bot Recommendations
                  - Recommendations
                  - Generations
                  - Generation
                  - Metadata
                  - Execution
                  - Discrepancy
                  - Reports
                  - Generate
                  - Artifact URL
                  - Aggregated Utterances
                  - Lists
                  - Imports
                  - Analytics
                  - Intent Metrics
                  - Intent Paths
                  - Intent Stage Metrics
                  - Sessions
                  - Session Metrics
                  - Tags
                  - ResourceARN
                  - Results
                  - Test Executions
                  - Records
                  - Test Sets
                  - Utterance Metrics
                  - Associated Transcripts
                  - Start Generation
                  - Test Set Generations
                  - Stopbotrecommendati
    overlays:
      - type: APIs.io Search
        url: overlays/modelslexv2-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/modelslexv2-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:modelslexv2
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---