---
name: Campaigns
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/campaigns.png
url: https://example.com/apis/campaigns.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Campaigns
apis:
  - name: connectcampaigns
    description: <p>Provide APIs to create and manage Amazon Connect Campaigns.</p>
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
            title: connectcampaigns
          paths:
            /campaigns:
              PUT:
                summary: CreateCampaign
                description: >-
                  <p>Creates a campaign for the specified Amazon Connect
                  account. This API is idempotent.</p>
                tags:
                  - Create
                  - Campaigns
                  - Campaigns
            /campaigns/{id}:
              GET:
                summary: DescribeCampaign
                description: <p>Describes the specific campaign.</p>
                tags:
                  - Describe
                  - Campaigns
                  - Campaigns
                  - Identifiers
            /connect-instance/{connectInstanceId}/config:
              GET:
                summary: GetConnectInstanceConfig
                description: <p>Get the specific Connect instance config.</p>
                tags:
                  - Get
                  - Connect
                  - Instances
                  - Configurations
                  - Campaigns
                  - Identifiers
                  - Instances
                  - Configurations
            /connect-instance/{connectInstanceId}/onboarding:
              PUT:
                summary: StartInstanceOnboardingJob
                description: >-
                  <p>Onboard the specific Amazon Connect instance to Connect
                  Campaigns.</p>
                tags:
                  - Start
                  - Instances
                  - Onboarding
                  - Jobs
                  - Campaigns
                  - Identifiers
                  - Instances
                  - Configurations
                  - Onboarding
            /campaigns/{id}/state:
              GET:
                summary: GetCampaignState
                description: >-
                  <p>Get state of a campaign for the specified Amazon Connect
                  account.</p>
                tags:
                  - Get
                  - Campaigns
                  - States
                  - Campaigns
                  - Identifiers
                  - Instances
                  - Configurations
                  - Onboarding
                  - States
            /campaigns-state:
              POST:
                summary: GetCampaignStateBatch
                description: >-
                  <p>Get state of campaigns for the specified Amazon Connect
                  account.</p>
                tags:
                  - Get
                  - Campaigns
                  - States
                  - Batches
                  - Campaigns
                  - Identifiers
                  - Instances
                  - Configurations
                  - Onboarding
                  - States
            /campaigns-summary:
              POST:
                summary: ListCampaigns
                description: >-
                  <p>Provides summary information about the campaigns under the
                  specified Amazon Connect account.</p>
                tags:
                  - Lists
                  - Campaigns
                  - Campaigns
                  - Identifiers
                  - Instances
                  - Configurations
                  - Onboarding
                  - States
                  - Summaries
            /tags/{arn}:
              DELETE:
                summary: UntagResource
                description: <p>Untag a resource.</p>
                tags:
                  - Untag
                  - Resources
                  - Campaigns
                  - Identifiers
                  - Instances
                  - Configurations
                  - Onboarding
                  - States
                  - Summaries
                  - Tags
                  - ARN
            /campaigns/{id}/pause:
              POST:
                summary: PauseCampaign
                description: >-
                  <p>Pauses a campaign for the specified Amazon Connect
                  account.</p>
                tags:
                  - Pause
                  - Campaigns
                  - Campaigns
                  - Identifiers
                  - Instances
                  - Configurations
                  - Onboarding
                  - States
                  - Summaries
                  - Tags
                  - ARN
                  - Pause
            /campaigns/{id}/dial-requests:
              PUT:
                summary: PutDialRequestBatch
                description: >-
                  <p>Creates dials requests for the specified campaign Amazon
                  Connect account. This API is idempotent.</p>
                tags:
                  - Put
                  - Dial
                  - Request
                  - Batches
                  - Campaigns
                  - Identifiers
                  - Instances
                  - Configurations
                  - Onboarding
                  - States
                  - Summaries
                  - Tags
                  - ARN
                  - Pause
                  - Dial
                  - Requests
            /campaigns/{id}/resume:
              POST:
                summary: ResumeCampaign
                description: >-
                  <p>Stops a campaign for the specified Amazon Connect
                  account.</p>
                tags:
                  - Resume
                  - Campaigns
                  - Campaigns
                  - Identifiers
                  - Instances
                  - Configurations
                  - Onboarding
                  - States
                  - Summaries
                  - Tags
                  - ARN
                  - Pause
                  - Dial
                  - Requests
                  - Resume
            /campaigns/{id}/start:
              POST:
                summary: StartCampaign
                description: >-
                  <p>Starts a campaign for the specified Amazon Connect
                  account.</p>
                tags:
                  - Start
                  - Campaigns
                  - Campaigns
                  - Identifiers
                  - Instances
                  - Configurations
                  - Onboarding
                  - States
                  - Summaries
                  - Tags
                  - ARN
                  - Pause
                  - Dial
                  - Requests
                  - Resume
                  - Start
            /campaigns/{id}/stop:
              POST:
                summary: StopCampaign
                description: >-
                  <p>Stops a campaign for the specified Amazon Connect
                  account.</p>
                tags:
                  - Stop
                  - Campaigns
                  - Campaigns
                  - Identifiers
                  - Instances
                  - Configurations
                  - Onboarding
                  - States
                  - Summaries
                  - Tags
                  - ARN
                  - Pause
                  - Dial
                  - Requests
                  - Resume
                  - Start
                  - Stop
            /campaigns/{id}/dialer-config:
              POST:
                summary: UpdateCampaignDialerConfig
                description: >-
                  <p>Updates the dialer config of a campaign. This API is
                  idempotent.</p>
                tags:
                  - Update
                  - Campaigns
                  - Dialer
                  - Configurations
                  - Campaigns
                  - Identifiers
                  - Instances
                  - Configurations
                  - Onboarding
                  - States
                  - Summaries
                  - Tags
                  - ARN
                  - Pause
                  - Dial
                  - Requests
                  - Resume
                  - Start
                  - Stop
                  - Dialer
            /campaigns/{id}/name:
              POST:
                summary: UpdateCampaignName
                description: <p>Updates the name of a campaign. This API is idempotent.</p>
                tags:
                  - Update
                  - Campaigns
                  - Names
                  - Campaigns
                  - Identifiers
                  - Instances
                  - Configurations
                  - Onboarding
                  - States
                  - Summaries
                  - Tags
                  - ARN
                  - Pause
                  - Dial
                  - Requests
                  - Resume
                  - Start
                  - Stop
                  - Dialer
                  - Names
            /campaigns/{id}/outbound-call-config:
              POST:
                summary: UpdateCampaignOutboundCallConfig
                description: >-
                  <p>Updates the outbound call config of a campaign. This API is
                  idemp
                tags:
                  - Update
                  - Campaigns
                  - Outbound
                  - Call
                  - Configurations
                  - Campaigns
                  - Identifiers
                  - Instances
                  - Configurations
                  - Onboarding
                  - States
                  - Summaries
                  - Tags
                  - ARN
                  - Pause
                  - Dial
                  - Requests
                  - Resume
                  - Start
                  - Stop
                  - Dialer
                  - Names
                  - Outbound
                  - Ca
    overlays:
      - type: APIs.io Search
        url: overlays/connectcampaigns-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/connectcampaigns-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:connectcampaigns
  - name: pinpoint-email
    description: >-
      <fullname>Amazon Pinpoint Email Service</fullname> <p>Welcome to the
      <i>Amazon Pinpoint Email API Reference</i>. This guide provides
      information about the Amazon Pinpoint Email API (version 1.0), including
      supported operations, data types, parameters, and schemas.</p> <p> <a
      href="https://aws.amazon.com/pinpoint">Amazon Pinpoint</a> is an AWS
      service that you can use to engage with your customers across multiple
      messaging channels. You can use Amazon Pinpoint to send email, SMS text
      messages, voice messages, and push notifications. The Amazon Pinpoint
      Email API provides programmatic access to options that are unique to the
      email channel and supplement the options provided by the Amazon Pinpoint
      API.</p> <p>If you're new to Amazon Pinpoint, you might find it helpful to
      also review the <a
      href="https://docs.aws.amazon.com/pinpoint/latest/developerguide/welcome.html">Amazon
      Pinpoint Developer Guide</a>. The <i>Amazon Pinpoint Developer Guide</i>
      provides tutorials, code samples, and procedures that demonstrate how to
      use Amazon Pinpoint features programmatically and how to integrate Amazon
      Pinpoint functionality into mobile apps and other types of applications.
      The guide also provides information about key topics such as Amazon
      Pinpoint integration with other AWS services and the limits that apply to
      using the service.</p> <p>The Amazon Pinpoint Email API is available in
      several AWS Regions and it provides an endpoint for each of these Regions.
      For a list of all the Regions and endpoints where the API is currently
      available, see <a
      href="https://docs.aws.amazon.com/general/latest/gr/rande.html#pinpoint_region">AWS
      Service Endpoints</a> in the <i>Amazon Web Services General Reference</i>.
      To learn more about AWS Regions, see <a
      href="https://docs.aws.amazon.com/general/latest/gr/rande-manage.html">Managing
      AWS Regions</a> in the <i>Amazon Web Services General Reference</i>.</p>
      <p>In each Region, AWS maintains multiple Availability Zones. These
      Availability Zones are physically isolated from each other, but are united
      by private, low-latency, high-throughput, and highly redundant network
      connections. These Availability Zones enable us to provide very high
      levels of availability and redundancy, while also minimizing latency. To
      learn more about the number of Availability Zones that are available in
      each Region, see <a
      href="http://aws.amazon.com/about-aws/global-infrastructure/">AWS Global
      Infrastructure</a>.</p>
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
            title: pinpoint-email
          paths:
            /v1/email/configuration-sets:
              GET:
                summary: ListConfigurationSets
                description: >-
                  <p>List all of the configuration sets associated with your
                  Amazon Pinpoint account in the current region.</p> <p>In
                  Amazon Pinpoint, <i>configuration sets</i> are groups of rules
                  that you can apply to the emails you send. You apply a
                  configuration set to an email by including a reference to the
                  configuration set in the headers of the email. When you apply
                  a configuration set to an email, all of the rules in that
                  configuration set are applied to the email.</p>
                tags:
                  - Lists
                  - Configurations
                  - Sets
                  - V1
                  - Email
                  - Configurations
                  - Sets
            /v1/email/configuration-sets/{ConfigurationSetName}/event-destinations:
              GET:
                summary: GetConfigurationSetEventDestinations
                description: >-
                  <p>Retrieve a list of event destinations that are associated
                  with a configuration set.</p> <p>In Amazon Pinpoint,
                  <i>events</i> include message sends, deliveries, opens,
                  clicks, bounces, and complaints. <i>Event destinations</i> are
                  places that you can send information about these events to.
                  For example, you can send event data to Amazon SNS to receive
                  notifications when you receive bounces or complaints, or you
                  can use Amazon Kinesis Data Firehose to stream data to Amazon
                  S3 for long-term storage.</p>
                tags:
                  - Get
                  - Configurations
                  - Sets
                  - Events
                  - Destinations
                  - V1
                  - Email
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
            /v1/email/dedicated-ip-pools:
              GET:
                summary: ListDedicatedIpPools
                description: >-
                  <p>List all of the dedicated IP pools that exist in your
                  Amazon Pinpoint account in the current AWS Region.</p>
                tags:
                  - Lists
                  - Dedicated
                  - IP
                  - Pools
                  - V1
                  - Email
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Dedicated
                  - IP
                  - Pools
            /v1/email/deliverability-dashboard/test:
              POST:
                summary: CreateDeliverabilityTestReport
                description: >-
                  <p>Create a new predictive inbox placement test. Predictive
                  inbox placement tests can help you predict how your messages
                  will be handled by various email providers around the world.
                  When you perform a predictive inbox placement test, you
                  provide a sample message that contains the content that you
                  plan to send to your customers. Amazon Pinpoint then sends
                  that message to special email addresses spread across several
                  major email providers. After about 24 hours, the test is
                  complete, and you can use the
                  <code>GetDeliverabilityTestReport</code> operation to view the
                  results of the test.</p>
                tags:
                  - Create
                  - Deliverability
                  - Tests
                  - Reports
                  - V1
                  - Email
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
            /v1/email/identities:
              GET:
                summary: ListEmailIdentities
                description: >-
                  <p>Returns a list of all of the email identities that are
                  associated with your Amazon Pinpoint account. An identity can
                  be either an email address or a domain. This operation returns
                  identities that are verified as well as those that aren't.</p>
                tags:
                  - Lists
                  - Email
                  - Identities
                  - V1
                  - Email
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
            /v1/email/configuration-sets/{ConfigurationSetName}:
              GET:
                summary: GetConfigurationSet
                description: >-
                  <p>Get information about an existing configuration set,
                  including the dedicated IP pool that it's associated with,
                  whether or not it's enabled for sending email, and more.</p>
                  <p>In Amazon Pinpoint, <i>configuration sets</i> are groups of
                  rules that you can apply to the emails you send. You apply a
                  configuration set to an email by including a reference to the
                  configuration set in the headers of the email. When you apply
                  a configuration set to an email, all of the rules in that
                  configuration set are applied to the email.</p>
                tags:
                  - Get
                  - Configurations
                  - Sets
                  - V1
                  - Email
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
            /v1/email/configuration-sets/{ConfigurationSetName}/event-destinations/{EventDestinationName}:
              PUT:
                summary: UpdateConfigurationSetEventDestination
                description: >-
                  <p>Update the configuration of an event destination for a
                  configuration set.</p> <p>In Amazon Pinpoint, <i>events</i>
                  include message sends, deliveries, opens, clicks, bounces, and
                  complaints. <i>Event destinations</i> are places that you can
                  send information about these events to. For example, you can
                  send event data to Amazon SNS to receive notifications when
                  you receive bounces or complaints, or you can use Amazon
                  Kinesis Data Firehose to stream data to Amazon S3 for
                  long-term storage.</p>
                tags:
                  - Update
                  - Configurations
                  - Sets
                  - Events
                  - Destinations
                  - V1
                  - Email
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Destinations
            /v1/email/dedicated-ip-pools/{PoolName}:
              DELETE:
                summary: DeleteDedicatedIpPool
                description: <p>Delete a dedicated IP pool.</p>
                tags:
                  - Delete
                  - Dedicated
                  - IP
                  - Pools
                  - V1
                  - Email
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Destinations
                  - Pools
            /v1/email/identities/{EmailIdentity}:
              GET:
                summary: GetEmailIdentity
                description: >-
                  <p>Provides information about a specific identity associated
                  with your Amazon Pinpoint account, including the identity's
                  verification status, its DKIM authentication status, and its
                  custom Mail-From settings.</p>
                tags:
                  - Get
                  - Email
                  - Identity
                  - V1
                  - Email
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Destinations
                  - Pools
                  - Identity
            /v1/email/account:
              GET:
                summary: GetAccount
                description: >-
                  <p>Obtain information about the email-sending status and
                  capabilities of your Amazon Pinpoint account in the current
                  AWS Region.</p>
                tags:
                  - Get
                  - Account
                  - V1
                  - Email
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Destinations
                  - Pools
                  - Identity
                  - Account
            /v1/email/deliverability-dashboard/blacklist-report:
              GET:
                summary: GetBlacklistReports
                description: >-
                  <p>Retrieve a list of the blacklists that your dedicated IP
                  addresses appear on.</p>
                tags:
                  - Get
                  - Blacklist
                  - Reports
                  - V1
                  - Email
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Destinations
                  - Pools
                  - Identity
                  - Account
                  - Blacklist
                  - Reports
            /v1/email/dedicated-ips/{IP}:
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
                  - V1
                  - Email
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Destinations
                  - Pools
                  - Identity
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
            /v1/email/dedicated-ips:
              GET:
                summary: GetDedicatedIps
                description: >-
                  <p>List the dedicated IP addresses that are associated with
                  your Amazon Pinpoint account.</p>
                tags:
                  - Get
                  - Dedicated
                  - IP Addresses
                  - V1
                  - Email
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Destinations
                  - Pools
                  - Identity
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
            /v1/email/deliverability-dashboard:
              PUT:
                summary: PutDeliverabilityDashboardOption
                description: >-
                  <p>Enable or disable the Deliverability dashboard for your
                  Amazon Pinpoint account. When you enable the Deliverability
                  dashboard, you gain access to reputation, deliverability, and
                  other metrics for the domains that you use to send email using
                  Amazon Pinpoint. You also gain the ability to perform
                  predictive inbox placement tests.</p> <p>When you use the
                  Deliverability dashboard, you pay a monthly subscription
                  charge, in addition to any other fees that you accrue by using
                  Amazon Pinpoint. For more information about the features and
                  cost of a Deliverability dashboard subscription, see <a
                  href="http://aws.amazon.com/pinpoint/pricing/">Amazon Pinpoint
                  Pricing</a>.</p>
                tags:
                  - Put
                  - Deliverability
                  - Dashboard
                  - Options
                  - V1
                  - Email
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Destinations
                  - Pools
                  - Identity
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
            /v1/email/deliverability-dashboard/test-reports/{ReportId}:
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
                  - V1
                  - Email
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Destinations
                  - Pools
                  - Identity
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Identifiers
            /v1/email/deliverability-dashboard/campaigns/{CampaignId}:
              GET:
                summary: GetDomainDeliverabilityCampaign
                description: >-
                  <p>Retrieve all the deliverability data for a specific
                  campaign. This data is available for a campaign only if the
                  campaign sent email by using a domain that the Deliverability
                  dashboard is enabled for
                  (<code>PutDeliverabilityDashboardOption</code> operation).</p>
                tags:
                  - Get
                  - Domains
                  - Deliverability
                  - Campaigns
                  - V1
                  - Email
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Destinations
                  - Pools
                  - Identity
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Identifiers
                  - Campaigns
            /v1/email/deliverability-dashboard/statistics-report/{Domain}:
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
                  - V1
                  - Email
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Destinations
                  - Pools
                  - Identity
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Identifiers
                  - Campaigns
                  - Domains
            /v1/email/deliverability-dashboard/test-reports:
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
                  - V1
                  - Email
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Destinations
                  - Pools
                  - Identity
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Identifiers
                  - Campaigns
                  - Domains
                  - Reports
            /v1/email/deliverability-dashboard/domains/{SubscribedDomain}/campaigns:
              GET:
                summary: ListDomainDeliverabilityCampaigns
                description: >-
                  <p>Retrieve deliverability data for all the campaigns that
                  used a specific domain to send email during a specified time
                  range. This data is available for a domain only if you enabled
                  the Deliverability dashboard
                  (<code>PutDeliverabilityDashboardOption</code> operation) for
                  the domain.</p>
                tags:
                  - Lists
                  - Domains
                  - Deliverability
                  - Campaigns
                  - V1
                  - Email
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Destinations
                  - Pools
                  - Identity
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Identifiers
                  - Campaigns
                  - Domains
                  - Reports
                  - Subscribed
                  - Campaigns
            /v1/email/tags:
              DELETE:
                summary: UntagResource
                description: >-
                  <p>Remove one or more tags (keys and values) from a specified
                  resource.</p>
                tags:
                  - Untag
                  - Resources
                  - V1
                  - Email
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Destinations
                  - Pools
                  - Identity
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Identifiers
                  - Campaigns
                  - Domains
                  - Reports
                  - Subscribed
                  - Campaigns
                  - Tags
            /v1/email/account/dedicated-ips/warmup:
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
                  - V1
                  - Email
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Destinations
                  - Pools
                  - Identity
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Identifiers
                  - Campaigns
                  - Domains
                  - Reports
                  - Subscribed
                  - Campaigns
                  - Tags
                  - Warmup
            /v1/email/account/sending:
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
                  - V1
                  - Email
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Destinations
                  - Pools
                  - Identity
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Identifiers
                  - Campaigns
                  - Domains
                  - Reports
                  - Subscribed
                  - Campaigns
                  - Tags
                  - Warmup
                  - Sending
            /v1/email/configuration-sets/{ConfigurationSetName}/delivery-options:
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
                  - V1
                  - Email
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Destinations
                  - Pools
                  - Identity
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Identifiers
                  - Campaigns
                  - Domains
                  - Reports
                  - Subscribed
                  - Campaigns
                  - Tags
                  - Warmup
                  - Sending
                  - Deliveries
                  - Options
            /v1/email/configuration-sets/{ConfigurationSetName}/reputation-options:
              PUT:
                summary: PutConfigurationSetReputationOptions
                description: >-
                  <p>Enable or disable collection of reputation metrics for
                  emails that you send using a particular configuration set in a
                  specific AWS Region.</p>
                tags:
                  - Put
                  - Configurations
                  - Sets
                  - Reputation
                  - Options
                  - V1
                  - Email
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Destinations
                  - Pools
                  - Identity
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Identifiers
                  - Campaigns
                  - Domains
                  - Reports
                  - Subscribed
                  - Campaigns
                  - Tags
                  - Warmup
                  - Sending
                  - Deliveries
                  - Options
                  - Reputation
            /v1/email/configuration-sets/{ConfigurationSetName}/sending:
              PUT:
                summary: PutConfigurationSetSendingOptions
                description: >-
                  <p>Enable or disable email sending for messages that use a
                  particular configuration set in a specific AWS Region.</p>
                tags:
                  - Put
                  - Configurations
                  - Sets
                  - Sending
                  - Options
                  - V1
                  - Email
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Destinations
                  - Pools
                  - Identity
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Identifiers
                  - Campaigns
                  - Domains
                  - Reports
                  - Subscribed
                  - Campaigns
                  - Tags
                  - Warmup
                  - Sending
                  - Deliveries
                  - Options
                  - Reputation
            /v1/email/configuration-sets/{ConfigurationSetName}/tracking-options:
              PUT:
                summary: PutConfigurationSetTrackingOptions
                description: >-
                  <p>Specify a custom domain to use for open and click tracking
                  elements in email that you send using Amazon Pinpoint.</p>
                tags:
                  - Put
                  - Configurations
                  - Sets
                  - Tracking
                  - Options
                  - V1
                  - Email
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Destinations
                  - Pools
                  - Identity
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Identifiers
                  - Campaigns
                  - Domains
                  - Reports
                  - Subscribed
                  - Campaigns
                  - Tags
                  - Warmup
                  - Sending
                  - Deliveries
                  - Options
                  - Reputation
                  - Tracking
            /v1/email/dedicated-ips/{IP}/pool:
              PUT:
                summary: PutDedicatedIpInPool
                description: >-
                  <p>Move a dedicated IP address to an existing dedicated IP
                  pool.</p> <note> <p>The dedicated IP address that you specify
                  must already exist, and must be associated with your Amazon
                  Pinpoint account. </p> <p>The dedicated IP pool you specify
                  must already exist. You can create a new pool by using the
                  <code>CreateDedicatedIpPool</code> operation.</p> </note>
                tags:
                  - Put
                  - Dedicated
                  - IP
                  - In
                  - Pools
                  - V1
                  - Email
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Destinations
                  - Pools
                  - Identity
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Identifiers
                  - Campaigns
                  - Domains
                  - Reports
                  - Subscribed
                  - Campaigns
                  - Tags
                  - Warmup
                  - Sending
                  - Deliveries
                  - Options
                  - Reputation
                  - Tracking
            /v1/email/dedicated-ips/{IP}/warmup:
              PUT:
                summary: PutDedicatedIpWarmupAttributes
                description: <p/>
                tags:
                  - Put
                  - Dedicated
                  - IP
                  - Warmup
                  - Attributes
                  - V1
                  - Email
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Destinations
                  - Pools
                  - Identity
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Identifiers
                  - Campaigns
                  - Domains
                  - Reports
                  - Subscribed
                  - Campaigns
                  - Tags
                  - Warmup
                  - Sending
                  - Deliveries
                  - Options
                  - Reputation
                  - Tracking
            /v1/email/identities/{EmailIdentity}/dkim:
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
                  - V1
                  - Email
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Destinations
                  - Pools
                  - Identity
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Identifiers
                  - Campaigns
                  - Domains
                  - Reports
                  - Subscribed
                  - Campaigns
                  - Tags
                  - Warmup
                  - Sending
                  - Deliveries
                  - Options
                  - Reputation
                  - Tracking
                  - DKIM
            /v1/email/identities/{EmailIdentity}/feedback:
              PUT:
                summary: PutEmailIdentityFeedbackAttributes
                description: >-
                  <p>Used to enable or disable feedback forwarding for an
                  identity. This setting determines what happens when an
                  identity is used to send an email that results in a bounce or
                  complaint event.</p> <p>When you enable feedback forwarding,
                  Amazon Pinpoint sends you email notifications when bounce or
                  complaint events occur. Amazon Pinpoint sends this
                  notification to the address that you specified in the
                  Return-Path header of the original email.</p> <p>When you
                  disable feedback forwarding, Amazon Pinpoint sends
                  notifications through other mechanisms, such as by notifying
                  an Amazon SNS topic. You're required to have a method of
                  tracking bounces and complaints. If you haven't set up another
                  mechanism for receiving bounce or complaint notifications,
                  Amazon Pinpoint sends an email notification when these events
                  occur (even if this setting is disabled).</p>
                tags:
                  - Put
                  - Email
                  - Identity
                  - Feedback
                  - Attributes
                  - V1
                  - Email
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Destinations
                  - Pools
                  - Identity
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Identifiers
                  - Campaigns
                  - Domains
                  - Reports
                  - Subscribed
                  - Campaigns
                  - Tags
                  - Warmup
                  - Sending
                  - Deliveries
                  - Options
                  - Reputation
                  - Tracking
                  - DKIM
                  - Feedback
            /v1/email/identities/{EmailIdentity}/mail-from:
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
                  - V1
                  - Email
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Destinations
                  - Pools
                  - Identity
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Identifiers
                  - Campaigns
                  - Domains
                  - Reports
                  - Subscribed
                  - Campaigns
                  - Tags
                  - Warmup
                  - Sending
                  - Deliveries
                  - Options
                  - Reputation
                  - Tracking
                  - DKIM
                  - Feedback
                  - Mail
                  - From
            /v1/email/outbound-emails:
              POST:
                summary: SendEmail
                description: >-
                  <p>Sends an email message. You can use the Amazon Pinpoint
                  Email API to send two types of messages:</p> <ul> <li> <p>
                  <b>Simple</b> – A standard email message. When you create this
                  type of message, you specify the sender, the recipient, and
                  the message body, and Amazon Pinpoint assembles the message
                  for you.</p> </li> <li> <p> <b>Raw</b> – A raw, MIME-formatted
                  email message. When you send this type of email, you have to
                  specify all of the message headers, as well as the message
                  body. You can use this message type to send messages that
                  contain attachments. The message that you specify has to be a
                  valid MIME message.</p> <
                tags:
                  - Send
                  - Email
                  - V1
                  - Email
                  - Configurations
                  - Sets
                  - Sets
                  - Names
                  - Events
                  - Destinations
                  - Dedicated
                  - IP
                  - Pools
                  - Deliverability
                  - Dashboard
                  - Tests
                  - Identities
                  - Destinations
                  - Pools
                  - Identity
                  - Account
                  - Blacklist
                  - Reports
                  - IP Addresses
                  - Identifiers
                  - Campaigns
                  - Domains
                  - Reports
                  - Subscribed
                  - Campaigns
                  - Tags
                  - Warmup
                  - Sending
                  - Deliveries
                  - Options
                  - Reputation
                  - Tracking
                  - DKIM
                  - Feedback
                  - Mail
                  - From
                  - Outbound
                  - Email
    overlays:
      - type: APIs.io Search
        url: overlays/pinpoint-email-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/pinpoint-email-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:pinpoint-email
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
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---