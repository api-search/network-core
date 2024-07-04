---
name: Analyzer
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/analyzer.png
url: https://example.com/apis/analyzer.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Analyzer
apis:
  - name: accessanalyzer
    description: >-
      <p>Identity and Access Management Access Analyzer helps you to set,
      verify, and refine your IAM policies by providing a suite of capabilities.
      Its features include findings for external and unused access, basic and
      custom policy checks for validating policies, and policy generation to
      generate fine-grained policies. To start using IAM Access Analyzer to
      identify external or unused access, you first need to create an
      analyzer.</p> <p> <b>External access analyzers</b> help identify potential
      risks of accessing resources by enabling you to identify any resource
      policies that grant access to an external principal. It does this by using
      logic-based reasoning to analyze resource-based policies in your Amazon
      Web Services environment. An external principal can be another Amazon Web
      Services account, a root user, an IAM user or role, a federated user, an
      Amazon Web Services service, or an anonymous user. You can also use IAM
      Access Analyzer to preview public and cross-account access to your
      resources before deploying permissions changes.</p> <p> <b>Unused access
      analyzers</b> help identify potential identity access risks by enabling
      you to identify unused IAM roles, unused access keys, unused console
      passwords, and IAM principals with unused service and action-level
      permissions.</p> <p>Beyond findings, IAM Access Analyzer provides basic
      and custom policy checks to validate IAM policies before deploying
      permissions changes. You can use policy generation to refine permissions
      by attaching a policy generated using access activity logged in CloudTrail
      logs. </p> <p>This guide describes the IAM Access Analyzer operations that
      you can call programmatically. For general information about IAM Access
      Analyzer, see <a
      href="https://docs.aws.amazon.com/IAM/latest/UserGuide/what-is-access-analyzer.html">Identity
      and Access Management Access Analyzer</a> in the <b>IAM User
      Guide</b>.</p>
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
            title: accessanalyzer
          paths:
            /archive-rule:
              PUT:
                summary: Apply Archive Rule
                description: >-
                  <p>Retroactively applies the archive rule to existing findings
                  that meet the archive rule criteria.</p>
                tags:
                  - Apply
                  - Archive
                  - Rules
                  - Archive
                  - Rules
            /policy/generation/{jobId}:
              GET:
                summary: Get Generated Policy
                description: >-
                  <p>Retrieves the policy that was generated using
                  <code>StartPolicyGeneration</code>. </p>
                tags:
                  - Get
                  - Generated
                  - Policies
                  - Archive
                  - Rules
                  - Identifiers
            /policy/check-access-not-granted:
              POST:
                summary: Check Access Not Granted
                description: >-
                  <p>Checks whether the specified access isn't allowed by a
                  policy.</p>
                tags:
                  - Checks
                  - Access
                  - Not
                  - Grants
                  - Archive
                  - Rules
                  - Identifiers
                  - Policies
                  - Checks
                  - Access
                  - Not
                  - Grants
            /policy/check-no-new-access:
              POST:
                summary: Check No New Access
                description: >-
                  <p>Checks whether new access is allowed for an updated policy
                  when compared to the existing policy.</p> <p>You can find
                  examples for reference policies and learn how to set up and
                  run a custom policy check for new access in the <a
                  href="https://github.com/aws-samples/iam-access-analyzer-custom-policy-check-samples">IAM
                  Access Analyzer custom policy checks samples</a> repository on
                  GitHub. The reference policies in this repository are meant to
                  be passed to the <code>existingPolicyDocument</code> request
                  parameter.</p>
                tags:
                  - Checks
                  - 'No'
                  - New
                  - Access
                  - Archive
                  - Rules
                  - Identifiers
                  - Policies
                  - Checks
                  - Access
                  - Not
                  - Grants
                  - 'No'
                  - New
            /access-preview:
              GET:
                summary: ListAccessPreviews
                description: >-
                  <p>Retrieves a list of access previews for the specified
                  analyzer.</p>
                tags:
                  - Lists
                  - Access
                  - Previews
                  - Archive
                  - Rules
                  - Identifiers
                  - Policies
                  - Checks
                  - Access
                  - Not
                  - Grants
                  - 'No'
                  - New
                  - Preview
            /analyzer:
              GET:
                summary: ListAnalyzers
                description: <p>Retrieves a list of analyzers.</p>
                tags:
                  - Lists
                  - Analyzers
                  - Archive
                  - Rules
                  - Identifiers
                  - Policies
                  - Checks
                  - Access
                  - Not
                  - Grants
                  - 'No'
                  - New
                  - Preview
                  - Analyzer
            /analyzer/{analyzerName}/archive-rule:
              GET:
                summary: ListArchiveRules
                description: >-
                  <p>Retrieves a list of archive rules created for the specified
                  analyzer.</p>
                tags:
                  - Lists
                  - Archive
                  - Rules
                  - Archive
                  - Rules
                  - Identifiers
                  - Policies
                  - Checks
                  - Access
                  - Not
                  - Grants
                  - 'No'
                  - New
                  - Preview
                  - Analyzer
                  - Names
            /analyzer/{analyzerName}:
              GET:
                summary: GetAnalyzer
                description: <p>Retrieves information about the specified analyzer.</p>
                tags:
                  - Get
                  - Analyzer
                  - Archive
                  - Rules
                  - Identifiers
                  - Policies
                  - Checks
                  - Access
                  - Not
                  - Grants
                  - 'No'
                  - New
                  - Preview
                  - Analyzer
                  - Names
            /analyzer/{analyzerName}/archive-rule/{ruleName}:
              PUT:
                summary: UpdateArchiveRule
                description: >-
                  <p>Updates the criteria and values for the specified archive
                  rule.</p>
                tags:
                  - Update
                  - Archive
                  - Rules
                  - Archive
                  - Rules
                  - Identifiers
                  - Policies
                  - Checks
                  - Access
                  - Not
                  - Grants
                  - 'No'
                  - New
                  - Preview
                  - Analyzer
                  - Names
            /access-preview/{accessPreviewId}:
              POST:
                summary: ListAccessPreviewFindings
                description: >-
                  <p>Retrieves a list of access preview findings generated by
                  the specified access preview.</p>
                tags:
                  - Lists
                  - Access
                  - Preview
                  - Findings
                  - Archive
                  - Rules
                  - Identifiers
                  - Policies
                  - Checks
                  - Access
                  - Not
                  - Grants
                  - 'No'
                  - New
                  - Preview
                  - Analyzer
                  - Names
            /analyzed-resource:
              POST:
                summary: ListAnalyzedResources
                description: >-
                  <p>Retrieves a list of resources of the specified type that
                  have been analyzed by the specified analyzer..</p>
                tags:
                  - Lists
                  - Analyzed
                  - Resources
                  - Archive
                  - Rules
                  - Identifiers
                  - Policies
                  - Checks
                  - Access
                  - Not
                  - Grants
                  - 'No'
                  - New
                  - Preview
                  - Analyzer
                  - Names
                  - Analyzed
                  - Resources
            /finding/{id}:
              GET:
                summary: GetFinding
                description: <p>Retrieves information about the specified finding.</p>
                tags:
                  - Get
                  - Findings
                  - Archive
                  - Rules
                  - Identifiers
                  - Policies
                  - Checks
                  - Access
                  - Not
                  - Grants
                  - 'No'
                  - New
                  - Preview
                  - Analyzer
                  - Names
                  - Analyzed
                  - Resources
                  - Findings
            /findingv2/{id}:
              GET:
                summary: GetFindingV2
                description: <p>Retrieves information about the specified finding.</p>
                tags:
                  - Get
                  - Findings
                  - V2
                  - Archive
                  - Rules
                  - Identifiers
                  - Policies
                  - Checks
                  - Access
                  - Not
                  - Grants
                  - 'No'
                  - New
                  - Preview
                  - Analyzer
                  - Names
                  - Analyzed
                  - Resources
                  - Findings
                  - Findings
            /finding:
              PUT:
                summary: UpdateFindings
                description: <p>Updates the status for the specified findings.</p>
                tags:
                  - Update
                  - Findings
                  - Archive
                  - Rules
                  - Identifiers
                  - Policies
                  - Checks
                  - Access
                  - Not
                  - Grants
                  - 'No'
                  - New
                  - Preview
                  - Analyzer
                  - Names
                  - Analyzed
                  - Resources
                  - Findings
                  - Findings
            /findingv2:
              POST:
                summary: ListFindingsV2
                description: >-
                  <p>Retrieves a list of findings generated by the specified
                  analyzer.</p> <p>To learn about filter keys that you can use
                  to retrieve a list of findings, see <a
                  href="https://docs.aws.amazon.com/IAM/latest/UserGuide/access-analyzer-reference-filter-keys.html">IAM
                  Access Analyzer filter keys</a> in the <b>IAM User
                  Guide</b>.</p>
                tags:
                  - Lists
                  - Findings
                  - V2
                  - Archive
                  - Rules
                  - Identifiers
                  - Policies
                  - Checks
                  - Access
                  - Not
                  - Grants
                  - 'No'
                  - New
                  - Preview
                  - Analyzer
                  - Names
                  - Analyzed
                  - Resources
                  - Findings
                  - Findings
            /policy/generation:
              PUT:
                summary: StartPolicyGeneration
                description: <p>Starts the policy generation request.</p>
                tags:
                  - Start
                  - Policies
                  - Generation
                  - Archive
                  - Rules
                  - Identifiers
                  - Policies
                  - Checks
                  - Access
                  - Not
                  - Grants
                  - 'No'
                  - New
                  - Preview
                  - Analyzer
                  - Names
                  - Analyzed
                  - Resources
                  - Findings
                  - Findings
                  - Generation
            /tags/{resourceArn}:
              DELETE:
                summary: UntagResource
                description: <p>Removes a tag from the specified resource.</p>
                tags:
                  - Untag
                  - Resources
                  - Archive
                  - Rules
                  - Identifiers
                  - Policies
                  - Checks
                  - Access
                  - Not
                  - Grants
                  - 'No'
                  - New
                  - Preview
                  - Analyzer
                  - Names
                  - Analyzed
                  - Resources
                  - Findings
                  - Findings
                  - Generation
                  - ARN
            /resource/scan:
              POST:
                summary: StartResourceScan
                description: >-
                  <p>Immediately starts a scan of the policies applied to the
                  specified resource.</p>
                tags:
                  - Start
                  - Resources
                  - Scans
                  - Archive
                  - Rules
                  - Identifiers
                  - Policies
                  - Checks
                  - Access
                  - Not
                  - Grants
                  - 'No'
                  - New
                  - Preview
                  - Analyzer
                  - Names
                  - Analyzed
                  - Resources
                  - Findings
                  - Findings
                  - Generation
                  - ARN
                  - Scans
            /policy/validation:
              POST:
                summary: ValidatePolicy
                description: >-
                  <p>Requests the validation of a policy and returns a list of
                  findings. The findings help you identify issues and provide
                  actionable recommendations to resolve the issue and enable you
                  to author functional policies that meet security best pract
                tags:
                  - Validate
                  - Policies
                  - Archive
                  - Rules
                  - Identifiers
                  - Policies
                  - Checks
                  - Access
                  - Not
                  - Grants
                  - 'No'
                  - New
                  - Preview
                  - Analyzer
                  - Names
                  - Analyzed
                  - Resources
                  - Findings
                  - Findings
                  - Generation
                  - ARN
                  - Scans
                  - Validations
    overlays:
      - type: APIs.io Search
        url: overlays/accessanalyzer-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/accessanalyzer-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:accessanalyzer
  - name: iotwireless
    description: >-
      <p>AWS IoT Wireless provides bi-directional communication between
      internet-connected wireless devices and the AWS Cloud. To onboard both
      LoRaWAN and Sidewalk devices to AWS IoT, use the IoT Wireless API. These
      wireless devices use the Low Power Wide Area Networking (LPWAN)
      communication protocol to communicate with AWS IoT.</p> <p>Using the API,
      you can perform create, read, update, and delete operations for your
      wireless devices, gateways, destinations, and profiles. After onboarding
      your devices, you can use the API operations to set log levels and monitor
      your devices with CloudWatch.</p> <p>You can also use the API operations
      to create multicast groups and schedule a multicast session for sending a
      downlink message to devices in the group. By using Firmware Updates
      Over-The-Air (FUOTA) API operations, you can create a FUOTA task and
      schedule a session to update the firmware of individual devices or an
      entire group of devices in a multicast group.</p>
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
            title: iotwireless
          paths:
            /partner-accounts:
              GET:
                summary: ListPartnerAccounts
                description: >-
                  <p>Lists the partner accounts associated with your AWS
                  account.</p>
                tags:
                  - Lists
                  - Partners
                  - Accounts
                  - Partners
                  - Accounts
            /fuota-tasks/{Id}/multicast-group:
              PUT:
                summary: AssociateMulticastGroupWithFuotaTask
                description: <p>Associate a multicast group with a FUOTA task.</p>
                tags:
                  - Associate
                  - Multicast
                  - Group
                  - With
                  - Fuota
                  - Tasks
                  - Partners
                  - Accounts
                  - Identifiers
                  - Multicast
                  - Group
            /fuota-tasks/{Id}/wireless-device:
              PUT:
                summary: AssociateWirelessDeviceWithFuotaTask
                description: <p>Associate a wireless device with a FUOTA task.</p>
                tags:
                  - Associate
                  - Wireless
                  - Device
                  - With
                  - Fuota
                  - Tasks
                  - Partners
                  - Accounts
                  - Identifiers
                  - Multicast
                  - Group
                  - Wireless
                  - Device
            /multicast-groups/{Id}/wireless-device:
              PUT:
                summary: AssociateWirelessDeviceWithMulticastGroup
                description: <p>Associates a wireless device with a multicast group.</p>
                tags:
                  - Associate
                  - Wireless
                  - Device
                  - With
                  - Multicast
                  - Group
                  - Partners
                  - Accounts
                  - Identifiers
                  - Multicast
                  - Group
                  - Wireless
                  - Device
            /wireless-devices/{Id}/thing:
              DELETE:
                summary: DisassociateWirelessDeviceFromThing
                description: >-
                  <p>Disassociates a wireless device from its currently
                  associated thing.</p>
                tags:
                  - Disassociate
                  - Wireless
                  - Device
                  - From
                  - Things
                  - Partners
                  - Accounts
                  - Identifiers
                  - Multicast
                  - Group
                  - Wireless
                  - Device
                  - Things
            /wireless-gateways/{Id}/certificate:
              GET:
                summary: GetWirelessGatewayCertificate
                description: >-
                  <p>Gets the ID of the certificate that is currently associated
                  with a wireless gateway.</p>
                tags:
                  - Get
                  - Wireless
                  - Gateway
                  - Certificates
                  - Partners
                  - Accounts
                  - Identifiers
                  - Multicast
                  - Group
                  - Wireless
                  - Device
                  - Things
                  - Certificates
            /wireless-gateways/{Id}/thing:
              DELETE:
                summary: DisassociateWirelessGatewayFromThing
                description: >-
                  <p>Disassociates a wireless gateway from its currently
                  associated thing.</p>
                tags:
                  - Disassociate
                  - Wireless
                  - Gateway
                  - From
                  - Things
                  - Partners
                  - Accounts
                  - Identifiers
                  - Multicast
                  - Group
                  - Wireless
                  - Device
                  - Things
                  - Certificates
            /multicast-groups/{Id}/session:
              PUT:
                summary: StartMulticastGroupSession
                description: <p>Starts a multicast group session.</p>
                tags:
                  - Start
                  - Multicast
                  - Group
                  - Sessions
                  - Partners
                  - Accounts
                  - Identifiers
                  - Multicast
                  - Group
                  - Wireless
                  - Device
                  - Things
                  - Certificates
                  - Sessions
            /destinations:
              GET:
                summary: ListDestinations
                description: <p>Lists the destinations registered to your AWS account.</p>
                tags:
                  - Lists
                  - Destinations
                  - Partners
                  - Accounts
                  - Identifiers
                  - Multicast
                  - Group
                  - Wireless
                  - Device
                  - Things
                  - Certificates
                  - Sessions
                  - Destinations
            /device-profiles:
              GET:
                summary: ListDeviceProfiles
                description: >-
                  <p>Lists the device profiles registered to your AWS
                  account.</p>
                tags:
                  - Lists
                  - Device
                  - Profiles
                  - Partners
                  - Accounts
                  - Identifiers
                  - Multicast
                  - Group
                  - Wireless
                  - Device
                  - Things
                  - Certificates
                  - Sessions
                  - Destinations
                  - Profiles
            /fuota-tasks:
              GET:
                summary: ListFuotaTasks
                description: <p>Lists the FUOTA tasks registered to your AWS account.</p>
                tags:
                  - Lists
                  - Fuota
                  - Tasks
                  - Partners
                  - Accounts
                  - Identifiers
                  - Multicast
                  - Group
                  - Wireless
                  - Device
                  - Things
                  - Certificates
                  - Sessions
                  - Destinations
                  - Profiles
                  - Fuota
                  - Tasks
            /multicast-groups:
              GET:
                summary: ListMulticastGroups
                description: >-
                  <p>Lists the multicast groups registered to your AWS
                  account.</p>
                tags:
                  - Lists
                  - Multicast
                  - Groups
                  - Partners
                  - Accounts
                  - Identifiers
                  - Multicast
                  - Group
                  - Wireless
                  - Device
                  - Things
                  - Certificates
                  - Sessions
                  - Destinations
                  - Profiles
                  - Fuota
                  - Tasks
                  - Groups
            /network-analyzer-configurations:
              GET:
                summary: ListNetworkAnalyzerConfigurations
                description: <p>Lists the network analyzer configurations.</p>
                tags:
                  - Lists
                  - Networks
                  - Analyzer
                  - Configurations
                  - Partners
                  - Accounts
                  - Identifiers
                  - Multicast
                  - Group
                  - Wireless
                  - Device
                  - Things
                  - Certificates
                  - Sessions
                  - Destinations
                  - Profiles
                  - Fuota
                  - Tasks
                  - Groups
                  - Networks
                  - Analyzer
                  - Configurations
            /service-profiles:
              GET:
                summary: ListServiceProfiles
                description: >-
                  <p>Lists the service profiles registered to your AWS
                  account.</p>
                tags:
                  - Lists
                  - Services
                  - Profiles
                  - Partners
                  - Accounts
                  - Identifiers
                  - Multicast
                  - Group
                  - Wireless
                  - Device
                  - Things
                  - Certificates
                  - Sessions
                  - Destinations
                  - Profiles
                  - Fuota
                  - Tasks
                  - Groups
                  - Networks
                  - Analyzer
                  - Configurations
                  - Services
            /wireless-devices:
              GET:
                summary: ListWirelessDevices
                description: >-
                  <p>Lists the wireless devices registered to your AWS
                  account.</p>
                tags:
                  - Lists
                  - Wireless
                  - Devices
                  - Partners
                  - Accounts
                  - Identifiers
                  - Multicast
                  - Group
                  - Wireless
                  - Device
                  - Things
                  - Certificates
                  - Sessions
                  - Destinations
                  - Profiles
                  - Fuota
                  - Tasks
                  - Groups
                  - Networks
                  - Analyzer
                  - Configurations
                  - Services
                  - Devices
            /wireless-gateways:
              GET:
                summary: ListWirelessGateways
                description: >-
                  <p>Lists the wireless gateways registered to your AWS
                  account.</p>
                tags:
                  - Lists
                  - Wireless
                  - Gateways
                  - Partners
                  - Accounts
                  - Identifiers
                  - Multicast
                  - Group
                  - Wireless
                  - Device
                  - Things
                  - Certificates
                  - Sessions
                  - Destinations
                  - Profiles
                  - Fuota
                  - Tasks
                  - Groups
                  - Networks
                  - Analyzer
                  - Configurations
                  - Services
                  - Devices
                  - Gateways
            /wireless-gateways/{Id}/tasks:
              GET:
                summary: GetWirelessGatewayTask
                description: <p>Gets information about a wireless gateway task.</p>
                tags:
                  - Get
                  - Wireless
                  - Gateway
                  - Tasks
                  - Partners
                  - Accounts
                  - Identifiers
                  - Multicast
                  - Group
                  - Wireless
                  - Device
                  - Things
                  - Certificates
                  - Sessions
                  - Destinations
                  - Profiles
                  - Fuota
                  - Tasks
                  - Groups
                  - Networks
                  - Analyzer
                  - Configurations
                  - Services
                  - Devices
                  - Gateways
            /wireless-gateway-task-definitions:
              GET:
                summary: ListWirelessGatewayTaskDefinitions
                description: >-
                  <p>List the wireless gateway tasks definitions registered to
                  your AWS account.</p>
                tags:
                  - Lists
                  - Wireless
                  - Gateway
                  - Tasks
                  - Definitions
                  - Partners
                  - Accounts
                  - Identifiers
                  - Multicast
                  - Group
                  - Wireless
                  - Device
                  - Things
                  - Certificates
                  - Sessions
                  - Destinations
                  - Profiles
                  - Fuota
                  - Tasks
                  - Groups
                  - Networks
                  - Analyzer
                  - Configurations
                  - Services
                  - Devices
                  - Gateways
                  - Gateway
                  - Tasks
                  - Definitions
            /destinations/{Name}:
              PATCH:
                summary: UpdateDestination
                description: <p>Updates properties of a destination.</p>
                tags:
                  - Update
                  - Destinations
                  - Partners
                  - Accounts
                  - Identifiers
                  - Multicast
                  - Group
                  - Wireless
                  - Device
                  - Things
                  - Certificates
                  - Sessions
                  - Destinations
                  - Profiles
                  - Fuota
                  - Tasks
                  - Groups
                  - Networks
                  - Analyzer
                  - Configurations
                  - Services
                  - Devices
                  - Gateways
                  - Gateway
                  - Tasks
                  - Definitions
                  - Names
            /device-profiles/{Id}:
              GET:
                summary: GetDeviceProfile
                description: <p>Gets information about a device profile.</p>
                tags:
                  - Get
                  - Device
                  - Profiles
                  - Partners
                  - Accounts
                  - Identifiers
                  - Multicast
                  - Group
                  - Wireless
                  - Device
                  - Things
                  - Certificates
                  - Sessions
                  - Destinations
                  - Profiles
                  - Fuota
                  - Tasks
                  - Groups
                  - Networks
                  - Analyzer
                  - Configurations
                  - Services
                  - Devices
                  - Gateways
                  - Gateway
                  - Tasks
                  - Definitions
                  - Names
            /fuota-tasks/{Id}:
              PATCH:
                summary: UpdateFuotaTask
                description: <p>Updates properties of a FUOTA task.</p>
                tags:
                  - Update
                  - Fuota
                  - Tasks
                  - Partners
                  - Accounts
                  - Identifiers
                  - Multicast
                  - Group
                  - Wireless
                  - Device
                  - Things
                  - Certificates
                  - Sessions
                  - Destinations
                  - Profiles
                  - Fuota
                  - Tasks
                  - Groups
                  - Networks
                  - Analyzer
                  - Configurations
                  - Services
                  - Devices
                  - Gateways
                  - Gateway
                  - Tasks
                  - Definitions
                  - Names
            /multicast-groups/{Id}:
              PATCH:
                summary: UpdateMulticastGroup
                description: <p>Updates properties of a multicast group session.</p>
                tags:
                  - Update
                  - Multicast
                  - Group
                  - Partners
                  - Accounts
                  - Identifiers
                  - Multicast
                  - Group
                  - Wireless
                  - Device
                  - Things
                  - Certificates
                  - Sessions
                  - Destinations
                  - Profiles
                  - Fuota
                  - Tasks
                  - Groups
                  - Networks
                  - Analyzer
                  - Configurations
                  - Services
                  - Devices
                  - Gateways
                  - Gateway
                  - Tasks
                  - Definitions
                  - Names
            /network-analyzer-configurations/{ConfigurationName}:
              PATCH:
                summary: UpdateNetworkAnalyzerConfiguration
                description: <p>Update network analyzer configuration.</p>
                tags:
                  - Update
                  - Networks
                  - Analyzer
                  - Configurations
                  - Partners
                  - Accounts
                  - Identifiers
                  - Multicast
                  - Group
                  - Wireless
                  - Device
                  - Things
                  - Certificates
                  - Sessions
                  - Destinations
                  - Profiles
                  - Fuota
                  - Tasks
                  - Groups
                  - Networks
                  - Analyzer
                  - Configurations
                  - Services
                  - Devices
                  - Gateways
                  - Gateway
                  - Tasks
                  - Definitions
                  - Names
                  - Configurations
            /wireless-devices/{Id}/data:
              POST:
                summary: SendDataToWirelessDevice
                description: <p>Sends a decrypted application data frame to a device.</p>
                tags:
                  - Send
                  - Data
                  - To
                  - Wireless
                  - Device
                  - Partners
                  - Accounts
                  - Identifiers
                  - Multicast
                  - Group
                  - Wireless
                  - Device
                  - Things
                  - Certificates
                  - Sessions
                  - Destinations
                  - Profiles
                  - Fuota
                  - Tasks
                  - Groups
                  - Networks
                  - Analyzer
                  - Configurations
                  - Services
                  - Devices
                  - Gateways
                  - Gateway
                  - Tasks
                  - Definitions
                  - Names
                  - Configurations
                  - Data
            /service-profiles/{Id}:
              GET:
                summary: GetServiceProfile
                description: <p>Gets information about a service profile.</p>
                tags:
                  - Get
                  - Services
                  - Profiles
                  - Partners
                  - Accounts
                  - Identifiers
                  - Multicast
                  - Group
                  - Wireless
                  - Device
                  - Things
                  - Certificates
                  - Sessions
                  - Destinations
                  - Profiles
                  - Fuota
                  - Tasks
                  - Groups
                  - Networks
                  - Analyzer
                  - Configurations
                  - Services
                  - Devices
                  - Gateways
                  - Gateway
                  - Tasks
                  - Definitions
                  - Names
                  - Configurations
                  - Data
            /wireless-devices/{Id}:
              PATCH:
                summary: UpdateWirelessDevice
                description: <p>Updates properties of a wireless device.</p>
                tags:
                  - Update
                  - Wireless
                  - Device
                  - Partners
                  - Accounts
                  - Identifiers
                  - Multicast
                  - Group
                  - Wireless
                  - Device
                  - Things
                  - Certificates
                  - Sessions
                  - Destinations
                  - Profiles
                  - Fuota
                  - Tasks
                  - Groups
                  - Networks
                  - Analyzer
                  - Configurations
                  - Services
                  - Devices
                  - Gateways
                  - Gateway
                  - Tasks
                  - Definitions
                  - Names
                  - Configurations
                  - Data
            /wireless_device_import_task/{Id}:
              PATCH:
                summary: UpdateWirelessDeviceImportTask
                description: <p>Update an import task to add more devices to the task.</p>
                tags:
                  - Update
                  - Wireless
                  - Device
                  - Import
                  - Tasks
                  - Partners
                  - Accounts
                  - Identifiers
                  - Multicast
                  - Group
                  - Wireless
                  - Device
                  - Things
                  - Certificates
                  - Sessions
                  - Destinations
                  - Profiles
                  - Fuota
                  - Tasks
                  - Groups
                  - Networks
                  - Analyzer
                  - Configurations
                  - Services
                  - Devices
                  - Gateways
                  - Gateway
                  - Tasks
                  - Definitions
                  - Names
                  - Configurations
                  - Data
            /wireless-gateways/{Id}:
              PATCH:
                summary: UpdateWirelessGateway
                description: <p>Updates properties of a wireless gateway.</p>
                tags:
                  - Update
                  - Wireless
                  - Gateway
                  - Partners
                  - Accounts
                  - Identifiers
                  - Multicast
                  - Group
                  - Wireless
                  - Device
                  - Things
                  - Certificates
                  - Sessions
                  - Destinations
                  - Profiles
                  - Fuota
                  - Tasks
                  - Groups
                  - Networks
                  - Analyzer
                  - Configurations
                  - Services
                  - Devices
                  - Gateways
                  - Gateway
                  - Tasks
                  - Definitions
                  - Names
                  - Configurations
                  - Data
            /wireless-gateway-task-definitions/{Id}:
              GET:
                summary: GetWirelessGatewayTaskDefinition
                description: >-
                  <p>Gets information about a wireless gateway task
                  definition.</p>
                tags:
                  - Get
                  - Wireless
                  - Gateway
                  - Tasks
                  - Definitions
                  - Partners
                  - Accounts
                  - Identifiers
                  - Multicast
                  - Group
                  - Wireless
                  - Device
                  - Things
                  - Certificates
                  - Sessions
                  - Destinations
                  - Profiles
                  - Fuota
                  - Tasks
                  - Groups
                  - Networks
                  - Analyzer
                  - Configurations
                  - Services
                  - Devices
                  - Gateways
                  - Gateway
                  - Tasks
                  - Definitions
                  - Names
                  - Configurations
                  - Data
            /wireless-devices/{Identifier}/deregister:
              PATCH:
                summary: DeregisterWirelessDevice
                description: <p>Deregister a wireless device from AWS IoT Wireless.</p>
                tags:
                  - Deregister
                  - Wireless
                  - Device
                  - Partners
                  - Accounts
                  - Identifiers
                  - Multicast
                  - Group
                  - Wireless
                  - Device
                  - Things
                  - Certificates
                  - Sessions
                  - Destinations
                  - Profiles
                  - Fuota
                  - Tasks
                  - Groups
                  - Networks
                  - Analyzer
                  - Configurations
                  - Services
                  - Devices
                  - Gateways
                  - Gateway
                  - Tasks
                  - Definitions
                  - Names
                  - Configurations
                  - Data
                  - Identifiers
                  - Deregister
            /partner-accounts/{PartnerAccountId}:
              PATCH:
                summary: UpdatePartnerAccount
                description: <p>Updates properties of a partner account.</p>
                tags:
                  - Update
                  - Partners
                  - Account
                  - Partners
                  - Accounts
                  - Identifiers
                  - Multicast
                  - Group
                  - Wireless
                  - Device
                  - Things
                  - Certificates
                  - Sessions
                  - Destinations
                  - Profiles
                  - Fuota
                  - Tasks
                  - Groups
                  - Networks
                  - Analyzer
                  - Configurations
                  - Services
                  - Devices
                  - Gateways
                  - Gateway
                  - Tasks
                  - Definitions
                  - Names
                  - Configurations
                  - Data
                  - Identifiers
                  - Deregister
                  - Account
            /fuota-tasks/{Id}/multicast-groups/{MulticastGroupId}:
              DELETE:
                summary: DisassociateMulticastGroupFromFuotaTask
                description: <p>Disassociates a multicast group from a fuota task.</p>
                tags:
                  - Disassociate
                  - Multicast
                  - Group
                  - From
                  - Fuota
                  - Tasks
                  - Partners
                  - Accounts
                  - Identifiers
                  - Multicast
                  - Group
                  - Wireless
                  - Device
                  - Things
                  - Certificates
                  - Sessions
                  - Destinations
                  - Profiles
                  - Fuota
                  - Tasks
                  - Groups
                  - Networks
                  - Analyzer
                  - Configurations
                  - Services
                  - Devices
                  - Gateways
                  - Gateway
                  - Tasks
                  - Definitions
                  - Names
                  - Configurations
                  - Data
                  - Identifiers
                  - Deregister
                  - Account
            /fuota-tasks/{Id}/wireless-devices/{WirelessDeviceId}:
              DELETE:
                summary: DisassociateWirelessDeviceFromFuotaTask
                description: <p>Disassociates a wireless device from a FUOTA task.</p>
                tags:
                  - Disassociate
                  - Wireless
                  - Device
                  - From
                  - Fuota
                  - Tasks
                  - Partners
                  - Accounts
                  - Identifiers
                  - Multicast
                  - Group
                  - Wireless
                  - Device
                  - Things
                  - Certificates
                  - Sessions
                  - Destinations
                  - Profiles
                  - Fuota
                  - Tasks
                  - Groups
                  - Networks
                  - Analyzer
                  - Configurations
                  - Services
                  - Devices
                  - Gateways
                  - Gateway
                  - Tasks
                  - Definitions
                  - Names
                  - Configurations
                  - Data
                  - Identifiers
                  - Deregister
                  - Account
            /multicast-groups/{Id}/wireless-devices/{WirelessDeviceId}:
              DELETE:
                summary: DisassociateWirelessDeviceFromMulticastGroup
                description: <p>Disassociates a wireless device from a multicast group.</p>
                tags:
                  - Disassociate
                  - Wireless
                  - Device
                  - From
                  - Multicast
                  - Group
                  - Partners
                  - Accounts
                  - Identifiers
                  - Multicast
                  - Group
                  - Wireless
                  - Device
                  - Things
                  - Certificates
                  - Sessions
                  - Destinations
                  - Profiles
                  - Fuota
                  - Tasks
                  - Groups
                  - Networks
                  - Analyzer
                  - Configurations
                  - Services
                  - Devices
                  - Gateways
                  - Gateway
                  - Tasks
                  - Definitions
                  - Names
                  - Configurations
                  - Data
                  - Identifiers
                  - Deregister
                  - Account
            /event-configurations-resource-types:
              PATCH:
                summary: UpdateEventConfigurationByResourceTypes
                description: <p>Update the event configuration based on resource types.</p>
                tags:
                  - Update
                  - Events
                  - Configurations
                  - By
                  - Resources
                  - Types
                  - Partners
                  - Accounts
                  - Identifiers
                  - Multicast
                  - Group
                  - Wireless
                  - Device
                  - Things
                  - Certificates
                  - Sessions
                  - Destinations
                  - Profiles
                  - Fuota
                  - Tasks
                  - Groups
                  - Networks
                  - Analyzer
                  - Configurations
                  - Services
                  - Devices
                  - Gateways
                  - Gateway
                  - Tasks
                  - Definitions
                  - Names
                  - Configurations
                  - Data
                  - Identifiers
                  - Deregister
                  - Account
                  - Events
                  - Resources
                  - Types
            /log-levels:
              POST:
                summary: UpdateLogLevelsByResourceTypes
                description: >-
                  <p>Set default log level, or log levels by resource types.
                  This can be for wireless device log options or wireless
                  gateways log options and is used to control the log messages
                  that'll be displayed in CloudWatch.</p>
                tags:
                  - Update
                  - Logs
                  - Levels
                  - By
                  - Resources
                  - Types
                  - Partners
                  - Accounts
                  - Identifiers
                  - Multicast
                  - Group
                  - Wireless
                  - Device
                  - Things
                  - Certificates
                  - Sessions
                  - Destinations
                  - Profiles
                  - Fuota
                  - Tasks
                  - Groups
                  - Networks
                  - Analyzer
                  - Configurations
                  - Services
                  - Devices
                  - Gateways
                  - Gateway
                  - Tasks
                  - Definitions
                  - Names
                  - Configurations
                  - Data
                  - Identifiers
                  - Deregister
                  - Account
                  - Events
                  - Resources
                  - Types
                  - Logs
                  - Levels
            /positions/{ResourceIdentifier}:
              PATCH:
                summary: UpdatePosition
                description: >-
                  <p>Update the position information of a resource.</p>
                  <important> <p>This action is no longer supported. Calls to
                  update the position information should use the <a
                  href="https://docs.aws.amazon.com/iot-wireless/2020-11-22/apireference/API_UpdateResourcePosition.html">UpdateResourcePosition</a>
                  API operation instead.</p> </important>
                tags:
                  - Update
                  - Positions
                  - Partners
                  - Accounts
                  - Identifiers
                  - Multicast
                  - Group
                  - Wireless
                  - Device
                  - Things
                  - Certificates
                  - Sessions
                  - Destinations
                  - Profiles
                  - Fuota
                  - Tasks
                  - Groups
                  - Networks
                  - Analyzer
                  - Configurations
                  - Services
                  - Devices
                  - Gateways
                  - Gateway
                  - Tasks
                  - Definitions
                  - Names
                  - Configurations
                  - Data
                  - Identifiers
                  - Deregister
                  - Account
                  - Events
                  - Resources
                  - Types
                  - Logs
                  - Levels
            /position-configurations/{ResourceIdentifier}:
              PUT:
                summary: PutPositionConfiguration
                description: >-
                  <p>Put position configuration for a given resource.</p>
                  <important> <p>This action is no longer supported. Calls to
                  update the position configuration should use the <a
                  href="https://docs.aws.amazon.com/iot-wireless/2020-11-22/apireference/API_UpdateResourcePosition.html">UpdateResourcePosition</a>
                  API operation instead.</p> </important>
                tags:
                  - Put
                  - Positions
                  - Configurations
                  - Partners
                  - Accounts
                  - Identifiers
                  - Multicast
                  - Group
                  - Wireless
                  - Device
                  - Things
                  - Certificates
                  - Sessions
                  - Destinations
                  - Profiles
                  - Fuota
                  - Tasks
                  - Groups
                  - Networks
                  - Analyzer
                  - Configurations
                  - Services
                  - Devices
                  - Gateways
                  - Gateway
                  - Tasks
                  - Definitions
                  - Names
                  - Configurations
                  - Data
                  - Identifiers
                  - Deregister
                  - Account
                  - Events
                  - Resources
                  - Types
                  - Logs
                  - Levels
            /position-estimate:
              POST:
                summary: GetPositionEstimate
                description: >-
                  <p>Get estimated position information as a payload in GeoJSON
                  format. The payload measurement data is resolved using solvers
                  that are provided by third-party vendors.</p>
                tags:
                  - Get
                  - Positions
                  - Estimates
                  - Partners
                  - Accounts
                  - Identifiers
                  - Multicast
                  - Group
                  - Wireless
                  - Device
                  - Things
                  - Certificates
                  - Sessions
                  - Destinations
                  - Profiles
                  - Fuota
                  - Tasks
                  - Groups
                  - Networks
                  - Analyzer
                  - Configurations
                  - Services
                  - Devices
                  - Gateways
                  - Gateway
                  - Tasks
                  - Definitions
                  - Names
                  - Configurations
                  - Data
                  - Identifiers
                  - Deregister
                  - Account
                  - Events
                  - Resources
                  - Types
                  - Logs
                  - Levels
                  - Positions
                  - Estimates
            /event-configurations/{Identifier}:
              PATCH:
                summary: UpdateResourceEventConfiguration
                description: >-
                  <p>Update the event configuration for a particular resource
                  identifier.</p>
                tags:
                  - Update
                  - Resources
                  - Events
                  - Configurations
                  - Partners
                  - Accounts
                  - Identifiers
                  - Multicast
                  - Group
                  - Wireless
                  - Device
                  - Things
                  - Certificates
                  - Sessions
                  - Destinations
                  - Profiles
                  - Fuota
                  - Tasks
                  - Groups
                  - Networks
                  - Analyzer
                  - Configurations
                  - Services
                  - Devices
                  - Gateways
                  - Gateway
                  - Tasks
                  - Definitions
                  - Names
                  - Configurations
                  - Data
                  - Identifiers
                  - Deregister
                  - Account
                  - Events
                  - Resources
                  - Types
                  - Logs
                  - Levels
                  - Positions
                  - Estimates
            /log-levels/{ResourceIdentifier}:
              DELETE:
                summary: ResetResourceLogLevel
                description: >-
                  <p>Removes the log-level override, if any, for a specific
                  resource-ID and resource-type. It can be used for a wireless
                  device or a wireless gateway.</p>
                tags:
                  - Reset
                  - Resources
                  - Logs
                  - Levels
                  - Partners
                  - Accounts
                  - Identifiers
                  - Multicast
                  - Group
                  - Wireless
                  - Device
                  - Things
                  - Certificates
                  - Sessions
                  - Destinations
                  - Profiles
                  - Fuota
                  - Tasks
                  - Groups
                  - Networks
                  - Analyzer
                  - Configurations
                  - Services
                  - Devices
                  - Gateways
                  - Gateway
                  - Tasks
                  - Definitions
                  - Names
                  - Configurations
                  - Data
                  - Identifiers
                  - Deregister
                  - Account
                  - Events
                  - Resources
                  - Types
                  - Logs
                  - Levels
                  - Positions
                  - Estimates
            /resource-positions/{ResourceIdentifier}:
              PATCH:
                summary: UpdateResourcePosition
                description: >-
                  <p>Update the position information of a given wireless device
                  or a wireless gateway resource. The position coordinates are
                  based on the <a
                  href="https://gisgeography.com/wgs84-world-geodetic-system/">
                  World Geodetic System (WGS84)</a>.</p>
                tags:
                  - Update
                  - Resources
                  - Positions
                  - Partners
                  - Accounts
                  - Identifiers
                  - Multicast
                  - Group
                  - Wireless
                  - Device
                  - Things
                  - Certificates
                  - Sessions
                  - Destinations
                  - Profiles
                  - Fuota
                  - Tasks
                  - Groups
                  - Networks
                  - Analyzer
                  - Configurations
                  - Services
                  - Devices
                  - Gateways
                  - Gateway
                  - Tasks
                  - Definitions
                  - Names
                  - Configurations
                  - Data
                  - Identifiers
                  - Deregister
                  - Account
                  - Events
                  - Resources
                  - Types
                  - Logs
                  - Levels
                  - Positions
                  - Estimates
            /service-endpoint:
              GET:
                summary: GetServiceEndpoint
                description: >-
                  <p>Gets the account-specific endpoint for Configuration and
                  Update Server (CUPS) protocol or LoRaWAN Network Server (LNS)
                  connections.</p>
                tags:
                  - Get
                  - Services
                  - Endpoints
                  - Partners
                  - Accounts
                  - Identifiers
                  - Multicast
                  - Group
                  - Wireless
                  - Device
                  - Things
                  - Certificates
                  - Sessions
                  - Destinations
                  - Profiles
                  - Fuota
                  - Tasks
                  - Groups
                  - Networks
                  - Analyzer
                  - Configurations
                  - Services
                  - Devices
                  - Gateways
                  - Gateway
                  - Tasks
                  - Definitions
                  - Names
                  - Configurations
                  - Data
                  - Identifiers
                  - Deregister
                  - Account
                  - Events
                  - Resources
                  - Types
                  - Logs
                  - Levels
                  - Positions
                  - Estimates
                  - Endpoints
            /wireless-devices/{Identifier}:
              GET:
                summary: GetWirelessDevice
                description: <p>Gets information about a wireless device.</p>
                tags:
                  - Get
                  - Wireless
                  - Device
                  - Partners
                  - Accounts
                  - Identifiers
                  - Multicast
                  - Group
                  - Wireless
                  - Device
                  - Things
                  - Certificates
                  - Sessions
                  - Destinations
                  - Profiles
                  - Fuota
                  - Tasks
                  - Groups
                  - Networks
                  - Analyzer
                  - Configurations
                  - Services
                  - Devices
                  - Gateways
                  - Gateway
                  - Tasks
                  - Definitions
                  - Names
                  - Configurations
                  - Data
                  - Identifiers
                  - Deregister
                  - Account
                  - Events
                  - Resources
                  - Types
                  - Logs
                  - Levels
                  - Positions
                  - Estimates
                  - Endpoints
            /wireless-devices/{Id}/statistics:
              GET:
                summary: GetWirelessDeviceStatistics
                description: <p>Gets operating information about a wireless device.</p>
                tags:
                  - Get
                  - Wireless
                  - Device
                  - Statistics
                  - Partners
                  - Accounts
                  - Identifiers
                  - Multicast
                  - Group
                  - Wireless
                  - Device
                  - Things
                  - Certificates
                  - Sessions
                  - Destinations
                  - Profiles
                  - Fuota
                  - Tasks
                  - Groups
                  - Networks
                  - Analyzer
                  - Configurations
                  - Services
                  - Devices
                  - Gateways
                  - Gateway
                  - Tasks
                  - Definitions
                  - Names
                  - Configurations
                  - Data
                  - Identifiers
                  - Deregister
                  - Account
                  - Events
                  - Resources
                  - Types
                  - Logs
                  - Levels
                  - Positions
                  - Estimates
                  - Endpoints
                  - Statistics
            /wireless-gateways/{Identifier}:
              GET:
                summary: GetWirelessGateway
                description: <p>Gets information about a wireless gateway.</p>
                tags:
                  - Get
                  - Wireless
                  - Gateway
                  - Partners
                  - Accounts
                  - Identifiers
                  - Multicast
                  - Group
                  - Wireless
                  - Device
                  - Things
                  - Certificates
                  - Sessions
                  - Destinations
                  - Profiles
                  - Fuota
                  - Tasks
                  - Groups
                  - Networks
                  - Analyzer
                  - Configurations
                  - Services
                  - Devices
                  - Gateways
                  - Gateway
                  - Tasks
                  - Definitions
                  - Names
                  - Configurations
                  - Data
                  - Identifiers
                  - Deregister
                  - Account
                  - Events
                  - Resources
                  - Types
                  - Logs
                  - Levels
                  - Positions
                  - Estimates
                  - Endpoints
                  - Statistics
            /wireless-gateways/{Id}/firmware-information:
              GET:
                summary: GetWirelessGatewayFirmwareInformation
                description: >-
                  <p>Gets the firmware version and other information about a
                  wireless gateway.</p>
                tags:
                  - Get
                  - Wireless
                  - Gateway
                  - Firmware
                  - Information
                  - Partners
                  - Accounts
                  - Identifiers
                  - Multicast
                  - Group
                  - Wireless
                  - Device
                  - Things
                  - Certificates
                  - Sessions
                  - Destinations
                  - Profiles
                  - Fuota
                  - Tasks
                  - Groups
                  - Networks
                  - Analyzer
                  - Configurations
                  - Services
                  - Devices
                  - Gateways
                  - Gateway
                  - Tasks
                  - Definitions
                  - Names
                  - Configurations
                  - Data
                  - Identifiers
                  - Deregister
                  - Account
                  - Events
                  - Resources
                  - Types
                  - Logs
                  - Levels
                  - Positions
                  - Estimates
                  - Endpoints
                  - Statistics
                  - Firmware
                  - Information
            /wireless-gateways/{Id}/statistics:
              GET:
                summary: GetWirelessGatewayStatistics
                description: <p>Gets operating information about a wireless gateway.</p>
                tags:
                  - Get
                  - Wireless
                  - Gateway
                  - Statistics
                  - Partners
                  - Accounts
                  - Identifiers
                  - Multicast
                  - Group
                  - Wireless
                  - Device
                  - Things
                  - Certificates
                  - Sessions
                  - Destinations
                  - Profiles
                  - Fuota
                  - Tasks
                  - Groups
                  - Networks
                  - Analyzer
                  - Configurations
                  - Services
                  - Devices
                  - Gateways
                  - Gateway
                  - Tasks
                  - Definitions
                  - Names
                  - Configurations
                  - Data
                  - Identifiers
                  - Deregister
                  - Account
                  - Events
                  - Resources
                  - Types
                  - Logs
                  - Levels
                  - Positions
                  - Estimates
                  - Endpoints
                  - Statistics
                  - Firmware
                  - Information
            /wireless_device_import_task:
              POST:
                summary: StartWirelessDeviceImportTask
                description: >-
                  <p>Start import task for provisioning Sidewalk devices in bulk
                  using an S3 CSV file.</p>
                tags:
                  - Start
                  - Wireless
                  - Device
                  - Import
                  - Tasks
                  - Partners
                  - Accounts
                  - Identifiers
                  - Multicast
                  - Group
                  - Wireless
                  - Device
                  - Things
                  - Certificates
                  - Sessions
                  - Destinations
                  - Profiles
                  - Fuota
                  - Tasks
                  - Groups
                  - Networks
                  - Analyzer
                  - Configurations
                  - Services
                  - Devices
                  - Gateways
                  - Gateway
                  - Tasks
                  - Definitions
                  - Names
                  - Configurations
                  - Data
                  - Identifiers
                  - Deregister
                  - Account
                  - Events
                  - Resources
                  - Types
                  - Logs
                  - Levels
                  - Positions
                  - Estimates
                  - Endpoints
                  - Statistics
                  - Firmware
                  - Information
                  - Wireless_device_import_task
            /event-configurations:
              GET:
                summary: ListEventConfigurations
                description: >-
                  <p>List event configurations where at least one event topic
                  has been enabled.</p>
                tags:
                  - Lists
                  - Events
                  - Configurations
                  - Partners
                  - Accounts
                  - Identifiers
                  - Multicast
                  - Group
                  - Wireless
                  - Device
                  - Things
                  - Certificates
                  - Sessions
                  - Destinations
                  - Profiles
                  - Fuota
                  - Tasks
                  - Groups
                  - Networks
                  - Analyzer
                  - Configurations
                  - Services
                  - Devices
                  - Gateways
                  - Gateway
                  - Tasks
                  - Definitions
                  - Names
                  - Configurations
                  - Data
                  - Identifiers
                  - Deregister
                  - Account
                  - Events
                  - Resources
                  - Types
                  - Logs
                  - Levels
                  - Positions
                  - Estimates
                  - Endpoints
                  - Statistics
                  - Firmware
                  - Information
                  - Wireless_device_import_task
            /fuota-tasks/{Id}/multicast-groups:
              GET:
                summary: ListMulticastGroupsByFuotaTask
                description: <p>List all multicast groups associated with a fuota task.</p>
                tags:
                  - Lists
                  - Multicast
                  - Groups
                  - By
                  - Fuota
                  - Tasks
                  - Partners
                  - Accounts
                  - Identifiers
                  - Multicast
                  - Group
                  - Wireless
                  - Device
                  - Things
                  - Certificates
                  - Sessions
                  - Destinations
                  - Profiles
                  - Fuota
                  - Tasks
                  - Groups
                  - Networks
                  - Analyzer
                  - Configurations
                  - Services
                  - Devices
                  - Gateways
                  - Gateway
                  - Tasks
                  - Definitions
                  - Names
                  - Configurations
                  - Data
                  - Identifiers
                  - Deregister
                  - Account
                  - Events
                  - Resources
                  - Types
                  - Logs
                  - Levels
                  - Positions
                  - Estimates
                  - Endpoints
                  - Statistics
                  - Firmware
                  - Information
                  - Wireless_device_import_task
            /position-configurations:
              GET:
                summary: ListPositionConfigurations
                description: >-
                  <p>List position configurations for a given resource, such as
                  positioning solvers.</p> <important> <p>This action is no
                  longer supported. Calls to retrieve position information
                  should use the <a
                  href="https://docs.aws.amazon.com/iot-wireless/2020-11-22/apireference/API_GetResourcePosition.html">GetResourcePosition</a>
                  API operation instead.</p> </important>
                tags:
                  - Lists
                  - Positions
                  - Configurations
                  - Partners
                  - Accounts
                  - Identifiers
                  - Multicast
                  - Group
                  - Wireless
                  - Device
                  - Things
                  - Certificates
                  - Sessions
                  - Destinations
                  - Profiles
                  - Fuota
                  - Tasks
                  - Groups
                  - Networks
                  - Analyzer
                  - Configurations
                  - Services
                  - Devices
                  - Gateways
                  - Gateway
                  - Tasks
                  - Definitions
                  - Names
                  - Configurations
                  - Data
                  - Identifiers
                  - Deregister
                  - Account
                  - Events
                  - Resources
                  - Types
                  - Logs
                  - Levels
                  - Positions
                  - Estimates
                  - Endpoints
                  - Statistics
                  - Firmware
                  - Information
                  - Wireless_device_import_task
            /tags:
              DELETE:
                summary: UntagResource
                description: <p>Removes one or more tags from a resource.</p>
                tags:
                  - Untag
                  - Resources
                  - Partners
                  - Accounts
                  - Identifiers
                  - Multicast
                  - Group
                  - Wireless
                  - Device
                  - Things
                  - Certificates
                  - Sessions
                  - Destinations
                  - Profiles
                  - Fuota
                  - Tasks
                  - Groups
                  - Networks
                  - Analyzer
                  - Configurations
                  - Services
                  - Devices
                  - Gateways
                  - Gateway
                  - Tasks
                  - Definitions
                  - Names
                  - Configurations
                  - Data
                  - Identifiers
                  - Deregister
                  - Account
                  - Events
                  - Resources
                  - Types
                  - Logs
                  - Levels
                  - Positions
                  - Estimates
                  - Endpoints
                  - Statistics
                  - Firmware
                  - Information
                  - Wireless_device_import_task
                  - Tags
            /wireless_device_import_tasks:
              GET:
                summary: ListWirelessDeviceImportTasks
                description: >-
                  <p>List wireless devices that have been added to an import
                  task.</p>
                tags:
                  - Lists
                  - Wireless
                  - Device
                  - Import
                  - Tasks
                  - Partners
                  - Accounts
                  - Identifiers
                  - Multicast
                  - Group
                  - Wireless
                  - Device
                  - Things
                  - Certificates
                  - Sessions
                  - Destinations
                  - Profiles
                  - Fuota
                  - Tasks
                  - Groups
                  - Networks
                  - Analyzer
                  - Configurations
                  - Services
                  - Devices
                  - Gateways
                  - Gateway
                  - Tasks
                  - Definitions
                  - Names
                  - Configurations
                  - Data
                  - Identifiers
                  - Deregister
                  - Account
                  - Events
                  - Resources
                  - Types
                  - Logs
                  - Levels
                  - Positions
                  - Estimates
                  - Endpoints
                  - Statistics
                  - Firmware
                  - Information
                  - Wireless_device_import_task
                  - Tags
                  - Wireless_device_import_tasks
            /multicast-groups/{Id}/data:
              POST:
                summary: SendDataToMulticastGroup
                description: <p>Sends the specified data to a multicast group.</p>
                tags:
                  - Send
                  - Data
                  - To
                  - Multicast
                  - Group
                  - Partners
                  - Accounts
                  - Identifiers
                  - Multicast
                  - Group
                  - Wireless
                  - Device
                  - Things
                  - Certificates
                  - Sessions
                  - Destinations
                  - Profiles
                  - Fuota
                  - Tasks
                  - Groups
                  - Networks
                  - Analyzer
                  - Configurations
                  - Services
                  - Devices
                  - Gateways
                  - Gateway
                  - Tasks
                  - Definitions
                  - Names
                  - Configurations
                  - Data
                  - Identifiers
                  - Deregister
                  - Account
                  - Events
                  - Resources
                  - Types
                  - Logs
                  - Levels
                  - Positions
                  - Estimates
                  - Endpoints
                  - Statistics
                  - Firmware
                  - Information
                  - Wireless_device_import_task
                  - Tags
                  - Wireless_device_import_tasks
            /multicast-groups/{Id}/bulk:
              POST:
                summary: StartBulkDisassociateWirelessDeviceFromMulticastGroup
                description: >-
                  <p>Starts a bulk disassociatin of all qualifying wireless
                  devices from a multicast group.</p>
                tags:
                  - Start
                  - Bulk
                  - Disassociate
                  - Wireless
                  - Device
                  - From
                  - Multicast
                  - Group
                  - Partners
                  - Accounts
                  - Identifiers
                  - Multicast
                  - Group
                  - Wireless
                  - Device
                  - Things
                  - Certificates
                  - Sessions
                  - Destinations
                  - Profiles
                  - Fuota
                  - Tasks
                  - Groups
                  - Networks
                  - Analyzer
                  - Configurations
                  - Services
                  - Devices
                  - Gateways
                  - Gateway
                  - Tasks
                  - Definitions
                  - Names
                  - Configurations
                  - Data
                  - Identifiers
                  - Deregister
                  - Account
                  - Events
                  - Resources
                  - Types
                  - Logs
                  - Levels
                  - Positions
                  - Estimates
                  - Endpoints
                  - Statistics
                  - Firmware
                  - Information
                  - Wireless_device_import_task
                  - Tags
                  - Wireless_device_import_tasks
                  - Bulk
            /wireless_single_device_import_task:
              POST:
                summary: StartSingleWirelessDeviceImportTask
                description: <p>Start import task for a single wireless device.</p>
                tags:
                  - Start
                  - Single
                  - Wireless
                  - Device
                  - Import
                  - Tasks
                  - Partners
                  - Accounts
                  - Identifiers
                  - Multicast
                  - Group
                  - Wireless
                  - Device
                  - Things
                  - Certificates
                  - Sessions
                  - Destinations
                  - Profiles
                  - Fuota
                  - Tasks
                  - Groups
                  - Networks
                  - Analyzer
                  - Configurations
                  - Services
                  - Devices
                  - Gateways
                  - Gateway
                  - Tasks
                  - Definitions
                  - Names
                  - Configurations
                  - Data
                  - Identifiers
                  - Deregister
                  - Account
                  - Events
                  - Resources
                  - Types
                  - Logs
                  - Levels
                  - Positions
                  - Estimates
                  - Endpoints
                  - Statistics
                  - Firmware
                  - Information
                  - Wireless_device_import_task
                  - Tags
                  - Wireless_device_import_tasks
                  - Bulk
                  - Wireless_single_device_import_task
            /wireless-devices/{Id}/test:
              POST:
                summary: TestWirelessDevice
                description: >-
                  <p>Simulates a provisioned device by sending an uplink data
                  payload of <code>Hello</
                tags:
                  - Tests
                  - Wireless
                  - Device
                  - Partners
                  - Accounts
                  - Identifiers
                  - Multicast
                  - Group
                  - Wireless
                  - Device
                  - Things
                  - Certificates
                  - Sessions
                  - Destinations
                  - Profiles
                  - Fuota
                  - Tasks
                  - Groups
                  - Networks
                  - Analyzer
                  - Configurations
                  - Services
                  - Devices
                  - Gateways
                  - Gateway
                  - Tasks
                  - Definitions
                  - Names
                  - Configurations
                  - Data
                  - Identifiers
                  - Deregister
                  - Account
                  - Events
                  - Resources
                  - Types
                  - Logs
                  - Levels
                  - Positions
                  - Estimates
                  - Endpoints
                  - Statistics
                  - Firmware
                  - Information
                  - Wireless_device_import_task
                  - Tags
                  - Wireless_device_import_tasks
                  - Bulk
                  - Wireless_single_device_import_task
                  - Te
    overlays:
      - type: APIs.io Search
        url: overlays/iotwireless-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/iotwireless-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:iotwireless
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---