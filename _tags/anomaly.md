---
name: Anomaly
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/anomaly.png
url: https://example.com/apis/anomaly.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Anomaly
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
  - name: logs
    description: >-
      <p>You can use Amazon CloudWatch Logs to monitor, store, and access your
      log files from EC2 instances, CloudTrail, and other sources. You can then
      retrieve the associated log data from CloudWatch Logs using the CloudWatch
      console. Alternatively, you can use CloudWatch Logs commands in the Amazon
      Web Services CLI, CloudWatch Logs API, or CloudWatch Logs SDK.</p> <p>You
      can use CloudWatch Logs to:</p> <ul> <li> <p> <b>Monitor logs from EC2
      instances in real time</b>: You can use CloudWatch Logs to monitor
      applications and systems using log data. For example, CloudWatch Logs can
      track the number of errors that occur in your application logs. Then, it
      can send you a notification whenever the rate of errors exceeds a
      threshold that you specify. CloudWatch Logs uses your log data for
      monitoring so no code changes are required. For example, you can monitor
      application logs for specific literal terms (such as
      "NullReferenceException"). You can also count the number of occurrences of
      a literal term at a particular position in log data (such as "404" status
      codes in an Apache access log). When the term you are searching for is
      found, CloudWatch Logs reports the data to a CloudWatch metric that you
      specify.</p> </li> <li> <p> <b>Monitor CloudTrail logged events</b>: You
      can create alarms in CloudWatch and receive notifications of particular
      API activity as captured by CloudTrail. You can use the notification to
      perform troubleshooting.</p> </li> <li> <p> <b>Archive log data</b>: You
      can use CloudWatch Logs to store your log data in highly durable storage.
      You can change the log retention setting so that any log events earlier
      than this setting are automatically deleted. The CloudWatch Logs agent
      helps to quickly send both rotated and non-rotated log data off of a host
      and into the log service. You can then access the raw log data when you
      need it.</p> </li> </ul>
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
            title: logs
          paths:
            /:
              POST:
                summary: UpdateLogAnomalyDetector
                description: <p>Updates an existing log anomaly det
                tags:
                  - Update
                  - Logs
                  - Anomaly
                  - Detect
    overlays:
      - type: APIs.io Search
        url: overlays/logs-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/logs-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:logs
  - name: lookoutmetrics
    description: >-
      <p>This is the <i>Amazon Lookout for Metrics API Reference</i>. For an
      introduction to the service with tutorials for getting started, visit <a
      href="https://docs.aws.amazon.com/lookoutmetrics/latest/dev">Amazon
      Lookout for Metrics Developer Guide</a>.</p>
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
            title: lookoutmetrics
          paths:
            /ActivateAnomalyDetector:
              POST:
                summary: ActivateAnomalyDetector
                description: <p>Activates an anomaly detector.</p>
                tags:
                  - Activate
                  - Anomaly
                  - Detectors
                  - Activate
                  - Anomaly
                  - Detectors
            /BackTestAnomalyDetector:
              POST:
                summary: BackTestAnomalyDetector
                description: >-
                  <p>Runs a backtest for anomaly detection for the specified
                  resource.</p>
                tags:
                  - Back
                  - Tests
                  - Anomaly
                  - Detectors
                  - Activate
                  - Anomaly
                  - Detectors
                  - Back
                  - Tests
            /CreateAlert:
              POST:
                summary: CreateAlert
                description: <p>Creates an alert for an anomaly detector.</p>
                tags:
                  - Create
                  - Alerts
                  - Activate
                  - Anomaly
                  - Detectors
                  - Back
                  - Tests
                  - Create
                  - Alerts
            /CreateAnomalyDetector:
              POST:
                summary: CreateAnomalyDetector
                description: <p>Creates an anomaly detector.</p>
                tags:
                  - Create
                  - Anomaly
                  - Detectors
                  - Activate
                  - Anomaly
                  - Detectors
                  - Back
                  - Tests
                  - Create
                  - Alerts
            /CreateMetricSet:
              POST:
                summary: CreateMetricSet
                description: <p>Creates a dataset.</p>
                tags:
                  - Create
                  - Metrics
                  - Sets
                  - Activate
                  - Anomaly
                  - Detectors
                  - Back
                  - Tests
                  - Create
                  - Alerts
                  - Metrics
                  - Sets
            /DeactivateAnomalyDetector:
              POST:
                summary: DeactivateAnomalyDetector
                description: <p>Deactivates an anomaly detector.</p>
                tags:
                  - Deactivate
                  - Anomaly
                  - Detectors
                  - Activate
                  - Anomaly
                  - Detectors
                  - Back
                  - Tests
                  - Create
                  - Alerts
                  - Metrics
                  - Sets
                  - Deactivate
            /DeleteAlert:
              POST:
                summary: DeleteAlert
                description: <p>Deletes an alert.</p>
                tags:
                  - Delete
                  - Alerts
                  - Activate
                  - Anomaly
                  - Detectors
                  - Back
                  - Tests
                  - Create
                  - Alerts
                  - Metrics
                  - Sets
                  - Deactivate
                  - Delete
            /DeleteAnomalyDetector:
              POST:
                summary: DeleteAnomalyDetector
                description: >-
                  <p>Deletes a detector. Deleting an anomaly detector will
                  delete all of its corresponding resources including any
                  configured datasets and alerts.</p>
                tags:
                  - Delete
                  - Anomaly
                  - Detectors
                  - Activate
                  - Anomaly
                  - Detectors
                  - Back
                  - Tests
                  - Create
                  - Alerts
                  - Metrics
                  - Sets
                  - Deactivate
                  - Delete
            /DescribeAlert:
              POST:
                summary: DescribeAlert
                description: >-
                  <p>Describes an alert.</p> <p>Amazon Lookout for Metrics API
                  actions are eventually consistent. If you do a read operation
                  on a resource immediately after creating or modifying it, use
                  retries to allow time for the write operation to complete.</p>
                tags:
                  - Describe
                  - Alerts
                  - Activate
                  - Anomaly
                  - Detectors
                  - Back
                  - Tests
                  - Create
                  - Alerts
                  - Metrics
                  - Sets
                  - Deactivate
                  - Delete
                  - Describe
            /DescribeAnomalyDetectionExecutions:
              POST:
                summary: DescribeAnomalyDetectionExecutions
                description: >-
                  <p>Returns information about the status of the specified
                  anomaly detection jobs.</p>
                tags:
                  - Describe
                  - Anomaly
                  - Detections
                  - Executions
                  - Activate
                  - Anomaly
                  - Detectors
                  - Back
                  - Tests
                  - Create
                  - Alerts
                  - Metrics
                  - Sets
                  - Deactivate
                  - Delete
                  - Describe
                  - Detections
                  - Executions
            /DescribeAnomalyDetector:
              POST:
                summary: DescribeAnomalyDetector
                description: >-
                  <p>Describes a detector.</p> <p>Amazon Lookout for Metrics API
                  actions are eventually consistent. If you do a read operation
                  on a resource immediately after creating or modifying it, use
                  retries to allow time for the write operation to complete.</p>
                tags:
                  - Describe
                  - Anomaly
                  - Detectors
                  - Activate
                  - Anomaly
                  - Detectors
                  - Back
                  - Tests
                  - Create
                  - Alerts
                  - Metrics
                  - Sets
                  - Deactivate
                  - Delete
                  - Describe
                  - Detections
                  - Executions
            /DescribeMetricSet:
              POST:
                summary: DescribeMetricSet
                description: >-
                  <p>Describes a dataset.</p> <p>Amazon Lookout for Metrics API
                  actions are eventually consistent. If you do a read operation
                  on a resource immediately after creating or modifying it, use
                  retries to allow time for the write operation to complete.</p>
                tags:
                  - Describe
                  - Metrics
                  - Sets
                  - Activate
                  - Anomaly
                  - Detectors
                  - Back
                  - Tests
                  - Create
                  - Alerts
                  - Metrics
                  - Sets
                  - Deactivate
                  - Delete
                  - Describe
                  - Detections
                  - Executions
            /DetectMetricSetConfig:
              POST:
                summary: DetectMetricSetConfig
                description: >-
                  <p>Detects an Amazon S3 dataset's file format, interval, and
                  offset.</p>
                tags:
                  - Detect
                  - Metrics
                  - Sets
                  - Configurations
                  - Activate
                  - Anomaly
                  - Detectors
                  - Back
                  - Tests
                  - Create
                  - Alerts
                  - Metrics
                  - Sets
                  - Deactivate
                  - Delete
                  - Describe
                  - Detections
                  - Executions
                  - Detect
                  - Configurations
            /GetAnomalyGroup:
              POST:
                summary: GetAnomalyGroup
                description: <p>Returns details about a group of anomalous metrics.</p>
                tags:
                  - Get
                  - Anomaly
                  - Group
                  - Activate
                  - Anomaly
                  - Detectors
                  - Back
                  - Tests
                  - Create
                  - Alerts
                  - Metrics
                  - Sets
                  - Deactivate
                  - Delete
                  - Describe
                  - Detections
                  - Executions
                  - Detect
                  - Configurations
                  - Get
                  - Group
            /GetDataQualityMetrics:
              POST:
                summary: GetDataQualityMetrics
                description: >-
                  <p>Returns details about the requested data quality
                  metrics.</p>
                tags:
                  - Get
                  - Data
                  - Quality
                  - Metrics
                  - Activate
                  - Anomaly
                  - Detectors
                  - Back
                  - Tests
                  - Create
                  - Alerts
                  - Metrics
                  - Sets
                  - Deactivate
                  - Delete
                  - Describe
                  - Detections
                  - Executions
                  - Detect
                  - Configurations
                  - Get
                  - Group
                  - Data
                  - Quality
                  - Metrics
            /GetFeedback:
              POST:
                summary: GetFeedback
                description: <p>Get feedback for an anomaly group.</p>
                tags:
                  - Get
                  - Feedback
                  - Activate
                  - Anomaly
                  - Detectors
                  - Back
                  - Tests
                  - Create
                  - Alerts
                  - Metrics
                  - Sets
                  - Deactivate
                  - Delete
                  - Describe
                  - Detections
                  - Executions
                  - Detect
                  - Configurations
                  - Get
                  - Group
                  - Data
                  - Quality
                  - Metrics
                  - Feedback
            /GetSampleData:
              POST:
                summary: GetSampleData
                description: >-
                  <p>Returns a selection of sample records from an Amazon S3
                  datasource.</p>
                tags:
                  - Get
                  - Samples
                  - Data
                  - Activate
                  - Anomaly
                  - Detectors
                  - Back
                  - Tests
                  - Create
                  - Alerts
                  - Metrics
                  - Sets
                  - Deactivate
                  - Delete
                  - Describe
                  - Detections
                  - Executions
                  - Detect
                  - Configurations
                  - Get
                  - Group
                  - Data
                  - Quality
                  - Metrics
                  - Feedback
                  - Samples
            /ListAlerts:
              POST:
                summary: ListAlerts
                description: >-
                  <p>Lists the alerts attached to a detector.</p> <p>Amazon
                  Lookout for Metrics API actions are eventually consistent. If
                  you do a read operation on a resource immediately after
                  creating or modifying it, use retries to allow time for the
                  write operation to complete.</p>
                tags:
                  - Lists
                  - Alerts
                  - Activate
                  - Anomaly
                  - Detectors
                  - Back
                  - Tests
                  - Create
                  - Alerts
                  - Metrics
                  - Sets
                  - Deactivate
                  - Delete
                  - Describe
                  - Detections
                  - Executions
                  - Detect
                  - Configurations
                  - Get
                  - Group
                  - Data
                  - Quality
                  - Metrics
                  - Feedback
                  - Samples
                  - Lists
                  - Alerts
            /ListAnomalyDetectors:
              POST:
                summary: ListAnomalyDetectors
                description: >-
                  <p>Lists the detectors in the current AWS Region.</p>
                  <p>Amazon Lookout for Metrics API actions are eventually
                  consistent. If you do a read operation on a resource
                  immediately after creating or modifying it, use retries to
                  allow time for the write operation to complete.</p>
                tags:
                  - Lists
                  - Anomaly
                  - Detectors
                  - Activate
                  - Anomaly
                  - Detectors
                  - Back
                  - Tests
                  - Create
                  - Alerts
                  - Metrics
                  - Sets
                  - Deactivate
                  - Delete
                  - Describe
                  - Detections
                  - Executions
                  - Detect
                  - Configurations
                  - Get
                  - Group
                  - Data
                  - Quality
                  - Metrics
                  - Feedback
                  - Samples
                  - Lists
                  - Alerts
                  - Detectors
            /ListAnomalyGroupRelatedMetrics:
              POST:
                summary: ListAnomalyGroupRelatedMetrics
                description: >-
                  <p>Returns a list of measures that are potential causes or
                  effects of an anomaly group.</p>
                tags:
                  - Lists
                  - Anomaly
                  - Group
                  - Related
                  - Metrics
                  - Activate
                  - Anomaly
                  - Detectors
                  - Back
                  - Tests
                  - Create
                  - Alerts
                  - Metrics
                  - Sets
                  - Deactivate
                  - Delete
                  - Describe
                  - Detections
                  - Executions
                  - Detect
                  - Configurations
                  - Get
                  - Group
                  - Data
                  - Quality
                  - Metrics
                  - Feedback
                  - Samples
                  - Lists
                  - Alerts
                  - Detectors
                  - Related
            /ListAnomalyGroupSummaries:
              POST:
                summary: ListAnomalyGroupSummaries
                description: <p>Returns a list of anomaly groups.</p>
                tags:
                  - Lists
                  - Anomaly
                  - Group
                  - Summaries
                  - Activate
                  - Anomaly
                  - Detectors
                  - Back
                  - Tests
                  - Create
                  - Alerts
                  - Metrics
                  - Sets
                  - Deactivate
                  - Delete
                  - Describe
                  - Detections
                  - Executions
                  - Detect
                  - Configurations
                  - Get
                  - Group
                  - Data
                  - Quality
                  - Metrics
                  - Feedback
                  - Samples
                  - Lists
                  - Alerts
                  - Detectors
                  - Related
                  - Summaries
            /ListAnomalyGroupTimeSeries:
              POST:
                summary: ListAnomalyGroupTimeSeries
                description: >-
                  <p>Gets a list of anomalous metrics for a measure in an
                  anomaly group.</p>
                tags:
                  - Lists
                  - Anomaly
                  - Group
                  - Time
                  - Series
                  - Activate
                  - Anomaly
                  - Detectors
                  - Back
                  - Tests
                  - Create
                  - Alerts
                  - Metrics
                  - Sets
                  - Deactivate
                  - Delete
                  - Describe
                  - Detections
                  - Executions
                  - Detect
                  - Configurations
                  - Get
                  - Group
                  - Data
                  - Quality
                  - Metrics
                  - Feedback
                  - Samples
                  - Lists
                  - Alerts
                  - Detectors
                  - Related
                  - Summaries
                  - Time
                  - Series
            /ListMetricSets:
              POST:
                summary: ListMetricSets
                description: >-
                  <p>Lists the datasets in the current AWS Region.</p> <p>Amazon
                  Lookout for Metrics API actions are eventually consistent. If
                  you do a read operation on a resource immediately after
                  creating or modifying it, use retries to allow time for the
                  write operation to complete.</p>
                tags:
                  - Lists
                  - Metrics
                  - Sets
                  - Activate
                  - Anomaly
                  - Detectors
                  - Back
                  - Tests
                  - Create
                  - Alerts
                  - Metrics
                  - Sets
                  - Deactivate
                  - Delete
                  - Describe
                  - Detections
                  - Executions
                  - Detect
                  - Configurations
                  - Get
                  - Group
                  - Data
                  - Quality
                  - Metrics
                  - Feedback
                  - Samples
                  - Lists
                  - Alerts
                  - Detectors
                  - Related
                  - Summaries
                  - Time
                  - Series
                  - Sets
            /tags/{resourceArn}:
              DELETE:
                summary: UntagResource
                description: >-
                  <p>Removes <a
                  href="https://docs.aws.amazon.com/lookoutmetrics/latest/dev/detectors-tags.html">tags</a>
                  from a detector, dataset, or alert.</p>
                tags:
                  - Untag
                  - Resources
                  - Activate
                  - Anomaly
                  - Detectors
                  - Back
                  - Tests
                  - Create
                  - Alerts
                  - Metrics
                  - Sets
                  - Deactivate
                  - Delete
                  - Describe
                  - Detections
                  - Executions
                  - Detect
                  - Configurations
                  - Get
                  - Group
                  - Data
                  - Quality
                  - Metrics
                  - Feedback
                  - Samples
                  - Lists
                  - Alerts
                  - Detectors
                  - Related
                  - Summaries
                  - Time
                  - Series
                  - Sets
                  - ARN
            /PutFeedback:
              POST:
                summary: PutFeedback
                description: <p>Add feedback for an anomalous metric.</p>
                tags:
                  - Put
                  - Feedback
                  - Activate
                  - Anomaly
                  - Detectors
                  - Back
                  - Tests
                  - Create
                  - Alerts
                  - Metrics
                  - Sets
                  - Deactivate
                  - Delete
                  - Describe
                  - Detections
                  - Executions
                  - Detect
                  - Configurations
                  - Get
                  - Group
                  - Data
                  - Quality
                  - Metrics
                  - Feedback
                  - Samples
                  - Lists
                  - Alerts
                  - Detectors
                  - Related
                  - Summaries
                  - Time
                  - Series
                  - Sets
                  - ARN
                  - Put
            /UpdateAlert:
              POST:
                summary: UpdateAlert
                description: <p>Make changes to an existing alert.</p>
                tags:
                  - Update
                  - Alerts
                  - Activate
                  - Anomaly
                  - Detectors
                  - Back
                  - Tests
                  - Create
                  - Alerts
                  - Metrics
                  - Sets
                  - Deactivate
                  - Delete
                  - Describe
                  - Detections
                  - Executions
                  - Detect
                  - Configurations
                  - Get
                  - Group
                  - Data
                  - Quality
                  - Metrics
                  - Feedback
                  - Samples
                  - Lists
                  - Alerts
                  - Detectors
                  - Related
                  - Summaries
                  - Time
                  - Series
                  - Sets
                  - ARN
                  - Put
                  - Update
            /UpdateAnomalyDetector:
              POST:
                summary: UpdateAnomalyDetector
                description: >-
                  <p>Updates a detector. After activation, you can only change a
                  detector's ingestion delay and description.</p>
                tags:
                  - Update
                  - Anomaly
                  - Detectors
                  - Activate
                  - Anomaly
                  - Detectors
                  - Back
                  - Tests
                  - Create
                  - Alerts
                  - Metrics
                  - Sets
                  - Deactivate
                  - Delete
                  - Describe
                  - Detections
                  - Executions
                  - Detect
                  - Configurations
                  - Get
                  - Group
                  - Data
                  - Quality
                  - Metrics
                  - Feedback
                  - Samples
                  - Lists
                  - Alerts
                  - Detectors
                  - Related
                  - Summaries
                  - Time
                  - Series
                  - Sets
                  - ARN
                  - Put
                  - Update
            /UpdateMetricSet:
              POST:
                summary: UpdateMetricSet
                description: <p>Updates a da
                tags:
                  - Update
                  - Metrics
                  - Sets
                  - Activate
                  - Anomaly
                  - Detectors
                  - Back
                  - Tests
                  - Create
                  - Alerts
                  - Metrics
                  - Sets
                  - Deactivate
                  - Delete
                  - Describe
                  - Detections
                  - Executions
                  - Detect
                  - Configurations
                  - Get
                  - Group
                  - Data
                  - Quality
                  - Metrics
                  - Feedback
                  - Samples
                  - Lists
                  - Alerts
                  - Detectors
                  - Related
                  - Summaries
                  - Time
                  - Series
                  - Sets
                  - ARN
                  - Put
                  - Upda
    overlays:
      - type: APIs.io Search
        url: overlays/lookoutmetrics-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/lookoutmetrics-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:lookoutmetrics
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---