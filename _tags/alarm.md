---
name: Alarm
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/alarm.png
url: https://example.com/apis/alarm.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Alarm
apis:
  - name: iotevents-data
    description: >-
      <p>IoT Events monitors your equipment or device fleets for failures or
      changes in operation, and triggers actions when such events occur. You can
      use IoT Events Data API commands to send inputs to detectors, list
      detectors, and view or update a detector's status.</p> <p> For more
      information, see <a
      href="https://docs.aws.amazon.com/iotevents/latest/developerguide/what-is-iotevents.html">What
      is IoT Events?</a> in the <i>IoT Events Developer Guide</i>.</p>
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
            title: iotevents-data
          paths:
            /alarms/acknowledge:
              POST:
                summary: BatchAcknowledgeAlarm
                description: >-
                  <p>Acknowledges one or more alarms. The alarms change to the
                  <code>ACKNOWLEDGED</code> state after you acknowledge
                  them.</p>
                tags:
                  - Batches
                  - Acknowledge
                  - Alarm
                  - Alarms
                  - Acknowledge
            /detectors/delete:
              POST:
                summary: BatchDeleteDetector
                description: >-
                  <p>Deletes one or more detectors that were created. When a
                  detector is deleted, its state will be cleared and the
                  detector will be removed from the list of detectors. The
                  deleted detector will no longer appear if referenced in the <a
                  href="https://docs.aws.amazon.com/iotevents/latest/apireference/API_iotevents-data_ListDetectors.html">ListDetectors</a>
                  API call.</p>
                tags:
                  - Batches
                  - Delete
                  - Detectors
                  - Alarms
                  - Acknowledge
                  - Detectors
                  - Delete
            /alarms/disable:
              POST:
                summary: BatchDisableAlarm
                description: >-
                  <p>Disables one or more alarms. The alarms change to the
                  <code>DISABLED</code> state after you disable them.</p>
                tags:
                  - Batches
                  - Disable
                  - Alarm
                  - Alarms
                  - Acknowledge
                  - Detectors
                  - Delete
                  - Disable
            /alarms/enable:
              POST:
                summary: BatchEnableAlarm
                description: >-
                  <p>Enables one or more alarms. The alarms change to the
                  <code>NORMAL</code> state after you enable them.</p>
                tags:
                  - Batches
                  - Enable
                  - Alarm
                  - Alarms
                  - Acknowledge
                  - Detectors
                  - Delete
                  - Disable
                  - Enable
            /inputs/messages:
              POST:
                summary: BatchPutMessage
                description: >-
                  <p>Sends a set of messages to the IoT Events system. Each
                  message payload is transformed into the input you specify
                  (<code>"inputName"</code>) and ingested into any detectors
                  that monitor that input. If multiple messages are sent, the
                  order in which the messages are processed isn't guaranteed. To
                  guarantee ordering, you must send messages one at a time and
                  wait for a successful response.</p>
                tags:
                  - Batches
                  - Put
                  - Messages
                  - Alarms
                  - Acknowledge
                  - Detectors
                  - Delete
                  - Disable
                  - Enable
                  - Inputs
                  - Messages
            /alarms/reset:
              POST:
                summary: BatchResetAlarm
                description: >-
                  <p>Resets one or more alarms. The alarms return to the
                  <code>NORMAL</code> state after you reset them.</p>
                tags:
                  - Batches
                  - Reset
                  - Alarm
                  - Alarms
                  - Acknowledge
                  - Detectors
                  - Delete
                  - Disable
                  - Enable
                  - Inputs
                  - Messages
                  - Reset
            /alarms/snooze:
              POST:
                summary: BatchSnoozeAlarm
                description: >-
                  <p>Changes one or more alarms to the snooze mode. The alarms
                  change to the <code>SNOOZE_DISABLED</code> state after you set
                  them to the snooze mode.</p>
                tags:
                  - Batches
                  - Snooze
                  - Alarm
                  - Alarms
                  - Acknowledge
                  - Detectors
                  - Delete
                  - Disable
                  - Enable
                  - Inputs
                  - Messages
                  - Reset
                  - Snooze
            /detectors:
              POST:
                summary: BatchUpdateDetector
                description: >-
                  <p>Updates the state, variable values, and timer settings of
                  one or more detectors (instances) of a specified detector
                  model.</p>
                tags:
                  - Batches
                  - Update
                  - Detectors
                  - Alarms
                  - Acknowledge
                  - Detectors
                  - Delete
                  - Disable
                  - Enable
                  - Inputs
                  - Messages
                  - Reset
                  - Snooze
            /alarms/{alarmModelName}/keyValues/:
              GET:
                summary: DescribeAlarm
                description: <p>Retrieves information about an alarm.</p>
                tags:
                  - Describe
                  - Alarm
                  - Alarms
                  - Acknowledge
                  - Detectors
                  - Delete
                  - Disable
                  - Enable
                  - Inputs
                  - Messages
                  - Reset
                  - Snooze
                  - Models
                  - Names
                  - Keys
                  - Values
            /detectors/{detectorModelName}/keyValues/:
              GET:
                summary: DescribeDetector
                description: >-
                  <p>Returns information about the specified detector
                  (instance).</p>
                tags:
                  - Describe
                  - Detectors
                  - Alarms
                  - Acknowledge
                  - Detectors
                  - Delete
                  - Disable
                  - Enable
                  - Inputs
                  - Messages
                  - Reset
                  - Snooze
                  - Models
                  - Names
                  - Keys
                  - Values
            /alarms/{alarmModelName}:
              GET:
                summary: ListAlarms
                description: >-
                  <p>Lists one or more alarms. The operation returns only the
                  metadata associated with each alarm.</p>
                tags:
                  - Lists
                  - Alarms
                  - Alarms
                  - Acknowledge
                  - Detectors
                  - Delete
                  - Disable
                  - Enable
                  - Inputs
                  - Messages
                  - Reset
                  - Snooze
                  - Models
                  - Names
                  - Keys
                  - Values
            /detectors/{detectorModelName}:
              GET:
                summary: ListDetectors
                description: <p>Lists detectors (the instances of a detector m
                tags:
                  - Lists
                  - Detectors
                  - Alarms
                  - Acknowledge
                  - Detectors
                  - Delete
                  - Disable
                  - Enable
                  - Inputs
                  - Messages
                  - Reset
                  - Snooze
                  - Models
                  - Names
                  - Keys
                  - Value
    overlays:
      - type: APIs.io Search
        url: overlays/iotevents-data-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/iotevents-data-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:iotevents-data
  - name: iotevents
    description: >-
      <p>AWS IoT Events monitors your equipment or device fleets for failures or
      changes in operation, and triggers actions when such events occur. You can
      use AWS IoT Events API operations to create, read, update, and delete
      inputs and detector models, and to list their versions.</p>
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
            title: iotevents
          paths:
            /alarm-models:
              GET:
                summary: ListAlarmModels
                description: >-
                  <p>Lists the alarm models that you created. The operation
                  returns only the metadata associated with each alarm
                  model.</p>
                tags:
                  - Lists
                  - Alarm
                  - Models
                  - Alarm
                  - Models
            /detector-models:
              GET:
                summary: ListDetectorModels
                description: >-
                  <p>Lists the detector models you have created. Only the
                  metadata associated with each detector model is returned.</p>
                tags:
                  - Lists
                  - Detectors
                  - Models
                  - Alarm
                  - Models
                  - Detectors
            /inputs:
              GET:
                summary: ListInputs
                description: <p>Lists the inputs you have created.</p>
                tags:
                  - Lists
                  - Inputs
                  - Alarm
                  - Models
                  - Detectors
                  - Inputs
            /alarm-models/{alarmModelName}:
              POST:
                summary: UpdateAlarmModel
                description: >-
                  <p>Updates an alarm model. Any alarms that were created based
                  on the previous version are deleted and then created again as
                  new data arrives.</p>
                tags:
                  - Update
                  - Alarm
                  - Models
                  - Alarm
                  - Models
                  - Detectors
                  - Inputs
                  - Models
                  - Names
            /detector-models/{detectorModelName}:
              POST:
                summary: UpdateDetectorModel
                description: >-
                  <p>Updates a detector model. Detectors (instances) spawned by
                  the previous version are deleted and then re-created as new
                  inputs arrive.</p>
                tags:
                  - Update
                  - Detectors
                  - Models
                  - Alarm
                  - Models
                  - Detectors
                  - Inputs
                  - Models
                  - Names
            /inputs/{inputName}:
              PUT:
                summary: UpdateInput
                description: <p>Updates an input.</p>
                tags:
                  - Update
                  - Inputs
                  - Alarm
                  - Models
                  - Detectors
                  - Inputs
                  - Models
                  - Names
            /analysis/detector-models/{analysisId}:
              GET:
                summary: DescribeDetectorModelAnalysis
                description: >-
                  <p>Retrieves runtime information about a detector model
                  analysis.</p> <note> <p>After AWS IoT Events starts analyzing
                  your detector model, you have up to 24 hours to retrieve the
                  analysis results.</p> </note>
                tags:
                  - Describe
                  - Detectors
                  - Models
                  - Analysis
                  - Alarm
                  - Models
                  - Detectors
                  - Inputs
                  - Models
                  - Names
                  - Identifiers
            /logging:
              PUT:
                summary: PutLoggingOptions
                description: >-
                  <p>Sets or updates the AWS IoT Events logging options.</p>
                  <p>If you update the value of any <code>loggingOptions</code>
                  field, it takes up to one minute for the change to take
                  effect. If you change the policy attached to the role you
                  specified in the <code>roleArn</code> field (for example, to
                  correct an invalid policy), it takes up to five minutes for
                  that change to take effect.</p>
                tags:
                  - Put
                  - Logging
                  - Options
                  - Alarm
                  - Models
                  - Detectors
                  - Inputs
                  - Models
                  - Names
                  - Identifiers
                  - Logging
            /analysis/detector-models/{analysisId}/results:
              GET:
                summary: GetDetectorModelAnalysisResults
                description: >-
                  <p>Retrieves one or more analysis results of the detector
                  model.</p> <note> <p>After AWS IoT Events starts analyzing
                  your detector model, you have up to 24 hours to retrieve the
                  analysis results.</p> </note>
                tags:
                  - Get
                  - Detectors
                  - Models
                  - Analysis
                  - Results
                  - Alarm
                  - Models
                  - Detectors
                  - Inputs
                  - Models
                  - Names
                  - Identifiers
                  - Logging
                  - Results
            /alarm-models/{alarmModelName}/versions:
              GET:
                summary: ListAlarmModelVersions
                description: >-
                  <p>Lists all the versions of an alarm model. The operation
                  returns only the metadata associated with each alarm model
                  version.</p>
                tags:
                  - Lists
                  - Alarm
                  - Models
                  - Versions
                  - Alarm
                  - Models
                  - Detectors
                  - Inputs
                  - Models
                  - Names
                  - Identifiers
                  - Logging
                  - Results
                  - Versions
            /detector-models/{detectorModelName}/versions:
              GET:
                summary: ListDetectorModelVersions
                description: >-
                  <p>Lists all the versions of a detector model. Only the
                  metadata associated with each detector model version is
                  returned.</p>
                tags:
                  - Lists
                  - Detectors
                  - Models
                  - Versions
                  - Alarm
                  - Models
                  - Detectors
                  - Inputs
                  - Models
                  - Names
                  - Identifiers
                  - Logging
                  - Results
                  - Versions
            /input-routings:
              POST:
                summary: ListInputRoutings
                description: <p> Lists one or more input routings. </p>
                tags:
                  - Lists
                  - Inputs
                  - Routings
                  - Alarm
                  - Models
                  - Detectors
                  - Inputs
                  - Models
                  - Names
                  - Identifiers
                  - Logging
                  - Results
                  - Versions
                  - Inputs
                  - Routings
            /tags:
              DELETE:
                summary: UntagResource
                description: <p>Removes the given tags (metadata) from the resource.</p>
                tags:
                  - Untag
                  - Resources
                  - Alarm
                  - Models
                  - Detectors
                  - Inputs
                  - Models
                  - Names
                  - Identifiers
                  - Logging
                  - Results
                  - Versions
                  - Inputs
                  - Routings
                  - Tags
            /analysis/detector-models/:
              POST:
                summary: StartDetectorModelAnalysis
                description: >-
                  <p>Performs an analysis of your detector model. For more
                  information, see <a
                  href="https://docs.aws.amazon.com/iotevents/latest/developerguide/iotevents-analyze-api.html">Troubleshooting
                  a detector model</a> in the <i>AWS IoT Events Developer Guid
                tags:
                  - Start
                  - Detectors
                  - Models
                  - Analysis
                  - Alarm
                  - Models
                  - Detectors
                  - Inputs
                  - Models
                  - Names
                  - Identifiers
                  - Logging
                  - Results
                  - Versions
                  - Inputs
                  - Routings
                  - Tags
                  - Analysis
    overlays:
      - type: APIs.io Search
        url: overlays/iotevents-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/iotevents-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:iotevents
  - name: resiliencehub
    description: >-
      <p>Resilience Hub helps you proactively prepare and protect your Amazon
      Web Services applications from disruptions. It offers continual resiliency
      assessment and validation that integrates into your software development
      lifecycle. This enables you to uncover resiliency weaknesses, ensure
      recovery time objective (RTO) and recovery point objective (RPO) targets
      for your applications are met, and resolve issues before they are released
      into production. </p>
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
            title: resiliencehub
          paths:
            /add-draft-app-version-resource-mappings:
              POST:
                summary: AddDraftAppVersionResourceMappings
                description: >-
                  <p>Adds the source of resource-maps to the draft version of an
                  application. During assessment, Resilience Hub will use these
                  resource-maps to resolve the latest physical ID for each
                  resource in the application template. For more information
                  about different types of resources suported by Resilience Hub
                  and how to add them in your application, see <a
                  href="https://docs.aws.amazon.com/resilience-hub/latest/userguide/how-app-manage.html">Step
                  2: How is your application managed?</a> in the Resilience Hub
                  User Guide.</p>
                tags:
                  - Add
                  - Draft
                  - Applications
                  - Versions
                  - Resources
                  - Mapping
                  - Add
                  - Draft
                  - Applications
                  - Versions
                  - Resources
                  - Mapping
            /batch-update-recommendation-status:
              POST:
                summary: BatchUpdateRecommendationStatus
                description: >-
                  <p>Enables you to include or exclude one or more operational
                  recommendations.</p>
                tags:
                  - Batches
                  - Update
                  - Recommendations
                  - Status
                  - Add
                  - Draft
                  - Applications
                  - Versions
                  - Resources
                  - Mapping
                  - Batches
                  - Update
                  - Recommendations
                  - Status
            /create-app:
              POST:
                summary: CreateApp
                description: >-
                  <p>Creates an Resilience Hub application. An Resilience Hub
                  application is a collection of Amazon Web Services resources
                  structured to prevent and recover Amazon Web Services
                  application disruptions. To describe a Resilience Hub
                  application, you provide an application name, resources from
                  one or more CloudFormation stacks, Resource Groups, Terraform
                  state files, AppRegistry applications, and an appropriate
                  resiliency policy. In addition, you can also add resources
                  that are located on Amazon Elastic Kubernetes Service (Amazon
                  EKS) clusters as optional resources. For more information
                  about the number of resources supported per application, see
                  <a
                  href="https://docs.aws.amazon.com/general/latest/gr/resiliencehub.html#limits_resiliencehub">Service
                  quotas</a>.</p> <p>After you create an Resilience Hub
                  application, you publish it so that you can run a resiliency
                  assessment on it. You can then use recommendations from the
                  assessment to improve resiliency by running another
                  assessment, comparing results, and then iterating the process
                  until you achieve your goals for recovery time objective (RTO)
                  and recovery point objective (RPO).</p>
                tags:
                  - Create
                  - Applications
                  - Add
                  - Draft
                  - Applications
                  - Versions
                  - Resources
                  - Mapping
                  - Batches
                  - Update
                  - Recommendations
                  - Status
                  - Create
            /create-app-version-app-component:
              POST:
                summary: CreateAppVersionAppComponent
                description: >-
                  <p>Creates a new Application Component in the Resilience Hub
                  application.</p> <note> <p>This API updates the Resilience Hub
                  application draft version. To use this Application Component
                  for running assessments, you must publish the Resilience Hub
                  application using the <code>PublishAppVersion</code> API.</p>
                  </note>
                tags:
                  - Create
                  - Applications
                  - Versions
                  - Components
                  - Add
                  - Draft
                  - Applications
                  - Versions
                  - Resources
                  - Mapping
                  - Batches
                  - Update
                  - Recommendations
                  - Status
                  - Create
                  - Components
            /create-app-version-resource:
              POST:
                summary: CreateAppVersionResource
                description: >-
                  <p>Adds a resource to the Resilience Hub application and
                  assigns it to the specified Application Components. If you
                  specify a new Application Component, Resilience Hub will
                  automatically create the Application Component.</p> <note>
                  <ul> <li> <p>This action has no effect outside Resilience
                  Hub.</p> </li> <li> <p>This API updates the Resilience Hub
                  application draft version. To use this resource for running
                  resiliency assessments, you must publish the Resilience Hub
                  application using the <code>PublishAppVersion</code> API.</p>
                  </li> <li> <p>To update application version with new
                  <code>physicalResourceID</code>, you must call
                  <code>ResolveAppVersionResources</code> API.</p> </li> </ul>
                  </note>
                tags:
                  - Create
                  - Applications
                  - Versions
                  - Resources
                  - Add
                  - Draft
                  - Applications
                  - Versions
                  - Resources
                  - Mapping
                  - Batches
                  - Update
                  - Recommendations
                  - Status
                  - Create
                  - Components
            /create-recommendation-template:
              POST:
                summary: CreateRecommendationTemplate
                description: >-
                  <p>Creates a new recommendation template for the Resilience
                  Hub application.</p>
                tags:
                  - Create
                  - Recommendations
                  - Templates
                  - Add
                  - Draft
                  - Applications
                  - Versions
                  - Resources
                  - Mapping
                  - Batches
                  - Update
                  - Recommendations
                  - Status
                  - Create
                  - Components
                  - Templates
            /create-resiliency-policy:
              POST:
                summary: CreateResiliencyPolicy
                description: >-
                  <p>Creates a resiliency policy for an application.</p> <note>
                  <p>Resilience Hub allows you to provide a value of zero for
                  <code>rtoInSecs</code> and <code>rpoInSecs</code> of your
                  resiliency policy. But, while assessing your application, the
                  lowest possible assessment result is near zero. Hence, if you
                  provide value zero for <code>rtoInSecs</code> and
                  <code>rpoInSecs</code>, the estimated workload RTO and
                  estimated workload RPO result will be near zero and the
                  <b>Compliance status</b> for your application will be set to
                  <b>Policy breached</b>.</p> </note>
                tags:
                  - Create
                  - Resiliency
                  - Policies
                  - Add
                  - Draft
                  - Applications
                  - Versions
                  - Resources
                  - Mapping
                  - Batches
                  - Update
                  - Recommendations
                  - Status
                  - Create
                  - Components
                  - Templates
                  - Resiliency
                  - Policies
            /delete-app:
              POST:
                summary: DeleteApp
                description: >-
                  <p>Deletes an Resilience Hub application. This is a
                  destructive action that can't be undone.</p>
                tags:
                  - Delete
                  - Applications
                  - Add
                  - Draft
                  - Applications
                  - Versions
                  - Resources
                  - Mapping
                  - Batches
                  - Update
                  - Recommendations
                  - Status
                  - Create
                  - Components
                  - Templates
                  - Resiliency
                  - Policies
                  - Delete
            /delete-app-assessment:
              POST:
                summary: DeleteAppAssessment
                description: >-
                  <p>Deletes an Resilience Hub application assessment. This is a
                  destructive action that can't be undone.</p>
                tags:
                  - Delete
                  - Applications
                  - Assessments
                  - Add
                  - Draft
                  - Applications
                  - Versions
                  - Resources
                  - Mapping
                  - Batches
                  - Update
                  - Recommendations
                  - Status
                  - Create
                  - Components
                  - Templates
                  - Resiliency
                  - Policies
                  - Delete
                  - Assessments
            /delete-app-input-source:
              POST:
                summary: DeleteAppInputSource
                description: >-
                  <p>Deletes the input source and all of its imported resources
                  from the Resilience Hub application.</p>
                tags:
                  - Delete
                  - Applications
                  - Inputs
                  - Source
                  - Add
                  - Draft
                  - Applications
                  - Versions
                  - Resources
                  - Mapping
                  - Batches
                  - Update
                  - Recommendations
                  - Status
                  - Create
                  - Components
                  - Templates
                  - Resiliency
                  - Policies
                  - Delete
                  - Assessments
                  - Inputs
                  - Source
            /delete-app-version-app-component:
              POST:
                summary: DeleteAppVersionAppComponent
                description: >-
                  <p>Deletes an Application Component from the Resilience Hub
                  application.</p> <note> <ul> <li> <p>This API updates the
                  Resilience Hub application draft version. To use this
                  Application Component for running assessments, you must
                  publish the Resilience Hub application using the
                  <code>PublishAppVersion</code> API.</p> </li> <li> <p>You will
                  not be able to delete an Application Component if it has
                  resources associated with it.</p> </li> </ul> </note>
                tags:
                  - Delete
                  - Applications
                  - Versions
                  - Components
                  - Add
                  - Draft
                  - Applications
                  - Versions
                  - Resources
                  - Mapping
                  - Batches
                  - Update
                  - Recommendations
                  - Status
                  - Create
                  - Components
                  - Templates
                  - Resiliency
                  - Policies
                  - Delete
                  - Assessments
                  - Inputs
                  - Source
            /delete-app-version-resource:
              POST:
                summary: DeleteAppVersionResource
                description: >-
                  <p>Deletes a resource from the Resilience Hub application.</p>
                  <note> <ul> <li> <p>You can only delete a manually added
                  resource. To exclude non-manually added resources, use the
                  <code>UpdateAppVersionResource</code> API.</p> </li> <li>
                  <p>This action has no effect outside Resilience Hub.</p> </li>
                  <li> <p>This API updates the Resilience Hub application draft
                  version. To use this resource for running resiliency
                  assessments, you must publish the Resilience Hub application
                  using the <code>PublishAppVersion</code> API.</p> </li> </ul>
                  </note>
                tags:
                  - Delete
                  - Applications
                  - Versions
                  - Resources
                  - Add
                  - Draft
                  - Applications
                  - Versions
                  - Resources
                  - Mapping
                  - Batches
                  - Update
                  - Recommendations
                  - Status
                  - Create
                  - Components
                  - Templates
                  - Resiliency
                  - Policies
                  - Delete
                  - Assessments
                  - Inputs
                  - Source
            /delete-recommendation-template:
              POST:
                summary: DeleteRecommendationTemplate
                description: >-
                  <p>Deletes a recommendation template. This is a destructive
                  action that can't be undone.</p>
                tags:
                  - Delete
                  - Recommendations
                  - Templates
                  - Add
                  - Draft
                  - Applications
                  - Versions
                  - Resources
                  - Mapping
                  - Batches
                  - Update
                  - Recommendations
                  - Status
                  - Create
                  - Components
                  - Templates
                  - Resiliency
                  - Policies
                  - Delete
                  - Assessments
                  - Inputs
                  - Source
            /delete-resiliency-policy:
              POST:
                summary: DeleteResiliencyPolicy
                description: >-
                  <p>Deletes a resiliency policy. This is a destructive action
                  that can't be undone.</p>
                tags:
                  - Delete
                  - Resiliency
                  - Policies
                  - Add
                  - Draft
                  - Applications
                  - Versions
                  - Resources
                  - Mapping
                  - Batches
                  - Update
                  - Recommendations
                  - Status
                  - Create
                  - Components
                  - Templates
                  - Resiliency
                  - Policies
                  - Delete
                  - Assessments
                  - Inputs
                  - Source
            /describe-app:
              POST:
                summary: DescribeApp
                description: <p>Describes an Resilience Hub application.</p>
                tags:
                  - Describe
                  - Applications
                  - Add
                  - Draft
                  - Applications
                  - Versions
                  - Resources
                  - Mapping
                  - Batches
                  - Update
                  - Recommendations
                  - Status
                  - Create
                  - Components
                  - Templates
                  - Resiliency
                  - Policies
                  - Delete
                  - Assessments
                  - Inputs
                  - Source
                  - Describe
            /describe-app-assessment:
              POST:
                summary: DescribeAppAssessment
                description: >-
                  <p>Describes an assessment for an Resilience Hub
                  application.</p>
                tags:
                  - Describe
                  - Applications
                  - Assessments
                  - Add
                  - Draft
                  - Applications
                  - Versions
                  - Resources
                  - Mapping
                  - Batches
                  - Update
                  - Recommendations
                  - Status
                  - Create
                  - Components
                  - Templates
                  - Resiliency
                  - Policies
                  - Delete
                  - Assessments
                  - Inputs
                  - Source
                  - Describe
            /describe-app-version:
              POST:
                summary: DescribeAppVersion
                description: <p>Describes the Resilience Hub application version.</p>
                tags:
                  - Describe
                  - Applications
                  - Versions
                  - Add
                  - Draft
                  - Applications
                  - Versions
                  - Resources
                  - Mapping
                  - Batches
                  - Update
                  - Recommendations
                  - Status
                  - Create
                  - Components
                  - Templates
                  - Resiliency
                  - Policies
                  - Delete
                  - Assessments
                  - Inputs
                  - Source
                  - Describe
            /describe-app-version-app-component:
              POST:
                summary: DescribeAppVersionAppComponent
                description: >-
                  <p>Describes an Application Component in the Resilience Hub
                  application.</p>
                tags:
                  - Describe
                  - Applications
                  - Versions
                  - Components
                  - Add
                  - Draft
                  - Applications
                  - Versions
                  - Resources
                  - Mapping
                  - Batches
                  - Update
                  - Recommendations
                  - Status
                  - Create
                  - Components
                  - Templates
                  - Resiliency
                  - Policies
                  - Delete
                  - Assessments
                  - Inputs
                  - Source
                  - Describe
            /describe-app-version-resource:
              POST:
                summary: DescribeAppVersionResource
                description: >-
                  <p>Describes a resource of the Resilience Hub application.</p>
                  <note> <p>This API accepts only one of the following
                  parameters to descibe the resource:</p> <ul> <li> <p>
                  <code>resourceName</code> </p> </li> <li> <p>
                  <code>logicalResourceId</code> </p> </li> <li> <p>
                  <code>physicalResourceId</code> (Along with
                  <code>physicalResourceId</code>, you can also provide
                  <code>awsAccountId</code>, and <code>awsRegion</code>)</p>
                  </li> </ul> </note>
                tags:
                  - Describe
                  - Applications
                  - Versions
                  - Resources
                  - Add
                  - Draft
                  - Applications
                  - Versions
                  - Resources
                  - Mapping
                  - Batches
                  - Update
                  - Recommendations
                  - Status
                  - Create
                  - Components
                  - Templates
                  - Resiliency
                  - Policies
                  - Delete
                  - Assessments
                  - Inputs
                  - Source
                  - Describe
            /describe-app-version-resources-resolution-status:
              POST:
                summary: DescribeAppVersionResourcesResolutionStatus
                description: >-
                  <p>Returns the resolution status for the specified resolution
                  identifier for an application version. If
                  <code>resolutionId</code> is not specified, the current
                  resolution status is returned.</p>
                tags:
                  - Describe
                  - Applications
                  - Versions
                  - Resources
                  - Resolutions
                  - Status
                  - Add
                  - Draft
                  - Applications
                  - Versions
                  - Resources
                  - Mapping
                  - Batches
                  - Update
                  - Recommendations
                  - Status
                  - Create
                  - Components
                  - Templates
                  - Resiliency
                  - Policies
                  - Delete
                  - Assessments
                  - Inputs
                  - Source
                  - Describe
                  - Resources
                  - Resolutions
            /describe-app-version-template:
              POST:
                summary: DescribeAppVersionTemplate
                description: <p>Describes details about an Resilience Hub application.</p>
                tags:
                  - Describe
                  - Applications
                  - Versions
                  - Templates
                  - Add
                  - Draft
                  - Applications
                  - Versions
                  - Resources
                  - Mapping
                  - Batches
                  - Update
                  - Recommendations
                  - Status
                  - Create
                  - Components
                  - Templates
                  - Resiliency
                  - Policies
                  - Delete
                  - Assessments
                  - Inputs
                  - Source
                  - Describe
                  - Resources
                  - Resolutions
            /describe-draft-app-version-resources-import-status:
              POST:
                summary: DescribeDraftAppVersionResourcesImportStatus
                description: >-
                  <p>Describes the status of importing resources to an
                  application version.</p> <note> <p>If you get a 404 error with
                  <code>ResourceImportStatusNotFoundAppMetadataException</code>,
                  you must call <code>importResourcesToDraftAppVersion</code>
                  after creating the application and before calling
                  <code>describeDraftAppVersionResourcesImportStatus</code> to
                  obtain the status.</p> </note>
                tags:
                  - Describe
                  - Draft
                  - Applications
                  - Versions
                  - Resources
                  - Import
                  - Status
                  - Add
                  - Draft
                  - Applications
                  - Versions
                  - Resources
                  - Mapping
                  - Batches
                  - Update
                  - Recommendations
                  - Status
                  - Create
                  - Components
                  - Templates
                  - Resiliency
                  - Policies
                  - Delete
                  - Assessments
                  - Inputs
                  - Source
                  - Describe
                  - Resources
                  - Resolutions
                  - Import
            /describe-resiliency-policy:
              POST:
                summary: DescribeResiliencyPolicy
                description: >-
                  <p>Describes a specified resiliency policy for an Resilience
                  Hub application. The returned policy object includes creation
                  time, data location constraints, the Amazon Resource Name
                  (ARN) for the policy, tags, tier, and more.</p>
                tags:
                  - Describe
                  - Resiliency
                  - Policies
                  - Add
                  - Draft
                  - Applications
                  - Versions
                  - Resources
                  - Mapping
                  - Batches
                  - Update
                  - Recommendations
                  - Status
                  - Create
                  - Components
                  - Templates
                  - Resiliency
                  - Policies
                  - Delete
                  - Assessments
                  - Inputs
                  - Source
                  - Describe
                  - Resources
                  - Resolutions
                  - Import
            /import-resources-to-draft-app-version:
              POST:
                summary: ImportResourcesToDraftAppVersion
                description: >-
                  <p>Imports resources to Resilience Hub application draft
                  version from different input sources. For more information
                  about the input sources supported by Resilience Hub, see <a
                  href="https://docs.aws.amazon.com/resilience-hub/latest/userguide/discover-structure.html">Discover
                  the structure and describe your Resilience Hub
                  application</a>.</p>
                tags:
                  - Import
                  - Resources
                  - To
                  - Draft
                  - Applications
                  - Versions
                  - Add
                  - Draft
                  - Applications
                  - Versions
                  - Resources
                  - Mapping
                  - Batches
                  - Update
                  - Recommendations
                  - Status
                  - Create
                  - Components
                  - Templates
                  - Resiliency
                  - Policies
                  - Delete
                  - Assessments
                  - Inputs
                  - Source
                  - Describe
                  - Resources
                  - Resolutions
                  - Import
                  - To
            /list-alarm-recommendations:
              POST:
                summary: ListAlarmRecommendations
                description: >-
                  <p>Lists the alarm recommendations for an Resilience Hub
                  application.</p>
                tags:
                  - Lists
                  - Alarm
                  - Recommendations
                  - Add
                  - Draft
                  - Applications
                  - Versions
                  - Resources
                  - Mapping
                  - Batches
                  - Update
                  - Recommendations
                  - Status
                  - Create
                  - Components
                  - Templates
                  - Resiliency
                  - Policies
                  - Delete
                  - Assessments
                  - Inputs
                  - Source
                  - Describe
                  - Resources
                  - Resolutions
                  - Import
                  - To
                  - Lists
                  - Alarm
                  - Recommendations
            /list-app-assessment-compliance-drifts:
              POST:
                summary: ListAppAssessmentComplianceDrifts
                description: >-
                  <p>List of compliance drifts that were detected while running
                  an assessment.</p>
                tags:
                  - Lists
                  - Applications
                  - Assessments
                  - Compliance
                  - Drifts
                  - Add
                  - Draft
                  - Applications
                  - Versions
                  - Resources
                  - Mapping
                  - Batches
                  - Update
                  - Recommendations
                  - Status
                  - Create
                  - Components
                  - Templates
                  - Resiliency
                  - Policies
                  - Delete
                  - Assessments
                  - Inputs
                  - Source
                  - Describe
                  - Resources
                  - Resolutions
                  - Import
                  - To
                  - Lists
                  - Alarm
                  - Recommendations
                  - Compliance
                  - Drifts
            /list-app-assessments:
              GET:
                summary: ListAppAssessments
                description: >-
                  <p>Lists the assessments for an Resilience Hub application.
                  You can use request parameters to refine the results for the
                  response object.</p>
                tags:
                  - Lists
                  - Applications
                  - Assessments
                  - Add
                  - Draft
                  - Applications
                  - Versions
                  - Resources
                  - Mapping
                  - Batches
                  - Update
                  - Recommendations
                  - Status
                  - Create
                  - Components
                  - Templates
                  - Resiliency
                  - Policies
                  - Delete
                  - Assessments
                  - Inputs
                  - Source
                  - Describe
                  - Resources
                  - Resolutions
                  - Import
                  - To
                  - Lists
                  - Alarm
                  - Recommendations
                  - Compliance
                  - Drifts
                  - Assessments
            /list-app-component-compliances:
              POST:
                summary: ListAppComponentCompliances
                description: >-
                  <p>Lists the compliances for an Resilience Hub Application
                  Component.</p>
                tags:
                  - Lists
                  - Applications
                  - Components
                  - Compliance
                  - Add
                  - Draft
                  - Applications
                  - Versions
                  - Resources
                  - Mapping
                  - Batches
                  - Update
                  - Recommendations
                  - Status
                  - Create
                  - Components
                  - Templates
                  - Resiliency
                  - Policies
                  - Delete
                  - Assessments
                  - Inputs
                  - Source
                  - Describe
                  - Resources
                  - Resolutions
                  - Import
                  - To
                  - Lists
                  - Alarm
                  - Recommendations
                  - Compliance
                  - Drifts
                  - Assessments
                  - Compliance
            /list-app-component-recommendations:
              POST:
                summary: ListAppComponentRecommendations
                description: >-
                  <p>Lists the recommendations for an Resilience Hub Application
                  Component.</p>
                tags:
                  - Lists
                  - Applications
                  - Components
                  - Recommendations
                  - Add
                  - Draft
                  - Applications
                  - Versions
                  - Resources
                  - Mapping
                  - Batches
                  - Update
                  - Recommendations
                  - Status
                  - Create
                  - Components
                  - Templates
                  - Resiliency
                  - Policies
                  - Delete
                  - Assessments
                  - Inputs
                  - Source
                  - Describe
                  - Resources
                  - Resolutions
                  - Import
                  - To
                  - Lists
                  - Alarm
                  - Recommendations
                  - Compliance
                  - Drifts
                  - Assessments
                  - Compliance
            /list-app-input-sources:
              POST:
                summary: ListAppInputSources
                description: >-
                  <p>Lists all the input sources of the Resilience Hub
                  application. For more information about the input sources
                  supported by Resilience Hub, see <a
                  href="https://docs.aws.amazon.com/resilience-hub/latest/userguide/discover-structure.html">Discover
                  the structure and describe your Resilience Hub
                  application</a>.</p>
                tags:
                  - Lists
                  - Applications
                  - Inputs
                  - Sources
                  - Add
                  - Draft
                  - Applications
                  - Versions
                  - Resources
                  - Mapping
                  - Batches
                  - Update
                  - Recommendations
                  - Status
                  - Create
                  - Components
                  - Templates
                  - Resiliency
                  - Policies
                  - Delete
                  - Assessments
                  - Inputs
                  - Source
                  - Describe
                  - Resources
                  - Resolutions
                  - Import
                  - To
                  - Lists
                  - Alarm
                  - Recommendations
                  - Compliance
                  - Drifts
                  - Assessments
                  - Compliance
                  - Sources
            /list-app-version-app-components:
              POST:
                summary: ListAppVersionAppComponents
                description: >-
                  <p>Lists all the Application Components in the Resilience Hub
                  application.</p>
                tags:
                  - Lists
                  - Applications
                  - Versions
                  - Components
                  - Add
                  - Draft
                  - Applications
                  - Versions
                  - Resources
                  - Mapping
                  - Batches
                  - Update
                  - Recommendations
                  - Status
                  - Create
                  - Components
                  - Templates
                  - Resiliency
                  - Policies
                  - Delete
                  - Assessments
                  - Inputs
                  - Source
                  - Describe
                  - Resources
                  - Resolutions
                  - Import
                  - To
                  - Lists
                  - Alarm
                  - Recommendations
                  - Compliance
                  - Drifts
                  - Assessments
                  - Compliance
                  - Sources
                  - Components
            /list-app-version-resource-mappings:
              POST:
                summary: ListAppVersionResourceMappings
                description: >-
                  <p>Lists how the resources in an application version are
                  mapped/sourced from. Mappings can be physical resource
                  identifiers, CloudFormation stacks, resource-groups, or an
                  application registry app.</p>
                tags:
                  - Lists
                  - Applications
                  - Versions
                  - Resources
                  - Mapping
                  - Add
                  - Draft
                  - Applications
                  - Versions
                  - Resources
                  - Mapping
                  - Batches
                  - Update
                  - Recommendations
                  - Status
                  - Create
                  - Components
                  - Templates
                  - Resiliency
                  - Policies
                  - Delete
                  - Assessments
                  - Inputs
                  - Source
                  - Describe
                  - Resources
                  - Resolutions
                  - Import
                  - To
                  - Lists
                  - Alarm
                  - Recommendations
                  - Compliance
                  - Drifts
                  - Assessments
                  - Compliance
                  - Sources
                  - Components
            /list-app-version-resources:
              POST:
                summary: ListAppVersionResources
                description: >-
                  <p>Lists all the resources in an Resilience Hub
                  application.</p>
                tags:
                  - Lists
                  - Applications
                  - Versions
                  - Resources
                  - Add
                  - Draft
                  - Applications
                  - Versions
                  - Resources
                  - Mapping
                  - Batches
                  - Update
                  - Recommendations
                  - Status
                  - Create
                  - Components
                  - Templates
                  - Resiliency
                  - Policies
                  - Delete
                  - Assessments
                  - Inputs
                  - Source
                  - Describe
                  - Resources
                  - Resolutions
                  - Import
                  - To
                  - Lists
                  - Alarm
                  - Recommendations
                  - Compliance
                  - Drifts
                  - Assessments
                  - Compliance
                  - Sources
                  - Components
            /list-app-versions:
              POST:
                summary: ListAppVersions
                description: >-
                  <p>Lists the different versions for the Resilience Hub
                  applications.</p>
                tags:
                  - Lists
                  - Applications
                  - Versions
                  - Add
                  - Draft
                  - Applications
                  - Versions
                  - Resources
                  - Mapping
                  - Batches
                  - Update
                  - Recommendations
                  - Status
                  - Create
                  - Components
                  - Templates
                  - Resiliency
                  - Policies
                  - Delete
                  - Assessments
                  - Inputs
                  - Source
                  - Describe
                  - Resources
                  - Resolutions
                  - Import
                  - To
                  - Lists
                  - Alarm
                  - Recommendations
                  - Compliance
                  - Drifts
                  - Assessments
                  - Compliance
                  - Sources
                  - Components
                  - Versions
            /list-apps:
              GET:
                summary: ListApps
                description: >-
                  <p>Lists your Resilience Hub applications.</p> <note> <p>You
                  can filter applications using only one filter at a time or
                  without using any filter. If you try to filter applications
                  using multiple filters, you will get the following error:</p>
                  <p> <code>An error occurred (ValidationException) when calling
                  the ListApps operation: Only one filter is supported for this
                  operation.</code> </p> </note>
                tags:
                  - Lists
                  - Applications
                  - Add
                  - Draft
                  - Applications
                  - Versions
                  - Resources
                  - Mapping
                  - Batches
                  - Update
                  - Recommendations
                  - Status
                  - Create
                  - Components
                  - Templates
                  - Resiliency
                  - Policies
                  - Delete
                  - Assessments
                  - Inputs
                  - Source
                  - Describe
                  - Resources
                  - Resolutions
                  - Import
                  - To
                  - Lists
                  - Alarm
                  - Recommendations
                  - Compliance
                  - Drifts
                  - Assessments
                  - Compliance
                  - Sources
                  - Components
                  - Versions
                  - Applications
            /list-recommendation-templates:
              GET:
                summary: ListRecommendationTemplates
                description: >-
                  <p>Lists the recommendation templates for the Resilience Hub
                  applications.</p>
                tags:
                  - Lists
                  - Recommendations
                  - Templates
                  - Add
                  - Draft
                  - Applications
                  - Versions
                  - Resources
                  - Mapping
                  - Batches
                  - Update
                  - Recommendations
                  - Status
                  - Create
                  - Components
                  - Templates
                  - Resiliency
                  - Policies
                  - Delete
                  - Assessments
                  - Inputs
                  - Source
                  - Describe
                  - Resources
                  - Resolutions
                  - Import
                  - To
                  - Lists
                  - Alarm
                  - Recommendations
                  - Compliance
                  - Drifts
                  - Assessments
                  - Compliance
                  - Sources
                  - Components
                  - Versions
                  - Applications
                  - Templates
            /list-resiliency-policies:
              GET:
                summary: ListResiliencyPolicies
                description: >-
                  <p>Lists the resiliency policies for the Resilience Hub
                  applications.</p>
                tags:
                  - Lists
                  - Resiliency
                  - Policies
                  - Add
                  - Draft
                  - Applications
                  - Versions
                  - Resources
                  - Mapping
                  - Batches
                  - Update
                  - Recommendations
                  - Status
                  - Create
                  - Components
                  - Templates
                  - Resiliency
                  - Policies
                  - Delete
                  - Assessments
                  - Inputs
                  - Source
                  - Describe
                  - Resources
                  - Resolutions
                  - Import
                  - To
                  - Lists
                  - Alarm
                  - Recommendations
                  - Compliance
                  - Drifts
                  - Assessments
                  - Compliance
                  - Sources
                  - Components
                  - Versions
                  - Applications
                  - Templates
                  - Policies
            /list-sop-recommendations:
              POST:
                summary: ListSopRecommendations
                description: >-
                  <p>Lists the standard operating procedure (SOP)
                  recommendations for the Resilience Hub applications.</p>
                tags:
                  - Lists
                  - Sop
                  - Recommendations
                  - Add
                  - Draft
                  - Applications
                  - Versions
                  - Resources
                  - Mapping
                  - Batches
                  - Update
                  - Recommendations
                  - Status
                  - Create
                  - Components
                  - Templates
                  - Resiliency
                  - Policies
                  - Delete
                  - Assessments
                  - Inputs
                  - Source
                  - Describe
                  - Resources
                  - Resolutions
                  - Import
                  - To
                  - Lists
                  - Alarm
                  - Recommendations
                  - Compliance
                  - Drifts
                  - Assessments
                  - Compliance
                  - Sources
                  - Components
                  - Versions
                  - Applications
                  - Templates
                  - Policies
                  - Sop
            /list-suggested-resiliency-policies:
              GET:
                summary: ListSuggestedResiliencyPolicies
                description: >-
                  <p>Lists the suggested resiliency policies for the Resilience
                  Hub applications.</p>
                tags:
                  - Lists
                  - Suggested
                  - Resiliency
                  - Policies
                  - Add
                  - Draft
                  - Applications
                  - Versions
                  - Resources
                  - Mapping
                  - Batches
                  - Update
                  - Recommendations
                  - Status
                  - Create
                  - Components
                  - Templates
                  - Resiliency
                  - Policies
                  - Delete
                  - Assessments
                  - Inputs
                  - Source
                  - Describe
                  - Resources
                  - Resolutions
                  - Import
                  - To
                  - Lists
                  - Alarm
                  - Recommendations
                  - Compliance
                  - Drifts
                  - Assessments
                  - Compliance
                  - Sources
                  - Components
                  - Versions
                  - Applications
                  - Templates
                  - Policies
                  - Sop
                  - Suggested
            /tags/{resourceArn}:
              DELETE:
                summary: UntagResource
                description: <p>Removes one or more tags from a resource.</p>
                tags:
                  - Untag
                  - Resources
                  - Add
                  - Draft
                  - Applications
                  - Versions
                  - Resources
                  - Mapping
                  - Batches
                  - Update
                  - Recommendations
                  - Status
                  - Create
                  - Components
                  - Templates
                  - Resiliency
                  - Policies
                  - Delete
                  - Assessments
                  - Inputs
                  - Source
                  - Describe
                  - Resources
                  - Resolutions
                  - Import
                  - To
                  - Lists
                  - Alarm
                  - Recommendations
                  - Compliance
                  - Drifts
                  - Assessments
                  - Compliance
                  - Sources
                  - Components
                  - Versions
                  - Applications
                  - Templates
                  - Policies
                  - Sop
                  - Suggested
                  - ARN
            /list-test-recommendations:
              POST:
                summary: ListTestRecommendations
                description: >-
                  <p>Lists the test recommendations for the Resilience Hub
                  application.</p>
                tags:
                  - Lists
                  - Tests
                  - Recommendations
                  - Add
                  - Draft
                  - Applications
                  - Versions
                  - Resources
                  - Mapping
                  - Batches
                  - Update
                  - Recommendations
                  - Status
                  - Create
                  - Components
                  - Templates
                  - Resiliency
                  - Policies
                  - Delete
                  - Assessments
                  - Inputs
                  - Source
                  - Describe
                  - Resources
                  - Resolutions
                  - Import
                  - To
                  - Lists
                  - Alarm
                  - Recommendations
                  - Compliance
                  - Drifts
                  - Assessments
                  - Compliance
                  - Sources
                  - Components
                  - Versions
                  - Applications
                  - Templates
                  - Policies
                  - Sop
                  - Suggested
                  - ARN
                  - Tests
            /list-unsupported-app-version-resources:
              POST:
                summary: ListUnsupportedAppVersionResources
                description: >-
                  <p>Lists the resources that are not currently supported in
                  Resilience Hub. An unsupported resource is a resource that
                  exists in the object that was used to create an app, but is
                  not supported by Resilience Hub.</p>
                tags:
                  - Lists
                  - Unsupported
                  - Applications
                  - Versions
                  - Resources
                  - Add
                  - Draft
                  - Applications
                  - Versions
                  - Resources
                  - Mapping
                  - Batches
                  - Update
                  - Recommendations
                  - Status
                  - Create
                  - Components
                  - Templates
                  - Resiliency
                  - Policies
                  - Delete
                  - Assessments
                  - Inputs
                  - Source
                  - Describe
                  - Resources
                  - Resolutions
                  - Import
                  - To
                  - Lists
                  - Alarm
                  - Recommendations
                  - Compliance
                  - Drifts
                  - Assessments
                  - Compliance
                  - Sources
                  - Components
                  - Versions
                  - Applications
                  - Templates
                  - Policies
                  - Sop
                  - Suggested
                  - ARN
                  - Tests
                  - Unsupported
            /publish-app-version:
              POST:
                summary: PublishAppVersion
                description: >-
                  <p>Publishes a new version of a specific Resilience Hub
                  application.</p>
                tags:
                  - Publish
                  - Applications
                  - Versions
                  - Add
                  - Draft
                  - Applications
                  - Versions
                  - Resources
                  - Mapping
                  - Batches
                  - Update
                  - Recommendations
                  - Status
                  - Create
                  - Components
                  - Templates
                  - Resiliency
                  - Policies
                  - Delete
                  - Assessments
                  - Inputs
                  - Source
                  - Describe
                  - Resources
                  - Resolutions
                  - Import
                  - To
                  - Lists
                  - Alarm
                  - Recommendations
                  - Compliance
                  - Drifts
                  - Assessments
                  - Compliance
                  - Sources
                  - Components
                  - Versions
                  - Applications
                  - Templates
                  - Policies
                  - Sop
                  - Suggested
                  - ARN
                  - Tests
                  - Unsupported
                  - Publish
            /put-draft-app-version-template:
              POST:
                summary: PutDraftAppVersionTemplate
                description: >-
                  <p>Adds or updates the app template for an Resilience Hub
                  application draft version.</p>
                tags:
                  - Put
                  - Draft
                  - Applications
                  - Versions
                  - Templates
                  - Add
                  - Draft
                  - Applications
                  - Versions
                  - Resources
                  - Mapping
                  - Batches
                  - Update
                  - Recommendations
                  - Status
                  - Create
                  - Components
                  - Templates
                  - Resiliency
                  - Policies
                  - Delete
                  - Assessments
                  - Inputs
                  - Source
                  - Describe
                  - Resources
                  - Resolutions
                  - Import
                  - To
                  - Lists
                  - Alarm
                  - Recommendations
                  - Compliance
                  - Drifts
                  - Assessments
                  - Compliance
                  - Sources
                  - Components
                  - Versions
                  - Applications
                  - Templates
                  - Policies
                  - Sop
                  - Suggested
                  - ARN
                  - Tests
                  - Unsupported
                  - Publish
                  - Put
            /remove-draft-app-version-resource-mappings:
              POST:
                summary: RemoveDraftAppVersionResourceMappings
                description: >-
                  <p>Removes resource mappings from a draft application
                  version.</p>
                tags:
                  - Removes
                  - Draft
                  - Applications
                  - Versions
                  - Resources
                  - Mapping
                  - Add
                  - Draft
                  - Applications
                  - Versions
                  - Resources
                  - Mapping
                  - Batches
                  - Update
                  - Recommendations
                  - Status
                  - Create
                  - Components
                  - Templates
                  - Resiliency
                  - Policies
                  - Delete
                  - Assessments
                  - Inputs
                  - Source
                  - Describe
                  - Resources
                  - Resolutions
                  - Import
                  - To
                  - Lists
                  - Alarm
                  - Recommendations
                  - Compliance
                  - Drifts
                  - Assessments
                  - Compliance
                  - Sources
                  - Components
                  - Versions
                  - Applications
                  - Templates
                  - Policies
                  - Sop
                  - Suggested
                  - ARN
                  - Tests
                  - Unsupported
                  - Publish
                  - Put
                  - Removes
            /resolve-app-version-resources:
              POST:
                summary: ResolveAppVersionResources
                description: <p>Resolves the resources for an application version.</p>
                tags:
                  - Resolve
                  - Applications
                  - Versions
                  - Resources
                  - Add
                  - Draft
                  - Applications
                  - Versions
                  - Resources
                  - Mapping
                  - Batches
                  - Update
                  - Recommendations
                  - Status
                  - Create
                  - Components
                  - Templates
                  - Resiliency
                  - Policies
                  - Delete
                  - Assessments
                  - Inputs
                  - Source
                  - Describe
                  - Resources
                  - Resolutions
                  - Import
                  - To
                  - Lists
                  - Alarm
                  - Recommendations
                  - Compliance
                  - Drifts
                  - Assessments
                  - Compliance
                  - Sources
                  - Components
                  - Versions
                  - Applications
                  - Templates
                  - Policies
                  - Sop
                  - Suggested
                  - ARN
                  - Tests
                  - Unsupported
                  - Publish
                  - Put
                  - Removes
                  - Resolve
            /start-app-assessment:
              POST:
                summary: StartAppAssessment
                description: >-
                  <p>Creates a new application assessment for an
                  application.</p>
                tags:
                  - Start
                  - Applications
                  - Assessments
                  - Add
                  - Draft
                  - Applications
                  - Versions
                  - Resources
                  - Mapping
                  - Batches
                  - Update
                  - Recommendations
                  - Status
                  - Create
                  - Components
                  - Templates
                  - Resiliency
                  - Policies
                  - Delete
                  - Assessments
                  - Inputs
                  - Source
                  - Describe
                  - Resources
                  - Resolutions
                  - Import
                  - To
                  - Lists
                  - Alarm
                  - Recommendations
                  - Compliance
                  - Drifts
                  - Assessments
                  - Compliance
                  - Sources
                  - Components
                  - Versions
                  - Applications
                  - Templates
                  - Policies
                  - Sop
                  - Suggested
                  - ARN
                  - Tests
                  - Unsupported
                  - Publish
                  - Put
                  - Removes
                  - Resolve
                  - Start
            /update-app:
              POST:
                summary: UpdateApp
                description: <p>Updates an application.</p>
                tags:
                  - Update
                  - Applications
                  - Add
                  - Draft
                  - Applications
                  - Versions
                  - Resources
                  - Mapping
                  - Batches
                  - Update
                  - Recommendations
                  - Status
                  - Create
                  - Components
                  - Templates
                  - Resiliency
                  - Policies
                  - Delete
                  - Assessments
                  - Inputs
                  - Source
                  - Describe
                  - Resources
                  - Resolutions
                  - Import
                  - To
                  - Lists
                  - Alarm
                  - Recommendations
                  - Compliance
                  - Drifts
                  - Assessments
                  - Compliance
                  - Sources
                  - Components
                  - Versions
                  - Applications
                  - Templates
                  - Policies
                  - Sop
                  - Suggested
                  - ARN
                  - Tests
                  - Unsupported
                  - Publish
                  - Put
                  - Removes
                  - Resolve
                  - Start
            /update-app-version:
              POST:
                summary: UpdateAppVersion
                description: >-
                  <p>Updates the Resilience Hub application version.</p> <note>
                  <p>This API updates the Resilience Hub application draft
                  version. To use this information for running resiliency
                  assessments, you must publish the Resilience Hub application
                  using the <code>PublishAppVersion</code> API.</p> </note>
                tags:
                  - Update
                  - Applications
                  - Versions
                  - Add
                  - Draft
                  - Applications
                  - Versions
                  - Resources
                  - Mapping
                  - Batches
                  - Update
                  - Recommendations
                  - Status
                  - Create
                  - Components
                  - Templates
                  - Resiliency
                  - Policies
                  - Delete
                  - Assessments
                  - Inputs
                  - Source
                  - Describe
                  - Resources
                  - Resolutions
                  - Import
                  - To
                  - Lists
                  - Alarm
                  - Recommendations
                  - Compliance
                  - Drifts
                  - Assessments
                  - Compliance
                  - Sources
                  - Components
                  - Versions
                  - Applications
                  - Templates
                  - Policies
                  - Sop
                  - Suggested
                  - ARN
                  - Tests
                  - Unsupported
                  - Publish
                  - Put
                  - Removes
                  - Resolve
                  - Start
            /update-app-version-app-component:
              POST:
                summary: UpdateAppVersionAppComponent
                description: >-
                  <p>Updates an existing Application Component in the Resilience
                  Hub application.</p> <note> <p>This API updates the Resilience
                  Hub application draft version. To use this Application
                  Component for running assessments, you must publish the
                  Resilience Hub application using the
                  <code>PublishAppVersion</code> API.</p> </note>
                tags:
                  - Update
                  - Applications
                  - Versions
                  - Components
                  - Add
                  - Draft
                  - Applications
                  - Versions
                  - Resources
                  - Mapping
                  - Batches
                  - Update
                  - Recommendations
                  - Status
                  - Create
                  - Components
                  - Templates
                  - Resiliency
                  - Policies
                  - Delete
                  - Assessments
                  - Inputs
                  - Source
                  - Describe
                  - Resources
                  - Resolutions
                  - Import
                  - To
                  - Lists
                  - Alarm
                  - Recommendations
                  - Compliance
                  - Drifts
                  - Assessments
                  - Compliance
                  - Sources
                  - Components
                  - Versions
                  - Applications
                  - Templates
                  - Policies
                  - Sop
                  - Suggested
                  - ARN
                  - Tests
                  - Unsupported
                  - Publish
                  - Put
                  - Removes
                  - Resolve
                  - Start
            /update-app-version-resource:
              POST:
                summary: UpdateAppVersionResource
                description: >-
                  <p>Updates the resource details in the Resilience Hub
                  application.</p> <note> <ul> <li> <p>This action has no effect
                  outside Resilience Hub.</p> </li> <li> <p>This API updates the
                  Resilience Hub application draft version. To use this resource
                  for running resiliency assessments, you must publish the
                  Resilience Hub application using the
                  <code>PublishAppVersion</code> API.</p> </li> <li> <p>To
                  update application version with new
                  <code>physicalResourceID</code>, you must call
                  <code>ResolveAppVersionResources</code> API.</p> </li> </ul>
                  </note>
                tags:
                  - Update
                  - Applications
                  - Versions
                  - Resources
                  - Add
                  - Draft
                  - Applications
                  - Versions
                  - Resources
                  - Mapping
                  - Batches
                  - Update
                  - Recommendations
                  - Status
                  - Create
                  - Components
                  - Templates
                  - Resiliency
                  - Policies
                  - Delete
                  - Assessments
                  - Inputs
                  - Source
                  - Describe
                  - Resources
                  - Resolutions
                  - Import
                  - To
                  - Lists
                  - Alarm
                  - Recommendations
                  - Compliance
                  - Drifts
                  - Assessments
                  - Compliance
                  - Sources
                  - Components
                  - Versions
                  - Applications
                  - Templates
                  - Policies
                  - Sop
                  - Suggested
                  - ARN
                  - Tests
                  - Unsupported
                  - Publish
                  - Put
                  - Removes
                  - Resolve
                  - Start
            /update-resiliency-policy:
              POST:
                summary: UpdateResiliencyPolicy
                description: >-
                  <p>Updates a resiliency policy.</p> <note> <p>Resilience Hub
                  allows you to provide a value of zero for
                  <code>rtoInSecs</code> and <code>rpoInSecs</code> of your
                  resiliency policy. But, while assessing your application, the
                  lowest possible assessment result is near zero. Hence, if you
                  provide value zero for <code>rtoInSecs</code> and
                  <code>rpoInSecs</code>, the estimated workload RTO and
                  estimated workload RPO result will be near zero and the
                  <b>Compliance status</b> for your application will be set to
                  <b>Policy breached</b>.</
                tags:
                  - Update
                  - Resiliency
                  - Policies
                  - Add
                  - Draft
                  - Applications
                  - Versions
                  - Resources
                  - Mapping
                  - Batches
                  - Update
                  - Recommendations
                  - Status
                  - Create
                  - Components
                  - Templates
                  - Resiliency
                  - Policies
                  - Delete
                  - Assessments
                  - Inputs
                  - Source
                  - Describe
                  - Resources
                  - Resolutions
                  - Import
                  - To
                  - Lists
                  - Alarm
                  - Recommendations
                  - Compliance
                  - Drifts
                  - Assessments
                  - Compliance
                  - Sources
                  - Components
                  - Versions
                  - Applications
                  - Templates
                  - Policies
                  - Sop
                  - Suggested
                  - ARN
                  - Tests
                  - Unsupported
                  - Publish
                  - Put
                  - Removes
                  - Resolve
                  - Sta
    overlays:
      - type: APIs.io Search
        url: overlays/resiliencehub-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/resiliencehub-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:resiliencehub
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---