---
name: Agent
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/agent.png
url: https://example.com/apis/agent.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Agent
apis:
  - name: bedrock-agent-runtime
    description: <p>Amazon Bedrock Agent</p>
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
            title: bedrock-agent-runtime
          paths:
            /agents/{agentId}/agentAliases/{agentAliasId}/sessions/{sessionId}/text:
              POST:
                summary: InvokeAgent
                description: >-
                  <p>Invokes the specified Bedrock model to run inference using
                  the input provided in the request body.</p>
                tags:
                  - Invoke
                  - Agent
                  - Identifiers
                  - Agent
                  - Aliases
                  - Alias
                  - Sessions
                  - Sessions
                  - Text
            /knowledgebases/{knowledgeBaseId}/retrieve:
              POST:
                summary: Retrieve
                description: <p>Retrieve from knowledge base.</p>
                tags:
                  - Retrieve
                  - Identifiers
                  - Agent
                  - Aliases
                  - Alias
                  - Sessions
                  - Sessions
                  - Text
                  - Base
                  - Retrieve
            /retrieveAndGenerate:
              POST:
                summary: RetrieveAndGenerate
                description: <p>RetrieveAndGenera
                tags:
                  - Retrieve
                  - And
                  - Generate
                  - Identifiers
                  - Agent
                  - Aliases
                  - Alias
                  - Sessions
                  - Sessions
                  - Text
                  - Base
                  - Retrieve
                  - And
                  - General
    overlays:
      - type: APIs.io Search
        url: overlays/bedrock-agent-runtime-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/bedrock-agent-runtime-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:bedrock-agent-runtime
  - name: bedrock-agent
    description: >-
      <p>An example service, deployed with the Octane Service creator, which
      will echo the string</p>
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
            title: bedrock-agent
          paths:
            /agents/{agentId}/agentversions/{agentVersion}/knowledgebases/:
              POST:
                summary: ListAgentKnowledgeBases
                description: >-
                  <p>List of Knowledge Bases associated to an existing Amazon
                  Bedrock Agent Version</p>
                tags:
                  - Lists
                  - Agent
                  - Knowledge
                  - Bases
                  - Identifiers
                  - Agent Versions
                  - Agent
                  - Versions
                  - Knowledgebases
            /agents/:
              POST:
                summary: ListAgents
                description: <p>Lists Agents</p>
                tags:
                  - Lists
                  - Agents
                  - Identifiers
                  - Agent Versions
                  - Agent
                  - Versions
                  - Knowledgebases
                  - Agents
            /agents/{agentId}/agentversions/{agentVersion}/actiongroups/:
              POST:
                summary: ListAgentActionGroups
                description: >-
                  <p>Lists an Action Group for existing Amazon Bedrock Agent
                  Version</p>
                tags:
                  - Lists
                  - Agent
                  - Actions
                  - Groups
                  - Identifiers
                  - Agent Versions
                  - Agent
                  - Versions
                  - Knowledgebases
                  - Agents
                  - Action Groups
            /agents/{agentId}/agentaliases/:
              POST:
                summary: ListAgentAliases
                description: <p>Lists all the Aliases for an Amazon Bedrock Agent</p>
                tags:
                  - Lists
                  - Agent
                  - Aliases
                  - Identifiers
                  - Agent Versions
                  - Agent
                  - Versions
                  - Knowledgebases
                  - Agents
                  - Action Groups
                  - Agent Aliases
            /knowledgebases/{knowledgeBaseId}/datasources/:
              POST:
                summary: ListDataSources
                description: <p>List data sources</p>
                tags:
                  - Lists
                  - Data
                  - Sources
                  - Identifiers
                  - Agent Versions
                  - Agent
                  - Versions
                  - Knowledgebases
                  - Agents
                  - Action Groups
                  - Agent Aliases
                  - Base
                  - Data Source
            /knowledgebases/:
              POST:
                summary: ListKnowledgeBases
                description: <p>List Knowledge Bases</p>
                tags:
                  - Lists
                  - Knowledge
                  - Bases
                  - Identifiers
                  - Agent Versions
                  - Agent
                  - Versions
                  - Knowledgebases
                  - Agents
                  - Action Groups
                  - Agent Aliases
                  - Base
                  - Data Source
            /agents/{agentId}/:
              PUT:
                summary: UpdateAgent
                description: <p>Updates an existing Amazon Bedrock Agent</p>
                tags:
                  - Update
                  - Agent
                  - Identifiers
                  - Agent Versions
                  - Agent
                  - Versions
                  - Knowledgebases
                  - Agents
                  - Action Groups
                  - Agent Aliases
                  - Base
                  - Data Source
            /agents/{agentId}/agentversions/{agentVersion}/actiongroups/{actionGroupId}/:
              PUT:
                summary: UpdateAgentActionGroup
                description: >-
                  <p>Updates an existing Action Group for Amazon Bedrock
                  Agent</p>
                tags:
                  - Update
                  - Agent
                  - Actions
                  - Group
                  - Identifiers
                  - Agent Versions
                  - Agent
                  - Versions
                  - Knowledgebases
                  - Agents
                  - Action Groups
                  - Agent Aliases
                  - Base
                  - Data Source
                  - Actions
                  - Group
            /agents/{agentId}/agentaliases/{agentAliasId}/:
              PUT:
                summary: UpdateAgentAlias
                description: <p>Updates an existing Alias for an Amazon Bedrock Agent</p>
                tags:
                  - Update
                  - Agent
                  - Alias
                  - Identifiers
                  - Agent Versions
                  - Agent
                  - Versions
                  - Knowledgebases
                  - Agents
                  - Action Groups
                  - Agent Aliases
                  - Base
                  - Data Source
                  - Actions
                  - Group
                  - Alias
            /agents/{agentId}/agentversions/{agentVersion}/:
              GET:
                summary: GetAgentVersion
                description: <p>Gets an Agent version for existing Amazon Bedrock Agent</p>
                tags:
                  - Get
                  - Agent
                  - Versions
                  - Identifiers
                  - Agent Versions
                  - Agent
                  - Versions
                  - Knowledgebases
                  - Agents
                  - Action Groups
                  - Agent Aliases
                  - Base
                  - Data Source
                  - Actions
                  - Group
                  - Alias
            /knowledgebases/{knowledgeBaseId}/datasources/{dataSourceId}:
              PUT:
                summary: UpdateDataSource
                description: <p>Update an existing data source</p>
                tags:
                  - Update
                  - Data
                  - Source
                  - Identifiers
                  - Agent Versions
                  - Agent
                  - Versions
                  - Knowledgebases
                  - Agents
                  - Action Groups
                  - Agent Aliases
                  - Base
                  - Data Source
                  - Actions
                  - Group
                  - Alias
                  - Data
                  - Source
            /knowledgebases/{knowledgeBaseId}:
              PUT:
                summary: UpdateKnowledgeBase
                description: <p>Update an existing knowledge base</p>
                tags:
                  - Update
                  - Knowledge
                  - Base
                  - Identifiers
                  - Agent Versions
                  - Agent
                  - Versions
                  - Knowledgebases
                  - Agents
                  - Action Groups
                  - Agent Aliases
                  - Base
                  - Data Source
                  - Actions
                  - Group
                  - Alias
                  - Data
                  - Source
            /agents/{agentId}/agentversions/{agentVersion}/knowledgebases/{knowledgeBaseId}/:
              PUT:
                summary: UpdateAgentKnowledgeBase
                description: >-
                  <p>Updates an existing Knowledge Base associated to an Amazon
                  Bedrock Agent</p>
                tags:
                  - Update
                  - Agent
                  - Knowledge
                  - Base
                  - Identifiers
                  - Agent Versions
                  - Agent
                  - Versions
                  - Knowledgebases
                  - Agents
                  - Action Groups
                  - Agent Aliases
                  - Base
                  - Data Source
                  - Actions
                  - Group
                  - Alias
                  - Data
                  - Source
                  - Knowledge
            /knowledgebases/{knowledgeBaseId}/datasources/{dataSourceId}/ingestionjobs/{ingestionJobId}:
              GET:
                summary: GetIngestionJob
                description: <p>Get an ingestion job</p>
                tags:
                  - Get
                  - Ingestion
                  - Jobs
                  - Identifiers
                  - Agent Versions
                  - Agent
                  - Versions
                  - Knowledgebases
                  - Agents
                  - Action Groups
                  - Agent Aliases
                  - Base
                  - Data Source
                  - Actions
                  - Group
                  - Alias
                  - Data
                  - Source
                  - Knowledge
                  - Ingestion Jobs
                  - Ingestion
                  - Jobs
            /agents/{agentId}/agentversions/:
              POST:
                summary: ListAgentVersions
                description: <p>Lists Agent Versions</p>
                tags:
                  - Lists
                  - Agent
                  - Versions
                  - Identifiers
                  - Agent Versions
                  - Agent
                  - Versions
                  - Knowledgebases
                  - Agents
                  - Action Groups
                  - Agent Aliases
                  - Base
                  - Data Source
                  - Actions
                  - Group
                  - Alias
                  - Data
                  - Source
                  - Knowledge
                  - Ingestion Jobs
                  - Ingestion
                  - Jobs
            /knowledgebases/{knowledgeBaseId}/datasources/{dataSourceId}/ingestionjobs/:
              PUT:
                summary: StartIngestionJob
                description: <p>Start a new ingestion job</p>
                tags:
                  - Start
                  - Ingestion
                  - Jobs
                  - Identifiers
                  - Agent Versions
                  - Agent
                  - Versions
                  - Knowledgebases
                  - Agents
                  - Action Groups
                  - Agent Aliases
                  - Base
                  - Data Source
                  - Actions
                  - Group
                  - Alias
                  - Data
                  - Source
                  - Knowledge
                  - Ingestion Jobs
                  - Ingestion
                  - Jobs
            /tags/{resourceArn}:
              DELETE:
                summary: UntagResource
                description: <p>Untag a re
                tags:
                  - Untag
                  - Resources
                  - Identifiers
                  - Agent Versions
                  - Agent
                  - Versions
                  - Knowledgebases
                  - Agents
                  - Action Groups
                  - Agent Aliases
                  - Base
                  - Data Source
                  - Actions
                  - Group
                  - Alias
                  - Data
                  - Source
                  - Knowledge
                  - Ingestion Jobs
                  - Ingestion
                  - Jobs
                  - A
    overlays:
      - type: APIs.io Search
        url: overlays/bedrock-agent-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/bedrock-agent-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:bedrock-agent
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
  - name: groundstation
    description: >-
      <p>Welcome to the AWS Ground Station API Reference. AWS Ground Station is
      a fully managed service that enables you to control satellite
      communications, downlink and process satellite data, and scale your
      satellite operations efficiently and cost-effectively without having to
      build or manage your own ground station infrastructure.</p>
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
            title: groundstation
          paths:
            /contact/{contactId}:
              GET:
                summary: DescribeContact
                description: <p>Describes an existing contact.</p>
                tags:
                  - Describe
                  - Contacts
                  - Identifiers
            /config:
              GET:
                summary: ListConfigs
                description: <p>Returns a list of <code>Config</code> objects.</p>
                tags:
                  - Lists
                  - Configurations
                  - Identifiers
                  - Configurations
            /dataflowEndpointGroup:
              GET:
                summary: ListDataflowEndpointGroups
                description: <p>Returns a list of <code>DataflowEndpoint</code> groups.</p>
                tags:
                  - Lists
                  - Dataflow
                  - Endpoints
                  - Groups
                  - Identifiers
                  - Configurations
                  - Endpoints
                  - Group
            /ephemeris:
              POST:
                summary: CreateEphemeris
                description: >-
                  <p>Creates an Ephemeris with the specified
                  <code>EphemerisData</code>.</p>
                tags:
                  - Create
                  - Ephemeris
                  - Identifiers
                  - Configurations
                  - Endpoints
                  - Group
                  - Ephemeris
            /missionprofile:
              GET:
                summary: ListMissionProfiles
                description: <p>Returns a list of mission profiles.</p>
                tags:
                  - Lists
                  - Mission
                  - Profiles
                  - Identifiers
                  - Configurations
                  - Endpoints
                  - Group
                  - Ephemeris
                  - Mission Profile
            /config/{configType}/{configId}:
              PUT:
                summary: UpdateConfig
                description: >-
                  <p>Updates the <code>Config</code> used when scheduling
                  contacts.</p> <p>Updating a <code>Config</code> will not
                  update the execution parameters for existing future contacts
                  scheduled with this <code>Config</code>.</p>
                tags:
                  - Update
                  - Configurations
                  - Identifiers
                  - Configurations
                  - Endpoints
                  - Group
                  - Ephemeris
                  - Mission Profile
                  - Types
            /dataflowEndpointGroup/{dataflowEndpointGroupId}:
              GET:
                summary: GetDataflowEndpointGroup
                description: <p>Returns the dataflow endpoint group.</p>
                tags:
                  - Get
                  - Dataflow
                  - Endpoints
                  - Group
                  - Identifiers
                  - Configurations
                  - Endpoints
                  - Group
                  - Ephemeris
                  - Mission Profile
                  - Types
                  - Dataflow
            /ephemeris/{ephemerisId}:
              PUT:
                summary: UpdateEphemeris
                description: <p>Updates an existing ephemeris</p>
                tags:
                  - Update
                  - Ephemeris
                  - Identifiers
                  - Configurations
                  - Endpoints
                  - Group
                  - Ephemeris
                  - Mission Profile
                  - Types
                  - Dataflow
            /missionprofile/{missionProfileId}:
              PUT:
                summary: UpdateMissionProfile
                description: >-
                  <p>Updates a mission profile.</p> <p>Updating a mission
                  profile will not update the execution parameters for existing
                  future contacts.</p>
                tags:
                  - Update
                  - Mission
                  - Profiles
                  - Identifiers
                  - Configurations
                  - Endpoints
                  - Group
                  - Ephemeris
                  - Mission Profile
                  - Types
                  - Dataflow
                  - Profiles
            /agent/{agentId}/configuration:
              GET:
                summary: GetAgentConfiguration
                description: >-
                  <note> <p> For use by AWS Ground Station Agent and shouldn't
                  be called directly.</p> </note> <p>Gets the latest
                  configuration information for a registered agent.</p>
                tags:
                  - Get
                  - Agent
                  - Configurations
                  - Identifiers
                  - Configurations
                  - Endpoints
                  - Group
                  - Ephemeris
                  - Mission Profile
                  - Types
                  - Dataflow
                  - Profiles
                  - Configurations
            /minute-usage:
              POST:
                summary: GetMinuteUsage
                description: <p>Returns the number of reserved minutes used by account.</p>
                tags:
                  - Get
                  - Minute
                  - Usage
                  - Identifiers
                  - Configurations
                  - Endpoints
                  - Group
                  - Ephemeris
                  - Mission Profile
                  - Types
                  - Dataflow
                  - Profiles
                  - Configurations
                  - Minute
                  - Usage
            /satellite/{satelliteId}:
              GET:
                summary: GetSatellite
                description: <p>Returns a satellite.</p>
                tags:
                  - Get
                  - Satellites
                  - Identifiers
                  - Configurations
                  - Endpoints
                  - Group
                  - Ephemeris
                  - Mission Profile
                  - Types
                  - Dataflow
                  - Profiles
                  - Configurations
                  - Minute
                  - Usage
            /contacts:
              POST:
                summary: ListContacts
                description: >-
                  <p>Returns a list of contacts.</p> <p>If
                  <code>statusList</code> contains AVAILABLE, the request must
                  include <code>groundStation</code>,
                  <code>missionprofileArn</code>, and <code>satelliteArn</code>.
                  </p>
                tags:
                  - Lists
                  - Contacts
                  - Identifiers
                  - Configurations
                  - Endpoints
                  - Group
                  - Ephemeris
                  - Mission Profile
                  - Types
                  - Dataflow
                  - Profiles
                  - Configurations
                  - Minute
                  - Usage
                  - Contacts
            /ephemerides:
              POST:
                summary: ListEphemerides
                description: <p>List existing ephemerides.</p>
                tags:
                  - Lists
                  - Ephemerides
                  - Identifiers
                  - Configurations
                  - Endpoints
                  - Group
                  - Ephemeris
                  - Mission Profile
                  - Types
                  - Dataflow
                  - Profiles
                  - Configurations
                  - Minute
                  - Usage
                  - Contacts
                  - Ephemerides
            /groundstation:
              GET:
                summary: ListGroundStations
                description: <p>Returns a list of ground stations. </p>
                tags:
                  - Lists
                  - Ground
                  - Stations
                  - Identifiers
                  - Configurations
                  - Endpoints
                  - Group
                  - Ephemeris
                  - Mission Profile
                  - Types
                  - Dataflow
                  - Profiles
                  - Configurations
                  - Minute
                  - Usage
                  - Contacts
                  - Ephemerides
                  - Groundstation
            /satellite:
              GET:
                summary: ListSatellites
                description: <p>Returns a list of satellites.</p>
                tags:
                  - Lists
                  - Satellites
                  - Identifiers
                  - Configurations
                  - Endpoints
                  - Group
                  - Ephemeris
                  - Mission Profile
                  - Types
                  - Dataflow
                  - Profiles
                  - Configurations
                  - Minute
                  - Usage
                  - Contacts
                  - Ephemerides
                  - Groundstation
                  - Satellites
            /tags/{resourceArn}:
              DELETE:
                summary: UntagResource
                description: <p>Deassigns a resource tag.</p>
                tags:
                  - Untag
                  - Resources
                  - Identifiers
                  - Configurations
                  - Endpoints
                  - Group
                  - Ephemeris
                  - Mission Profile
                  - Types
                  - Dataflow
                  - Profiles
                  - Configurations
                  - Minute
                  - Usage
                  - Contacts
                  - Ephemerides
                  - Groundstation
                  - Satellites
                  - ARN
            /agent:
              POST:
                summary: RegisterAgent
                description: >-
                  <note> <p> For use by AWS Ground Station Agent and shouldn't
                  be called directly.</p> </note> <p> Registers a new agent with
                  AWS Ground Station. </p>
                tags:
                  - Register
                  - Agent
                  - Identifiers
                  - Configurations
                  - Endpoints
                  - Group
                  - Ephemeris
                  - Mission Profile
                  - Types
                  - Dataflow
                  - Profiles
                  - Configurations
                  - Minute
                  - Usage
                  - Contacts
                  - Ephemerides
                  - Groundstation
                  - Satellites
                  - ARN
                  - Agent
            /contact:
              POST:
                summary: ReserveContact
                description: <p>Reserves a contact using specified parameters.</p>
                tags:
                  - Reserve
                  - Contacts
                  - Identifiers
                  - Configurations
                  - Endpoints
                  - Group
                  - Ephemeris
                  - Mission Profile
                  - Types
                  - Dataflow
                  - Profiles
                  - Configurations
                  - Minute
                  - Usage
                  - Contacts
                  - Ephemerides
                  - Groundstation
                  - Satellites
                  - ARN
                  - Agent
                  - Contacts
            /agent/{agentId}:
              PUT:
                summary: UpdateAgentStatus
                description: >-
                  <note> <p> For use by AWS Ground Station Agent and shouldn't
                  be called directly.</p> </note> <p>Update the status of the 
                tags:
                  - Update
                  - Agent
                  - Status
                  - Identifiers
                  - Configurations
                  - Endpoints
                  - Group
                  - Ephemeris
                  - Mission Profile
                  - Types
                  - Dataflow
                  - Profiles
                  - Configurations
                  - Minute
                  - Usage
                  - Contacts
                  - Ephemerides
                  - Groundstation
                  - Satellites
                  - ARN
                  - Agent
                  - Conta
    overlays:
      - type: APIs.io Search
        url: overlays/groundstation-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/groundstation-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:groundstation
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
  - name: Symphony Agent API
    description: >-
      The Symphony Agent is responsible for encryption and decryption of
      messages and content sent to and from a bot.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://docs.developers.symphony.com/bots/overview-of-rest-api/agent-api
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: >-
          https://docs.developers.symphony.com/bots/overview-of-rest-api/agent-api
      - type: OpenAPI
        data:
          openapi: 3.0.1
          info:
            title: Agent API
          paths:
            /v3/health:
              get:
                tags:
                  - Checks
                  - Health
                  - Status
                  - V3
                  - Health
                summary: Checks health status
                description: >
                  _Available on Agent 2.57.0 and above._


                  Returns the connectivity status of your Agent server. If your
                  Agent server is started and running, the status value will be
                  `UP`
            /v3/health/extended:
              get:
                tags:
                  - Checks
                  - Health
                  - Status
                  - Of
                  - Services
                  - And
                  - Users
                  - V3
                  - Health
                  - Extended
                summary: Checks health status of services and users
                description: >
                  _Available on Agent 2.57.0 and above._


                  Returns the connectivity status of the Agent services
                  (**pod**, **key manager** and **datafeed**) as well as users

                  connectivity (**agentservice** and **ceservice**).


                  The global status will be set to `DOWN` if at least one of the
                  sub-status is also `DOWN`.
            /v4/message/import:
              post:
                tags:
                  - Import
                  - Messages
                  - From
                  - Other
                  - Systems
                  - Into
                  - Symphony.
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                summary: Import messages from other systems into Symphony.
                description: >
                  Sends a message to be imported into the system.

                  Allows you to override the timestamp and author of the message
                  with your desired values.

                  The requesting user must have the Content Management role.

                  The user that the message is intended to have come from must
                  also be present in the conversation.

                  The intended message timestamp must be a valid time from the
                  past. It cannot be a future timestamp.

                  Optionally the original message ID can be specified to
                  identify the imported message for the purpose of repeat
                  imports.
            /v4/message/blast:
              post:
                tags:
                  - Post
                  - Message
                  - To
                  - Multiple
                  - Existing
                  - Streams.
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                summary: Post a message to multiple existing streams.
                description: >
                  Post a new message to the given list of streams. The stream
                  can be a chatroom,

                  an IM or a multiparty IM.


                  You may include an attachment on the message.


                  The message can be provided as MessageMLV2 or PresentationML.
                  Both formats support Freemarker templates.


                  The optional parameter "data" can be used to provide a JSON
                  payload containing entity data.

                  If the message contains explicit references to entity data (in
                  "data-entity-id" element attributes),

                  this parameter is required.


                  If the message is in MessageML and fails schema validation a
                  client error results


                  This endpoint is idempotent, it means that a 200 response will
                  be returned even if the message has not been

                  delivered to some streams. Check the `errors` map from the
                  response in order to see on which stream(s) the

                  message has not been delivered.


                  The maximum number of streams where the message can be sent is
                  limitted to 100.


                  Regarding authentication, you must either use the sessionToken
                  which was created for delegated app access

                  or both the sessionToken and keyManagerToken together.
            /v1/message/{id}:
              get:
                tags:
                  - Get
                  - Message
                  - By
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                summary: Get a message by ID
            /v1/message/search:
              get:
                tags:
                  - Search
                  - Messages
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                summary: Search messages
                description: >
                  Search messages according to the specified criteria. The
                  "query" parameter takes a search query defined as

                  "field:value" pairs combined by the operator "AND" (e.g.
                  "text:foo AND autor:bar"). Supported fields are
                   (case-insensitive): "text", "author", "hashtag", "cashtag", "mention", "signal", "fromDate", "toDate",
                   "streamId", "streamType".
                   "text" search requires a "streamId" to be specified.
                   "streamType" accepts one of the following values: "chat" (IMs and MIMs), "im", "mim", "chatroom", "post".
                   "signal" queries can only be combined with "fromDate", "toDate", "skip" and "limit" parameters.
              post:
                tags:
                  - Search
                  - Messages
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                summary: Search messages
                description: Search messages according to the specified criteria.
            /v1/stream/{sid}/attachment:
              get:
                tags:
                  - Download
                  - An
                  - Attachment.
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                summary: Download an attachment.
                description: >-
                  Downloads the attachment body by the attachment ID, stream ID,
                  and message ID.
            /v4/stream/{sid}/message:
              get:
                tags:
                  - Get
                  - Messages
                  - From
                  - An
                  - Existing
                  - Stream.
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                summary: Get messages from an existing stream.
                description: >
                  A caller can fetch all unseen messages by passing the
                  timestamp of

                  the last message seen as the since parameter and the number of
                  messages

                  with the same timestamp value already seen as the skip
                  parameter. This

                  means that every message will be seen exactly once even in the
                  case that

                  an additional message is processed with the same timestamp as
                  the last

                  message returned by the previous call, and the case where
                  there are

                  more than maxMessages with the same timestamp value.


                  This method is intended for historic queries and is generally
                  reliable

                  but if guaranteed delivery of every message in real time is
                  required

                  then the equivilent firehose method should be called.
            /v4/stream/{sid}/message/create:
              post:
                tags:
                  - Post
                  - Message
                  - To
                  - One
                  - Existing
                  - Stream.
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                summary: Post a message to one existing stream.
                description: >
                  Post a new message to the given stream. The stream can be a
                  chatroom,,an IM or a multiparty IM.


                  You may include an attachment on the message.


                  The message can be provided as MessageMLV2 or PresentationML.
                  Both formats support Freemarker templates.


                  The optional parameter "data" can be used to provide a JSON
                  payload containing entity data.

                  If the message contains explicit references to entity data (in
                  "data-entity-id" element attributes),

                  this parameter is required.


                  If the message is in MessageML and fails schema validation a
                  client error will be returned.


                  If the message is sent then 200 is returned.


                  Regarding authentication, you must either use the sessionToken
                  which was created for delegated app access

                  or both the sessionToken and keyManagerToken together.
            /v4/stream/{sid}/message/{mid}/update:
              post:
                tags:
                  - Update
                  - An
                  - Existing
                  - Message.
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                summary: Update an existing message.
                description: >
                  Update an existing message. The existing message must be a
                  valid social message, that has not been deleted.


                  The message can be provided as MessageMLV2 or PresentationML.
                  Both formats support Freemarker templates.


                  The optional parameter "data" can be used to provide a JSON
                  payload containing entity data.

                  If the message contains explicit references to entity data (in
                  "data-entity-id" element attributes),

                  this parameter is required.


                  Regarding authentication, you must either use the sessionToken
                  which was created for delegated app access

                  or both the sessionToken and keyManagerToken together.


                  Starting with SBE v24.1, attachments are supported.
            /v3/stream/{sid}/share:
              post:
                tags:
                  - Share
                  - Piece
                  - Of
                  - Content
                  - Into
                  - Symphony
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                  - Share
                summary: PROVISIONAL -  Share a piece of content into Symphony
                description: >
                  Given a 3rd party content (eg. news article), it can share to
                  the given stream.

                  The stream can be a chatroom, an IM or a multiparty IM.
            /v1/util/echo:
              post:
                tags:
                  - Test
                  - Endpoint,
                  - Returns
                  - Input.
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                  - Share
                  - Util
                  - Echo
                summary: Test endpoint, returns input.
            /v1/signals/list:
              get:
                tags:
                  - List
                  - Signals
                  - For
                  - The
                  - Requesting
                  - User.
                  - This
                  - Includes
                  - That
                  - User
                  - Has
                  - Created
                  - And
                  - Public
                  - |-
                    Signals
                    to
                  - Which
                  - They
                  - |
                    Subscribed.
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                  - Share
                  - Util
                  - Echo
                  - Signals
                  - List
                summary: >
                  List signals for the requesting user. This includes signals
                  that the user has created and public signals

                  to which they subscribed.
            /v1/signals/{id}/get:
              get:
                tags:
                  - Get
                  - Details
                  - Of
                  - The
                  - Requested
                  - Signal.
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                  - Share
                  - Util
                  - Echo
                  - Signals
                  - List
                  - Get
                summary: Get details of the requested signal.
            /v1/signals/create:
              post:
                tags:
                  - Create
                  - Signal.
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                  - Share
                  - Util
                  - Echo
                  - Signals
                  - List
                  - Get
                summary: Create a signal.
            /v1/signals/{id}/update:
              post:
                tags:
                  - Update
                  - Signal.
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                  - Share
                  - Util
                  - Echo
                  - Signals
                  - List
                  - Get
                summary: Update a signal.
            /v1/signals/{id}/delete:
              post:
                tags:
                  - Delete
                  - Signal.
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                  - Share
                  - Util
                  - Echo
                  - Signals
                  - List
                  - Get
                  - Delete
                summary: Delete a signal.
            /v1/signals/{id}/subscribe:
              post:
                tags:
                  - Subscribe
                  - To
                  - Signal.
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                  - Share
                  - Util
                  - Echo
                  - Signals
                  - List
                  - Get
                  - Delete
                  - Subscribe
                summary: Subscribe to a Signal.
            /v1/signals/{id}/unsubscribe:
              post:
                tags:
                  - Unsubscribe
                  - To
                  - Signal.
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                  - Share
                  - Util
                  - Echo
                  - Signals
                  - List
                  - Get
                  - Delete
                  - Subscribe
                  - Unsubscribe
                summary: Unsubscribe to a Signal.
            /v1/signals/{id}/subscribers:
              get:
                tags:
                  - Get
                  - The
                  - Subscribers
                  - Of
                  - Signal
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                  - Share
                  - Util
                  - Echo
                  - Signals
                  - List
                  - Get
                  - Delete
                  - Subscribe
                  - Unsubscribe
                  - Subscribers
                summary: Get the subscribers of a signal
            /v1/info:
              get:
                tags:
                  - Get
                  - Information
                  - About
                  - The
                  - Agent
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                  - Share
                  - Util
                  - Echo
                  - Signals
                  - List
                  - Get
                  - Delete
                  - Subscribe
                  - Unsubscribe
                  - Subscribers
                  - Info
                summary: Get information about the Agent
            /v1/dlp/policies:
              get:
                tags:
                  - Get
                  - All
                  - Policies
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                  - Share
                  - Util
                  - Echo
                  - Signals
                  - List
                  - Get
                  - Delete
                  - Subscribe
                  - Unsubscribe
                  - Subscribers
                  - Info
                  - Dlp
                  - Policies
                summary: Get all policies
                description: Get all policies
              post:
                tags:
                  - Creates
                  - Policy
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                  - Share
                  - Util
                  - Echo
                  - Signals
                  - List
                  - Get
                  - Delete
                  - Subscribe
                  - Unsubscribe
                  - Subscribers
                  - Info
                  - Dlp
                  - Policies
                summary: Creates a policy
                description: >
                  Creates a new policy with dictionary references.


                  At the time of policy creation, the caller should only provide
                  - contentTypes, name, scopes and type. The rest of the
                  information is populated automatically.


                  Note - You need to enable the policy after creation to start
                  enforcing the policy.
            /v1/dlp/policies/{policyId}:
              get:
                tags:
                  - Get
                  - Policy
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                  - Share
                  - Util
                  - Echo
                  - Signals
                  - List
                  - Get
                  - Delete
                  - Subscribe
                  - Unsubscribe
                  - Subscribers
                  - Info
                  - Dlp
                  - Policies
                summary: Get a policy
                description: Get a policy
              put:
                tags:
                  - Updates
                  - Policy.
                  - Cannot
                  - Be
                  - Used
                  - For
                  - Creation.
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                  - Share
                  - Util
                  - Echo
                  - Signals
                  - List
                  - Get
                  - Delete
                  - Subscribe
                  - Unsubscribe
                  - Subscribers
                  - Info
                  - Dlp
                  - Policies
                summary: Updates a policy. Cannot be used for creation.
                description: >
                  Update the policy (name, type, contentTypes, scopes) and also
                  the dictionaries for a policy.

                  Warning: If you send empty list of dictionaries during the
                  update operation, then all the

                  dictionaries for this policy are deleted and policy is
                  automatically disabled.

                  Note: The policy should already exist.
              delete:
                tags:
                  - Delete
                  - Policy
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                  - Share
                  - Util
                  - Echo
                  - Signals
                  - List
                  - Get
                  - Delete
                  - Subscribe
                  - Unsubscribe
                  - Subscribers
                  - Info
                  - Dlp
                  - Policies
                summary: Delete a policy
                description: |
                  Delete a policy.
                  Note: Only disabled policy can be deleted
            /v1/dlp/policies/{policyId}/enable:
              post:
                tags:
                  - Enables
                  - Policy.
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                  - Share
                  - Util
                  - Echo
                  - Signals
                  - List
                  - Get
                  - Delete
                  - Subscribe
                  - Unsubscribe
                  - Subscribers
                  - Info
                  - Dlp
                  - Policies
                  - Enable
                summary: Enables a policy.
                description: Enables a policy.
            /v1/dlp/policies/{policyId}/disable:
              post:
                tags:
                  - Disables
                  - Policy.
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                  - Share
                  - Util
                  - Echo
                  - Signals
                  - List
                  - Get
                  - Delete
                  - Subscribe
                  - Unsubscribe
                  - Subscribers
                  - Info
                  - Dlp
                  - Policies
                  - Enable
                  - Disable
                summary: Disables a policy.
                description: Disables a policy.
            /v1/dlp/dictionaries:
              get:
                tags:
                  - Get
                  - All
                  - Dictionary
                  - Metadatas
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                  - Share
                  - Util
                  - Echo
                  - Signals
                  - List
                  - Get
                  - Delete
                  - Subscribe
                  - Unsubscribe
                  - Subscribers
                  - Info
                  - Dlp
                  - Policies
                  - Enable
                  - Disable
                  - Dictionaries
                summary: Get all dictionary metadatas
                description: >
                  Get all dictionary metadatas with the latest version. Each
                  dictionary object will only contain meta data of the content.
              post:
                tags:
                  - Create
                  - Dictionary
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                  - Share
                  - Util
                  - Echo
                  - Signals
                  - List
                  - Get
                  - Delete
                  - Subscribe
                  - Unsubscribe
                  - Subscribers
                  - Info
                  - Dlp
                  - Policies
                  - Enable
                  - Disable
                  - Dictionaries
                summary: Create a dictionary
                description: >
                  Creates a dictionary with basic metadata and no content. Only
                  "name" and "type" field is used to create a new dictionary
                  entry.
            /v1/dlp/dictionaries/{dictId}:
              get:
                tags:
                  - Get
                  - Dictionary
                  - Metadata
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                  - Share
                  - Util
                  - Echo
                  - Signals
                  - List
                  - Get
                  - Delete
                  - Subscribe
                  - Unsubscribe
                  - Subscribers
                  - Info
                  - Dlp
                  - Policies
                  - Enable
                  - Disable
                  - Dictionaries
                summary: Get dictionary metadata
                description: Get basic information for a dictionary.
              put:
                tags:
                  - Updates
                  - Dictionary
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                  - Share
                  - Util
                  - Echo
                  - Signals
                  - List
                  - Get
                  - Delete
                  - Subscribe
                  - Unsubscribe
                  - Subscribers
                  - Info
                  - Dlp
                  - Policies
                  - Enable
                  - Disable
                  - Dictionaries
                summary: Updates a dictionary
                description: |
                  Updates the dictionary's basic metadata without content.
                  This API cannot be used for creating a new dictionary.
                  In case of update only "name" can be changed.
                  Note: All related policies will also have versions updated.
              delete:
                tags:
                  - Delete
                  - Dictionary
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                  - Share
                  - Util
                  - Echo
                  - Signals
                  - List
                  - Get
                  - Delete
                  - Subscribe
                  - Unsubscribe
                  - Subscribers
                  - Info
                  - Dlp
                  - Policies
                  - Enable
                  - Disable
                  - Dictionaries
                summary: Delete a dictionary
                description: |
                  Deletes a dictionary.
                  Note: All related policies will be affected.
            /v1/dlp/dictionaries/{dictId}/data/download:
              get:
                tags:
                  - Downloads
                  - Base
                  - '64'
                  - Encoded
                  - Dictionary
                  - Content.
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                  - Share
                  - Util
                  - Echo
                  - Signals
                  - List
                  - Get
                  - Delete
                  - Subscribe
                  - Unsubscribe
                  - Subscribers
                  - Info
                  - Dlp
                  - Policies
                  - Enable
                  - Disable
                  - Dictionaries
                  - Data
                  - Download
                summary: Downloads Base 64 encoded dictionary content.
                description: Downloads Base 64 encoded dictionary content.
            /v1/dlp/dictionaries/{dictId}/data/upload:
              post:
                tags:
                  - Override
                  - Dictionary
                  - Content
                  - With
                  - Provided
                  - Content.
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                  - Share
                  - Util
                  - Echo
                  - Signals
                  - List
                  - Get
                  - Delete
                  - Subscribe
                  - Unsubscribe
                  - Subscribers
                  - Info
                  - Dlp
                  - Policies
                  - Enable
                  - Disable
                  - Dictionaries
                  - Data
                  - Download
                  - Upload
                summary: Override dictionary content with provided content.
                description: Override dictionary content with provided content.
            /v1/dlp/violations/message:
              get:
                tags:
                  - Get
                  - Violations
                  - As
                  - Result
                  - Of
                  - Policy
                  - Enforcement
                  - 'On'
                  - Messages.
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                  - Share
                  - Util
                  - Echo
                  - Signals
                  - List
                  - Get
                  - Delete
                  - Subscribe
                  - Unsubscribe
                  - Subscribers
                  - Info
                  - Dlp
                  - Policies
                  - Enable
                  - Disable
                  - Dictionaries
                  - Data
                  - Download
                  - Upload
                  - Violations
                summary: Get violations as a result of policy enforcement on messages.
            /v1/dlp/violations/stream:
              get:
                tags:
                  - Get
                  - Violations
                  - As
                  - Result
                  - Of
                  - Policy
                  - Enforcement
                  - 'On'
                  - Streams.
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                  - Share
                  - Util
                  - Echo
                  - Signals
                  - List
                  - Get
                  - Delete
                  - Subscribe
                  - Unsubscribe
                  - Subscribers
                  - Info
                  - Dlp
                  - Policies
                  - Enable
                  - Disable
                  - Dictionaries
                  - Data
                  - Download
                  - Upload
                  - Violations
                summary: Get violations as a result of policy enforcement on streams.
            /v1/dlp/violations/signal:
              get:
                tags:
                  - Get
                  - Violations
                  - As
                  - Result
                  - Of
                  - Policy
                  - Enforcement
                  - 'On'
                  - Signals.
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                  - Share
                  - Util
                  - Echo
                  - Signals
                  - List
                  - Get
                  - Delete
                  - Subscribe
                  - Unsubscribe
                  - Subscribers
                  - Info
                  - Dlp
                  - Policies
                  - Enable
                  - Disable
                  - Dictionaries
                  - Data
                  - Download
                  - Upload
                  - Violations
                  - Signal
                summary: Get violations as a result of policy enforcement on signals.
            /v3/dlp/policies:
              get:
                tags:
                  - Get
                  - All
                  - Policies
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                  - Share
                  - Util
                  - Echo
                  - Signals
                  - List
                  - Get
                  - Delete
                  - Subscribe
                  - Unsubscribe
                  - Subscribers
                  - Info
                  - Dlp
                  - Policies
                  - Enable
                  - Disable
                  - Dictionaries
                  - Data
                  - Download
                  - Upload
                  - Violations
                  - Signal
                summary: Get all policies
                description: Get all policies
              post:
                tags:
                  - Creates
                  - Policy
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                  - Share
                  - Util
                  - Echo
                  - Signals
                  - List
                  - Get
                  - Delete
                  - Subscribe
                  - Unsubscribe
                  - Subscribers
                  - Info
                  - Dlp
                  - Policies
                  - Enable
                  - Disable
                  - Dictionaries
                  - Data
                  - Download
                  - Upload
                  - Violations
                  - Signal
                summary: Creates a policy
                description: >
                  Creates a new policy with dictionary references.

                  At the time of policy creation, the caller should only provide
                  - contentTypes, name, scopes and type.

                  The rest of the information is populated automatically.

                  Note - You need to enable the policy after creation to start
                  enforcing the policy.
            /v3/dlp/policies/{policyId}:
              get:
                tags:
                  - Get
                  - Policy
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                  - Share
                  - Util
                  - Echo
                  - Signals
                  - List
                  - Get
                  - Delete
                  - Subscribe
                  - Unsubscribe
                  - Subscribers
                  - Info
                  - Dlp
                  - Policies
                  - Enable
                  - Disable
                  - Dictionaries
                  - Data
                  - Download
                  - Upload
                  - Violations
                  - Signal
                summary: Get a policy
                description: Get a policy
            /v3/dlp/policies/{policyId}/update:
              post:
                tags:
                  - Updates
                  - Policy.
                  - Cannot
                  - Be
                  - Used
                  - For
                  - Creation.
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                  - Share
                  - Util
                  - Echo
                  - Signals
                  - List
                  - Get
                  - Delete
                  - Subscribe
                  - Unsubscribe
                  - Subscribers
                  - Info
                  - Dlp
                  - Policies
                  - Enable
                  - Disable
                  - Dictionaries
                  - Data
                  - Download
                  - Upload
                  - Violations
                  - Signal
                summary: Updates a policy. Cannot be used for creation.
                description: >
                  Update the policy (name, type, contentTypes, scopes) and also
                  the dictionaries for a policy.

                  Warning: If you send empty list of dictionaries during the
                  update operation, then all the

                  dictionaries for this policy are deleted and policy is
                  automatically disabled.

                  Note: The policy should already exist.
            /v3/dlp/policies/{policyId}/delete:
              post:
                tags:
                  - Delete
                  - Policy
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                  - Share
                  - Util
                  - Echo
                  - Signals
                  - List
                  - Get
                  - Delete
                  - Subscribe
                  - Unsubscribe
                  - Subscribers
                  - Info
                  - Dlp
                  - Policies
                  - Enable
                  - Disable
                  - Dictionaries
                  - Data
                  - Download
                  - Upload
                  - Violations
                  - Signal
                summary: Delete a policy
                description: |
                  Delete a policy.
                  Note: Only disabled policy can be deleted
            /v3/dlp/policies/{policyId}/enable:
              post:
                tags:
                  - Enables
                  - Policy.
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                  - Share
                  - Util
                  - Echo
                  - Signals
                  - List
                  - Get
                  - Delete
                  - Subscribe
                  - Unsubscribe
                  - Subscribers
                  - Info
                  - Dlp
                  - Policies
                  - Enable
                  - Disable
                  - Dictionaries
                  - Data
                  - Download
                  - Upload
                  - Violations
                  - Signal
                summary: Enables a policy.
                description: Enables a policy.
            /v3/dlp/policies/{policyId}/disable:
              post:
                tags:
                  - Disables
                  - Policy.
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                  - Share
                  - Util
                  - Echo
                  - Signals
                  - List
                  - Get
                  - Delete
                  - Subscribe
                  - Unsubscribe
                  - Subscribers
                  - Info
                  - Dlp
                  - Policies
                  - Enable
                  - Disable
                  - Dictionaries
                  - Data
                  - Download
                  - Upload
                  - Violations
                  - Signal
                summary: Disables a policy.
                description: Disables a policy.
            /v3/dlp/violations/message:
              get:
                tags:
                  - Get
                  - Violations
                  - As
                  - Result
                  - Of
                  - Policy
                  - Enforcement
                  - 'On'
                  - Messages.
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                  - Share
                  - Util
                  - Echo
                  - Signals
                  - List
                  - Get
                  - Delete
                  - Subscribe
                  - Unsubscribe
                  - Subscribers
                  - Info
                  - Dlp
                  - Policies
                  - Enable
                  - Disable
                  - Dictionaries
                  - Data
                  - Download
                  - Upload
                  - Violations
                  - Signal
                summary: Get violations as a result of policy enforcement on messages.
                description: >-
                  Retrieves DLP v3 message related violations for a given time
                  range
            /v3/dlp/violations/stream:
              get:
                tags:
                  - Get
                  - Violations
                  - As
                  - Result
                  - Of
                  - Policy
                  - Enforcement
                  - 'On'
                  - Streams.
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                  - Share
                  - Util
                  - Echo
                  - Signals
                  - List
                  - Get
                  - Delete
                  - Subscribe
                  - Unsubscribe
                  - Subscribers
                  - Info
                  - Dlp
                  - Policies
                  - Enable
                  - Disable
                  - Dictionaries
                  - Data
                  - Download
                  - Upload
                  - Violations
                  - Signal
                summary: Get violations as a result of policy enforcement on streams.
                description: >-
                  Retrieves DLP v3 signal related violations for a given time
                  range
            /v3/dlp/violations/signal:
              get:
                tags:
                  - Get
                  - Violations
                  - As
                  - Result
                  - Of
                  - Policy
                  - Enforcement
                  - 'On'
                  - Signals.
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                  - Share
                  - Util
                  - Echo
                  - Signals
                  - List
                  - Get
                  - Delete
                  - Subscribe
                  - Unsubscribe
                  - Subscribers
                  - Info
                  - Dlp
                  - Policies
                  - Enable
                  - Disable
                  - Dictionaries
                  - Data
                  - Download
                  - Upload
                  - Violations
                  - Signal
                summary: Get violations as a result of policy enforcement on signals.
                description: >-
                  Retrieves DLP v3 signal related violations for a given time
                  range
            /v3/dlp/violation/attachment:
              get:
                tags:
                  - Get
                  - Attachments
                  - That
                  - Were
                  - Sent
                  - As
                  - Part
                  - Of
                  - Messages
                  - Flagged
                  - By
                  - The
                  - System.
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                  - Share
                  - Util
                  - Echo
                  - Signals
                  - List
                  - Get
                  - Delete
                  - Subscribe
                  - Unsubscribe
                  - Subscribers
                  - Info
                  - Dlp
                  - Policies
                  - Enable
                  - Disable
                  - Dictionaries
                  - Data
                  - Download
                  - Upload
                  - Violations
                  - Signal
                  - Violation
                summary: >-
                  Get attachments that were sent as part of messages that were
                  flagged by the DLP System.
                description: >-
                  Retrieves attachments from related message violations as a
                  base64 encoded String.
            /v1/audittrail/privilegeduser:
              get:
                tags:
                  - Get
                  - List
                  - Of
                  - Actions
                  - Performed
                  - By
                  - Privileged
                  - Account
                  - Acting
                  - As
                  - User
                  - Given
                  - Period
                  - Time.
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                  - Share
                  - Util
                  - Echo
                  - Signals
                  - List
                  - Get
                  - Delete
                  - Subscribe
                  - Unsubscribe
                  - Subscribers
                  - Info
                  - Dlp
                  - Policies
                  - Enable
                  - Disable
                  - Dictionaries
                  - Data
                  - Download
                  - Upload
                  - Violations
                  - Signal
                  - Violation
                  - Audittrail
                  - Privilegeduser
                summary: >-
                  Get a list of  actions performed by a privileged account
                  acting as privileged user given a period of time.
                description: >-
                  Get a list of actions performed by a privileged account acting
                  as privileged user given a period of time.
            /v5/datafeeds:
              get:
                tags:
                  - Read
                  - List
                  - Of
                  - Real
                  - Time
                  - Messages
                  - Events
                  - Stream
                  - ("datafeed").
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                  - Share
                  - Util
                  - Echo
                  - Signals
                  - List
                  - Get
                  - Delete
                  - Subscribe
                  - Unsubscribe
                  - Subscribers
                  - Info
                  - Dlp
                  - Policies
                  - Enable
                  - Disable
                  - Dictionaries
                  - Data
                  - Download
                  - Upload
                  - Violations
                  - Signal
                  - Violation
                  - Audittrail
                  - Privilegeduser
                  - V5
                  - Datafeeds
                summary: Read list of real time messages / events stream ("datafeed").
                description: >
                  _Available on Agent 2.57.0 and above._


                  The datafeed provides messages and events from all
                  conversations that the user

                  is in. The types of events surfaced in the datafeed can be
                  found in the [Real Time Events](./docs/real-time-events.md)
                  list.


                  Returns the list of the datafeeds for the user.

                  Any datafeed ID of the list can then be used as input to the
                  Read Messages/Events Stream v4 endpoint.
              post:
                tags:
                  - Create
                  - New
                  - Real
                  - Time
                  - Messages
                  - Events
                  - Stream
                  - ("datafeed").
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                  - Share
                  - Util
                  - Echo
                  - Signals
                  - List
                  - Get
                  - Delete
                  - Subscribe
                  - Unsubscribe
                  - Subscribers
                  - Info
                  - Dlp
                  - Policies
                  - Enable
                  - Disable
                  - Dictionaries
                  - Data
                  - Download
                  - Upload
                  - Violations
                  - Signal
                  - Violation
                  - Audittrail
                  - Privilegeduser
                  - V5
                  - Datafeeds
                summary: Create a new real time messages / events stream ("datafeed").
                description: >
                  _Available on Agent 2.57.0 and above._


                  The datafeed provides messages and events from all
                  conversations that the user

                  is in. The types of events surfaced in the datafeed can be
                  found in the Real Time Events list.

                  (see definition on top of the file)


                  Returns the ID of the datafeed that has just been created.

                  This ID should then be used as input to the Read
                  Messages/Events Stream v4 endpoint.
            /v5/datafeeds/{datafeedId}:
              delete:
                tags:
                  - Delete
                  - The
                  - Specified
                  - Real
                  - Time
                  - Message
                  - Event
                  - Stream
                  - ("datafeed").
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                  - Share
                  - Util
                  - Echo
                  - Signals
                  - List
                  - Get
                  - Delete
                  - Subscribe
                  - Unsubscribe
                  - Subscribers
                  - Info
                  - Dlp
                  - Policies
                  - Enable
                  - Disable
                  - Dictionaries
                  - Data
                  - Download
                  - Upload
                  - Violations
                  - Signal
                  - Violation
                  - Audittrail
                  - Privilegeduser
                  - V5
                  - Datafeeds
                summary: >-
                  Delete the specified real time message / event stream
                  ("datafeed").
                description: >
                  _Available on Agent 2.57.0 and above._


                  The datafeed provides messages and events from all
                  conversations that the user

                  is in. The types of events surfaced in the datafeed can be
                  found in the Real Time Events list.

                  (see definition on top of the file)


                  Delete the specified datafeed.
            /v5/datafeeds/{datafeedId}/read:
              post:
                tags:
                  - Read
                  - The
                  - Specified
                  - Real
                  - Time
                  - Message
                  - Event
                  - Stream
                  - ("datafeed").
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                  - Share
                  - Util
                  - Echo
                  - Signals
                  - List
                  - Get
                  - Delete
                  - Subscribe
                  - Unsubscribe
                  - Subscribers
                  - Info
                  - Dlp
                  - Policies
                  - Enable
                  - Disable
                  - Dictionaries
                  - Data
                  - Download
                  - Upload
                  - Violations
                  - Signal
                  - Violation
                  - Audittrail
                  - Privilegeduser
                  - V5
                  - Datafeeds
                  - Read
                summary: >-
                  Read the specified real time message / event stream
                  ("datafeed").
                description: >
                  _Available on Agent 2.57.0 and above._


                  The datafeed provides messages and events from all
                  conversations that the user

                  is in. The types of events surfaced in the datafeed can be
                  found in the Real Time Events list.

                  (see definition on top of the file)


                  Read the specified datafeed.


                  The ackId sent as parameter can be empty for the first call.
                  In the response an ackId will be sent back and it can be used
                  for

                  the next call: in this way you acknowledge that you have
                  received the events that came with that ackId; datafeed will
                  remove the events

                  associated with that ackId from your queue
            /v5/events/read:
              post:
                tags:
                  - Read
                  - Real
                  - Time
                  - Events
                  - From
                  - An
                  - Event
                  - Stream
                  - (aka
                  - Datafeed)
                  - V3
                  - Health
                  - Extended
                  - V4
                  - Message
                  - Import
                  - Blast
                  - V1
                  - Id
                  - Search
                  - Stream
                  - Sid
                  - Attachment
                  - Create
                  - Mid
                  - Update
                  - Share
                  - Util
                  - Echo
                  - Signals
                  - List
                  - Get
                  - Delete
                  - Subscribe
                  - Unsubscribe
                  - Subscribers
                  - Info
                  - Dlp
                  - Policies
                  - Enable
                  - Disable
                  - Dictionaries
                  - Data
                  - Download
                  - Upload
                  - Violations
                  - Signal
                  - Violation
                  - Audittrail
                  - Privilegeduser
                  - V5
                  - Datafeeds
                  - Read
                  - Events
                summary: Read Real Time Events from an event stream (aka datafeed)
                description: >
                  _Available on Agent 22.5.1 and above.This endpoint provides

                  messages and events from all conversations that the user is in
                  or events

                  from the whole pod depending on the "type" field value.

                  When "type":"fanout" is provided in the body, then only events
                  from streams 

                  the accountbelongs to are returned. Otherwise, if "type":
                  "datahose" is provided

                  in the body, then events returned are not limited to the
                  streams user

                  belongs to. In this case, at least one event type must be
                  provided in the

                  "filters" field. In case you are using a datahose feed and
                  retrieving

                  SOCIALMESSAGE events, ceservice account must be properly
                  configured in

                  the Agent.The types of events returned can be found in the
                  Real Time

                  Events list (see definition on top of the file). The ackId
                  sent as parameter

                  can be empty for the first call. In the response an ackId will
                  be sent back

                  and it can be used for the next call: in this way you
                  acknowledge that

                  you have received the events that came with that ackId.

                  If you have several instances of the same bot, they must share
                  the same feed so 

                  that events are spread across all bot instances. To do so, you
                  must: share the same 

                  service account provide the same "tag" and same "filte
    aid: symphony:symphony-agent-api
    overlays:
      - type: APIs.io Search
        url: overlays/agent-openapi-search.yml
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---