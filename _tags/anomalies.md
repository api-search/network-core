---
name: Anomalies
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/anomalies.png
url: https://example.com/apis/anomalies.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Anomalies
apis:
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
  - name: lookoutvision
    description: >-
      <p>This is the Amazon Lookout for Vision API Reference. It provides
      descriptions of actions, data types, common parameters, and common
      errors.</p> <p>Amazon Lookout for Vision enables you to find visual
      defects in industrial products, accurately and at scale. It uses computer
      vision to identify missing components in an industrial product, damage to
      vehicles or structures, irregularities in production lines, and even
      minuscule defects in silicon wafers — or any other physical item where
      quality is important such as a missing capacitor on printed circuit
      boards.</p>
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
            title: lookoutvision
          paths:
            /2020-11-20/projects/{projectName}/datasets:
              POST:
                summary: CreateDataset
                description: >-
                  <p>Creates a new dataset in an Amazon Lookout for Vision
                  project. <code>CreateDataset</code> can create a training or a
                  test dataset from a valid dataset source
                  (<code>DatasetSource</code>).</p> <p>If you want a single
                  dataset project, specify <code>train</code> for the value of
                  <code>DatasetType</code>.</p> <p>To have a project with
                  separate training and test datasets, call
                  <code>CreateDataset</code> twice. On the first call, specify
                  <code>train</code> for the value of <code>DatasetType</code>.
                  On the second call, specify <code>test</code> for the value of
                  <code>DatasetType</code>. </p> <p>This operation requires
                  permissions to perform the
                  <code>lookoutvision:CreateDataset</code> operation.</p>
                tags:
                  - Create
                  - Datasets
                  - Names
                  - Datasets
            /2020-11-20/projects/{projectName}/models:
              GET:
                summary: ListModels
                description: >-
                  <p>Lists the versions of a model in an Amazon Lookout for
                  Vision project.</p> <p>The <code>ListModels</code> operation
                  is eventually consistent. Recent calls to
                  <code>CreateModel</code> might take a while to appear in the
                  response from <code>ListProjects</code>.</p> <p>This operation
                  requires permissions to perform the
                  <code>lookoutvision:ListModels</code> operation.</p>
                tags:
                  - Lists
                  - Models
                  - Names
                  - Datasets
                  - Models
            /2020-11-20/projects:
              GET:
                summary: ListProjects
                description: >-
                  <p>Lists the Amazon Lookout for Vision projects in your AWS
                  account that are in the AWS Region in which you call
                  <code>ListProjects</code>.</p> <p>The
                  <code>ListProjects</code> operation is eventually consistent.
                  Recent calls to <code>CreateProject</code> and
                  <code>DeleteProject</code> might take a while to appear in the
                  response from <code>ListProjects</code>.</p> <p>This operation
                  requires permissions to perform the
                  <code>lookoutvision:ListProjects</code> operation.</p>
                tags:
                  - Lists
                  - Projects
                  - Names
                  - Datasets
                  - Models
                  - '2020'
                  - '11'
                  - '20'
                  - Projects
            /2020-11-20/projects/{projectName}/datasets/{datasetType}:
              GET:
                summary: DescribeDataset
                description: >-
                  <p>Describe an Amazon Lookout for Vision dataset.</p> <p>This
                  operation requires permissions to perform the
                  <code>lookoutvision:DescribeDataset</code> operation.</p>
                tags:
                  - Describe
                  - Datasets
                  - Names
                  - Datasets
                  - Models
                  - '2020'
                  - '11'
                  - '20'
                  - Projects
                  - Datasets
                  - Types
            /2020-11-20/projects/{projectName}/models/{modelVersion}:
              GET:
                summary: DescribeModel
                description: >-
                  <p>Describes a version of an Amazon Lookout for Vision
                  model.</p> <p>This operation requires permissions to perform
                  the <code>lookoutvision:DescribeModel</code> operation.</p>
                tags:
                  - Describe
                  - Models
                  - Names
                  - Datasets
                  - Models
                  - '2020'
                  - '11'
                  - '20'
                  - Projects
                  - Datasets
                  - Types
                  - Models
                  - Versions
            /2020-11-20/projects/{projectName}:
              GET:
                summary: DescribeProject
                description: >-
                  <p>Describes an Amazon Lookout for Vision project.</p> <p>This
                  operation requires permissions to perform the
                  <code>lookoutvision:DescribeProject</code> operation.</p>
                tags:
                  - Describe
                  - Projects
                  - Names
                  - Datasets
                  - Models
                  - '2020'
                  - '11'
                  - '20'
                  - Projects
                  - Datasets
                  - Types
                  - Models
                  - Versions
            /2020-11-20/projects/{projectName}/modelpackagingjobs/{jobName}:
              GET:
                summary: DescribeModelPackagingJob
                description: >-
                  <p>Describes an Amazon Lookout for Vision model packaging job.
                  </p> <p>This operation requires permissions to perform the
                  <code>lookoutvision:DescribeModelPackagingJob</code>
                  operation.</p> <p>For more information, see <i>Using your
                  Amazon Lookout for Vision model on an edge device</i> in the
                  Amazon Lookout for Vision Developer Guide. </p>
                tags:
                  - Describe
                  - Models
                  - Packaging
                  - Jobs
                  - Names
                  - Datasets
                  - Models
                  - '2020'
                  - '11'
                  - '20'
                  - Projects
                  - Datasets
                  - Types
                  - Models
                  - Versions
                  - Model Packaging Jobs
                  - Jobs
            /2020-11-20/projects/{projectName}/models/{modelVersion}/detect:
              POST:
                summary: DetectAnomalies
                description: >-
                  <p>Detects anomalies in an image that you supply. </p> <p>The
                  response from <code>DetectAnomalies</code> includes a boolean
                  prediction that the image contains one or more anomalies and a
                  confidence value for the prediction. If the model is an image
                  segmentation model, the response also includes segmentation
                  information for each type of anomaly found in the image.</p>
                  <note> <p>Before calling <code>DetectAnomalies</code>, you
                  must first start your model with the <a>StartModel</a>
                  operation. You are charged for the amount of time, in minutes,
                  that a model runs and for the number of anomaly detection
                  units that your model uses. If you are not using a model, use
                  the <a>StopModel</a> operation to stop your model. </p>
                  </note> <p>For more information, see <i>Detecting anomalies in
                  an image</i> in the Amazon Lookout for Vision developer
                  guide.</p> <p>This operation requires permissions to perform
                  the <code>lookoutvision:DetectAnomalies</code> operation.</p>
                tags:
                  - Detect
                  - Anomalies
                  - Names
                  - Datasets
                  - Models
                  - '2020'
                  - '11'
                  - '20'
                  - Projects
                  - Datasets
                  - Types
                  - Models
                  - Versions
                  - Model Packaging Jobs
                  - Jobs
                  - Detect
            /2020-11-20/projects/{projectName}/datasets/{datasetType}/entries:
              PATCH:
                summary: UpdateDatasetEntries
                description: >-
                  <p>Adds or updates one or more JSON Line entries in a dataset.
                  A JSON Line includes information about an image used for
                  training or testing an Amazon Lookout for Vision model.</p>
                  <p>To update an existing JSON Line, use the
                  <code>source-ref</code> field to identify the JSON Line. The
                  JSON line that you supply replaces the existing JSON line. Any
                  existing annotations that are not in the new JSON line are
                  removed from the dataset. </p> <p>For more information, see
                  <i>Defining JSON lines for anomaly classification</i> in the
                  Amazon Lookout for Vision Developer Guide. </p> <note> <p>The
                  images you reference in the <code>source-ref</code> field of a
                  JSON line, must be in the same S3 bucket as the existing
                  images in the dataset. </p> </note> <p>Updating a dataset
                  might take a while to complete. To check the current status,
                  call <a>DescribeDataset</a> and check the <code>Status</code>
                  field in the response.</p> <p>This operation requires
                  permissions to perform the
                  <code>lookoutvision:UpdateDatasetEntries</code> operation.</p>
                tags:
                  - Update
                  - Datasets
                  - Entries
                  - Names
                  - Datasets
                  - Models
                  - '2020'
                  - '11'
                  - '20'
                  - Projects
                  - Datasets
                  - Types
                  - Models
                  - Versions
                  - Model Packaging Jobs
                  - Jobs
                  - Detect
                  - Entries
            /2020-11-20/projects/{projectName}/modelpackagingjobs:
              POST:
                summary: StartModelPackagingJob
                description: >-
                  <p>Starts an Amazon Lookout for Vision model packaging job. A
                  model packaging job creates an AWS IoT Greengrass component
                  for a Lookout for Vision model. You can use the component to
                  deploy your model to an edge device managed by Greengrass.
                  </p> <p>Use the <a>DescribeModelPackagingJob</a> API to
                  determine the current status of the job. The model packaging
                  job is complete if the value of <code>Status</code> is
                  <code>SUCCEEDED</code>.</p> <p>To deploy the component to the
                  target device, use the component name and component version
                  with the AWS IoT Greengrass <a
                  href="https://docs.aws.amazon.com/greengrass/v2/APIReference/API_CreateDeployment.html">CreateDeployment</a>
                  API.</p> <p>This operation requires the following
                  permissions:</p> <ul> <li> <p>
                  <code>lookoutvision:StartModelPackagingJob</code> </p> </li>
                  <li> <p> <code>s3:PutObject</code> </p> </li> <li> <p>
                  <code>s3:GetBucketLocation</code> </p> </li> <li> <p>
                  <code>kms:GenerateDataKey</code> </p> </li> <li> <p>
                  <code>greengrass:CreateComponentVersion</code> </p> </li> <li>
                  <p> <code>greengrass:DescribeComponent</code> </p> </li> <li>
                  <p>(Optional) <code>greengrass:TagResource</code>. Only
                  required if you want to tag the component.</p> </li> </ul>
                  <p>For more information, see <i>Using your Amazon Lookout for
                  Vision model on an edge device</i> in the Amazon Lookout for
                  Vision Developer Guide. </p>
                tags:
                  - Start
                  - Models
                  - Packaging
                  - Jobs
                  - Names
                  - Datasets
                  - Models
                  - '2020'
                  - '11'
                  - '20'
                  - Projects
                  - Datasets
                  - Types
                  - Models
                  - Versions
                  - Model Packaging Jobs
                  - Jobs
                  - Detect
                  - Entries
            /2020-11-20/tags/{resourceArn}:
              DELETE:
                summary: UntagResource
                description: >-
                  <p>Removes one or more tags from an Amazon Lookout for Vision
                  model. For more information, see <i>Tagging a model</i> in the
                  <i>Amazon Lookout for Vision Developer Guide</i>. </p> <p>This
                  operation requires permissions to perform the
                  <code>lookoutvision:UntagResource</code> operation.</p>
                tags:
                  - Untag
                  - Resources
                  - Names
                  - Datasets
                  - Models
                  - '2020'
                  - '11'
                  - '20'
                  - Projects
                  - Datasets
                  - Types
                  - Models
                  - Versions
                  - Model Packaging Jobs
                  - Jobs
                  - Detect
                  - Entries
                  - ARN
            /2020-11-20/projects/{projectName}/models/{modelVersion}/start:
              POST:
                summary: StartModel
                description: >-
                  <p>Starts the running of the version of an Amazon Lookout for
                  Vision model. Starting a model takes a while to complete. To
                  check the current state of the model, use
                  <a>DescribeModel</a>.</p> <p>A model is ready to use when its
                  status is <code>HOSTED</code>.</p> <p>Once the model is
                  running, you can detect custom labels in new images by calling
                  <a>DetectAnomalies</a>.</p> <note> <p>You are charged for the
                  amount of time that the model is running. To stop a running
                  model, call <a>StopModel</a>.</p> </note> <p>This operation
                  requires permissions to perform the
                  <code>lookoutvision:StartModel</code> operation.</p>
                tags:
                  - Start
                  - Models
                  - Names
                  - Datasets
                  - Models
                  - '2020'
                  - '11'
                  - '20'
                  - Projects
                  - Datasets
                  - Types
                  - Models
                  - Versions
                  - Model Packaging Jobs
                  - Jobs
                  - Detect
                  - Entries
                  - ARN
                  - Start
            /2020-11-20/projects/{projectName}/models/{modelVersion}/stop:
              POST:
                summary: StopModel
                description: >-
                  <p>Stops the hosting of a running model. The operation might
                  take a while to complete. To check the current status, call
                  <a>DescribeModel</a>. </p> <p>After the model hosting stops,
                  the <code>Status</code> of the model is
                  <code>TRAINED</code>.</p> <p>This operation requires
                  permissions to perform the
                  <code>lookoutvision:StopModel</code> oper
                tags:
                  - Stop
                  - Models
                  - Names
                  - Datasets
                  - Models
                  - '2020'
                  - '11'
                  - '20'
                  - Projects
                  - Datasets
                  - Types
                  - Models
                  - Versions
                  - Model Packaging Jobs
                  - Jobs
                  - Detect
                  - Entries
                  - ARN
                  - Start
                  - St
    overlays:
      - type: APIs.io Search
        url: overlays/lookoutvision-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/lookoutvision-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:lookoutvision
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---