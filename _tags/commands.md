---
name: Commands
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/commands.png
url: https://example.com/apis/commands.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Commands
apis:
  - aid: twilio:twilio-super-sim-api
    name: Twilio Super SIM API
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
            title: Twilio - Supersim
            license:
              name: Apache 2.0
              url: https://www.apache.org/licenses/LICENSE-2.0.html
          openapi: 3.0.1
          paths:
            /v1/Sims/{SimSid}/BillingPeriods:
              description: Billing Period for an IoT Super SIM
              get:
                description: Retrieve a list of Billing Periods for a Super SIM.
                tags:
                  - Sims
                  - Sim
                  - Sid
                  - Billing
                  - Periods
            /v1/ESimProfiles:
              description: eSIM Profiles that can be loaded onto consumer eUICC SIMs
              post:
                description: Order an eSIM Profile.
                tags:
                  - Sims
                  - Sim
                  - Sid
                  - Billing
                  - Periods
                  - Profiles
              get:
                description: Retrieve a list of eSIM Profiles.
                tags:
                  - Sims
                  - Sim
                  - Sid
                  - Billing
                  - Periods
                  - Profiles
            /v1/ESimProfiles/{Sid}:
              description: eSIM Profiles that can be loaded onto consumer eUICC SIMs
              get:
                description: Fetch an eSIM Profile.
                tags:
                  - Sims
                  - Sim
                  - Sid
                  - Billing
                  - Periods
                  - Profiles
            /v1/Fleets:
              description: >-
                Configure shared settings inherited by all Super SIMs assigned
                to the Fleet
              post:
                description: Create a Fleet
                tags:
                  - Sims
                  - Sim
                  - Sid
                  - Billing
                  - Periods
                  - Profiles
                  - Fleets
              get:
                description: Retrieve a list of Fleets from your account.
                tags:
                  - Sims
                  - Sim
                  - Sid
                  - Billing
                  - Periods
                  - Profiles
                  - Fleets
            /v1/Fleets/{Sid}:
              description: >-
                Configure shared settings inherited by all Super SIMs assigned
                to the Fleet
              get:
                description: Fetch a Fleet instance from your account.
                tags:
                  - Sims
                  - Sim
                  - Sid
                  - Billing
                  - Periods
                  - Profiles
                  - Fleets
              post:
                description: >-
                  Updates the given properties of a Super SIM Fleet instance
                  from your account.
                tags:
                  - Sims
                  - Sim
                  - Sid
                  - Billing
                  - Periods
                  - Profiles
                  - Fleets
            /v1/IpCommands:
              description: Machine-to-machine IP Commands sent to/from Super SIMs
              post:
                description: Send an IP Command to a Super SIM.
                tags:
                  - Sims
                  - Sim
                  - Sid
                  - Billing
                  - Periods
                  - Profiles
                  - Fleets
                  - Ip
                  - Commands
              get:
                description: Retrieve a list of IP Commands from your account.
                tags:
                  - Sims
                  - Sim
                  - Sid
                  - Billing
                  - Periods
                  - Profiles
                  - Fleets
                  - Ip
                  - Commands
            /v1/IpCommands/{Sid}:
              description: Machine-to-machine IP Commands sent to/from Super SIMs
              get:
                description: Fetch IP Command instance from your account.
                tags:
                  - Sims
                  - Sim
                  - Sid
                  - Billing
                  - Periods
                  - Profiles
                  - Fleets
                  - Ip
                  - Commands
            /v1/Networks/{Sid}:
              description: Mobile operator networks to which Super SIMs can connect
              get:
                description: Fetch a Network resource.
                tags:
                  - Sims
                  - Sim
                  - Sid
                  - Billing
                  - Periods
                  - Profiles
                  - Fleets
                  - Ip
                  - Commands
                  - Networks
            /v1/Networks:
              description: Mobile operator networks to which Super SIMs can connect
              get:
                description: Retrieve a list of Network resources.
                tags:
                  - Sims
                  - Sim
                  - Sid
                  - Billing
                  - Periods
                  - Profiles
                  - Fleets
                  - Ip
                  - Commands
                  - Networks
            /v1/NetworkAccessProfiles:
              description: 'TODO: Resource-level docs'
              post:
                description: Create a new Network Access Profile
                tags:
                  - Sims
                  - Sim
                  - Sid
                  - Billing
                  - Periods
                  - Profiles
                  - Fleets
                  - Ip
                  - Commands
                  - Networks
                  - Network
                  - Access
              get:
                description: Retrieve a list of Network Access Profiles from your account.
                tags:
                  - Sims
                  - Sim
                  - Sid
                  - Billing
                  - Periods
                  - Profiles
                  - Fleets
                  - Ip
                  - Commands
                  - Networks
                  - Network
                  - Access
            /v1/NetworkAccessProfiles/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: Fetch a Network Access Profile instance from your account.
                tags:
                  - Sims
                  - Sim
                  - Sid
                  - Billing
                  - Periods
                  - Profiles
                  - Fleets
                  - Ip
                  - Commands
                  - Networks
                  - Network
                  - Access
              post:
                description: >-
                  Updates the given properties of a Network Access Profile in
                  your account.
                tags:
                  - Sims
                  - Sim
                  - Sid
                  - Billing
                  - Periods
                  - Profiles
                  - Fleets
                  - Ip
                  - Commands
                  - Networks
                  - Network
                  - Access
            /v1/NetworkAccessProfiles/{NetworkAccessProfileSid}/Networks:
              description: >-
                Mobile operator networks which Network Access Profiles allow
                access to
              get:
                description: >-
                  Retrieve a list of Network Access Profile resource's Network
                  resource.
                tags:
                  - Sims
                  - Sim
                  - Sid
                  - Billing
                  - Periods
                  - Profiles
                  - Fleets
                  - Ip
                  - Commands
                  - Networks
                  - Network
                  - Access
                  - Profile
              post:
                description: Add a Network resource to the Network Access Profile resource.
                tags:
                  - Sims
                  - Sim
                  - Sid
                  - Billing
                  - Periods
                  - Profiles
                  - Fleets
                  - Ip
                  - Commands
                  - Networks
                  - Network
                  - Access
                  - Profile
            /v1/NetworkAccessProfiles/{NetworkAccessProfileSid}/Networks/{Sid}:
              description: >-
                Mobile operator networks which Network Access Profiles allow
                access to
              delete:
                description: >-
                  Remove a Network resource from the Network Access Profile
                  resource's.
                tags:
                  - Sims
                  - Sim
                  - Sid
                  - Billing
                  - Periods
                  - Profiles
                  - Fleets
                  - Ip
                  - Commands
                  - Networks
                  - Network
                  - Access
                  - Profile
              get:
                description: Fetch a Network Access Profile resource's Network resource.
                tags:
                  - Sims
                  - Sim
                  - Sid
                  - Billing
                  - Periods
                  - Profiles
                  - Fleets
                  - Ip
                  - Commands
                  - Networks
                  - Network
                  - Access
                  - Profile
            /v1/SettingsUpdates:
              description: 'TODO: Resource-level docs'
              get:
                description: Retrieve a list of Settings Updates.
                tags:
                  - Sims
                  - Sim
                  - Sid
                  - Billing
                  - Periods
                  - Profiles
                  - Fleets
                  - Ip
                  - Commands
                  - Networks
                  - Network
                  - Access
                  - Profile
                  - Settings
                  - Updates
            /v1/Sims:
              description: Individual IoT Super SIMs
              post:
                description: Register a Super SIM to your Account
                tags:
                  - Sims
                  - Sim
                  - Sid
                  - Billing
                  - Periods
                  - Profiles
                  - Fleets
                  - Ip
                  - Commands
                  - Networks
                  - Network
                  - Access
                  - Profile
                  - Settings
                  - Updates
              get:
                description: Retrieve a list of Super SIMs from your account.
                tags:
                  - Sims
                  - Sim
                  - Sid
                  - Billing
                  - Periods
                  - Profiles
                  - Fleets
                  - Ip
                  - Commands
                  - Networks
                  - Network
                  - Access
                  - Profile
                  - Settings
                  - Updates
            /v1/Sims/{Sid}:
              description: Individual IoT Super SIMs
              get:
                description: Fetch a Super SIM instance from your account.
                tags:
                  - Sims
                  - Sim
                  - Sid
                  - Billing
                  - Periods
                  - Profiles
                  - Fleets
                  - Ip
                  - Commands
                  - Networks
                  - Network
                  - Access
                  - Profile
                  - Settings
                  - Updates
              post:
                description: >-
                  Updates the given properties of a Super SIM instance from your
                  account.
                tags:
                  - Sims
                  - Sim
                  - Sid
                  - Billing
                  - Periods
                  - Profiles
                  - Fleets
                  - Ip
                  - Commands
                  - Networks
                  - Network
                  - Access
                  - Profile
                  - Settings
                  - Updates
            /v1/Sims/{SimSid}/IpAddresses:
              description: IP Addresses for a Super SIM configured to use a VPN connection
              get:
                description: Retrieve a list of IP Addresses for the given Super SIM.
                tags:
                  - Sims
                  - Sim
                  - Sid
                  - Billing
                  - Periods
                  - Profiles
                  - Fleets
                  - Ip
                  - Commands
                  - Networks
                  - Network
                  - Access
                  - Profile
                  - Settings
                  - Updates
                  - Addresses
            /v1/SmsCommands:
              description: Machine-to-machine SMS Commands sent to/from SIMs
              post:
                description: Send SMS Command to a Sim.
                tags:
                  - Sims
                  - Sim
                  - Sid
                  - Billing
                  - Periods
                  - Profiles
                  - Fleets
                  - Ip
                  - Commands
                  - Networks
                  - Network
                  - Access
                  - Profile
                  - Settings
                  - Updates
                  - Addresses
                  - Sms
              get:
                description: Retrieve a list of SMS Commands from your account.
                tags:
                  - Sims
                  - Sim
                  - Sid
                  - Billing
                  - Periods
                  - Profiles
                  - Fleets
                  - Ip
                  - Commands
                  - Networks
                  - Network
                  - Access
                  - Profile
                  - Settings
                  - Updates
                  - Addresses
                  - Sms
            /v1/SmsCommands/{Sid}:
              description: Machine-to-machine SMS Commands sent to/from SIMs
              get:
                description: Fetch SMS Command instance from your account.
                tags:
                  - Sims
                  - Sim
                  - Sid
                  - Billing
                  - Periods
                  - Profiles
                  - Fleets
                  - Ip
                  - Commands
                  - Networks
                  - Network
                  - Access
                  - Profile
                  - Settings
                  - Updates
                  - Addresses
                  - Sms
            /v1/UsageRecords:
              description: Usage information for Sim resources
              get:
                description: List UsageRecords
                tags:
                  - Sims
                  - Sim
                  - Sid
                  - Billing
                  - Periods
                  - Profiles
                  - Fleets
                  - Ip
                  - Commands
                  - Networks
                  - Network
                  - Access
                  - Profile
                  - Settings
                  - Updates
                  - Addresses
                  - Sms
                  - Usage
                  - Records
          tags:
            - name: SupersimV1BillingPeriod
            - name: SupersimV1EsimProfile
            - name: SupersimV1Fleet
            - name: SupersimV1IpCommand
            - name: SupersimV1Network
            - name: SupersimV1NetworkAccessProfile
            - name: SupersimV1NetworkAccessProfileNetwork
            - name: SupersimV1SettingsUpdate
            - name: SupersimV1Sim
            - name: SupersimV1SimIpAddress
            - name: SupersimV1SmsCommand
            - name: SupersimV1UsageRecord
          x-maturity:
            - name: GA
              description: This product is Generally Available.
            - name: Beta
              description: >-
                PLEASE NOTE that this is a Beta product that is subject to
                change. U
    overlays:
      - type: APIs.io Search
        url: overlays/super-sim-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/super-sim-openapi-api-evangelist-ratings.yml
  - aid: twilio:twilio-wireless-api
    name: Twilio Wireless API
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
            title: Twilio - Wireless
            license:
              name: Apache 2.0
              url: https://www.apache.org/licenses/LICENSE-2.0.html
          openapi: 3.0.1
          paths:
            /v1/UsageRecords:
              description: Aggregated Usage information for all SIMs on an Account
              get:
                description: ''
                tags:
                  - Usage
                  - Records
            /v1/Commands/{Sid}:
              description: Machine-to-machine commands sent to/from devices
              get:
                description: Fetch a Command instance from your account.
                tags:
                  - Usage
                  - Records
                  - Commands
                  - Sid
              delete:
                description: Delete a Command instance from your account.
                tags:
                  - Usage
                  - Records
                  - Commands
                  - Sid
            /v1/Commands:
              description: Machine-to-machine commands sent to/from devices
              get:
                description: Retrieve a list of Commands from your account.
                tags:
                  - Usage
                  - Records
                  - Commands
                  - Sid
              post:
                description: Send a Command to a Sim.
                tags:
                  - Usage
                  - Records
                  - Commands
                  - Sid
            /v1/Sims/{SimSid}/DataSessions:
              description: Data session information for SIMs
              get:
                description: ''
                tags:
                  - Usage
                  - Records
                  - Commands
                  - Sid
                  - Sims
                  - Sim
                  - Data
                  - Sessions
            /v1/RatePlans:
              description: Capabilities and restrictions for SIMs
              get:
                description: ''
                tags:
                  - Usage
                  - Records
                  - Commands
                  - Sid
                  - Sims
                  - Sim
                  - Data
                  - Sessions
                  - Rate
                  - Plans
              post:
                description: ''
                tags:
                  - Usage
                  - Records
                  - Commands
                  - Sid
                  - Sims
                  - Sim
                  - Data
                  - Sessions
                  - Rate
                  - Plans
            /v1/RatePlans/{Sid}:
              description: Capabilities and restrictions for SIMs
              get:
                description: ''
                tags:
                  - Usage
                  - Records
                  - Commands
                  - Sid
                  - Sims
                  - Sim
                  - Data
                  - Sessions
                  - Rate
                  - Plans
              post:
                description: ''
                tags:
                  - Usage
                  - Records
                  - Commands
                  - Sid
                  - Sims
                  - Sim
                  - Data
                  - Sessions
                  - Rate
                  - Plans
              delete:
                description: ''
                tags:
                  - Usage
                  - Records
                  - Commands
                  - Sid
                  - Sims
                  - Sim
                  - Data
                  - Sessions
                  - Rate
                  - Plans
            /v1/Sims/{Sid}:
              description: A resource representing a Programmable Wireless SIM
              get:
                description: Fetch a Sim resource on your Account.
                tags:
                  - Usage
                  - Records
                  - Commands
                  - Sid
                  - Sims
                  - Sim
                  - Data
                  - Sessions
                  - Rate
                  - Plans
              post:
                description: >-
                  Updates the given properties of a Sim resource on your
                  Account.
                tags:
                  - Usage
                  - Records
                  - Commands
                  - Sid
                  - Sims
                  - Sim
                  - Data
                  - Sessions
                  - Rate
                  - Plans
              delete:
                description: Delete a Sim resource on your Account.
                tags:
                  - Usage
                  - Records
                  - Commands
                  - Sid
                  - Sims
                  - Sim
                  - Data
                  - Sessions
                  - Rate
                  - Plans
            /v1/Sims:
              description: A resource representing a Programmable Wireless SIM
              get:
                description: Retrieve a list of Sim resources on your Account.
                tags:
                  - Usage
                  - Records
                  - Commands
                  - Sid
                  - Sims
                  - Sim
                  - Data
                  - Sessions
                  - Rate
                  - Plans
            /v1/Sims/{SimSid}/UsageRecords:
              description: Usage information for SIMs
              get:
                description: ''
                tags:
                  - Usage
                  - Records
                  - Commands
                  - Sid
                  - Sims
                  - Sim
                  - Data
                  - Sessions
                  - Rate
                  - Plans
          tags:
            - name: WirelessV1Command
            - name: WirelessV1DataSession
            - name: WirelessV1RatePlan
            - name: WirelessV1Sim
            - name: WirelessV1UsageRecord
          x-maturity:
            - name: GA
              description: This product is G
    overlays:
      - type: APIs.io Search
        url: overlays/wireless-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/wireless-openapi-api-evangelist-ratings.yml
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---