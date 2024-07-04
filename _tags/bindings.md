---
name: Bindings
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/bindings.png
url: https://example.com/apis/bindings.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Bindings
apis:
  - aid: twilio:twilio-conversations-api
    name: Twilio Conversations API
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
            title: Twilio - Conversations
            license:
              name: Apache 2.0
              url: https://www.apache.org/licenses/LICENSE-2.0.html
          openapi: 3.0.1
          paths:
            /v1/Configuration:
              description: >-
                The Configuration resource manages a set of account-level
                settings applicable to the Conversations API.
              get:
                description: >-
                  Fetch the global configuration of conversations on your
                  account
                tags:
                  - Configuration
              post:
                description: >-
                  Update the global configuration of conversations on your
                  account
                tags:
                  - Configuration
            /v1/Configuration/Addresses:
              description: >-
                Address Configuration resource manages the configurations
                related to a unique address within Conversations
              get:
                description: Retrieve a list of address configurations for an account
                tags:
                  - Configuration
                  - Addresses
              post:
                description: Create a new address configuration
                tags:
                  - Configuration
                  - Addresses
            /v1/Configuration/Addresses/{Sid}:
              description: >-
                Address Configuration resource manages the configurations
                related to a unique address within Conversations
              get:
                description: 'Fetch an address configuration '
                tags:
                  - Configuration
                  - Addresses
                  - Sid
              post:
                description: Update an existing address configuration
                tags:
                  - Configuration
                  - Addresses
                  - Sid
              delete:
                description: Remove an existing address configuration
                tags:
                  - Configuration
                  - Addresses
                  - Sid
            /v1/Configuration/Webhooks:
              description: >-
                A Webhook resource manages a service-level set of callback URLs
                and their configuration for receiving all conversation events.
              get:
                description: ''
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
              post:
                description: ''
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
            /v1/Conversations:
              description: >-
                A Conversation resource represents an omnichannel group
                conversation with an ordered list of messages and a participant
                roster.
              post:
                description: Create a new conversation in your account's default service
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
              get:
                description: >-
                  Retrieve a list of conversations in your account's default
                  service
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
            /v1/Conversations/{Sid}:
              description: >-
                A Conversation resource represents an omnichannel group
                conversation with an ordered list of messages and a participant
                roster.
              post:
                description: >-
                  Update an existing conversation in your account's default
                  service
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
              delete:
                description: Remove a conversation from your account's default service
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
              get:
                description: Fetch a conversation from your account's default service
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
            /v1/Conversations/{ConversationSid}/Messages:
              description: A Message resource represents a message in a conversation.
              post:
                description: Add a new message to the conversation
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
                  - Conversation
                  - Messages
              get:
                description: Retrieve a list of all messages in the conversation
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
                  - Conversation
                  - Messages
            /v1/Conversations/{ConversationSid}/Messages/{Sid}:
              description: A Message resource represents a message in a conversation.
              post:
                description: Update an existing message in the conversation
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
                  - Conversation
                  - Messages
              delete:
                description: Remove a message from the conversation
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
                  - Conversation
                  - Messages
              get:
                description: Fetch a message from the conversation
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
                  - Conversation
                  - Messages
            /v1/Conversations/{ConversationSid}/Messages/{MessageSid}/Receipts/{Sid}:
              description: >-
                A Message Receipt resource represents a delivery/read receipt of
                a message in a conversation.
              get:
                description: >-
                  Fetch the delivery and read receipts of the conversation
                  message
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
                  - Conversation
                  - Messages
                  - Message
                  - Receipts
            /v1/Conversations/{ConversationSid}/Messages/{MessageSid}/Receipts:
              description: >-
                A Message Receipt resource represents a delivery/read receipt of
                a message in a conversation.
              get:
                description: >-
                  Retrieve a list of all delivery and read receipts of the
                  conversation message
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
                  - Conversation
                  - Messages
                  - Message
                  - Receipts
            /v1/Conversations/{ConversationSid}/Participants:
              description: A Participant resource represents a member of the conversation.
              post:
                description: Add a new participant to the conversation
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
                  - Conversation
                  - Messages
                  - Message
                  - Receipts
                  - Participants
              get:
                description: Retrieve a list of all participants of the conversation
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
                  - Conversation
                  - Messages
                  - Message
                  - Receipts
                  - Participants
            /v1/Conversations/{ConversationSid}/Participants/{Sid}:
              description: A Participant resource represents a member of the conversation.
              post:
                description: Update an existing participant in the conversation
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
                  - Conversation
                  - Messages
                  - Message
                  - Receipts
                  - Participants
              delete:
                description: Remove a participant from the conversation
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
                  - Conversation
                  - Messages
                  - Message
                  - Receipts
                  - Participants
              get:
                description: Fetch a participant of the conversation
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
                  - Conversation
                  - Messages
                  - Message
                  - Receipts
                  - Participants
            /v1/Conversations/{ConversationSid}/Webhooks:
              description: >-
                A Scoped Webhook resource manages a set of callback URLs and
                their configuration for receiving events specific to one
                conversation.
              get:
                description: Retrieve a list of all webhooks scoped to the conversation
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
                  - Conversation
                  - Messages
                  - Message
                  - Receipts
                  - Participants
              post:
                description: Create a new webhook scoped to the conversation
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
                  - Conversation
                  - Messages
                  - Message
                  - Receipts
                  - Participants
            /v1/Conversations/{ConversationSid}/Webhooks/{Sid}:
              description: >-
                A Scoped Webhook resource manages a set of callback URLs and
                their configuration for receiving events specific to one
                conversation.
              get:
                description: Fetch the configuration of a conversation-scoped webhook
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
                  - Conversation
                  - Messages
                  - Message
                  - Receipts
                  - Participants
              post:
                description: Update an existing conversation-scoped webhook
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
                  - Conversation
                  - Messages
                  - Message
                  - Receipts
                  - Participants
              delete:
                description: Remove an existing webhook scoped to the conversation
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
                  - Conversation
                  - Messages
                  - Message
                  - Receipts
                  - Participants
            /v1/Credentials:
              description: A Credential resource represents a push notification credential.
              post:
                description: Add a new push notification credential to your account
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
                  - Conversation
                  - Messages
                  - Message
                  - Receipts
                  - Participants
                  - Credentials
              get:
                description: >-
                  Retrieve a list of all push notification credentials on your
                  account
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
                  - Conversation
                  - Messages
                  - Message
                  - Receipts
                  - Participants
                  - Credentials
            /v1/Credentials/{Sid}:
              description: A Credential resource represents a push notification credential.
              post:
                description: >-
                  Update an existing push notification credential on your
                  account
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
                  - Conversation
                  - Messages
                  - Message
                  - Receipts
                  - Participants
                  - Credentials
              delete:
                description: Remove a push notification credential from your account
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
                  - Conversation
                  - Messages
                  - Message
                  - Receipts
                  - Participants
                  - Credentials
              get:
                description: Fetch a push notification credential from your account
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
                  - Conversation
                  - Messages
                  - Message
                  - Receipts
                  - Participants
                  - Credentials
            /v1/ParticipantConversations:
              description: >-
                Participant Conversations resource represents a list of
                Conversations that this Participant belongs to belonging to a
                default conversation service.
              get:
                description: >-
                  Retrieve a list of all Conversations that this Participant
                  belongs to by identity or by address. Only one parameter
                  should be specified.
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
                  - Conversation
                  - Messages
                  - Message
                  - Receipts
                  - Participants
                  - Credentials
                  - Participant
            /v1/Roles:
              description: >-
                A Role resource represents a set of permissions granted to a
                user within a service or a conversation.
              post:
                description: Create a new user role in your account's default service
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
                  - Conversation
                  - Messages
                  - Message
                  - Receipts
                  - Participants
                  - Credentials
                  - Participant
                  - Roles
              get:
                description: >-
                  Retrieve a list of all user roles in your account's default
                  service
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
                  - Conversation
                  - Messages
                  - Message
                  - Receipts
                  - Participants
                  - Credentials
                  - Participant
                  - Roles
            /v1/Roles/{Sid}:
              description: >-
                A Role resource represents a set of permissions granted to a
                user within a service or a conversation.
              post:
                description: Update an existing user role in your account's default service
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
                  - Conversation
                  - Messages
                  - Message
                  - Receipts
                  - Participants
                  - Credentials
                  - Participant
                  - Roles
              delete:
                description: Remove a user role from your account's default service
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
                  - Conversation
                  - Messages
                  - Message
                  - Receipts
                  - Participants
                  - Credentials
                  - Participant
                  - Roles
              get:
                description: Fetch a user role from your account's default service
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
                  - Conversation
                  - Messages
                  - Message
                  - Receipts
                  - Participants
                  - Credentials
                  - Participant
                  - Roles
            /v1/Services:
              description: >-
                A Service resource is a top-level conversation resource
                container that serves as a data silo.
              post:
                description: Create a new conversation service on your account
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
                  - Conversation
                  - Messages
                  - Message
                  - Receipts
                  - Participants
                  - Credentials
                  - Participant
                  - Roles
                  - Services
              get:
                description: Retrieve a list of all conversation services on your account
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
                  - Conversation
                  - Messages
                  - Message
                  - Receipts
                  - Participants
                  - Credentials
                  - Participant
                  - Roles
                  - Services
            /v1/Services/{Sid}:
              description: >-
                A Service resource is a top-level conversation resource
                container that serves as a data silo.
              delete:
                description: >-
                  Remove a conversation service with all its nested resources
                  from your account
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
                  - Conversation
                  - Messages
                  - Message
                  - Receipts
                  - Participants
                  - Credentials
                  - Participant
                  - Roles
                  - Services
              get:
                description: Fetch a conversation service from your account
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
                  - Conversation
                  - Messages
                  - Message
                  - Receipts
                  - Participants
                  - Credentials
                  - Participant
                  - Roles
                  - Services
            /v1/Services/{ChatServiceSid}/Bindings/{Sid}:
              description: >-
                A Binding resource represents a push notification binding and
                its configuration, for delivering conversation events to mobile
                or web endpoints.
              delete:
                description: >-
                  Remove a push notification binding from the conversation
                  service
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
                  - Conversation
                  - Messages
                  - Message
                  - Receipts
                  - Participants
                  - Credentials
                  - Participant
                  - Roles
                  - Services
                  - Chat
                  - Service
                  - Bindings
              get:
                description: >-
                  Fetch a push notification binding from the conversation
                  service
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
                  - Conversation
                  - Messages
                  - Message
                  - Receipts
                  - Participants
                  - Credentials
                  - Participant
                  - Roles
                  - Services
                  - Chat
                  - Service
                  - Bindings
            /v1/Services/{ChatServiceSid}/Bindings:
              description: >-
                A Binding resource represents a push notification binding and
                its configuration, for delivering conversation events to mobile
                or web endpoints.
              get:
                description: >-
                  Retrieve a list of all push notification bindings in the
                  conversation service
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
                  - Conversation
                  - Messages
                  - Message
                  - Receipts
                  - Participants
                  - Credentials
                  - Participant
                  - Roles
                  - Services
                  - Chat
                  - Service
                  - Bindings
            /v1/Services/{ChatServiceSid}/Configuration:
              description: >-
                A Service Configuration resource manages service-level settings
                applicable to the Conversation API.
              get:
                description: Fetch the configuration of a conversation service
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
                  - Conversation
                  - Messages
                  - Message
                  - Receipts
                  - Participants
                  - Credentials
                  - Participant
                  - Roles
                  - Services
                  - Chat
                  - Service
                  - Bindings
              post:
                description: Update configuration settings of a conversation service
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
                  - Conversation
                  - Messages
                  - Message
                  - Receipts
                  - Participants
                  - Credentials
                  - Participant
                  - Roles
                  - Services
                  - Chat
                  - Service
                  - Bindings
            /v1/Services/{ChatServiceSid}/Conversations:
              description: >-
                A Service Conversation resource represents an omnichannel group
                conversation with an ordered list of messages and a participant
                roster.
              post:
                description: Create a new conversation in your service
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
                  - Conversation
                  - Messages
                  - Message
                  - Receipts
                  - Participants
                  - Credentials
                  - Participant
                  - Roles
                  - Services
                  - Chat
                  - Service
                  - Bindings
              get:
                description: Retrieve a list of conversations in your service
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
                  - Conversation
                  - Messages
                  - Message
                  - Receipts
                  - Participants
                  - Credentials
                  - Participant
                  - Roles
                  - Services
                  - Chat
                  - Service
                  - Bindings
            /v1/Services/{ChatServiceSid}/Conversations/{Sid}:
              description: >-
                A Service Conversation resource represents an omnichannel group
                conversation with an ordered list of messages and a participant
                roster.
              post:
                description: Update an existing conversation in your service
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
                  - Conversation
                  - Messages
                  - Message
                  - Receipts
                  - Participants
                  - Credentials
                  - Participant
                  - Roles
                  - Services
                  - Chat
                  - Service
                  - Bindings
              delete:
                description: Remove a conversation from your service
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
                  - Conversation
                  - Messages
                  - Message
                  - Receipts
                  - Participants
                  - Credentials
                  - Participant
                  - Roles
                  - Services
                  - Chat
                  - Service
                  - Bindings
              get:
                description: Fetch a conversation from your service
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
                  - Conversation
                  - Messages
                  - Message
                  - Receipts
                  - Participants
                  - Credentials
                  - Participant
                  - Roles
                  - Services
                  - Chat
                  - Service
                  - Bindings
            /v1/Services/{ChatServiceSid}/Conversations/{ConversationSid}/Messages:
              description: >-
                A Service Message resource represents a message in a
                conversation within a specific service.
              post:
                description: Add a new message to the conversation in a specific service
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
                  - Conversation
                  - Messages
                  - Message
                  - Receipts
                  - Participants
                  - Credentials
                  - Participant
                  - Roles
                  - Services
                  - Chat
                  - Service
                  - Bindings
              get:
                description: Retrieve a list of all messages in the conversation
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
                  - Conversation
                  - Messages
                  - Message
                  - Receipts
                  - Participants
                  - Credentials
                  - Participant
                  - Roles
                  - Services
                  - Chat
                  - Service
                  - Bindings
            /v1/Services/{ChatServiceSid}/Conversations/{ConversationSid}/Messages/{Sid}:
              description: >-
                A Service Message resource represents a message in a
                conversation within a specific service.
              post:
                description: Update an existing message in the conversation
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
                  - Conversation
                  - Messages
                  - Message
                  - Receipts
                  - Participants
                  - Credentials
                  - Participant
                  - Roles
                  - Services
                  - Chat
                  - Service
                  - Bindings
              delete:
                description: Remove a message from the conversation
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
                  - Conversation
                  - Messages
                  - Message
                  - Receipts
                  - Participants
                  - Credentials
                  - Participant
                  - Roles
                  - Services
                  - Chat
                  - Service
                  - Bindings
              get:
                description: Fetch a message from the conversation
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
                  - Conversation
                  - Messages
                  - Message
                  - Receipts
                  - Participants
                  - Credentials
                  - Participant
                  - Roles
                  - Services
                  - Chat
                  - Service
                  - Bindings
            /v1/Services/{ChatServiceSid}/Conversations/{ConversationSid}/Messages/{MessageSid}/Receipts/{Sid}:
              description: >-
                A Service Message Receipt resource represents a delivery/read
                receipt of a message in a conversation.
              get:
                description: >-
                  Fetch the delivery and read receipts of the conversation
                  message
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
                  - Conversation
                  - Messages
                  - Message
                  - Receipts
                  - Participants
                  - Credentials
                  - Participant
                  - Roles
                  - Services
                  - Chat
                  - Service
                  - Bindings
            /v1/Services/{ChatServiceSid}/Conversations/{ConversationSid}/Messages/{MessageSid}/Receipts:
              description: >-
                A Service Message Receipt resource represents a delivery/read
                receipt of a message in a conversation.
              get:
                description: >-
                  Retrieve a list of all delivery and read receipts of the
                  conversation message
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
                  - Conversation
                  - Messages
                  - Message
                  - Receipts
                  - Participants
                  - Credentials
                  - Participant
                  - Roles
                  - Services
                  - Chat
                  - Service
                  - Bindings
            /v1/Services/{ChatServiceSid}/Conversations/{ConversationSid}/Participants:
              description: >-
                A Service Participant resource represents a member of the
                conversation within a specific service.
              post:
                description: >-
                  Add a new participant to the conversation in a specific
                  service
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
                  - Conversation
                  - Messages
                  - Message
                  - Receipts
                  - Participants
                  - Credentials
                  - Participant
                  - Roles
                  - Services
                  - Chat
                  - Service
                  - Bindings
              get:
                description: Retrieve a list of all participants of the conversation
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
                  - Conversation
                  - Messages
                  - Message
                  - Receipts
                  - Participants
                  - Credentials
                  - Participant
                  - Roles
                  - Services
                  - Chat
                  - Service
                  - Bindings
            /v1/Services/{ChatServiceSid}/Conversations/{ConversationSid}/Participants/{Sid}:
              description: >-
                A Service Participant resource represents a member of the
                conversation within a specific service.
              post:
                description: Update an existing participant in the conversation
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
                  - Conversation
                  - Messages
                  - Message
                  - Receipts
                  - Participants
                  - Credentials
                  - Participant
                  - Roles
                  - Services
                  - Chat
                  - Service
                  - Bindings
              delete:
                description: Remove a participant from the conversation
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
                  - Conversation
                  - Messages
                  - Message
                  - Receipts
                  - Participants
                  - Credentials
                  - Participant
                  - Roles
                  - Services
                  - Chat
                  - Service
                  - Bindings
              get:
                description: Fetch a participant of the conversation
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
                  - Conversation
                  - Messages
                  - Message
                  - Receipts
                  - Participants
                  - Credentials
                  - Participant
                  - Roles
                  - Services
                  - Chat
                  - Service
                  - Bindings
            /v1/Services/{ChatServiceSid}/Conversations/{ConversationSid}/Webhooks:
              description: >-
                A Conversation-scoped Webhook resource manages a set of callback
                URLs and their configuration for receiving events specific to
                one conversation.
              post:
                description: >-
                  Create a new webhook scoped to the conversation in a specific
                  service
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
                  - Conversation
                  - Messages
                  - Message
                  - Receipts
                  - Participants
                  - Credentials
                  - Participant
                  - Roles
                  - Services
                  - Chat
                  - Service
                  - Bindings
              get:
                description: Retrieve a list of all webhooks scoped to the conversation
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
                  - Conversation
                  - Messages
                  - Message
                  - Receipts
                  - Participants
                  - Credentials
                  - Participant
                  - Roles
                  - Services
                  - Chat
                  - Service
                  - Bindings
            /v1/Services/{ChatServiceSid}/Conversations/{ConversationSid}/Webhooks/{Sid}:
              description: >-
                A Conversation-scoped Webhook resource manages a set of callback
                URLs and their configuration for receiving events specific to
                one conversation.
              post:
                description: Update an existing conversation-scoped webhook
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
                  - Conversation
                  - Messages
                  - Message
                  - Receipts
                  - Participants
                  - Credentials
                  - Participant
                  - Roles
                  - Services
                  - Chat
                  - Service
                  - Bindings
              delete:
                description: Remove an existing webhook scoped to the conversation
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
                  - Conversation
                  - Messages
                  - Message
                  - Receipts
                  - Participants
                  - Credentials
                  - Participant
                  - Roles
                  - Services
                  - Chat
                  - Service
                  - Bindings
              get:
                description: Fetch the configuration of a conversation-scoped webhook
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
                  - Conversation
                  - Messages
                  - Message
                  - Receipts
                  - Participants
                  - Credentials
                  - Participant
                  - Roles
                  - Services
                  - Chat
                  - Service
                  - Bindings
            /v1/Services/{ChatServiceSid}/Configuration/Notifications:
              description: >-
                A Service Notification resource manages a set of settings to
                determine push notification behavior at service level.
              post:
                description: Update push notification service settings
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
                  - Conversation
                  - Messages
                  - Message
                  - Receipts
                  - Participants
                  - Credentials
                  - Participant
                  - Roles
                  - Services
                  - Chat
                  - Service
                  - Bindings
                  - Notifications
              get:
                description: Fetch push notification service settings
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
                  - Conversation
                  - Messages
                  - Message
                  - Receipts
                  - Participants
                  - Credentials
                  - Participant
                  - Roles
                  - Services
                  - Chat
                  - Service
                  - Bindings
                  - Notifications
            /v1/Services/{ChatServiceSid}/ParticipantConversations:
              description: >-
                Service Participant Conversations resource represents a list of
                Conversations that this Participant belongs to belonging to a
                specific conversation service.
              get:
                description: >-
                  Retrieve a list of all Conversations that this Participant
                  belongs to by identity or by address. Only one parameter
                  should be specified.
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
                  - Conversation
                  - Messages
                  - Message
                  - Receipts
                  - Participants
                  - Credentials
                  - Participant
                  - Roles
                  - Services
                  - Chat
                  - Service
                  - Bindings
                  - Notifications
            /v1/Services/{ChatServiceSid}/Roles:
              description: >-
                A Service Role resource represents a set of permissions granted
                to a user within a service or a conversation.
              post:
                description: Create a new user role in your service
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
                  - Conversation
                  - Messages
                  - Message
                  - Receipts
                  - Participants
                  - Credentials
                  - Participant
                  - Roles
                  - Services
                  - Chat
                  - Service
                  - Bindings
                  - Notifications
              get:
                description: Retrieve a list of all user roles in your service
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
                  - Conversation
                  - Messages
                  - Message
                  - Receipts
                  - Participants
                  - Credentials
                  - Participant
                  - Roles
                  - Services
                  - Chat
                  - Service
                  - Bindings
                  - Notifications
            /v1/Services/{ChatServiceSid}/Roles/{Sid}:
              description: >-
                A Service Role resource represents a set of permissions granted
                to a user within a service or a conversation.
              post:
                description: Update an existing user role in your service
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
                  - Conversation
                  - Messages
                  - Message
                  - Receipts
                  - Participants
                  - Credentials
                  - Participant
                  - Roles
                  - Services
                  - Chat
                  - Service
                  - Bindings
                  - Notifications
              delete:
                description: Remove a user role from your service
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
                  - Conversation
                  - Messages
                  - Message
                  - Receipts
                  - Participants
                  - Credentials
                  - Participant
                  - Roles
                  - Services
                  - Chat
                  - Service
                  - Bindings
                  - Notifications
              get:
                description: Fetch a user role from your service
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
                  - Conversation
                  - Messages
                  - Message
                  - Receipts
                  - Participants
                  - Credentials
                  - Participant
                  - Roles
                  - Services
                  - Chat
                  - Service
                  - Bindings
                  - Notifications
            /v1/Services/{ChatServiceSid}/Users:
              description: >-
                A Service User resource represents a conversation user belonging
                to a specific conversation service.
              post:
                description: Add a new conversation user to your service
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
                  - Conversation
                  - Messages
                  - Message
                  - Receipts
                  - Participants
                  - Credentials
                  - Participant
                  - Roles
                  - Services
                  - Chat
                  - Service
                  - Bindings
                  - Notifications
                  - Users
              get:
                description: Retrieve a list of all conversation users in your service
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
                  - Conversation
                  - Messages
                  - Message
                  - Receipts
                  - Participants
                  - Credentials
                  - Participant
                  - Roles
                  - Services
                  - Chat
                  - Service
                  - Bindings
                  - Notifications
                  - Users
            /v1/Services/{ChatServiceSid}/Users/{Sid}:
              description: >-
                A Service User resource represents a conversation user belonging
                to a specific conversation service.
              post:
                description: Update an existing conversation user in your service
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
                  - Conversation
                  - Messages
                  - Message
                  - Receipts
                  - Participants
                  - Credentials
                  - Participant
                  - Roles
                  - Services
                  - Chat
                  - Service
                  - Bindings
                  - Notifications
                  - Users
              delete:
                description: Remove a conversation user from your service
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
                  - Conversation
                  - Messages
                  - Message
                  - Receipts
                  - Participants
                  - Credentials
                  - Participant
                  - Roles
                  - Services
                  - Chat
                  - Service
                  - Bindings
                  - Notifications
                  - Users
              get:
                description: Fetch a conversation user from your service
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
                  - Conversation
                  - Messages
                  - Message
                  - Receipts
                  - Participants
                  - Credentials
                  - Participant
                  - Roles
                  - Services
                  - Chat
                  - Service
                  - Bindings
                  - Notifications
                  - Users
            /v1/Services/{ChatServiceSid}/Users/{UserSid}/Conversations/{ConversationSid}:
              description: >-
                A Service User Conversation resource represents a conversation
                of the user belonging to a specific conversation service.
              post:
                description: Update a specific User Conversation.
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
                  - Conversation
                  - Messages
                  - Message
                  - Receipts
                  - Participants
                  - Credentials
                  - Participant
                  - Roles
                  - Services
                  - Chat
                  - Service
                  - Bindings
                  - Notifications
                  - Users
                  - User
              delete:
                description: Delete a specific User Conversation.
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
                  - Conversation
                  - Messages
                  - Message
                  - Receipts
                  - Participants
                  - Credentials
                  - Participant
                  - Roles
                  - Services
                  - Chat
                  - Service
                  - Bindings
                  - Notifications
                  - Users
                  - User
              get:
                description: Fetch a specific User Conversation.
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
                  - Conversation
                  - Messages
                  - Message
                  - Receipts
                  - Participants
                  - Credentials
                  - Participant
                  - Roles
                  - Services
                  - Chat
                  - Service
                  - Bindings
                  - Notifications
                  - Users
                  - User
            /v1/Services/{ChatServiceSid}/Users/{UserSid}/Conversations:
              description: >-
                A Service User Conversation resource represents a conversation
                of the user belonging to a specific conversation service.
              get:
                description: Retrieve a list of all User Conversations for the User.
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
                  - Conversation
                  - Messages
                  - Message
                  - Receipts
                  - Participants
                  - Credentials
                  - Participant
                  - Roles
                  - Services
                  - Chat
                  - Service
                  - Bindings
                  - Notifications
                  - Users
                  - User
            /v1/Services/{ChatServiceSid}/Configuration/Webhooks:
              description: >-
                A service webhook configuration resource manages a service-level
                set of callback URLs and their configuration for receiving all
                the corresponding service events.
              post:
                description: Update a specific Webhook.
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
                  - Conversation
                  - Messages
                  - Message
                  - Receipts
                  - Participants
                  - Credentials
                  - Participant
                  - Roles
                  - Services
                  - Chat
                  - Service
                  - Bindings
                  - Notifications
                  - Users
                  - User
              get:
                description: Fetch a specific service webhook configuration.
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
                  - Conversation
                  - Messages
                  - Message
                  - Receipts
                  - Participants
                  - Credentials
                  - Participant
                  - Roles
                  - Services
                  - Chat
                  - Service
                  - Bindings
                  - Notifications
                  - Users
                  - User
            /v1/Users:
              description: >-
                A User resource represents a conversation user belonging to a
                default conversation service.
              post:
                description: Add a new conversation user to your account's default service
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
                  - Conversation
                  - Messages
                  - Message
                  - Receipts
                  - Participants
                  - Credentials
                  - Participant
                  - Roles
                  - Services
                  - Chat
                  - Service
                  - Bindings
                  - Notifications
                  - Users
                  - User
              get:
                description: >-
                  Retrieve a list of all conversation users in your account's
                  default service
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
                  - Conversation
                  - Messages
                  - Message
                  - Receipts
                  - Participants
                  - Credentials
                  - Participant
                  - Roles
                  - Services
                  - Chat
                  - Service
                  - Bindings
                  - Notifications
                  - Users
                  - User
            /v1/Users/{Sid}:
              description: >-
                A User resource represents a conversation user belonging to a
                default conversation service.
              post:
                description: >-
                  Update an existing conversation user in your account's default
                  service
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
                  - Conversation
                  - Messages
                  - Message
                  - Receipts
                  - Participants
                  - Credentials
                  - Participant
                  - Roles
                  - Services
                  - Chat
                  - Service
                  - Bindings
                  - Notifications
                  - Users
                  - User
              delete:
                description: Remove a conversation user from your account's default service
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
                  - Conversation
                  - Messages
                  - Message
                  - Receipts
                  - Participants
                  - Credentials
                  - Participant
                  - Roles
                  - Services
                  - Chat
                  - Service
                  - Bindings
                  - Notifications
                  - Users
                  - User
              get:
                description: Fetch a conversation user from your account's default service
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
                  - Conversation
                  - Messages
                  - Message
                  - Receipts
                  - Participants
                  - Credentials
                  - Participant
                  - Roles
                  - Services
                  - Chat
                  - Service
                  - Bindings
                  - Notifications
                  - Users
                  - User
            /v1/Users/{UserSid}/Conversations/{ConversationSid}:
              description: >-
                A User Conversation resource represents a conversation of the
                user belonging to a default conversation service.
              post:
                description: Update a specific User Conversation.
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
                  - Conversation
                  - Messages
                  - Message
                  - Receipts
                  - Participants
                  - Credentials
                  - Participant
                  - Roles
                  - Services
                  - Chat
                  - Service
                  - Bindings
                  - Notifications
                  - Users
                  - User
              delete:
                description: Delete a specific User Conversation.
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
                  - Conversation
                  - Messages
                  - Message
                  - Receipts
                  - Participants
                  - Credentials
                  - Participant
                  - Roles
                  - Services
                  - Chat
                  - Service
                  - Bindings
                  - Notifications
                  - Users
                  - User
              get:
                description: Fetch a specific User Conversation.
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
                  - Conversation
                  - Messages
                  - Message
                  - Receipts
                  - Participants
                  - Credentials
                  - Participant
                  - Roles
                  - Services
                  - Chat
                  - Service
                  - Bindings
                  - Notifications
                  - Users
                  - User
            /v1/Users/{UserSid}/Conversations:
              description: >-
                A User Conversation resource represents a conversation of the
                user belonging to a default conversation service.
              get:
                description: Retrieve a list of all User Conversations for the User.
                tags:
                  - Configuration
                  - Addresses
                  - Sid
                  - Webhooks
                  - Conversations
                  - Conversation
                  - Messages
                  - Message
                  - Receipts
                  - Participants
                  - Credentials
                  - Participant
                  - Roles
                  - Services
                  - Chat
                  - Service
                  - Bindings
                  - Notifications
                  - Users
                  - User
          tags:
            - name: ConversationsV1AddressConfiguration
            - name: ConversationsV1Binding
            - name: ConversationsV1Configuration
            - name: ConversationsV1Conversation
            - name: ConversationsV1Credential
            - name: ConversationsV1DeliveryReceipt
            - name: ConversationsV1Message
            - name: ConversationsV1Notification
            - name: ConversationsV1Participant
            - name: ConversationsV1ParticipantConversation
            - name: ConversationsV1Role
            - name: ConversationsV1Service
            - name: ConversationsV1User
            - name: ConversationsV1UserConversation
            - name: ConversationsV1Webhook
          x-maturity:
            - name: GA
              description: This product is G
    overlays:
      - type: APIs.io Search
        url: overlays/conversations-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/conversations-openapi-api-evangelist-ratings.yml
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
  - aid: twilio:twilio-notify-api
    name: Twilio Notify API
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
            title: Twilio - Notify
            license:
              name: Apache 2.0
              url: https://www.apache.org/licenses/LICENSE-2.0.html
          openapi: 3.0.1
          paths:
            /v1/Services/{ServiceSid}/Bindings/{Sid}:
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
            /v1/Services/{ServiceSid}/Bindings:
              description: 'TODO: Resource-level docs'
              post:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Bindings
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Bindings
            /v1/Credentials:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Bindings
                  - Credentials
              post:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Bindings
                  - Credentials
            /v1/Credentials/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Bindings
                  - Credentials
              post:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Bindings
                  - Credentials
              delete:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Bindings
                  - Credentials
            /v1/Services/{ServiceSid}/Notifications:
              description: 'TODO: Resource-level docs'
              post:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Bindings
                  - Credentials
                  - Notifications
            /v1/Services:
              description: 'TODO: Resource-level docs'
              post:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Bindings
                  - Credentials
                  - Notifications
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Bindings
                  - Credentials
                  - Notifications
            /v1/Services/{Sid}:
              description: 'TODO: Resource-level docs'
              delete:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Bindings
                  - Credentials
                  - Notifications
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Bindings
                  - Credentials
                  - Notifications
              post:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Bindings
                  - Credentials
                  - Notifications
          tags:
            - name: NotifyV1Binding
            - name: NotifyV1Credential
            - name: NotifyV1Notification
            - name: NotifyV1Service
          x-maturity:
            - name: Beta
              description: >-
                PLEASE NOTE that this is a Beta product that is subject to
                change. U
    overlays:
      - type: APIs.io Search
        url: overlays/notify-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/notify-openapi-api-evangelist-ratings.yml
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---