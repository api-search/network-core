---
name: Anonymize
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/anonymize.png
url: https://example.com/apis/anonymize.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Anonymize
apis:
  - aid: twilio:twilio-video-api
    name: Twilio Video API
    description: >-
      Twilio Video is a programmable real-time communications platform that
      allows you to add video chat functionality to your web, iOS, and Android
      applications. The platform provides APIs, SDKs, and helper tools to
      capture, distribute, record, and render high quality audio and video
      applications.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://www.twilio.com/docs/video
    baseURL: https:/api.twilio.com
    tags: []
    properties:
      - type: Documentation
        url: https://www.twilio.com/docs/video
      - type: OpenAPI
        data:
          info:
            title: Twilio - Video
            license:
              name: Apache 2.0
              url: https://www.apache.org/licenses/LICENSE-2.0.html
          openapi: 3.0.1
          paths:
            /v1/Compositions/{Sid}:
              description: Recording compositions
              get:
                description: >-
                  Returns a single Composition resource identified by a
                  Composition SID.
                tags:
                  - Compositions
                  - Sid
              delete:
                description: >-
                  Delete a Recording Composition resource identified by a
                  Composition SID.
                tags:
                  - Compositions
                  - Sid
            /v1/Compositions:
              description: Recording compositions
              get:
                description: List of all Recording compositions.
                tags:
                  - Compositions
                  - Sid
              post:
                description: ''
                tags:
                  - Compositions
                  - Sid
            /v1/CompositionHooks/{Sid}:
              description: Recording composition hooks
              get:
                description: >-
                  Returns a single CompositionHook resource identified by a
                  CompositionHook SID.
                tags:
                  - Compositions
                  - Sid
                  - Composition
                  - Hooks
              delete:
                description: >-
                  Delete a Recording CompositionHook resource identified by a
                  `CompositionHook SID`.
                tags:
                  - Compositions
                  - Sid
                  - Composition
                  - Hooks
              post:
                description: ''
                tags:
                  - Compositions
                  - Sid
                  - Composition
                  - Hooks
            /v1/CompositionHooks:
              description: Recording composition hooks
              get:
                description: List of all Recording CompositionHook resources.
                tags:
                  - Compositions
                  - Sid
                  - Composition
                  - Hooks
              post:
                description: ''
                tags:
                  - Compositions
                  - Sid
                  - Composition
                  - Hooks
            /v1/CompositionSettings/Default:
              description: Recording composition settings
              get:
                description: ''
                tags:
                  - Compositions
                  - Sid
                  - Composition
                  - Hooks
                  - Settings
                  - Default
              post:
                description: ''
                tags:
                  - Compositions
                  - Sid
                  - Composition
                  - Hooks
                  - Settings
                  - Default
            /v1/Recordings/{Sid}:
              description: Single-track, single-media recordings
              get:
                description: >-
                  Returns a single Recording resource identified by a Recording
                  SID.
                tags:
                  - Compositions
                  - Sid
                  - Composition
                  - Hooks
                  - Settings
                  - Default
                  - Recordings
              delete:
                description: Delete a Recording resource identified by a Recording SID.
                tags:
                  - Compositions
                  - Sid
                  - Composition
                  - Hooks
                  - Settings
                  - Default
                  - Recordings
            /v1/Recordings:
              description: Single-track, single-media recordings
              get:
                description: List of all Track recordings.
                tags:
                  - Compositions
                  - Sid
                  - Composition
                  - Hooks
                  - Settings
                  - Default
                  - Recordings
            /v1/RecordingSettings/Default:
              description: Recording settings
              get:
                description: ''
                tags:
                  - Compositions
                  - Sid
                  - Composition
                  - Hooks
                  - Settings
                  - Default
                  - Recordings
                  - Recording
              post:
                description: ''
                tags:
                  - Compositions
                  - Sid
                  - Composition
                  - Hooks
                  - Settings
                  - Default
                  - Recordings
                  - Recording
            /v1/Rooms/{Sid}:
              description: Video rooms with one or more participants
              get:
                description: ''
                tags:
                  - Compositions
                  - Sid
                  - Composition
                  - Hooks
                  - Settings
                  - Default
                  - Recordings
                  - Recording
                  - Rooms
              post:
                description: ''
                tags:
                  - Compositions
                  - Sid
                  - Composition
                  - Hooks
                  - Settings
                  - Default
                  - Recordings
                  - Recording
                  - Rooms
            /v1/Rooms:
              description: Video rooms with one or more participants
              post:
                description: ''
                tags:
                  - Compositions
                  - Sid
                  - Composition
                  - Hooks
                  - Settings
                  - Default
                  - Recordings
                  - Recording
                  - Rooms
              get:
                description: ''
                tags:
                  - Compositions
                  - Sid
                  - Composition
                  - Hooks
                  - Settings
                  - Default
                  - Recordings
                  - Recording
                  - Rooms
            /v1/Rooms/{RoomSid}/Participants/{Sid}:
              description: Participants in video rooms
              get:
                description: ''
                tags:
                  - Compositions
                  - Sid
                  - Composition
                  - Hooks
                  - Settings
                  - Default
                  - Recordings
                  - Recording
                  - Rooms
                  - Room
                  - Participants
              post:
                description: ''
                tags:
                  - Compositions
                  - Sid
                  - Composition
                  - Hooks
                  - Settings
                  - Default
                  - Recordings
                  - Recording
                  - Rooms
                  - Room
                  - Participants
            /v1/Rooms/{RoomSid}/Participants:
              description: Participants in video rooms
              get:
                description: ''
                tags:
                  - Compositions
                  - Sid
                  - Composition
                  - Hooks
                  - Settings
                  - Default
                  - Recordings
                  - Recording
                  - Rooms
                  - Room
                  - Participants
            /v1/Rooms/{RoomSid}/Participants/{Sid}/Anonymize:
              description: 'TODO: Resource-level docs'
              post:
                description: ''
                tags:
                  - Compositions
                  - Sid
                  - Composition
                  - Hooks
                  - Settings
                  - Default
                  - Recordings
                  - Recording
                  - Rooms
                  - Room
                  - Participants
                  - Anonymize
            /v1/Rooms/{RoomSid}/Participants/{ParticipantSid}/PublishedTracks/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: >-
                  Returns a single Track resource represented by TrackName or
                  SID.
                tags:
                  - Compositions
                  - Sid
                  - Composition
                  - Hooks
                  - Settings
                  - Default
                  - Recordings
                  - Recording
                  - Rooms
                  - Room
                  - Participants
                  - Anonymize
                  - Participant
                  - Published
                  - Tracks
            /v1/Rooms/{RoomSid}/Participants/{ParticipantSid}/PublishedTracks:
              description: 'TODO: Resource-level docs'
              get:
                description: >-
                  Returns a list of tracks associated with a given Participant.
                  Only `currently` Published Tracks are in the list resource.
                tags:
                  - Compositions
                  - Sid
                  - Composition
                  - Hooks
                  - Settings
                  - Default
                  - Recordings
                  - Recording
                  - Rooms
                  - Room
                  - Participants
                  - Anonymize
                  - Participant
                  - Published
                  - Tracks
            /v1/Rooms/{RoomSid}/Participants/{ParticipantSid}/SubscribeRules:
              description: 'TODO: Resource-level docs'
              get:
                description: Returns a list of Subscribe Rules for the Participant.
                tags:
                  - Compositions
                  - Sid
                  - Composition
                  - Hooks
                  - Settings
                  - Default
                  - Recordings
                  - Recording
                  - Rooms
                  - Room
                  - Participants
                  - Anonymize
                  - Participant
                  - Published
                  - Tracks
                  - Subscribe
                  - Rules
              post:
                description: Update the Subscribe Rules for the Participant
                tags:
                  - Compositions
                  - Sid
                  - Composition
                  - Hooks
                  - Settings
                  - Default
                  - Recordings
                  - Recording
                  - Rooms
                  - Room
                  - Participants
                  - Anonymize
                  - Participant
                  - Published
                  - Tracks
                  - Subscribe
                  - Rules
            /v1/Rooms/{RoomSid}/Participants/{ParticipantSid}/SubscribedTracks/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: >-
                  Returns a single Track resource represented by `track_sid`. 
                  Note: This is one resource with the Video API that requires a
                  SID, be Track Name on the subscriber side is not guaranteed to
                  be unique.
                tags:
                  - Compositions
                  - Sid
                  - Composition
                  - Hooks
                  - Settings
                  - Default
                  - Recordings
                  - Recording
                  - Rooms
                  - Room
                  - Participants
                  - Anonymize
                  - Participant
                  - Published
                  - Tracks
                  - Subscribe
                  - Rules
                  - Subscribed
            /v1/Rooms/{RoomSid}/Participants/{ParticipantSid}/SubscribedTracks:
              description: 'TODO: Resource-level docs'
              get:
                description: >-
                  Returns a list of tracks that are subscribed for the
                  participant.
                tags:
                  - Compositions
                  - Sid
                  - Composition
                  - Hooks
                  - Settings
                  - Default
                  - Recordings
                  - Recording
                  - Rooms
                  - Room
                  - Participants
                  - Anonymize
                  - Participant
                  - Published
                  - Tracks
                  - Subscribe
                  - Rules
                  - Subscribed
            /v1/Rooms/{RoomSid}/Recordings/{Sid}:
              description: Single-track, single-media room recordings
              get:
                description: ''
                tags:
                  - Compositions
                  - Sid
                  - Composition
                  - Hooks
                  - Settings
                  - Default
                  - Recordings
                  - Recording
                  - Rooms
                  - Room
                  - Participants
                  - Anonymize
                  - Participant
                  - Published
                  - Tracks
                  - Subscribe
                  - Rules
                  - Subscribed
              delete:
                description: ''
                tags:
                  - Compositions
                  - Sid
                  - Composition
                  - Hooks
                  - Settings
                  - Default
                  - Recordings
                  - Recording
                  - Rooms
                  - Room
                  - Participants
                  - Anonymize
                  - Participant
                  - Published
                  - Tracks
                  - Subscribe
                  - Rules
                  - Subscribed
            /v1/Rooms/{RoomSid}/Recordings:
              description: Single-track, single-media room recordings
              get:
                description: ''
                tags:
                  - Compositions
                  - Sid
                  - Composition
                  - Hooks
                  - Settings
                  - Default
                  - Recordings
                  - Recording
                  - Rooms
                  - Room
                  - Participants
                  - Anonymize
                  - Participant
                  - Published
                  - Tracks
                  - Subscribe
                  - Rules
                  - Subscribed
            /v1/Rooms/{RoomSid}/RecordingRules:
              description: 'TODO: Resource-level docs'
              get:
                description: Returns a list of Recording Rules for the Room.
                tags:
                  - Compositions
                  - Sid
                  - Composition
                  - Hooks
                  - Settings
                  - Default
                  - Recordings
                  - Recording
                  - Rooms
                  - Room
                  - Participants
                  - Anonymize
                  - Participant
                  - Published
                  - Tracks
                  - Subscribe
                  - Rules
                  - Subscribed
              post:
                description: Update the Recording Rules for the Room
                tags:
                  - Compositions
                  - Sid
                  - Composition
                  - Hooks
                  - Settings
                  - Default
                  - Recordings
                  - Recording
                  - Rooms
                  - Room
                  - Participants
                  - Anonymize
                  - Participant
                  - Published
                  - Tracks
                  - Subscribe
                  - Rules
                  - Subscribed
          tags:
            - name: VideoV1Anonymize
            - name: VideoV1Composition
            - name: VideoV1CompositionHook
            - name: VideoV1CompositionSettings
            - name: VideoV1Participant
            - name: VideoV1PublishedTrack
            - name: VideoV1Recording
            - name: VideoV1RecordingRules
            - name: VideoV1RecordingSettings
            - name: VideoV1Room
            - name: VideoV1RoomRecording
            - name: VideoV1SubscribeRules
            - name: VideoV1SubscribedTrack
          x-maturity:
            - name: GA
              description: This product is G
    overlays:
      - type: APIs.io Search
        url: overlays/video-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/video-openapi-api-evangelist-ratings.yml
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---