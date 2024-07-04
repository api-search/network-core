---
name: Collections
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/collections.png
url: https://example.com/apis/collections.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Collections
apis:
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
  - name: location
    description: >-
      <p>"Suite of geospatial services including Maps, Places, Routes, Tracking,
      and Geofencing"</p>
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
            title: location
          paths:
            /tracking/v0/trackers/{TrackerName}/consumers:
              POST:
                summary: AssociateTrackerConsumer
                description: >-
                  <p>Creates an association between a geofence collection and a
                  tracker resource. This allows the tracker resource to
                  communicate location data to the linked geofence collection.
                  </p> <p>You can associate up to five geofence collections to
                  each tracker resource.</p> <note> <p>Currently not supported —
                  Cross-account configurations, such as creating associations
                  between a tracker resource in one account and a geofence
                  collection in another account.</p> </note>
                tags:
                  - Associate
                  - Trackers
                  - Consumer
                  - Trackers
                  - Names
                  - Consumers
            /tracking/v0/trackers/{TrackerName}/delete-positions:
              POST:
                summary: BatchDeleteDevicePositionHistory
                description: >-
                  <p>Deletes the position history of one or more devices from a
                  tracker resource.</p>
                tags:
                  - Batches
                  - Delete
                  - Device
                  - Positions
                  - History
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
            /geofencing/v0/collections/{CollectionName}/delete-geofences:
              POST:
                summary: BatchDeleteGeofence
                description: >-
                  <p>Deletes a batch of geofences from a geofence
                  collection.</p> <note> <p>This operation deletes the resource
                  permanently.</p> </note>
                tags:
                  - Batches
                  - Delete
                  - Geofences
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
            /geofencing/v0/collections/{CollectionName}/positions:
              POST:
                summary: BatchEvaluateGeofences
                description: >-
                  <p>Evaluates device positions against the geofence geometries
                  from a given geofence collection.</p> <p>This operation always
                  returns an empty response because geofences are asynchronously
                  evaluated. The evaluation determines if the device has entered
                  or exited a geofenced area, and then publishes one of the
                  following events to Amazon EventBridge:</p> <ul> <li> <p>
                  <code>ENTER</code> if Amazon Location determines that the
                  tracked device has entered a geofenced area.</p> </li> <li>
                  <p> <code>EXIT</code> if Amazon Location determines that the
                  tracked device has exited a geofenced area.</p> </li> </ul>
                  <note> <p>The last geofence that a device was observed within
                  is tracked for 30 days after the most recent device position
                  update.</p> </note> <note> <p>Geofence evaluation uses the
                  given device position. It does not account for the optional
                  <code>Accuracy</code> of a
                  <code>DevicePositionUpdate</code>.</p> </note> <note> <p>The
                  <code>DeviceID</code> is used as a string to represent the
                  device. You do not need to have a <code>Tracker</code>
                  associated with the <code>DeviceID</code>.</p> </note>
                tags:
                  - Batches
                  - Evaluate
                  - Geofences
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
            /tracking/v0/trackers/{TrackerName}/get-positions:
              POST:
                summary: BatchGetDevicePosition
                description: >-
                  <p>Lists the latest device positions for requested
                  devices.</p>
                tags:
                  - Batches
                  - Get
                  - Device
                  - Positions
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
            /geofencing/v0/collections/{CollectionName}/put-geofences:
              POST:
                summary: BatchPutGeofence
                description: >-
                  <p>A batch request for storing geofence geometries into a
                  given geofence collection, or updates the geometry of an
                  existing geofence if a geofence ID is included in the
                  request.</p>
                tags:
                  - Batches
                  - Put
                  - Geofences
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
            /tracking/v0/trackers/{TrackerName}/positions:
              POST:
                summary: BatchUpdateDevicePosition
                description: >-
                  <p>Uploads position update data for one or more devices to a
                  tracker resource (up to 10 devices per batch). Amazon Location
                  uses the data when it reports the last known device position
                  and position history. Amazon Location retains location data
                  for 30 days.</p> <note> <p>Position updates are handled based
                  on the <code>PositionFiltering</code> property of the tracker.
                  When <code>PositionFiltering</code> is set to
                  <code>TimeBased</code>, updates are evaluated against linked
                  geofence collections, and location data is stored at a maximum
                  of one position per 30 second interval. If your update
                  frequency is more often than every 30 seconds, only one update
                  per 30 seconds is stored for each unique device ID.</p>
                  <p>When <code>PositionFiltering</code> is set to
                  <code>DistanceBased</code> filtering, location data is stored
                  and evaluated against linked geofence collections only if the
                  device has moved more than 30 m (98.4 ft).</p> <p>When
                  <code>PositionFiltering</code> is set to
                  <code>AccuracyBased</code> filtering, location data is stored
                  and evaluated against linked geofence collections only if the
                  device has moved more than the measured accuracy. For example,
                  if two consecutive updates from a device have a horizontal
                  accuracy of 5 m and 10 m, the second update is neither stored
                  or evaluated if the device has moved less than 15 m. If
                  <code>PositionFiltering</code> is set to
                  <code>AccuracyBased</code> filtering, Amazon Location uses the
                  default value <code>{ "Horizontal": 0}</code> when accuracy is
                  not provided on a <code>DevicePositionUpdate</code>.</p>
                  </note>
                tags:
                  - Batches
                  - Update
                  - Device
                  - Positions
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
            /routes/v0/calculators/{CalculatorName}/calculate/route:
              POST:
                summary: CalculateRoute
                description: >-
                  <p> <a
                  href="https://docs.aws.amazon.com/location/latest/developerguide/calculate-route.html">Calculates
                  a route</a> given the following required parameters:
                  <code>DeparturePosition</code> and
                  <code>DestinationPosition</code>. Requires that you first <a
                  href="https://docs.aws.amazon.com/location-routes/latest/APIReference/API_CreateRouteCalculator.html">create
                  a route calculator resource</a>.</p> <p>By default, a request
                  that doesn't specify a departure time uses the best time of
                  day to travel with the best traffic conditions when
                  calculating the route.</p> <p>Additional options include:</p>
                  <ul> <li> <p> <a
                  href="https://docs.aws.amazon.com/location/latest/developerguide/departure-time.html">Specifying
                  a departure time</a> using either <code>DepartureTime</code>
                  or <code>DepartNow</code>. This calculates a route based on
                  predictive traffic data at the given time. </p> <note> <p>You
                  can't specify both <code>DepartureTime</code> and
                  <code>DepartNow</code> in a single request. Specifying both
                  parameters returns a validation error.</p> </note> </li> <li>
                  <p> <a
                  href="https://docs.aws.amazon.com/location/latest/developerguide/travel-mode.html">Specifying
                  a travel mode</a> using TravelMode sets the transportation
                  mode used to calculate the routes. This also lets you specify
                  additional route preferences in <code>CarModeOptions</code> if
                  traveling by <code>Car</code>, or
                  <code>TruckModeOptions</code> if traveling by
                  <code>Truck</code>.</p> <note> <p>If you specify
                  <code>walking</code> for the travel mode and your data
                  provider is Esri, the start and destination must be within
                  40km.</p> </note> </li> </ul>
                tags:
                  - Calculate
                  - Routes
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
            /routes/v0/calculators/{CalculatorName}/calculate/route-matrix:
              POST:
                summary: CalculateRouteMatrix
                description: >-
                  <p> <a
                  href="https://docs.aws.amazon.com/location/latest/developerguide/calculate-route-matrix.html">
                  Calculates a route matrix</a> given the following required
                  parameters: <code>DeparturePositions</code> and
                  <code>DestinationPositions</code>.
                  <code>CalculateRouteMatrix</code> calculates routes and
                  returns the travel time and travel distance from each
                  departure position to each destination position in the
                  request. For example, given departure positions A and B, and
                  destination positions X and Y,
                  <code>CalculateRouteMatrix</code> will return time and
                  distance for routes from A to X, A to Y, B to X, and B to Y
                  (in that order). The number of results returned (and routes
                  calculated) will be the number of
                  <code>DeparturePositions</code> times the number of
                  <code>DestinationPositions</code>.</p> <note> <p>Your account
                  is charged for each route calculated, not the number of
                  requests.</p> </note> <p>Requires that you first <a
                  href="https://docs.aws.amazon.com/location-routes/latest/APIReference/API_CreateRouteCalculator.html">create
                  a route calculator resource</a>.</p> <p>By default, a request
                  that doesn't specify a departure time uses the best time of
                  day to travel with the best traffic conditions when
                  calculating routes.</p> <p>Additional options include:</p>
                  <ul> <li> <p> <a
                  href="https://docs.aws.amazon.com/location/latest/developerguide/departure-time.html">
                  Specifying a departure time</a> using either
                  <code>DepartureTime</code> or <code>DepartNow</code>. This
                  calculates routes based on predictive traffic data at the
                  given time. </p> <note> <p>You can't specify both
                  <code>DepartureTime</code> and <code>DepartNow</code> in a
                  single request. Specifying both parameters returns a
                  validation error.</p> </note> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/location/latest/developerguide/travel-mode.html">Specifying
                  a travel mode</a> using TravelMode sets the transportation
                  mode used to calculate the routes. This also lets you specify
                  additional route preferences in <code>CarModeOptions</code> if
                  traveling by <code>Car</code>, or
                  <code>TruckModeOptions</code> if traveling by
                  <code>Truck</code>.</p> </li> </ul>
                tags:
                  - Calculate
                  - Routes
                  - Matrix
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
            /geofencing/v0/collections:
              POST:
                summary: CreateGeofenceCollection
                description: >-
                  <p>Creates a geofence collection, which manages and stores
                  geofences.</p>
                tags:
                  - Create
                  - Geofences
                  - Collections
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
            /metadata/v0/keys:
              POST:
                summary: CreateKey
                description: >-
                  <p>Creates an API key resource in your Amazon Web Services
                  account, which lets you grant actions for Amazon Location
                  resources to the API key bearer.</p> <note> <p>For more
                  information, see <a
                  href="https://docs.aws.amazon.com/location/latest/developerguide/using-apikeys.html">Using
                  API keys</a>.</p> </note>
                tags:
                  - Create
                  - Keys
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
            /maps/v0/maps:
              POST:
                summary: CreateMap
                description: >-
                  <p>Creates a map resource in your Amazon Web Services account,
                  which provides map tiles of different styles sourced from
                  global location data providers.</p> <note> <p>If your
                  application is tracking or routing assets you use in your
                  business, such as delivery vehicles or employees, you must not
                  use Esri as your geolocation provider. See section 82 of the
                  <a href="http://aws.amazon.com/service-terms">Amazon Web
                  Services service terms</a> for more details.</p> </note>
                tags:
                  - Create
                  - Maps
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
            /places/v0/indexes:
              POST:
                summary: CreatePlaceIndex
                description: >-
                  <p>Creates a place index resource in your Amazon Web Services
                  account. Use a place index resource to geocode addresses and
                  other text queries by using the
                  <code>SearchPlaceIndexForText</code> operation, and reverse
                  geocode coordinates by using the
                  <code>SearchPlaceIndexForPosition</code> operation, and enable
                  autosuggestions by using the
                  <code>SearchPlaceIndexForSuggestions</code> operation.</p>
                  <note> <p>If your application is tracking or routing assets
                  you use in your business, such as delivery vehicles or
                  employees, you must not use Esri as your geolocation provider.
                  See section 82 of the <a
                  href="http://aws.amazon.com/service-terms">Amazon Web Services
                  service terms</a> for more details.</p> </note>
                tags:
                  - Create
                  - Places
                  - Index
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
            /routes/v0/calculators:
              POST:
                summary: CreateRouteCalculator
                description: >-
                  <p>Creates a route calculator resource in your Amazon Web
                  Services account.</p> <p>You can send requests to a route
                  calculator resource to estimate travel time, distance, and get
                  directions. A route calculator sources traffic and road
                  network data from your chosen data provider.</p> <note> <p>If
                  your application is tracking or routing assets you use in your
                  business, such as delivery vehicles or employees, you must not
                  use Esri as your geolocation provider. See section 82 of the
                  <a href="http://aws.amazon.com/service-terms">Amazon Web
                  Services service terms</a> for more details.</p> </note>
                tags:
                  - Create
                  - Routes
                  - Calculators
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
                  - Routes
                  - Calculators
            /tracking/v0/trackers:
              POST:
                summary: CreateTracker
                description: >-
                  <p>Creates a tracker resource in your Amazon Web Services
                  account, which lets you retrieve current and historical
                  location of devices.</p>
                tags:
                  - Create
                  - Trackers
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
                  - Routes
                  - Calculators
                  - Tracking
                  - Trackers
            /geofencing/v0/collections/{CollectionName}:
              PATCH:
                summary: UpdateGeofenceCollection
                description: >-
                  <p>Updates the specified properties of a given geofence
                  collection.</p>
                tags:
                  - Update
                  - Geofences
                  - Collections
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
                  - Routes
                  - Calculators
                  - Tracking
                  - Trackers
            /metadata/v0/keys/{KeyName}:
              PATCH:
                summary: UpdateKey
                description: >-
                  <p>Updates the specified properties of a given API key
                  resource.</p>
                tags:
                  - Update
                  - Keys
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
                  - Routes
                  - Calculators
                  - Tracking
                  - Trackers
                  - Keys
            /maps/v0/maps/{MapName}:
              PATCH:
                summary: UpdateMap
                description: >-
                  <p>Updates the specified properties of a given map
                  resource.</p>
                tags:
                  - Update
                  - Maps
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
                  - Routes
                  - Calculators
                  - Tracking
                  - Trackers
                  - Keys
                  - Maps
            /places/v0/indexes/{IndexName}:
              PATCH:
                summary: UpdatePlaceIndex
                description: >-
                  <p>Updates the specified properties of a given place index
                  resource.</p>
                tags:
                  - Update
                  - Places
                  - Index
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
                  - Routes
                  - Calculators
                  - Tracking
                  - Trackers
                  - Keys
                  - Maps
                  - Index
            /routes/v0/calculators/{CalculatorName}:
              PATCH:
                summary: UpdateRouteCalculator
                description: >-
                  <p>Updates the specified properties for a given route
                  calculator resource.</p>
                tags:
                  - Update
                  - Routes
                  - Calculators
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
                  - Routes
                  - Calculators
                  - Tracking
                  - Trackers
                  - Keys
                  - Maps
                  - Index
            /tracking/v0/trackers/{TrackerName}:
              PATCH:
                summary: UpdateTracker
                description: >-
                  <p>Updates the specified properties of a given tracker
                  resource.</p>
                tags:
                  - Update
                  - Trackers
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
                  - Routes
                  - Calculators
                  - Tracking
                  - Trackers
                  - Keys
                  - Maps
                  - Index
            /tracking/v0/trackers/{TrackerName}/consumers/{ConsumerArn}:
              DELETE:
                summary: DisassociateTrackerConsumer
                description: >-
                  <p>Removes the association between a tracker resource and a
                  geofence collection.</p> <note> <p>Once you unlink a tracker
                  resource from a geofence collection, the tracker positions
                  will no longer be automatically evaluated against
                  geofences.</p> </note>
                tags:
                  - Disassociate
                  - Trackers
                  - Consumer
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
                  - Routes
                  - Calculators
                  - Tracking
                  - Trackers
                  - Keys
                  - Maps
                  - Index
                  - Consumer
                  - ARN
            /tracking/v0/trackers/{TrackerName}/devices/{DeviceId}/positions/latest:
              GET:
                summary: GetDevicePosition
                description: >-
                  <p>Retrieves a device's most recent position according to its
                  sample time.</p> <note> <p>Device positions are deleted after
                  30 days.</p> </note>
                tags:
                  - Get
                  - Device
                  - Positions
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
                  - Routes
                  - Calculators
                  - Tracking
                  - Trackers
                  - Keys
                  - Maps
                  - Index
                  - Consumer
                  - ARN
                  - Devices
                  - Device
                  - Identifiers
                  - Latest
            /tracking/v0/trackers/{TrackerName}/devices/{DeviceId}/list-positions:
              POST:
                summary: GetDevicePositionHistory
                description: >-
                  <p>Retrieves the device position history from a tracker
                  resource within a specified range of time.</p> <note>
                  <p>Device positions are deleted after 30 days.</p> </note>
                tags:
                  - Get
                  - Device
                  - Positions
                  - History
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
                  - Routes
                  - Calculators
                  - Tracking
                  - Trackers
                  - Keys
                  - Maps
                  - Index
                  - Consumer
                  - ARN
                  - Devices
                  - Device
                  - Identifiers
                  - Latest
                  - Lists
            /geofencing/v0/collections/{CollectionName}/geofences/{GeofenceId}:
              PUT:
                summary: PutGeofence
                description: >-
                  <p>Stores a geofence geometry in a given geofence collection,
                  or updates the geometry of an existing geofence if a geofence
                  ID is included in the request. </p>
                tags:
                  - Put
                  - Geofences
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
                  - Routes
                  - Calculators
                  - Tracking
                  - Trackers
                  - Keys
                  - Maps
                  - Index
                  - Consumer
                  - ARN
                  - Devices
                  - Device
                  - Identifiers
                  - Latest
                  - Lists
                  - Geofences
            /maps/v0/maps/{MapName}/glyphs/{FontStack}/{FontUnicodeRange}:
              GET:
                summary: GetMapGlyphs
                description: <p>Retrieves glyphs used to display labels on a map.</p>
                tags:
                  - Get
                  - Maps
                  - Glyphs
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
                  - Routes
                  - Calculators
                  - Tracking
                  - Trackers
                  - Keys
                  - Maps
                  - Index
                  - Consumer
                  - ARN
                  - Devices
                  - Device
                  - Identifiers
                  - Latest
                  - Lists
                  - Geofences
                  - Glyphs
                  - Fonts
                  - Stack
                  - Unicode
                  - Ranges
            /maps/v0/maps/{MapName}/sprites/{FileName}:
              GET:
                summary: GetMapSprites
                description: >-
                  <p>Retrieves the sprite sheet corresponding to a map resource.
                  The sprite sheet is a PNG image paired with a JSON document
                  describing the offsets of individual icons that will be
                  displayed on a rendered map.</p>
                tags:
                  - Get
                  - Maps
                  - Sprites
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
                  - Routes
                  - Calculators
                  - Tracking
                  - Trackers
                  - Keys
                  - Maps
                  - Index
                  - Consumer
                  - ARN
                  - Devices
                  - Device
                  - Identifiers
                  - Latest
                  - Lists
                  - Geofences
                  - Glyphs
                  - Fonts
                  - Stack
                  - Unicode
                  - Ranges
                  - Sprites
                  - File
            /maps/v0/maps/{MapName}/style-descriptor:
              GET:
                summary: GetMapStyleDescriptor
                description: >-
                  <p>Retrieves the map style descriptor from a map resource.
                  </p> <p>The style descriptor contains speciﬁcations on how
                  features render on a map. For example, what data to display,
                  what order to display the data in, and the style for the data.
                  Style descriptors follow the Mapbox Style Specification.</p>
                tags:
                  - Get
                  - Maps
                  - Styles
                  - Descriptions
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
                  - Routes
                  - Calculators
                  - Tracking
                  - Trackers
                  - Keys
                  - Maps
                  - Index
                  - Consumer
                  - ARN
                  - Devices
                  - Device
                  - Identifiers
                  - Latest
                  - Lists
                  - Geofences
                  - Glyphs
                  - Fonts
                  - Stack
                  - Unicode
                  - Ranges
                  - Sprites
                  - File
                  - Styles
                  - Descriptions
            /maps/v0/maps/{MapName}/tiles/{Z}/{X}/{Y}:
              GET:
                summary: GetMapTile
                description: >-
                  <p>Retrieves a vector data tile from the map resource. Map
                  tiles are used by clients to render a map. they're addressed
                  using a grid arrangement with an X coordinate, Y coordinate,
                  and Z (zoom) level. </p> <p>The origin (0, 0) is the top left
                  of the map. Increasing the zoom level by 1 doubles both the X
                  and Y dimensions, so a tile containing data for the entire
                  world at (0/0/0) will be split into 4 tiles at zoom 1 (1/0/0,
                  1/0/1, 1/1/0, 1/1/1).</p>
                tags:
                  - Get
                  - Maps
                  - Tiles
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
                  - Routes
                  - Calculators
                  - Tracking
                  - Trackers
                  - Keys
                  - Maps
                  - Index
                  - Consumer
                  - ARN
                  - Devices
                  - Device
                  - Identifiers
                  - Latest
                  - Lists
                  - Geofences
                  - Glyphs
                  - Fonts
                  - Stack
                  - Unicode
                  - Ranges
                  - Sprites
                  - File
                  - Styles
                  - Descriptions
                  - Tiles
            /places/v0/indexes/{IndexName}/places/{PlaceId}:
              GET:
                summary: GetPlace
                description: >-
                  <p>Finds a place by its unique ID. A <code>PlaceId</code> is
                  returned by other search operations.</p> <note> <p>A PlaceId
                  is valid only if all of the following are the same in the
                  original search request and the call to
                  <code>GetPlace</code>.</p> <ul> <li> <p>Customer Amazon Web
                  Services account</p> </li> <li> <p>Amazon Web Services
                  Region</p> </li> <li> <p>Data provider specified in the place
                  index resource</p> </li> </ul> </note>
                tags:
                  - Get
                  - Places
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
                  - Routes
                  - Calculators
                  - Tracking
                  - Trackers
                  - Keys
                  - Maps
                  - Index
                  - Consumer
                  - ARN
                  - Devices
                  - Device
                  - Identifiers
                  - Latest
                  - Lists
                  - Geofences
                  - Glyphs
                  - Fonts
                  - Stack
                  - Unicode
                  - Ranges
                  - Sprites
                  - File
                  - Styles
                  - Descriptions
                  - Tiles
                  - Places
            /tracking/v0/trackers/{TrackerName}/list-positions:
              POST:
                summary: ListDevicePositions
                description: <p>A batch request to retrieve all device positions.</p>
                tags:
                  - Lists
                  - Device
                  - Positions
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
                  - Routes
                  - Calculators
                  - Tracking
                  - Trackers
                  - Keys
                  - Maps
                  - Index
                  - Consumer
                  - ARN
                  - Devices
                  - Device
                  - Identifiers
                  - Latest
                  - Lists
                  - Geofences
                  - Glyphs
                  - Fonts
                  - Stack
                  - Unicode
                  - Ranges
                  - Sprites
                  - File
                  - Styles
                  - Descriptions
                  - Tiles
                  - Places
            /geofencing/v0/list-collections:
              POST:
                summary: ListGeofenceCollections
                description: >-
                  <p>Lists geofence collections in your Amazon Web Services
                  account.</p>
                tags:
                  - Lists
                  - Geofences
                  - Collections
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
                  - Routes
                  - Calculators
                  - Tracking
                  - Trackers
                  - Keys
                  - Maps
                  - Index
                  - Consumer
                  - ARN
                  - Devices
                  - Device
                  - Identifiers
                  - Latest
                  - Lists
                  - Geofences
                  - Glyphs
                  - Fonts
                  - Stack
                  - Unicode
                  - Ranges
                  - Sprites
                  - File
                  - Styles
                  - Descriptions
                  - Tiles
                  - Places
            /geofencing/v0/collections/{CollectionName}/list-geofences:
              POST:
                summary: ListGeofences
                description: <p>Lists geofences stored in a given geofence collection.</p>
                tags:
                  - Lists
                  - Geofences
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
                  - Routes
                  - Calculators
                  - Tracking
                  - Trackers
                  - Keys
                  - Maps
                  - Index
                  - Consumer
                  - ARN
                  - Devices
                  - Device
                  - Identifiers
                  - Latest
                  - Lists
                  - Geofences
                  - Glyphs
                  - Fonts
                  - Stack
                  - Unicode
                  - Ranges
                  - Sprites
                  - File
                  - Styles
                  - Descriptions
                  - Tiles
                  - Places
            /metadata/v0/list-keys:
              POST:
                summary: ListKeys
                description: >-
                  <p>Lists API key resources in your Amazon Web Services
                  account.</p>
                tags:
                  - Lists
                  - Keys
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
                  - Routes
                  - Calculators
                  - Tracking
                  - Trackers
                  - Keys
                  - Maps
                  - Index
                  - Consumer
                  - ARN
                  - Devices
                  - Device
                  - Identifiers
                  - Latest
                  - Lists
                  - Geofences
                  - Glyphs
                  - Fonts
                  - Stack
                  - Unicode
                  - Ranges
                  - Sprites
                  - File
                  - Styles
                  - Descriptions
                  - Tiles
                  - Places
            /maps/v0/list-maps:
              POST:
                summary: ListMaps
                description: >-
                  <p>Lists map resources in your Amazon Web Services
                  account.</p>
                tags:
                  - Lists
                  - Maps
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
                  - Routes
                  - Calculators
                  - Tracking
                  - Trackers
                  - Keys
                  - Maps
                  - Index
                  - Consumer
                  - ARN
                  - Devices
                  - Device
                  - Identifiers
                  - Latest
                  - Lists
                  - Geofences
                  - Glyphs
                  - Fonts
                  - Stack
                  - Unicode
                  - Ranges
                  - Sprites
                  - File
                  - Styles
                  - Descriptions
                  - Tiles
                  - Places
            /places/v0/list-indexes:
              POST:
                summary: ListPlaceIndexes
                description: >-
                  <p>Lists place index resources in your Amazon Web Services
                  account.</p>
                tags:
                  - Lists
                  - Places
                  - Indexes
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
                  - Routes
                  - Calculators
                  - Tracking
                  - Trackers
                  - Keys
                  - Maps
                  - Index
                  - Consumer
                  - ARN
                  - Devices
                  - Device
                  - Identifiers
                  - Latest
                  - Lists
                  - Geofences
                  - Glyphs
                  - Fonts
                  - Stack
                  - Unicode
                  - Ranges
                  - Sprites
                  - File
                  - Styles
                  - Descriptions
                  - Tiles
                  - Places
            /routes/v0/list-calculators:
              POST:
                summary: ListRouteCalculators
                description: >-
                  <p>Lists route calculator resources in your Amazon Web
                  Services account.</p>
                tags:
                  - Lists
                  - Routes
                  - Calculators
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
                  - Routes
                  - Calculators
                  - Tracking
                  - Trackers
                  - Keys
                  - Maps
                  - Index
                  - Consumer
                  - ARN
                  - Devices
                  - Device
                  - Identifiers
                  - Latest
                  - Lists
                  - Geofences
                  - Glyphs
                  - Fonts
                  - Stack
                  - Unicode
                  - Ranges
                  - Sprites
                  - File
                  - Styles
                  - Descriptions
                  - Tiles
                  - Places
            /tags/{ResourceArn}:
              DELETE:
                summary: UntagResource
                description: >-
                  <p>Removes one or more tags from the specified Amazon Location
                  resource.</p>
                tags:
                  - Untag
                  - Resources
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
                  - Routes
                  - Calculators
                  - Tracking
                  - Trackers
                  - Keys
                  - Maps
                  - Index
                  - Consumer
                  - ARN
                  - Devices
                  - Device
                  - Identifiers
                  - Latest
                  - Lists
                  - Geofences
                  - Glyphs
                  - Fonts
                  - Stack
                  - Unicode
                  - Ranges
                  - Sprites
                  - File
                  - Styles
                  - Descriptions
                  - Tiles
                  - Places
                  - Resources
            /tracking/v0/trackers/{TrackerName}/list-consumers:
              POST:
                summary: ListTrackerConsumers
                description: >-
                  <p>Lists geofence collections currently associated to the
                  given tracker resource.</p>
                tags:
                  - Lists
                  - Trackers
                  - Consumers
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
                  - Routes
                  - Calculators
                  - Tracking
                  - Trackers
                  - Keys
                  - Maps
                  - Index
                  - Consumer
                  - ARN
                  - Devices
                  - Device
                  - Identifiers
                  - Latest
                  - Lists
                  - Geofences
                  - Glyphs
                  - Fonts
                  - Stack
                  - Unicode
                  - Ranges
                  - Sprites
                  - File
                  - Styles
                  - Descriptions
                  - Tiles
                  - Places
                  - Resources
            /tracking/v0/list-trackers:
              POST:
                summary: ListTrackers
                description: >-
                  <p>Lists tracker resources in your Amazon Web Services
                  account.</p>
                tags:
                  - Lists
                  - Trackers
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
                  - Routes
                  - Calculators
                  - Tracking
                  - Trackers
                  - Keys
                  - Maps
                  - Index
                  - Consumer
                  - ARN
                  - Devices
                  - Device
                  - Identifiers
                  - Latest
                  - Lists
                  - Geofences
                  - Glyphs
                  - Fonts
                  - Stack
                  - Unicode
                  - Ranges
                  - Sprites
                  - File
                  - Styles
                  - Descriptions
                  - Tiles
                  - Places
                  - Resources
            /places/v0/indexes/{IndexName}/search/position:
              POST:
                summary: SearchPlaceIndexForPosition
                description: >-
                  <p>Reverse geocodes a given coordinate and returns a legible
                  address. Allows you to search for Places or points of interest
                  near a given position.</p>
                tags:
                  - Search
                  - Places
                  - Index
                  - For
                  - Positions
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
                  - Routes
                  - Calculators
                  - Tracking
                  - Trackers
                  - Keys
                  - Maps
                  - Index
                  - Consumer
                  - ARN
                  - Devices
                  - Device
                  - Identifiers
                  - Latest
                  - Lists
                  - Geofences
                  - Glyphs
                  - Fonts
                  - Stack
                  - Unicode
                  - Ranges
                  - Sprites
                  - File
                  - Styles
                  - Descriptions
                  - Tiles
                  - Places
                  - Resources
                  - Search
                  - Positions
            /places/v0/indexes/{IndexName}/search/suggestions:
              POST:
                summary: SearchPlaceIndexForSuggestions
                description: >-
                  <p>Generates suggestions for addresses and points of interest
                  based on partial or misspelled free-form text. This operation
                  is also known as autocomplete, autosuggest, or fuzzy
                  matching.</p> <p>Optional parameters let you narrow your
                  search results by bounding box or country, or bias your search
                  toward a specific position on the globe.</p> <note> <p>You can
                  search for suggested place names near a specified position by
                  using <code>BiasPosition</code>, or filter results within a
                  bounding box by using <code>FilterBBox</code>. These
                  parameters are mutually exclusive; using both
                  <code>BiasPosition</code> and <code>FilterBBox</code> in the
                  same command returns an error.</p> </note>
                tags:
                  - Search
                  - Places
                  - Index
                  - For
                  - Suggestions
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
                  - Routes
                  - Calculators
                  - Tracking
                  - Trackers
                  - Keys
                  - Maps
                  - Index
                  - Consumer
                  - ARN
                  - Devices
                  - Device
                  - Identifiers
                  - Latest
                  - Lists
                  - Geofences
                  - Glyphs
                  - Fonts
                  - Stack
                  - Unicode
                  - Ranges
                  - Sprites
                  - File
                  - Styles
                  - Descriptions
                  - Tiles
                  - Places
                  - Resources
                  - Search
                  - Positions
                  - Suggestions
            /places/v0/indexes/{IndexName}/search/text:
              POST:
                summary: SearchPlaceIndexForText
                description: >-
                  <p>Geocodes free-form text, such as an address, name, city, or
                  region to allow you to search for Places or points of
                  interest. </p> <p>Optional parameters let you narrow your
                  search results by bounding box or country, or bias your search
                  toward a specific position on the globe.</p> <note> <p>You can
                  search for places near a given position using
                  <code>BiasPosition</code>, or filter results within a bounding
                  box using <code>FilterBBox</code>. Providing both parameters
                  simultaneously returns an error.</p> </note> <p>Search results
                  are returned in order of highest to lowest rele
                tags:
                  - Search
                  - Places
                  - Index
                  - For
                  - Text
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
                  - Routes
                  - Calculators
                  - Tracking
                  - Trackers
                  - Keys
                  - Maps
                  - Index
                  - Consumer
                  - ARN
                  - Devices
                  - Device
                  - Identifiers
                  - Latest
                  - Lists
                  - Geofences
                  - Glyphs
                  - Fonts
                  - Stack
                  - Unicode
                  - Ranges
                  - Sprites
                  - File
                  - Styles
                  - Descriptions
                  - Tiles
                  - Places
                  - Resources
                  - Search
                  - Positions
                  - Suggestions
                  - Te
    overlays:
      - type: APIs.io Search
        url: overlays/location-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/location-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:location
  - name: route53
    description: "<p>Amazon Route\_53 is a highly available and scalable Domain Name System (DNS) web service.</p> <p>You can use Route\_53 to:</p> <ul> <li> <p>Register domain names.</p> <p>For more information, see <a href=\"https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/welcome-domain-registration.html\">How domain registration works</a>.</p> </li> <li> <p>Route internet traffic to the resources for your domain</p> <p>For more information, see <a href=\"https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/welcome-dns-service.html\">How internet traffic is routed to your website or web application</a>.</p> </li> <li> <p>Check the health of your resources.</p> <p>For more information, see <a href=\"https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/welcome-health-checks.html\">How Route\_53 checks the health of your resources</a>.</p> </li> </ul>"
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
            title: route53
          paths:
            /2013-04-01/keysigningkey/{HostedZoneId}/{Name}/activate:
              POST:
                summary: ActivateKeySigningKey
                description: >-
                  <p>Activates a key-signing key (KSK) so that it can be used
                  for signing by DNSSEC. This operation changes the KSK status
                  to <code>ACTIVE</code>.</p>
                tags:
                  - Activate
                  - Keys
                  - Signing
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
            /2013-04-01/hostedzone/{Id}/associatevpc:
              POST:
                summary: AssociateVPCWithHostedZone
                description: >-
                  <p>Associates an Amazon VPC with a private hosted zone. </p>
                  <important> <p>To perform the association, the VPC and the
                  private hosted zone must already exist. You can't convert a
                  public hosted zone into a private hosted zone.</p>
                  </important> <note> <p>If you want to associate a VPC that was
                  created by using one Amazon Web Services account with a
                  private hosted zone that was created by using a different
                  account, the Amazon Web Services account that created the
                  private hosted zone must first submit a
                  <code>CreateVPCAssociationAuthorization</code> request. Then
                  the account that created the VPC must submit an
                  <code>AssociateVPCWithHostedZone</code> request.</p> </note>
                  <note> <p>When granting access, the hosted zone and the Amazon
                  VPC must belong to the same partition. A partition is a group
                  of Amazon Web Services Regions. Each Amazon Web Services
                  account is scoped to one partition.</p> <p>The following are
                  the supported partitions:</p> <ul> <li> <p> <code>aws</code> -
                  Amazon Web Services Regions</p> </li> <li> <p>
                  <code>aws-cn</code> - China Regions</p> </li> <li> <p>
                  <code>aws-us-gov</code> - Amazon Web Services GovCloud (US)
                  Region</p> </li> </ul> <p>For more information, see <a
                  href="https://docs.aws.amazon.com/general/latest/gr/aws-arns-and-namespaces.html">Access
                  Management</a> in the <i>Amazon Web Services General
                  Reference</i>.</p> </note>
                tags:
                  - Associate
                  - With
                  - Hosted
                  - Zones
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
            /2013-04-01/cidrcollection/{CidrCollectionId}:
              GET:
                summary: ListCidrLocations
                description: >-
                  <p>Returns a paginated list of CIDR locations for the given
                  collection (metadata only, does not include CIDR blocks).</p>
                tags:
                  - Lists
                  - CIDR
                  - Locations
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
            /2013-04-01/hostedzone/{Id}/rrset/:
              POST:
                summary: ChangeResourceRecordSets
                description: >-
                  <p>Creates, changes, or deletes a resource record set, which
                  contains authoritative DNS information for a specified domain
                  name or subdomain name. For example, you can use
                  <code>ChangeResourceRecordSets</code> to create a resource
                  record set that routes traffic for test.example.com to a web
                  server that has an IP address of 192.0.2.44.</p> <p>
                  <b>Deleting Resource Record Sets</b> </p> <p>To delete a
                  resource record set, you must specify all the same values that
                  you specified when you created it.</p> <p> <b>Change Batches
                  and Transactional Changes</b> </p> <p>The request body must
                  include a document with a
                  <code>ChangeResourceRecordSetsRequest</code> element. The
                  request body contains a list of change items, known as a
                  change batch. Change batches are considered transactional
                  changes. Route 53 validates the changes in the request and
                  then either makes all or none of the changes in the change
                  batch request. This ensures that DNS routing isn't adversely
                  affected by partial changes to the resource record sets in a
                  hosted zone. </p> <p>For example, suppose a change batch
                  request contains two changes: it deletes the
                  <code>CNAME</code> resource record set for www.example.com and
                  creates an alias resource record set for www.example.com. If
                  validation for both records succeeds, Route 53 deletes the
                  first resource record set and creates the second resource
                  record set in a single operation. If validation for either the
                  <code>DELETE</code> or the <code>CREATE</code> action fails,
                  then the request is canceled, and the original
                  <code>CNAME</code> record continues to exist.</p> <note> <p>If
                  you try to delete the same resource record set more than once
                  in a single change batch, Route 53 returns an
                  <code>InvalidChangeBatch</code> error.</p> </note> <p>
                  <b>Traffic Flow</b> </p> <p>To create resource record sets for
                  complex routing configurations, use either the traffic flow
                  visual editor in the Route 53 console or the API actions for
                  traffic policies and traffic policy instances. Save the
                  configuration as a traffic policy, then associate the traffic
                  policy with one or more domain names (such as example.com) or
                  subdomain names (such as www.example.com), in the same hosted
                  zone or in multiple hosted zones. You can roll back the
                  updates if the new configuration isn't performing as expected.
                  For more information, see <a
                  href="https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/traffic-flow.html">Using
                  Traffic Flow to Route DNS Traffic</a> in the <i>Amazon Route
                  53 Developer Guide</i>.</p> <p> <b>Create, Delete, and
                  Upsert</b> </p> <p>Use
                  <code>ChangeResourceRecordsSetsRequest</code> to perform the
                  following actions:</p> <ul> <li> <p> <code>CREATE</code>:
                  Creates a resource record set that has the specified
                  values.</p> </li> <li> <p> <code>DELETE</code>: Deletes an
                  existing resource record set that has the specified
                  values.</p> </li> <li> <p> <code>UPSERT</code>: If a resource
                  set doesn't exist, Route 53 creates it. If a resource set
                  exists Route 53 updates it with the values in the request.
                  </p> </li> </ul> <p> <b>Syntaxes for Creating, Updating, and
                  Deleting Resource Record Sets</b> </p> <p>The syntax for a
                  request depends on the type of resource record set that you
                  want to create, delete, or update, such as weighted, alias, or
                  failover. The XML elements in your request must appear in the
                  order listed in the syntax. </p> <p>For an example for each
                  type of resource record set, see "Examples."</p> <p>Don't
                  refer to the syntax in the "Parameter Syntax" section, which
                  includes all of the elements for every kind of resource record
                  set that you can create, delete, or update by using
                  <code>ChangeResourceRecordSets</code>. </p> <p> <b>Change
                  Propagation to Route 53 DNS Servers</b> </p> <p>When you
                  submit a <code>ChangeResourceRecordSets</code> request, Route
                  53 propagates your changes to all of the Route 53
                  authoritative DNS servers managing the hosted zone. While your
                  changes are propagating, <code>GetChange</code> returns a
                  status of <code>PENDING</code>. When propagation is complete,
                  <code>GetChange</code> returns a status of
                  <code>INSYNC</code>. Changes generally propagate to all Route
                  53 name servers managing the hosted zone within 60 seconds.
                  For more information, see <a
                  href="https://docs.aws.amazon.com/Route53/latest/APIReference/API_GetChange.html">GetChange</a>.</p>
                  <p> <b>Limits on ChangeResourceRecordSets Requests</b> </p>
                  <p>For information about the limits on a
                  <code>ChangeResourceRecordSets</code> request, see <a
                  href="https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/DNSLimitations.html">Limits</a>
                  in the <i>Amazon Route 53 Developer Guide</i>.</p>
                tags:
                  - Change
                  - Resources
                  - Record
                  - Sets
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
            /2013-04-01/tags/{ResourceType}/{ResourceId}:
              GET:
                summary: ListTagsForResource
                description: >-
                  <p>Lists tags for one health check or hosted zone. </p> <p>For
                  information about using tags for cost allocation, see <a
                  href="https://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/cost-alloc-tags.html">Using
                  Cost Allocation Tags</a> in the <i>Billing and Cost Management
                  User Guide</i>.</p>
                tags:
                  - Lists
                  - Tags
                  - For
                  - Resources
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
            /2013-04-01/cidrcollection:
              GET:
                summary: ListCidrCollections
                description: >-
                  <p>Returns a paginated list of CIDR collections in the Amazon
                  Web Services account (metadata only).</p>
                tags:
                  - Lists
                  - CIDR
                  - Collections
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
            /2013-04-01/healthcheck:
              GET:
                summary: ListHealthChecks
                description: >-
                  <p>Retrieve a list of the health checks that are associated
                  with the current Amazon Web Services account. </p>
                tags:
                  - Lists
                  - Health
                  - Checks
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
                  - Health Check
            /2013-04-01/hostedzone:
              GET:
                summary: ListHostedZones
                description: >-
                  <p>Retrieves a list of the public and private hosted zones
                  that are associated with the current Amazon Web Services
                  account. The response includes a <code>HostedZones</code>
                  child element for each hosted zone.</p> <p>Amazon Route 53
                  returns a maximum of 100 items in each response. If you have a
                  lot of hosted zones, you can use the <code>maxitems</code>
                  parameter to list them in groups of up to 100.</p>
                tags:
                  - Lists
                  - Hosted
                  - Zones
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
                  - Health Check
                  - Hosted Zones
            /2013-04-01/keysigningkey:
              POST:
                summary: CreateKeySigningKey
                description: >-
                  <p>Creates a new key-signing key (KSK) associated with a
                  hosted zone. You can only have two KSKs per hosted zone.</p>
                tags:
                  - Create
                  - Keys
                  - Signing
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
                  - Health Check
                  - Hosted Zones
                  - Key Signing
            /2013-04-01/queryloggingconfig:
              GET:
                summary: ListQueryLoggingConfigs
                description: >-
                  <p>Lists the configurations for DNS query logging that are
                  associated with the current Amazon Web Services account or the
                  configuration that is associated with a specified hosted
                  zone.</p> <p>For more information about DNS query logs, see <a
                  href="https://docs.aws.amazon.com/Route53/latest/APIReference/API_CreateQueryLoggingConfig.html">CreateQueryLoggingConfig</a>.
                  Additional information, including the format of DNS query
                  logs, appears in <a
                  href="https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/query-logs.html">Logging
                  DNS Queries</a> in the <i>Amazon Route 53 Developer
                  Guide</i>.</p>
                tags:
                  - Lists
                  - Queries
                  - Logging
                  - Configurations
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
                  - Health Check
                  - Hosted Zones
                  - Key Signing
                  - Query Logging Configurations
            /2013-04-01/delegationset:
              GET:
                summary: ListReusableDelegationSets
                description: >-
                  <p>Retrieves a list of the reusable delegation sets that are
                  associated with the current Amazon Web Services account.</p>
                tags:
                  - Lists
                  - Reusable
                  - Delegation
                  - Sets
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
                  - Health Check
                  - Hosted Zones
                  - Key Signing
                  - Query Logging Configurations
                  - Delegation Sets
            /2013-04-01/trafficpolicy:
              POST:
                summary: CreateTrafficPolicy
                description: >-
                  <p>Creates a traffic policy, which you use to create multiple
                  DNS resource record sets for one domain name (such as
                  example.com) or one subdomain name (such as
                  www.example.com).</p>
                tags:
                  - Create
                  - Traffic
                  - Policies
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
                  - Health Check
                  - Hosted Zones
                  - Key Signing
                  - Query Logging Configurations
                  - Delegation Sets
                  - Traffic Policies
            /2013-04-01/trafficpolicyinstance:
              POST:
                summary: CreateTrafficPolicyInstance
                description: >-
                  <p>Creates resource record sets in a specified hosted zone
                  based on the settings in a specified traffic policy version.
                  In addition, <code>CreateTrafficPolicyInstance</code>
                  associates the resource record sets with a specified domain
                  name (such as example.com) or subdomain name (such as
                  www.example.com). Amazon Route 53 responds to DNS queries for
                  the domain or subdomain name by using the resource record sets
                  that <code>CreateTrafficPolicyInstance</code> created.</p>
                  <note> <p>After you submit an
                  <code>CreateTrafficPolicyInstance</code> request, there's a
                  brief delay while Amazon Route 53 creates the resource record
                  sets that are specified in the traffic policy definition. Use
                  <code>GetTrafficPolicyInstance</code> with the <code>id</code>
                  of new traffic policy instance to confirm that the
                  <code>CreateTrafficPolicyInstance</code> request completed
                  successfully. For more information, see the <code>State</code>
                  response element.</p> </note>
                tags:
                  - Create
                  - Traffic
                  - Policies
                  - Instances
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
                  - Health Check
                  - Hosted Zones
                  - Key Signing
                  - Query Logging Configurations
                  - Delegation Sets
                  - Traffic Policies
                  - Traffic Policy Instances
            /2013-04-01/trafficpolicy/{Id}:
              POST:
                summary: CreateTrafficPolicyVersion
                description: >-
                  <p>Creates a new version of an existing traffic policy. When
                  you create a new version of a traffic policy, you specify the
                  ID of the traffic policy that you want to update and a
                  JSON-formatted document that describes the new version. You
                  use traffic policies to create multiple DNS resource record
                  sets for one domain name (such as example.com) or one
                  subdomain name (such as www.example.com). You can create a
                  maximum of 1000 versions of a traffic policy. If you reach the
                  limit and need to create another version, you'll need to start
                  a new traffic policy.</p>
                tags:
                  - Create
                  - Traffic
                  - Policies
                  - Versions
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
                  - Health Check
                  - Hosted Zones
                  - Key Signing
                  - Query Logging Configurations
                  - Delegation Sets
                  - Traffic Policies
                  - Traffic Policy Instances
            /2013-04-01/hostedzone/{Id}/authorizevpcassociation:
              GET:
                summary: ListVPCAssociationAuthorizations
                description: >-
                  <p>Gets a list of the VPCs that were created by other accounts
                  and that can be associated with a specified hosted zone
                  because you've submitted one or more
                  <code>CreateVPCAssociationAuthorization</code> requests. </p>
                  <p>The response includes a <code>VPCs</code> element with a
                  <code>VPC</code> child element for each VPC that can be
                  associated with the hosted zone.</p>
                tags:
                  - Lists
                  - Association
                  - Authorization
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
                  - Health Check
                  - Hosted Zones
                  - Key Signing
                  - Query Logging Configurations
                  - Delegation Sets
                  - Traffic Policies
                  - Traffic Policy Instances
                  - Authorizers VPC Association
            /2013-04-01/keysigningkey/{HostedZoneId}/{Name}/deactivate:
              POST:
                summary: DeactivateKeySigningKey
                description: >-
                  <p>Deactivates a key-signing key (KSK) so that it will not be
                  used for signing by DNSSEC. This operation changes the KSK
                  status to <code>INACTIVE</code>.</p>
                tags:
                  - Deactivate
                  - Keys
                  - Signing
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
                  - Health Check
                  - Hosted Zones
                  - Key Signing
                  - Query Logging Configurations
                  - Delegation Sets
                  - Traffic Policies
                  - Traffic Policy Instances
                  - Authorizers VPC Association
                  - Deactivate
            /2013-04-01/healthcheck/{HealthCheckId}:
              POST:
                summary: UpdateHealthCheck
                description: >-
                  <p>Updates an existing health check. Note that some values
                  can't be updated. </p> <p>For more information about updating
                  health checks, see <a
                  href="https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/health-checks-creating-deleting.html">Creating,
                  Updating, and Deleting Health Checks</a> in the <i>Amazon
                  Route 53 Developer Guide</i>.</p>
                tags:
                  - Update
                  - Health
                  - Checks
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
                  - Health Check
                  - Hosted Zones
                  - Key Signing
                  - Query Logging Configurations
                  - Delegation Sets
                  - Traffic Policies
                  - Traffic Policy Instances
                  - Authorizers VPC Association
                  - Deactivate
                  - Health
                  - Checks
            /2013-04-01/hostedzone/{Id}:
              POST:
                summary: UpdateHostedZoneComment
                description: <p>Updates the comment for a specified hosted zone.</p>
                tags:
                  - Update
                  - Hosted
                  - Zones
                  - Comments
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
                  - Health Check
                  - Hosted Zones
                  - Key Signing
                  - Query Logging Configurations
                  - Delegation Sets
                  - Traffic Policies
                  - Traffic Policy Instances
                  - Authorizers VPC Association
                  - Deactivate
                  - Health
                  - Checks
            /2013-04-01/keysigningkey/{HostedZoneId}/{Name}:
              DELETE:
                summary: DeleteKeySigningKey
                description: >-
                  <p>Deletes a key-signing key (KSK). Before you can delete a
                  KSK, you must deactivate it. The KSK must be deactivated
                  before you can delete it regardless of whether the hosted zone
                  is enabled for DNSSEC signing.</p> <p>You can use <a
                  href="https://docs.aws.amazon.com/Route53/latest/APIReference/API_DeactivateKeySigningKey.html">DeactivateKeySigningKey</a>
                  to deactivate the key before you delete it.</p> <p>Use <a
                  href="https://docs.aws.amazon.com/Route53/latest/APIReference/API_GetDNSSEC.html">GetDNSSEC</a>
                  to verify that the KSK is in an <code>INACTIVE</code>
                  status.</p>
                tags:
                  - Delete
                  - Keys
                  - Signing
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
                  - Health Check
                  - Hosted Zones
                  - Key Signing
                  - Query Logging Configurations
                  - Delegation Sets
                  - Traffic Policies
                  - Traffic Policy Instances
                  - Authorizers VPC Association
                  - Deactivate
                  - Health
                  - Checks
            /2013-04-01/queryloggingconfig/{Id}:
              GET:
                summary: GetQueryLoggingConfig
                description: >-
                  <p>Gets information about a specified configuration for DNS
                  query logging.</p> <p>For more information about DNS query
                  logs, see <a
                  href="https://docs.aws.amazon.com/Route53/latest/APIReference/API_CreateQueryLoggingConfig.html">CreateQueryLoggingConfig</a>
                  and <a
                  href="https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/query-logs.html">Logging
                  DNS Queries</a>.</p>
                tags:
                  - Get
                  - Queries
                  - Logging
                  - Configurations
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
                  - Health Check
                  - Hosted Zones
                  - Key Signing
                  - Query Logging Configurations
                  - Delegation Sets
                  - Traffic Policies
                  - Traffic Policy Instances
                  - Authorizers VPC Association
                  - Deactivate
                  - Health
                  - Checks
            /2013-04-01/delegationset/{Id}:
              GET:
                summary: GetReusableDelegationSet
                description: >-
                  <p>Retrieves information about a specified reusable delegation
                  set, including the four name servers that are assigned to the
                  delegation set.</p>
                tags:
                  - Get
                  - Reusable
                  - Delegation
                  - Sets
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
                  - Health Check
                  - Hosted Zones
                  - Key Signing
                  - Query Logging Configurations
                  - Delegation Sets
                  - Traffic Policies
                  - Traffic Policy Instances
                  - Authorizers VPC Association
                  - Deactivate
                  - Health
                  - Checks
            /2013-04-01/trafficpolicy/{Id}/{Version}:
              POST:
                summary: UpdateTrafficPolicyComment
                description: >-
                  <p>Updates the comment for a specified traffic policy
                  version.</p>
                tags:
                  - Update
                  - Traffic
                  - Policies
                  - Comments
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
                  - Health Check
                  - Hosted Zones
                  - Key Signing
                  - Query Logging Configurations
                  - Delegation Sets
                  - Traffic Policies
                  - Traffic Policy Instances
                  - Authorizers VPC Association
                  - Deactivate
                  - Health
                  - Checks
                  - Versions
            /2013-04-01/trafficpolicyinstance/{Id}:
              POST:
                summary: UpdateTrafficPolicyInstance
                description: "<note> <p>After you submit a <code>UpdateTrafficPolicyInstance</code> request, there's a brief delay while Route\_53 creates the resource record sets that are specified in the traffic policy definition. Use <code>GetTrafficPolicyInstance</code> with the <code>id</code> of updated traffic policy instance confirm that the <code>UpdateTrafficPolicyInstance</code> request completed successfully. For more information, see the <code>State</code> response element.</p> </note> <p>Updates the resource record sets in a specified hosted zone that were created based on the settings in a specified traffic policy version.</p> <p>When you update a traffic policy instance, Amazon Route 53 continues to respond to DNS queries for the root resource record set name (such as example.com) while it replaces one group of resource record sets with another. Route 53 performs the following operations:</p> <ol> <li> <p>Route 53 creates a new group of resource record sets based on the specified traffic policy. This is true regardless of how significant the differences are between the existing resource record sets and the new resource record sets. </p> </li> <li> <p>When all of the new resource record sets have been created, Route 53 starts to respond to DNS queries for the root resource record set name (such as example.com) by using the new resource record sets.</p> </li> <li> <p>Route 53 deletes the old group of resource record sets that are associated with the root resource record set name.</p> </li> </ol>"
                tags:
                  - Update
                  - Traffic
                  - Policies
                  - Instances
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
                  - Health Check
                  - Hosted Zones
                  - Key Signing
                  - Query Logging Configurations
                  - Delegation Sets
                  - Traffic Policies
                  - Traffic Policy Instances
                  - Authorizers VPC Association
                  - Deactivate
                  - Health
                  - Checks
                  - Versions
            /2013-04-01/hostedzone/{Id}/deauthorizevpcassociation:
              POST:
                summary: DeleteVPCAssociationAuthorization
                description: >-
                  <p>Removes authorization to submit an
                  <code>AssociateVPCWithHostedZone</code> request to associate a
                  specified VPC with a hosted zone that was created by a
                  different account. You must use the account that created the
                  hosted zone to submit a
                  <code>DeleteVPCAssociationAuthorization</code> request.</p>
                  <important> <p>Sending this request only prevents the Amazon
                  Web Services account that created the VPC from associating the
                  VPC with the Amazon Route 53 hosted zone in the future. If the
                  VPC is already associated with the hosted zone,
                  <code>DeleteVPCAssociationAuthorization</code> won't
                  disassociate the VPC from the hosted zone. If you want to
                  delete an existing association, use
                  <code>DisassociateVPCFromHostedZone</code>.</p> </important>
                tags:
                  - Delete
                  - Association
                  - Authorization
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
                  - Health Check
                  - Hosted Zones
                  - Key Signing
                  - Query Logging Configurations
                  - Delegation Sets
                  - Traffic Policies
                  - Traffic Policy Instances
                  - Authorizers VPC Association
                  - Deactivate
                  - Health
                  - Checks
                  - Versions
                  - Deauthorize VPC Association
            /2013-04-01/hostedzone/{Id}/disable-dnssec:
              POST:
                summary: DisableHostedZoneDNSSEC
                description: >-
                  <p>Disables DNSSEC signing in a specific hosted zone. This
                  action does not deactivate any key-signing keys (KSKs) that
                  are active in the hosted zone.</p>
                tags:
                  - Disable
                  - Hosted
                  - Zones
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
                  - Health Check
                  - Hosted Zones
                  - Key Signing
                  - Query Logging Configurations
                  - Delegation Sets
                  - Traffic Policies
                  - Traffic Policy Instances
                  - Authorizers VPC Association
                  - Deactivate
                  - Health
                  - Checks
                  - Versions
                  - Deauthorize VPC Association
                  - Disable
                  - DNS Security
            /2013-04-01/hostedzone/{Id}/disassociatevpc:
              POST:
                summary: DisassociateVPCFromHostedZone
                description: >-
                  <p>Disassociates an Amazon Virtual Private Cloud (Amazon VPC)
                  from an Amazon Route 53 private hosted zone. Note the
                  following:</p> <ul> <li> <p>You can't disassociate the last
                  Amazon VPC from a private hosted zone.</p> </li> <li> <p>You
                  can't convert a private hosted zone into a public hosted
                  zone.</p> </li> <li> <p>You can submit a
                  <code>DisassociateVPCFromHostedZone</code> request using
                  either the account that created the hosted zone or the account
                  that created the Amazon VPC.</p> </li> <li> <p>Some services,
                  such as Cloud Map and Amazon Elastic File System (Amazon EFS)
                  automatically create hosted zones and associate VPCs with the
                  hosted zones. A service can create a hosted zone using your
                  account or using its own account. You can disassociate a VPC
                  from a hosted zone only if the service created the hosted zone
                  using your account.</p> <p>When you run <a
                  href="https://docs.aws.amazon.com/Route53/latest/APIReference/API_ListHostedZonesByVPC.html">DisassociateVPCFromHostedZone</a>,
                  if the hosted zone has a value for <code>OwningAccount</code>,
                  you can use <code>DisassociateVPCFromHostedZone</code>. If the
                  hosted zone has a value for <code>OwningService</code>, you
                  can't use <code>DisassociateVPCFromHostedZone</code>.</p>
                  </li> </ul> <note> <p>When revoking access, the hosted zone
                  and the Amazon VPC must belong to the same partition. A
                  partition is a group of Amazon Web Services Regions. Each
                  Amazon Web Services account is scoped to one partition.</p>
                  <p>The following are the supported partitions:</p> <ul> <li>
                  <p> <code>aws</code> - Amazon Web Services Regions</p> </li>
                  <li> <p> <code>aws-cn</code> - China Regions</p> </li> <li>
                  <p> <code>aws-us-gov</code> - Amazon Web Services GovCloud
                  (US) Region</p> </li> </ul> <p>For more information, see <a
                  href="https://docs.aws.amazon.com/general/latest/gr/aws-arns-and-namespaces.html">Access
                  Management</a> in the <i>Amazon Web Services General
                  Reference</i>.</p> </note>
                tags:
                  - Disassociate
                  - From
                  - Hosted
                  - Zones
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
                  - Health Check
                  - Hosted Zones
                  - Key Signing
                  - Query Logging Configurations
                  - Delegation Sets
                  - Traffic Policies
                  - Traffic Policy Instances
                  - Authorizers VPC Association
                  - Deactivate
                  - Health
                  - Checks
                  - Versions
                  - Deauthorize VPC Association
                  - Disable
                  - DNS Security
                  - Disassociate VPC
            /2013-04-01/hostedzone/{Id}/enable-dnssec:
              POST:
                summary: EnableHostedZoneDNSSEC
                description: <p>Enables DNSSEC signing in a specific hosted zone.</p>
                tags:
                  - Enable
                  - Hosted
                  - Zones
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
                  - Health Check
                  - Hosted Zones
                  - Key Signing
                  - Query Logging Configurations
                  - Delegation Sets
                  - Traffic Policies
                  - Traffic Policy Instances
                  - Authorizers VPC Association
                  - Deactivate
                  - Health
                  - Checks
                  - Versions
                  - Deauthorize VPC Association
                  - Disable
                  - DNS Security
                  - Disassociate VPC
                  - Enable
            /2013-04-01/accountlimit/{Type}:
              GET:
                summary: GetAccountLimit
                description: >-
                  <p>Gets the specified limit for the current account, for
                  example, the maximum number of health checks that you can
                  create using the account.</p> <p>For the default limit, see <a
                  href="https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/DNSLimitations.html">Limits</a>
                  in the <i>Amazon Route 53 Developer Guide</i>. To request a
                  higher limit, <a
                  href="https://console.aws.amazon.com/support/home#/case/create?issueType=service-limit-increase&amp;limitType=service-code-route53">open
                  a case</a>.</p> <note> <p>You can also view account limits in
                  Amazon Web Services Trusted Advisor. Sign in to the Amazon Web
                  Services Management Console and open the Trusted Advisor
                  console at <a
                  href="https://console.aws.amazon.com/trustedadvisor">https://console.aws.amazon.com/trustedadvisor/</a>.
                  Then choose <b>Service limits</b> in the navigation pane.</p>
                  </note>
                tags:
                  - Get
                  - Account
                  - Limits
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
                  - Health Check
                  - Hosted Zones
                  - Key Signing
                  - Query Logging Configurations
                  - Delegation Sets
                  - Traffic Policies
                  - Traffic Policy Instances
                  - Authorizers VPC Association
                  - Deactivate
                  - Health
                  - Checks
                  - Versions
                  - Deauthorize VPC Association
                  - Disable
                  - DNS Security
                  - Disassociate VPC
                  - Enable
            /2013-04-01/change/{Id}:
              GET:
                summary: GetChange
                description: >-
                  <p>Returns the current status of a change batch request. The
                  status is one of the following values:</p> <ul> <li> <p>
                  <code>PENDING</code> indicates that the changes in this
                  request have not propagated to all Amazon Route 53 DNS servers
                  managing the hosted zone. This is the initial status of all
                  change batch requests.</p> </li> <li> <p> <code>INSYNC</code>
                  indicates that the changes have propagated to all Route 53 DNS
                  servers managing the hosted zone. </p> </li> </ul>
                tags:
                  - Get
                  - Change
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
                  - Health Check
                  - Hosted Zones
                  - Key Signing
                  - Query Logging Configurations
                  - Delegation Sets
                  - Traffic Policies
                  - Traffic Policy Instances
                  - Authorizers VPC Association
                  - Deactivate
                  - Health
                  - Checks
                  - Versions
                  - Deauthorize VPC Association
                  - Disable
                  - DNS Security
                  - Disassociate VPC
                  - Enable
            /2013-04-01/checkeripranges:
              GET:
                summary: GetCheckerIpRanges
                description: >-
                  <p>Route 53 does not perform authorization for this API
                  because it retrieves information that is already available to
                  the public.</p> <important> <p>
                  <code>GetCheckerIpRanges</code> still works, but we recommend
                  that you download ip-ranges.json, which includes IP address
                  ranges for all Amazon Web Services services. For more
                  information, see <a
                  href="https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/route-53-ip-addresses.html">IP
                  Address Ranges of Amazon Route 53 Servers</a> in the <i>Amazon
                  Route 53 Developer Guide</i>.</p> </important>
                tags:
                  - Get
                  - Checker
                  - IP
                  - Ranges
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
                  - Health Check
                  - Hosted Zones
                  - Key Signing
                  - Query Logging Configurations
                  - Delegation Sets
                  - Traffic Policies
                  - Traffic Policy Instances
                  - Authorizers VPC Association
                  - Deactivate
                  - Health
                  - Checks
                  - Versions
                  - Deauthorize VPC Association
                  - Disable
                  - DNS Security
                  - Disassociate VPC
                  - Enable
                  - Checker IP Ranges
            /2013-04-01/hostedzone/{Id}/dnssec:
              GET:
                summary: GetDNSSEC
                description: >-
                  <p>Returns information about DNSSEC for a specific hosted
                  zone, including the key-signing keys (KSKs) in the hosted
                  zone.</p>
                tags:
                  - Get
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
                  - Health Check
                  - Hosted Zones
                  - Key Signing
                  - Query Logging Configurations
                  - Delegation Sets
                  - Traffic Policies
                  - Traffic Policy Instances
                  - Authorizers VPC Association
                  - Deactivate
                  - Health
                  - Checks
                  - Versions
                  - Deauthorize VPC Association
                  - Disable
                  - DNS Security
                  - Disassociate VPC
                  - Enable
                  - Checker IP Ranges
            /2013-04-01/geolocation:
              GET:
                summary: GetGeoLocation
                description: >-
                  <p>Gets information about whether a specified geographic
                  location is supported for Amazon Route 53 geolocation resource
                  record sets.</p> <p>Route 53 does not perform authorization
                  for this API because it retrieves information that is already
                  available to the public.</p> <p>Use the following syntax to
                  determine whether a continent is supported for
                  geolocation:</p> <p> <code>GET
                  /2013-04-01/geolocation?continentcode=<i>two-letter
                  abbreviation for a continent</i> </code> </p> <p>Use the
                  following syntax to determine whether a country is supported
                  for geolocation:</p> <p> <code>GET
                  /2013-04-01/geolocation?countrycode=<i>two-character country
                  code</i> </code> </p> <p>Use the following syntax to determine
                  whether a subdivision of a country is supported for
                  geolocation:</p> <p> <code>GET
                  /2013-04-01/geolocation?countrycode=<i>two-character country
                  code</i>&amp;subdivisioncode=<i>subdivision code</i> </code>
                  </p>
                tags:
                  - Get
                  - Geo
                  - Locations
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
                  - Health Check
                  - Hosted Zones
                  - Key Signing
                  - Query Logging Configurations
                  - Delegation Sets
                  - Traffic Policies
                  - Traffic Policy Instances
                  - Authorizers VPC Association
                  - Deactivate
                  - Health
                  - Checks
                  - Versions
                  - Deauthorize VPC Association
                  - Disable
                  - DNS Security
                  - Disassociate VPC
                  - Enable
                  - Checker IP Ranges
                  - Geolocation
            /2013-04-01/healthcheckcount:
              GET:
                summary: GetHealthCheckCount
                description: >-
                  <p>Retrieves the number of health checks that are associated
                  with the current Amazon Web Services account.</p>
                tags:
                  - Get
                  - Health
                  - Checks
                  - Count
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
                  - Health Check
                  - Hosted Zones
                  - Key Signing
                  - Query Logging Configurations
                  - Delegation Sets
                  - Traffic Policies
                  - Traffic Policy Instances
                  - Authorizers VPC Association
                  - Deactivate
                  - Health
                  - Checks
                  - Versions
                  - Deauthorize VPC Association
                  - Disable
                  - DNS Security
                  - Disassociate VPC
                  - Enable
                  - Checker IP Ranges
                  - Geolocation
                  - Health Check
            /2013-04-01/healthcheck/{HealthCheckId}/lastfailurereason:
              GET:
                summary: GetHealthCheckLastFailureReason
                description: >-
                  <p>Gets the reason that a specified health check failed most
                  recently.</p>
                tags:
                  - Get
                  - Health
                  - Checks
                  - Last
                  - Failure
                  - Reasons
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
                  - Health Check
                  - Hosted Zones
                  - Key Signing
                  - Query Logging Configurations
                  - Delegation Sets
                  - Traffic Policies
                  - Traffic Policy Instances
                  - Authorizers VPC Association
                  - Deactivate
                  - Health
                  - Checks
                  - Versions
                  - Deauthorize VPC Association
                  - Disable
                  - DNS Security
                  - Disassociate VPC
                  - Enable
                  - Checker IP Ranges
                  - Geolocation
                  - Health Check
                  - Last Failure Reasons
            /2013-04-01/healthcheck/{HealthCheckId}/status:
              GET:
                summary: GetHealthCheckStatus
                description: >-
                  <p>Gets status of a specified health check. </p> <important>
                  <p>This API is intended for use during development to diagnose
                  behavior. It doesn’t support production use-cases with high
                  query rates that require immediate and actionable
                  responses.</p> </important>
                tags:
                  - Get
                  - Health
                  - Checks
                  - Status
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
                  - Health Check
                  - Hosted Zones
                  - Key Signing
                  - Query Logging Configurations
                  - Delegation Sets
                  - Traffic Policies
                  - Traffic Policy Instances
                  - Authorizers VPC Association
                  - Deactivate
                  - Health
                  - Checks
                  - Versions
                  - Deauthorize VPC Association
                  - Disable
                  - DNS Security
                  - Disassociate VPC
                  - Enable
                  - Checker IP Ranges
                  - Geolocation
                  - Health Check
                  - Last Failure Reasons
                  - Status
            /2013-04-01/hostedzonecount:
              GET:
                summary: GetHostedZoneCount
                description: >-
                  <p>Retrieves the number of hosted zones that are associated
                  with the current Amazon Web Services account.</p>
                tags:
                  - Get
                  - Hosted
                  - Zones
                  - Count
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
                  - Health Check
                  - Hosted Zones
                  - Key Signing
                  - Query Logging Configurations
                  - Delegation Sets
                  - Traffic Policies
                  - Traffic Policy Instances
                  - Authorizers VPC Association
                  - Deactivate
                  - Health
                  - Checks
                  - Versions
                  - Deauthorize VPC Association
                  - Disable
                  - DNS Security
                  - Disassociate VPC
                  - Enable
                  - Checker IP Ranges
                  - Geolocation
                  - Health Check
                  - Last Failure Reasons
                  - Status
                  - Hosted Zone Count
            /2013-04-01/hostedzonelimit/{Id}/{Type}:
              GET:
                summary: GetHostedZoneLimit
                description: >-
                  <p>Gets the specified limit for a specified hosted zone, for
                  example, the maximum number of records that you can create in
                  the hosted zone. </p> <p>For the default limit, see <a
                  href="https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/DNSLimitations.html">Limits</a>
                  in the <i>Amazon Route 53 Developer Guide</i>. To request a
                  higher limit, <a
                  href="https://console.aws.amazon.com/support/home#/case/create?issueType=service-limit-increase&amp;limitType=service-code-route53">open
                  a case</a>.</p>
                tags:
                  - Get
                  - Hosted
                  - Zones
                  - Limits
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
                  - Health Check
                  - Hosted Zones
                  - Key Signing
                  - Query Logging Configurations
                  - Delegation Sets
                  - Traffic Policies
                  - Traffic Policy Instances
                  - Authorizers VPC Association
                  - Deactivate
                  - Health
                  - Checks
                  - Versions
                  - Deauthorize VPC Association
                  - Disable
                  - DNS Security
                  - Disassociate VPC
                  - Enable
                  - Checker IP Ranges
                  - Geolocation
                  - Health Check
                  - Last Failure Reasons
                  - Status
                  - Hosted Zone Count
            /2013-04-01/reusabledelegationsetlimit/{Id}/{Type}:
              GET:
                summary: GetReusableDelegationSetLimit
                description: >-
                  <p>Gets the maximum number of hosted zones that you can
                  associate with the specified reusable delegation set.</p>
                  <p>For the default limit, see <a
                  href="https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/DNSLimitations.html">Limits</a>
                  in the <i>Amazon Route 53 Developer Guide</i>. To request a
                  higher limit, <a
                  href="https://console.aws.amazon.com/support/home#/case/create?issueType=service-limit-increase&amp;limitType=service-code-route53">open
                  a case</a>.</p>
                tags:
                  - Get
                  - Reusable
                  - Delegation
                  - Sets
                  - Limits
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
                  - Health Check
                  - Hosted Zones
                  - Key Signing
                  - Query Logging Configurations
                  - Delegation Sets
                  - Traffic Policies
                  - Traffic Policy Instances
                  - Authorizers VPC Association
                  - Deactivate
                  - Health
                  - Checks
                  - Versions
                  - Deauthorize VPC Association
                  - Disable
                  - DNS Security
                  - Disassociate VPC
                  - Enable
                  - Checker IP Ranges
                  - Geolocation
                  - Health Check
                  - Last Failure Reasons
                  - Status
                  - Hosted Zone Count
            /2013-04-01/trafficpolicyinstancecount:
              GET:
                summary: GetTrafficPolicyInstanceCount
                description: >-
                  <p>Gets the number of traffic policy instances that are
                  associated with the current Amazon Web Services account.</p>
                tags:
                  - Get
                  - Traffic
                  - Policies
                  - Instances
                  - Count
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
                  - Health Check
                  - Hosted Zones
                  - Key Signing
                  - Query Logging Configurations
                  - Delegation Sets
                  - Traffic Policies
                  - Traffic Policy Instances
                  - Authorizers VPC Association
                  - Deactivate
                  - Health
                  - Checks
                  - Versions
                  - Deauthorize VPC Association
                  - Disable
                  - DNS Security
                  - Disassociate VPC
                  - Enable
                  - Checker IP Ranges
                  - Geolocation
                  - Health Check
                  - Last Failure Reasons
                  - Status
                  - Hosted Zone Count
                  - Traffic Policy Instance Count
            /2013-04-01/cidrcollection/{CidrCollectionId}/cidrblocks:
              GET:
                summary: ListCidrBlocks
                description: >-
                  <p>Returns a paginated list of location objects and their CIDR
                  blocks.</p>
                tags:
                  - Lists
                  - CIDR
                  - Blocks
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
                  - Health Check
                  - Hosted Zones
                  - Key Signing
                  - Query Logging Configurations
                  - Delegation Sets
                  - Traffic Policies
                  - Traffic Policy Instances
                  - Authorizers VPC Association
                  - Deactivate
                  - Health
                  - Checks
                  - Versions
                  - Deauthorize VPC Association
                  - Disable
                  - DNS Security
                  - Disassociate VPC
                  - Enable
                  - Checker IP Ranges
                  - Geolocation
                  - Health Check
                  - Last Failure Reasons
                  - Status
                  - Hosted Zone Count
                  - Traffic Policy Instance Count
                  - CIDR Blocks
            /2013-04-01/geolocations:
              GET:
                summary: ListGeoLocations
                description: >-
                  <p>Retrieves a list of supported geographic locations.</p>
                  <p>Countries are listed first, and continents are listed last.
                  If Amazon Route 53 supports subdivisions for a country (for
                  example, states or provinces), the subdivisions for that
                  country are listed in alphabetical order immediately after the
                  corresponding country.</p> <p>Route 53 does not perform
                  authorization for this API because it retrieves information
                  that is already available to the public.</p> <p>For a list of
                  supported geolocation codes, see the <a
                  href="https://docs.aws.amazon.com/Route53/latest/APIReference/API_GeoLocation.html">GeoLocation</a>
                  data type.</p>
                tags:
                  - Lists
                  - Geo
                  - Locations
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
                  - Health Check
                  - Hosted Zones
                  - Key Signing
                  - Query Logging Configurations
                  - Delegation Sets
                  - Traffic Policies
                  - Traffic Policy Instances
                  - Authorizers VPC Association
                  - Deactivate
                  - Health
                  - Checks
                  - Versions
                  - Deauthorize VPC Association
                  - Disable
                  - DNS Security
                  - Disassociate VPC
                  - Enable
                  - Checker IP Ranges
                  - Geolocation
                  - Health Check
                  - Last Failure Reasons
                  - Status
                  - Hosted Zone Count
                  - Traffic Policy Instance Count
                  - CIDR Blocks
                  - Geolocation
            /2013-04-01/hostedzonesbyname:
              GET:
                summary: ListHostedZonesByName
                description: >-
                  <p>Retrieves a list of your hosted zones in lexicographic
                  order. The response includes a <code>HostedZones</code> child
                  element for each hosted zone created by the current Amazon Web
                  Services account. </p> <p> <code>ListHostedZonesByName</code>
                  sorts hosted zones by name with the labels reversed. For
                  example:</p> <p> <code>com.example.www.</code> </p> <p>Note
                  the trailing dot, which can change the sort order in some
                  circumstances.</p> <p>If the domain name includes escape
                  characters or Punycode, <code>ListHostedZonesByName</code>
                  alphabetizes the domain name using the escaped or Punycoded
                  value, which is the format that Amazon Route 53 saves in its
                  database. For example, to create a hosted zone for
                  exämple.com, you specify ex\344mple.com for the domain name.
                  <code>ListHostedZonesByName</code> alphabetizes it as:</p> <p>
                  <code>com.ex\344mple.</code> </p> <p>The labels are reversed
                  and alphabetized using the escaped value. For more information
                  about valid domain name formats, including internationalized
                  domain names, see <a
                  href="https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/DomainNameFormat.html">DNS
                  Domain Name Format</a> in the <i>Amazon Route 53 Developer
                  Guide</i>.</p> <p>Route 53 returns up to 100 items in each
                  response. If you have a lot of hosted zones, use the
                  <code>MaxItems</code> parameter to list them in groups of up
                  to 100. The response includes values that help navigate from
                  one group of <code>MaxItems</code> hosted zones to the
                  next:</p> <ul> <li> <p>The <code>DNSName</code> and
                  <code>HostedZoneId</code> elements in the response contain the
                  values, if any, specified for the <code>dnsname</code> and
                  <code>hostedzoneid</code> parameters in the request that
                  produced the current response.</p> </li> <li> <p>The
                  <code>MaxItems</code> element in the response contains the
                  value, if any, that you specified for the
                  <code>maxitems</code> parameter in the request that produced
                  the current response.</p> </li> <li> <p>If the value of
                  <code>IsTruncated</code> in the response is true, there are
                  more hosted zones associated with the current Amazon Web
                  Services account. </p> <p>If <code>IsTruncated</code> is
                  false, this response includes the last hosted zone that is
                  associated with the current account. The
                  <code>NextDNSName</code> element and
                  <code>NextHostedZoneId</code> elements are omitted from the
                  response.</p> </li> <li> <p>The <code>NextDNSName</code> and
                  <code>NextHostedZoneId</code> elements in the response contain
                  the domain name and the hosted zone ID of the next hosted zone
                  that is associated with the current Amazon Web Services
                  account. If you want to list more hosted zones, make another
                  call to <code>ListHostedZonesByName</code>, and specify the
                  value of <code>NextDNSName</code> and
                  <code>NextHostedZoneId</code> in the <code>dnsname</code> and
                  <code>hostedzoneid</code> parameters, respectively.</p> </li>
                  </ul>
                tags:
                  - Lists
                  - Hosted
                  - Zones
                  - By
                  - Names
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
                  - Health Check
                  - Hosted Zones
                  - Key Signing
                  - Query Logging Configurations
                  - Delegation Sets
                  - Traffic Policies
                  - Traffic Policy Instances
                  - Authorizers VPC Association
                  - Deactivate
                  - Health
                  - Checks
                  - Versions
                  - Deauthorize VPC Association
                  - Disable
                  - DNS Security
                  - Disassociate VPC
                  - Enable
                  - Checker IP Ranges
                  - Geolocation
                  - Health Check
                  - Last Failure Reasons
                  - Status
                  - Hosted Zone Count
                  - Traffic Policy Instance Count
                  - CIDR Blocks
                  - Geolocation
                  - Hosted Zones
            /2013-04-01/hostedzonesbyvpc:
              GET:
                summary: ListHostedZonesByVPC
                description: >-
                  <p>Lists all the private hosted zones that a specified VPC is
                  associated with, regardless of which Amazon Web Services
                  account or Amazon Web Services service owns the hosted zones.
                  The <code>HostedZoneOwner</code> structure in the response
                  contains one of the following values:</p> <ul> <li> <p>An
                  <code>OwningAccount</code> element, which contains the account
                  number of either the current Amazon Web Services account or
                  another Amazon Web Services account. Some services, such as
                  Cloud Map, create hosted zones using the current account. </p>
                  </li> <li> <p>An <code>OwningService</code> element, which
                  identifies the Amazon Web Services service that created and
                  owns the hosted zone. For example, if a hosted zone was
                  created by Amazon Elastic File System (Amazon EFS), the value
                  of <code>Owner</code> is <code>efs.amazonaws.com</code>. </p>
                  </li> </ul> <note> <p>When listing private hosted zones, the
                  hosted zone and the Amazon VPC must belong to the same
                  partition where the hosted zones were created. A partition is
                  a group of Amazon Web Services Regions. Each Amazon Web
                  Services account is scoped to one partition.</p> <p>The
                  following are the supported partitions:</p> <ul> <li> <p>
                  <code>aws</code> - Amazon Web Services Regions</p> </li> <li>
                  <p> <code>aws-cn</code> - China Regions</p> </li> <li> <p>
                  <code>aws-us-gov</code> - Amazon Web Services GovCloud (US)
                  Region</p> </li> </ul> <p>For more information, see <a
                  href="https://docs.aws.amazon.com/general/latest/gr/aws-arns-and-namespaces.html">Access
                  Management</a> in the <i>Amazon Web Services General
                  Reference</i>.</p> </note>
                tags:
                  - Lists
                  - Hosted
                  - Zones
                  - By
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
                  - Health Check
                  - Hosted Zones
                  - Key Signing
                  - Query Logging Configurations
                  - Delegation Sets
                  - Traffic Policies
                  - Traffic Policy Instances
                  - Authorizers VPC Association
                  - Deactivate
                  - Health
                  - Checks
                  - Versions
                  - Deauthorize VPC Association
                  - Disable
                  - DNS Security
                  - Disassociate VPC
                  - Enable
                  - Checker IP Ranges
                  - Geolocation
                  - Health Check
                  - Last Failure Reasons
                  - Status
                  - Hosted Zone Count
                  - Traffic Policy Instance Count
                  - CIDR Blocks
                  - Geolocation
                  - Hosted Zones
                  - Hosted Zones
            /2013-04-01/hostedzone/{Id}/rrset:
              GET:
                summary: ListResourceRecordSets
                description: >-
                  <p>Lists the resource record sets in a specified hosted
                  zone.</p> <p> <code>ListResourceRecordSets</code> returns up
                  to 300 resource record sets at a time in ASCII order,
                  beginning at a position specified by the <code>name</code> and
                  <code>type</code> elements.</p> <p> <b>Sort order</b> </p> <p>
                  <code>ListResourceRecordSets</code> sorts results first by DNS
                  name with the labels reversed, for example:</p> <p>
                  <code>com.example.www.</code> </p> <p>Note the trailing dot,
                  which can change the sort order when the record name contains
                  characters that appear before <code>.</code> (decimal 46) in
                  the ASCII table. These characters include the following:
                  <code>! " # $ % &amp; ' ( ) * + , -</code> </p> <p>When
                  multiple records have the same DNS name,
                  <code>ListResourceRecordSets</code> sorts results by the
                  record type.</p> <p> <b>Specifying where to start listing
                  records</b> </p> <p>You can use the name and type elements to
                  specify the resource record set that the list begins with:</p>
                  <dl> <dt>If you do not specify Name or Type</dt> <dd> <p>The
                  results begin with the first resource record set that the
                  hosted zone contains.</p> </dd> <dt>If you specify Name but
                  not Type</dt> <dd> <p>The results begin with the first
                  resource record set in the list whose name is greater than or
                  equal to <code>Name</code>.</p> </dd> <dt>If you specify Type
                  but not Name</dt> <dd> <p>Amazon Route 53 returns the
                  <code>InvalidInput</code> error.</p> </dd> <dt>If you specify
                  both Name and Type</dt> <dd> <p>The results begin with the
                  first resource record set in the list whose name is greater
                  than or equal to <code>Name</code>, and whose type is greater
                  than or equal to <code>Type</code>.</p> </dd> </dl> <p>
                  <b>Resource record sets that are PENDING</b> </p> <p>This
                  action returns the most current version of the records. This
                  includes records that are <code>PENDING</code>, and that are
                  not yet available on all Route 53 DNS servers.</p> <p>
                  <b>Changing resource record sets</b> </p> <p>To ensure that
                  you get an accurate listing of the resource record sets for a
                  hosted zone at a point in time, do not submit a
                  <code>ChangeResourceRecordSets</code> request while you're
                  paging through the results of a
                  <code>ListResourceRecordSets</code> request. If you do, some
                  pages may display results without the latest changes while
                  other pages display results with the latest changes.</p> <p>
                  <b>Displaying the next page of results</b> </p> <p>If a
                  <code>ListResourceRecordSets</code> command returns more than
                  one page of results, the value of <code>IsTruncated</code> is
                  <code>true</code>. To display the next page of results, get
                  the values of <code>NextRecordName</code>,
                  <code>NextRecordType</code>, and
                  <code>NextRecordIdentifier</code> (if any) from the response.
                  Then submit another <code>ListResourceRecordSets</code>
                  request, and specify those values for
                  <code>StartRecordName</code>, <code>StartRecordType</code>,
                  and <code>StartRecordIdentifier</code>.</p>
                tags:
                  - Lists
                  - Resources
                  - Record
                  - Sets
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
                  - Health Check
                  - Hosted Zones
                  - Key Signing
                  - Query Logging Configurations
                  - Delegation Sets
                  - Traffic Policies
                  - Traffic Policy Instances
                  - Authorizers VPC Association
                  - Deactivate
                  - Health
                  - Checks
                  - Versions
                  - Deauthorize VPC Association
                  - Disable
                  - DNS Security
                  - Disassociate VPC
                  - Enable
                  - Checker IP Ranges
                  - Geolocation
                  - Health Check
                  - Last Failure Reasons
                  - Status
                  - Hosted Zone Count
                  - Traffic Policy Instance Count
                  - CIDR Blocks
                  - Geolocation
                  - Hosted Zones
                  - Hosted Zones
            /2013-04-01/tags/{ResourceType}:
              POST:
                summary: ListTagsForResources
                description: >-
                  <p>Lists tags for up to 10 health checks or hosted zones.</p>
                  <p>For information about using tags for cost allocation, see
                  <a
                  href="https://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/cost-alloc-tags.html">Using
                  Cost Allocation Tags</a> in the <i>Billing and Cost Management
                  User Guide</i>.</p>
                tags:
                  - Lists
                  - Tags
                  - For
                  - Resources
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
                  - Health Check
                  - Hosted Zones
                  - Key Signing
                  - Query Logging Configurations
                  - Delegation Sets
                  - Traffic Policies
                  - Traffic Policy Instances
                  - Authorizers VPC Association
                  - Deactivate
                  - Health
                  - Checks
                  - Versions
                  - Deauthorize VPC Association
                  - Disable
                  - DNS Security
                  - Disassociate VPC
                  - Enable
                  - Checker IP Ranges
                  - Geolocation
                  - Health Check
                  - Last Failure Reasons
                  - Status
                  - Hosted Zone Count
                  - Traffic Policy Instance Count
                  - CIDR Blocks
                  - Geolocation
                  - Hosted Zones
                  - Hosted Zones
            /2013-04-01/trafficpolicies:
              GET:
                summary: ListTrafficPolicies
                description: >-
                  <p>Gets information about the latest version for every traffic
                  policy that is associated with the current Amazon Web Services
                  account. Policies are listed in the order that they were
                  created in. </p> <p>For information about how of deleting a
                  traffic policy affects the response from
                  <code>ListTrafficPolicies</code>, see <a
                  href="https://docs.aws.amazon.com/Route53/latest/APIReference/API_DeleteTrafficPolicy.html">DeleteTrafficPolicy</a>.
                  </p>
                tags:
                  - Lists
                  - Traffic
                  - Policies
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
                  - Health Check
                  - Hosted Zones
                  - Key Signing
                  - Query Logging Configurations
                  - Delegation Sets
                  - Traffic Policies
                  - Traffic Policy Instances
                  - Authorizers VPC Association
                  - Deactivate
                  - Health
                  - Checks
                  - Versions
                  - Deauthorize VPC Association
                  - Disable
                  - DNS Security
                  - Disassociate VPC
                  - Enable
                  - Checker IP Ranges
                  - Geolocation
                  - Health Check
                  - Last Failure Reasons
                  - Status
                  - Hosted Zone Count
                  - Traffic Policy Instance Count
                  - CIDR Blocks
                  - Geolocation
                  - Hosted Zones
                  - Hosted Zones
                  - Traffic Policies
            /2013-04-01/trafficpolicyinstances:
              GET:
                summary: ListTrafficPolicyInstances
                description: >-
                  <p>Gets information about the traffic policy instances that
                  you created by using the current Amazon Web Services
                  account.</p> <note> <p>After you submit an
                  <code>UpdateTrafficPolicyInstance</code> request, there's a
                  brief delay while Amazon Route 53 creates the resource record
                  sets that are specified in the traffic policy definition. For
                  more information, see the <code>State</code> response
                  element.</p> </note> <p>Route 53 returns a maximum of 100
                  items in each response. If you have a lot of traffic policy
                  instances, you can use the <code>MaxItems</code> parameter to
                  list them in groups of up to 100.</p>
                tags:
                  - Lists
                  - Traffic
                  - Policies
                  - Instances
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
                  - Health Check
                  - Hosted Zones
                  - Key Signing
                  - Query Logging Configurations
                  - Delegation Sets
                  - Traffic Policies
                  - Traffic Policy Instances
                  - Authorizers VPC Association
                  - Deactivate
                  - Health
                  - Checks
                  - Versions
                  - Deauthorize VPC Association
                  - Disable
                  - DNS Security
                  - Disassociate VPC
                  - Enable
                  - Checker IP Ranges
                  - Geolocation
                  - Health Check
                  - Last Failure Reasons
                  - Status
                  - Hosted Zone Count
                  - Traffic Policy Instance Count
                  - CIDR Blocks
                  - Geolocation
                  - Hosted Zones
                  - Hosted Zones
                  - Traffic Policies
                  - Traffic Policy Instances
            /2013-04-01/trafficpolicyinstances/hostedzone:
              GET:
                summary: ListTrafficPolicyInstancesByHostedZone
                description: >-
                  <p>Gets information about the traffic policy instances that
                  you created in a specified hosted zone.</p> <note> <p>After
                  you submit a <code>CreateTrafficPolicyInstance</code> or an
                  <code>UpdateTrafficPolicyInstance</code> request, there's a
                  brief delay while Amazon Route 53 creates the resource record
                  sets that are specified in the traffic policy definition. For
                  more information, see the <code>State</code> response
                  element.</p> </note> <p>Route 53 returns a maximum of 100
                  items in each response. If you have a lot of traffic policy
                  instances, you can use the <code>MaxItems</code> parameter to
                  list them in groups of up to 100.</p>
                tags:
                  - Lists
                  - Traffic
                  - Policies
                  - Instances
                  - By
                  - Hosted
                  - Zones
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
                  - Health Check
                  - Hosted Zones
                  - Key Signing
                  - Query Logging Configurations
                  - Delegation Sets
                  - Traffic Policies
                  - Traffic Policy Instances
                  - Authorizers VPC Association
                  - Deactivate
                  - Health
                  - Checks
                  - Versions
                  - Deauthorize VPC Association
                  - Disable
                  - DNS Security
                  - Disassociate VPC
                  - Enable
                  - Checker IP Ranges
                  - Geolocation
                  - Health Check
                  - Last Failure Reasons
                  - Status
                  - Hosted Zone Count
                  - Traffic Policy Instance Count
                  - CIDR Blocks
                  - Geolocation
                  - Hosted Zones
                  - Hosted Zones
                  - Traffic Policies
                  - Traffic Policy Instances
            /2013-04-01/trafficpolicyinstances/trafficpolicy:
              GET:
                summary: ListTrafficPolicyInstancesByPolicy
                description: >-
                  <p>Gets information about the traffic policy instances that
                  you created by using a specify traffic policy version.</p>
                  <note> <p>After you submit a
                  <code>CreateTrafficPolicyInstance</code> or an
                  <code>UpdateTrafficPolicyInstance</code> request, there's a
                  brief delay while Amazon Route 53 creates the resource record
                  sets that are specified in the traffic policy definition. For
                  more information, see the <code>State</code> response
                  element.</p> </note> <p>Route 53 returns a maximum of 100
                  items in each response. If you have a lot of traffic policy
                  instances, you can use the <code>MaxItems</code> parameter to
                  list them in groups of up to 100.</p>
                tags:
                  - Lists
                  - Traffic
                  - Policies
                  - Instances
                  - By
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
                  - Health Check
                  - Hosted Zones
                  - Key Signing
                  - Query Logging Configurations
                  - Delegation Sets
                  - Traffic Policies
                  - Traffic Policy Instances
                  - Authorizers VPC Association
                  - Deactivate
                  - Health
                  - Checks
                  - Versions
                  - Deauthorize VPC Association
                  - Disable
                  - DNS Security
                  - Disassociate VPC
                  - Enable
                  - Checker IP Ranges
                  - Geolocation
                  - Health Check
                  - Last Failure Reasons
                  - Status
                  - Hosted Zone Count
                  - Traffic Policy Instance Count
                  - CIDR Blocks
                  - Geolocation
                  - Hosted Zones
                  - Hosted Zones
                  - Traffic Policies
                  - Traffic Policy Instances
            /2013-04-01/trafficpolicies/{Id}/versions:
              GET:
                summary: ListTrafficPolicyVersions
                description: >-
                  <p>Gets information about all of the versions for a specified
                  traffic policy.</p> <p>Traffic policy versions are listed in
                  numerical order by <code>VersionNumber</code>.</p>
                tags:
                  - Lists
                  - Traffic
                  - Policies
                  - Versions
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
                  - Health Check
                  - Hosted Zones
                  - Key Signing
                  - Query Logging Configurations
                  - Delegation Sets
                  - Traffic Policies
                  - Traffic Policy Instances
                  - Authorizers VPC Association
                  - Deactivate
                  - Health
                  - Checks
                  - Versions
                  - Deauthorize VPC Association
                  - Disable
                  - DNS Security
                  - Disassociate VPC
                  - Enable
                  - Checker IP Ranges
                  - Geolocation
                  - Health Check
                  - Last Failure Reasons
                  - Status
                  - Hosted Zone Count
                  - Traffic Policy Instance Count
                  - CIDR Blocks
                  - Geolocation
                  - Hosted Zones
                  - Hosted Zones
                  - Traffic Policies
                  - Traffic Policy Instances
                  - Versions
            /2013-04-01/testdnsanswer:
              GET:
                summary: TestDNSAnswer
                description: >-
                  <p>Gets the value that Amazon Route 53 returns in response to
                  a DNS request for a specified record name and type. You can
                  optionally specify the IP address of a DNS resolver, an EDNS0
                  client subnet IP address, and a subnet mask. </p> <p>This call
                  only supports querying public hosted zones.</p> <note> <p>The
                  <code>TestDnsAnswer </code> returns information similar to
                  what you would expect from the answer section of the
                  <code>dig</code> command. Therefore, if you query for the name
                  servers of a subdomain that point to the parent name servers,
                  those will not be returned.</
                tags:
                  - Tests
                  - Answers
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
                  - Health Check
                  - Hosted Zones
                  - Key Signing
                  - Query Logging Configurations
                  - Delegation Sets
                  - Traffic Policies
                  - Traffic Policy Instances
                  - Authorizers VPC Association
                  - Deactivate
                  - Health
                  - Checks
                  - Versions
                  - Deauthorize VPC Association
                  - Disable
                  - DNS Security
                  - Disassociate VPC
                  - Enable
                  - Checker IP Ranges
                  - Geolocation
                  - Health Check
                  - Last Failure Reasons
                  - Status
                  - Hosted Zone Count
                  - Traffic Policy Instance Count
                  - CIDR Blocks
                  - Geolocation
                  - Hosted Zones
                  - Hosted Zones
                  - Traffic Policies
                  - Traffic Policy Instances
                  - Versions
                  - Testdnsansw
    overlays:
      - type: APIs.io Search
        url: overlays/route53-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/route53-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:route53
  - name: sagemaker-geospatial
    description: >-
      <p>Provides APIs for creating and managing SageMaker geospatial
      resources.</p>
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
            title: sagemaker-geospatial
          paths:
            /earth-observation-jobs/{Arn}:
              GET:
                summary: GetEarthObservationJob
                description: >-
                  <p>Get the details for a previously initiated Earth
                  Observation job.</p>
                tags:
                  - Get
                  - Earth
                  - Observation
                  - Jobs
                  - ARN
            /vector-enrichment-jobs/{Arn}:
              GET:
                summary: GetVectorEnrichmentJob
                description: >-
                  <p>Retrieves details of a Vector Enrichment Job for a given
                  job Amazon Resource Name (ARN).</p>
                tags:
                  - Get
                  - Vectors
                  - Enrichment
                  - Jobs
                  - ARN
            /export-earth-observation-job:
              POST:
                summary: ExportEarthObservationJob
                description: >-
                  <p>Use this operation to export results of an Earth
                  Observation job and optionally source images used as input to
                  the EOJ to an Amazon S3 location.</p>
                tags:
                  - Export
                  - Earth
                  - Observation
                  - Jobs
                  - ARN
                  - Export
                  - Earth
                  - Observation
                  - Jobs
            /export-vector-enrichment-jobs:
              POST:
                summary: ExportVectorEnrichmentJob
                description: >-
                  <p>Use this operation to copy results of a Vector Enrichment
                  job to an Amazon S3 location.</p>
                tags:
                  - Export
                  - Vectors
                  - Enrichment
                  - Jobs
                  - ARN
                  - Export
                  - Earth
                  - Observation
                  - Jobs
                  - Vectors
                  - Enrichment
                  - Jobs
            /raster-data-collection/{Arn}:
              GET:
                summary: GetRasterDataCollection
                description: >-
                  <p>Use this operation to get details of a specific raster data
                  collection.</p>
                tags:
                  - Get
                  - Raster
                  - Data
                  - Collections
                  - ARN
                  - Export
                  - Earth
                  - Observation
                  - Jobs
                  - Vectors
                  - Enrichment
                  - Jobs
            /tile/{z}/{x}/{y}:
              GET:
                summary: GetTile
                description: >-
                  <p>Gets a web mercator tile for the given Earth Observation
                  job.</p>
                tags:
                  - Get
                  - Tiles
                  - ARN
                  - Export
                  - Earth
                  - Observation
                  - Jobs
                  - Vectors
                  - Enrichment
                  - Jobs
                  - Tiles
            /list-earth-observation-jobs:
              POST:
                summary: ListEarthObservationJobs
                description: >-
                  <p>Use this operation to get a list of the Earth Observation
                  jobs associated with the calling Amazon Web Services
                  account.</p>
                tags:
                  - Lists
                  - Earth
                  - Observation
                  - Jobs
                  - ARN
                  - Export
                  - Earth
                  - Observation
                  - Jobs
                  - Vectors
                  - Enrichment
                  - Jobs
                  - Tiles
                  - Lists
            /raster-data-collections:
              GET:
                summary: ListRasterDataCollections
                description: <p>Use this operation to get raster data collections.</p>
                tags:
                  - Lists
                  - Raster
                  - Data
                  - Collections
                  - ARN
                  - Export
                  - Earth
                  - Observation
                  - Jobs
                  - Vectors
                  - Enrichment
                  - Jobs
                  - Tiles
                  - Lists
                  - Raster
                  - Data
                  - Collections
            /tags/{ResourceArn}:
              DELETE:
                summary: UntagResource
                description: <p>The resource you want to untag.</p>
                tags:
                  - Untag
                  - Resources
                  - ARN
                  - Export
                  - Earth
                  - Observation
                  - Jobs
                  - Vectors
                  - Enrichment
                  - Jobs
                  - Tiles
                  - Lists
                  - Raster
                  - Data
                  - Collections
                  - Resources
            /list-vector-enrichment-jobs:
              POST:
                summary: ListVectorEnrichmentJobs
                description: <p>Retrieves a list of vector enrichment jobs.</p>
                tags:
                  - Lists
                  - Vectors
                  - Enrichment
                  - Jobs
                  - ARN
                  - Export
                  - Earth
                  - Observation
                  - Jobs
                  - Vectors
                  - Enrichment
                  - Jobs
                  - Tiles
                  - Lists
                  - Raster
                  - Data
                  - Collections
                  - Resources
            /search-raster-data-collection:
              POST:
                summary: SearchRasterDataCollection
                description: >-
                  <p>Allows you run image query on a specific raster data
                  collection to get a list of the satellite imagery matching the
                  selected filters.</p>
                tags:
                  - Search
                  - Raster
                  - Data
                  - Collections
                  - ARN
                  - Export
                  - Earth
                  - Observation
                  - Jobs
                  - Vectors
                  - Enrichment
                  - Jobs
                  - Tiles
                  - Lists
                  - Raster
                  - Data
                  - Collections
                  - Resources
                  - Search
                  - Collections
            /earth-observation-jobs:
              POST:
                summary: StartEarthObservationJob
                description: <p>Use this operation to create an Earth observation job.</p>
                tags:
                  - Start
                  - Earth
                  - Observation
                  - Jobs
                  - ARN
                  - Export
                  - Earth
                  - Observation
                  - Jobs
                  - Vectors
                  - Enrichment
                  - Jobs
                  - Tiles
                  - Lists
                  - Raster
                  - Data
                  - Collections
                  - Resources
                  - Search
                  - Collections
            /vector-enrichment-jobs:
              POST:
                summary: StartVectorEnrichmentJob
                description: >-
                  <p>Creates a Vector Enrichment job for the supplied job type.
                  Currently, there are two supported job types: reverse
                  geocoding and map matching.</p>
                tags:
                  - Start
                  - Vectors
                  - Enrichment
                  - Jobs
                  - ARN
                  - Export
                  - Earth
                  - Observation
                  - Jobs
                  - Vectors
                  - Enrichment
                  - Jobs
                  - Tiles
                  - Lists
                  - Raster
                  - Data
                  - Collections
                  - Resources
                  - Search
                  - Collections
            /earth-observation-jobs/stop:
              POST:
                summary: StopEarthObservationJob
                description: >-
                  <p>Use this operation to stop an existing earth observation
                  job.</p>
                tags:
                  - Stop
                  - Earth
                  - Observation
                  - Jobs
                  - ARN
                  - Export
                  - Earth
                  - Observation
                  - Jobs
                  - Vectors
                  - Enrichment
                  - Jobs
                  - Tiles
                  - Lists
                  - Raster
                  - Data
                  - Collections
                  - Resources
                  - Search
                  - Collections
                  - Stop
            /vector-enrichment-jobs/stop:
              POST:
                summary: StopVectorEnrichmentJob
                description: <p>Stops the Vector Enrichment job for a given j
                tags:
                  - Stop
                  - Vectors
                  - Enrichment
                  - Jobs
                  - ARN
                  - Export
                  - Earth
                  - Observation
                  - Jobs
                  - Vectors
                  - Enrichment
                  - Jobs
                  - Tiles
                  - Lists
                  - Raster
                  - Data
                  - Collections
                  - Resources
                  - Search
                  - Collections
                  - St
    overlays:
      - type: APIs.io Search
        url: overlays/sagemaker-geospatial-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/sagemaker-geospatial-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:sagemaker-geospatial
  - aid: box:box-collections-api
    name: Box Collections API
    description: Needs a description
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.box.com/
    baseURL: https://api.example.com
    tags: []
    properties:
      - type: Documentation
        url: https://developer.box.com/
      - type: OpenAPI
        data:
          openapi: 3.1.0
          info:
            title: Box Collections API
          paths:
            /collections:
              get:
                summary: List all collections
                tags:
                  - List
                  - All
                  - Collections
                  - Collections
                description: |-
                  Retrieves all collections for a given user.

                  Currently, only the `favorites` collection
                  is supported.
            /collections/{collection_id}/items:
              get:
                summary: List collection items
                tags:
                  - List
                  - Collection
                  - Items
                  - Collections
                  - Collection_id
                  - Items
                description: |-
                  Retrieves the files and/or folders contained within
                  this
    overlays:
      - type: APIs.io Search
        url: overlays/collections-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/collections-openapi-api-evangelist-ratings.yml
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---