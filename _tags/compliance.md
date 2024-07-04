---
name: Compliance
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/compliance.png
url: https://example.com/apis/compliance.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Compliance
apis:
  - name: Adyen Hosted Onboarding API
    description: >-
      The Fund API provides endpoints for managing the funds in the accounts on
      your platform. These management operations include, for example, the
      transfer of funds from one account to another, the payout of funds to an
      account holder, and the retrieval of balances in an account.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: >-
      https://docs.adyen.com/marketplaces-and-platforms/collect-verification-details/hosted/
    baseURL: https://api.example.com
    tags: []
    properties:
      - type: Documentation
        url: >-
          https://docs.adyen.com/marketplaces-and-platforms/collect-verification-details/hosted/
      - type: OpenAPI
        data:
          openapi: 3.1.0
          info:
            x-publicVersion: true
            title: Hosted Onboarding API
            x-timestamp: '2023-05-30T15:27:20Z'
          x-groups:
            - Hosted Onboarding Page
            - PCI Compliance Questionnaire Page
          tags:
            - name: Hosted Onboarding Page
            - name: PCI Compliance Questionnaire Page
          paths:
            /getOnboardingUrl:
              post:
                tags:
                  - Get
                  - Link
                  - To
                  - Adyen-hosted
                  - Onboarding
                  - Page
                  - Onboarding
                  - URL
                summary: Get a link to a Adyen-hosted onboarding page
                description: >-
                  Returns a link to an Adyen-hosted onboarding page (HOP) that
                  you can send to your account holder. For more information on
                  how to use HOP, refer to [Hosted
                  onboarding](https://docs.adyen.com/marketplaces-and-platforms/classic/collect-verification-details/hosted-onboarding-page). 
            /getPciQuestionnaireUrl:
              post:
                tags:
                  - Get
                  - Link
                  - To
                  - Compliance
                  - Questionnaires
                  - Onboarding
                  - URL
                  - PCI
                  - Questionnaires
                summary: Get a link to a PCI compliance questionnaire
                description: >-
                  Returns a link to a PCI compliance questionnaire that you can
                  send to your account holder.
                   > You should only use this endpoint if you have a [partner platform setup](https://docs.adyen.com/marketplaces-and-platform
    overlays:
      - type: APIs.io Search
        url: overlays/hosted-onboarding-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/hosted-onboarding-openapi-api-evangelist-ratings.yml
    aid: adyen:adyen-hosted-onboarding-api
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
  - name: FactSet Real-Time Quotes API
    description: >-
      The Quotes API combines endpoints for retrieving security end-of-day,
      delayed, and realtime prices with performance key figures and basic
      reference data on the security and market level.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.factset.com/api-catalog/real-time-quotes-api
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: >-
          https://developer.factset.com/api-catalog/real-time-quotes-api#overview
      - type: SDKs
        url: >-
          https://developer.factset.com/api-catalog/real-time-quotes-api#sdkLibrary
      - type: Jupyter Notebooks
        url: >-
          https://developer.factset.com/api-catalog/real-time-quotes-api#notebooks
      - type: Code Snippets
        url: >-
          https://developer.factset.com/api-catalog/real-time-quotes-api#codeSnippet
      - type: Change Log
        url: >-
          https://developer.factset.com/api-catalog/real-time-quotes-api#changelog
      - type: OpenAPI
        data:
          openapi: 3.0.0
          info:
            title: Quotes API For Digital Portals
            license:
              name: Apache License, Version 2.0
              url: https://www.apache.org/licenses/LICENSE-2.0
          paths:
            /basic/assetClass/list:
              get:
                tags:
                  - List
                  - Of
                  - Asset
                  - Classes.
                  - Class
                  - List
                description: List of asset classes as defined by FactSet Digital Solutions.
                summary: List of asset classes.
            /basic/backgroundText/type/list:
              post:
                tags:
                  - List
                  - Of
                  - Background
                  - Text
                  - Types.
                  - Class
                  - List
                  - Text
                  - Type
                summary: List of background text types.
                description: List of background text types.
            /basic/benchmark/type/list:
              get:
                tags:
                  - List
                  - Of
                  - Benchmark
                  - Types.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                summary: List of benchmark types.
                description: List of benchmark types.
            /basic/delivery/list:
              post:
                tags:
                  - List
                  - Of
                  - Deliveries.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                summary: List of deliveries.
                description: List of deliveries.
            /basic/frequency/type/list:
              get:
                tags:
                  - List
                  - Of
                  - Frequency
                  - Types.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                summary: List of frequency types.
                description: List of frequency types.
            /basic/language/get:
              get:
                tags:
                  - Details
                  - For
                  - Language.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                description: Details for a language.
                summary: Details for a language.
            /basic/language/getByCode:
              get:
                tags:
                  - Details
                  - For
                  - Language
                  - Identified
                  - By
                  - Code.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                description: Details for a language identified by code.
                summary: Details for a language identified by code.
            /basic/language/list:
              get:
                tags:
                  - List
                  - Of
                  - Languages.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                description: List of languages.
                summary: List of languages.
            /basic/market/get:
              get:
                tags:
                  - Details
                  - Of
                  - Market.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                description: Details of a market.
                summary: Details of a market.
            /basic/market/list:
              post:
                tags:
                  - List
                  - Of
                  - Markets.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                description: List of markets.
                summary: List of markets.
            /basic/market/group/list:
              get:
                tags:
                  - List
                  - Of
                  - Market
                  - Groups.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                description: List of market groups.
                summary: List of market groups.
            /basic/market/type/list:
              get:
                tags:
                  - List
                  - Of
                  - Market
                  - Types.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                description: List of market types.
                summary: List of market types.
            /basic/media/kind/list:
              get:
                tags:
                  - List
                  - Of
                  - Media
                  - Kinds.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                summary: List of media kinds.
                description: List of media kinds.
            /basic/media/type/list:
              post:
                tags:
                  - List
                  - Of
                  - Internet
                  - Media
                  - Types.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                description: >-
                  List of Internet media types. See
                  http://www.iana.org/assignments/media-types/ for further
                  details. Not all such Internet media types are available on
                  the MDG.
                summary: List of Internet media types.
            /basic/mic/operating/list:
              post:
                tags:
                  - List
                  - Of
                  - Operating
                  - Market
                  - Identifier
                  - Codes
                  - C).
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                summary: List of operating market identifier codes (MIC).
                description: List of operating market identifier codes (MIC).
            /basic/region/get:
              get:
                tags:
                  - Details
                  - For
                  - Region.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                summary: Details for a region.
                description: Details for a geographic, political, or economic region.
            /basic/region/list:
              get:
                tags:
                  - List
                  - Of
                  - Regions.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                summary: List of regions.
                description: List of geographic, political, and economic regions.
            /basic/region/continent/get:
              get:
                tags:
                  - Details
                  - For
                  - Continent.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                summary: Details for a continent.
                description: Details for a continent.
            /basic/region/continent/list:
              get:
                tags:
                  - List
                  - Of
                  - Continents.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                summary: List of continents.
                description: List of continents.
            /basic/region/country/get:
              get:
                tags:
                  - Details
                  - For
                  - Country.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                summary: Details for a country.
                description: Details for a country.
            /basic/region/country/getByCode:
              get:
                tags:
                  - Details
                  - For
                  - Country
                  - Identified
                  - By
                  - Code.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                summary: Details for a country identified by code.
                description: Details for a country identified by code.
            /basic/region/country/list:
              get:
                tags:
                  - List
                  - Of
                  - Countries.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                summary: List of countries.
                description: List of countries.
            /basic/timezone/get:
              get:
                tags:
                  - Details
                  - Of
                  - Timezone.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                description: >-
                  Details of a timezone identified by id, as specified by the
                  Internet Assigned Numbers Authority. See
                  http://www.iana.org/time-zones for further details. Not all
                  such timezones are available on the MDG.
                summary: Details of a timezone.
            /basic/timezone/getByName:
              get:
                tags:
                  - Details
                  - Of
                  - Timezone
                  - Identified
                  - By
                  - Name.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                description: >-
                  Details of a timezone identified by name, as specified by the
                  Internet Assigned Numbers Authority. See
                  http://www.iana.org/time-zones for further details. Not all
                  such timezones are available on the MDG.
                summary: Details of a timezone identified by name.
            /basic/timezone/list:
              post:
                tags:
                  - List
                  - Of
                  - Timezones.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                description: >-
                  List of timezones identified by id, as specified by the
                  Internet Assigned Numbers Authority. See
                  http://www.iana.org/time-zones for further details. Not all
                  such timezones are available on the MDG.
                summary: List of timezones.
            /basic/valueUnit/get:
              get:
                tags:
                  - Details
                  - Of
                  - Value
                  - Unit.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                summary: Details of a value unit.
                description: Details of a value unit.
            /basic/valueUnit/list:
              post:
                tags:
                  - List
                  - Of
                  - Value
                  - Units.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                summary: List of value units.
                description: List of value units.
            /basic/valueUnit/alternative/list:
              get:
                tags:
                  - List
                  - Of
                  - Alternative
                  - Units.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                description: List of alternative units.
                summary: List of alternative units.
            /basic/valueUnit/currency/list:
              post:
                tags:
                  - List
                  - Of
                  - Currencies.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                summary: List of currencies.
                description: List of currencies.
            /basic/valueUnit/currency/fractional/get:
              get:
                tags:
                  - Details
                  - Of
                  - Fractional
                  - Currency.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                summary: Details of a fractional currency.
                description: Details of a fractional currency.
            /basic/valueUnit/currency/fractional/list:
              get:
                tags:
                  - List
                  - Of
                  - Fractional
                  - Currencies.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                summary: List of fractional currencies.
                description: List of fractional currencies.
            /basic/valueUnit/currency/main/list:
              post:
                tags:
                  - List
                  - Of
                  - Main
                  - Currencies.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                summary: List of main currencies.
                description: List of main currencies.
            /category/get:
              get:
                tags:
                  - Details
                  - Of
                  - Category.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                summary: Details of a category.
                description: Details of a category.
            /category/list:
              get:
                tags:
                  - List
                  - Of
                  - Categories.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                summary: List of categories.
                description: List of categories.
            /category/listByLevel:
              get:
                tags:
                  - List
                  - Of
                  - Categories
                  - Assigned
                  - To
                  - Category
                  - Level.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                summary: List of categories assigned to a category level.
                description: List of categories assigned to a category level.
            /category/listBySystem:
              get:
                tags:
                  - List
                  - Of
                  - Categories
                  - Assigned
                  - To
                  - Category
                  - System.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                summary: List of categories assigned to a category system.
                description: List of categories assigned to a category system.
            /category/dataset/list:
              get:
                tags:
                  - List
                  - Of
                  - Entitled
                  - Category
                  - Datasets.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                summary: List of entitled category datasets.
                description: List of entitled category datasets.
            /category/instrument/list:
              get:
                tags:
                  - List
                  - Of
                  - Instruments
                  - Where
                  - Specific
                  - Dataset
                  - Has
                  - Assigned
                  - Given
                  - Category.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                summary: >-
                  List of instruments where a specific dataset has assigned a
                  given category.
                description: >-
                  List of instruments where a specific dataset has assigned a
                  given category.
            /category/level/get:
              get:
                tags:
                  - Details
                  - Of
                  - Category
                  - Level.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                summary: Details of a category level.
                description: Details of a category level.
            /category/path/get:
              get:
                tags:
                  - Path
                  - From
                  - The
                  - First
                  - Level
                  - To
                  - Of
                  - Specific
                  - Category.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                summary: Path from the first level to the level of a specific category.
                description: Path from the first level to the level of a specific category.
            /category/system/get:
              get:
                tags:
                  - Details
                  - Of
                  - An
                  - Entitled
                  - Category
                  - System.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                summary: Details of an entitled category system.
                description: Details of an entitled category system.
            /category/system/list:
              get:
                tags:
                  - List
                  - Of
                  - Entitled
                  - Category
                  - Systems.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                summary: List of entitled category systems.
                description: List of entitled category systems.
            /category/system/type/list:
              get:
                tags:
                  - List
                  - Of
                  - Category
                  - System
                  - Types.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                summary: List of category system types.
                description: List of category system types.
            /instrument/get:
              get:
                tags:
                  - Basic
                  - Data
                  - For
                  - An
                  - Instrument.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                description: Basic data for an instrument.
                summary: Basic data for an instrument.
            /instrument/getByNotation:
              get:
                tags:
                  - Basic
                  - Data
                  - For
                  - An
                  - Instrument.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                description: Basic data for an instrument.
                summary: Basic data for an instrument.
            /instrument/backgroundText/list:
              get:
                tags:
                  - Background
                  - Texts
                  - Of
                  - An
                  - Instrument.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                summary: Background texts of an instrument.
                description: Background texts of an instrument.
            /instrument/backgroundText/type/list:
              post:
                tags:
                  - List
                  - Of
                  - Background
                  - Text
                  - Types
                  - For
                  - Instruments.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                summary: List of background text types for instruments.
                description: List of background text types for instruments.
            /instrument/benchmark/list:
              post:
                tags:
                  - List
                  - Of
                  - Benchmarks
                  - Financial
                  - Instrument.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                summary: List of benchmarks of a financial instrument.
                description: >-
                  Provides a list of benchmark notations for a selected
                  financial instrument, optionally restricted to specific
                  benchmark types.
            /instrument/category/list:
              post:
                tags:
                  - List
                  - Of
                  - Categories
                  - Assigned
                  - To
                  - Specific
                  - Instrument
                  - The
                  - Application
                  - Is
                  - Entitled
                  - See.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                summary: >-
                  List of categories assigned to a specific instrument the
                  application is entitled to see.
                description: >-
                  List of categories assigned to a specific instrument the
                  application is entitled to see. Optionally it is possible to
                  restrict the output to only list those for a specific category
                  dataset.
            /instrument/complianceProperty/list:
              post:
                tags:
                  - List
                  - Of
                  - Compliance
                  - Properties
                  - For
                  - Instruments.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                summary: List of compliance properties for instruments.
                description: List of compliance properties for instruments.
            /instrument/complianceProperty/listByInstrument:
              get:
                tags:
                  - Compliance
                  - Properties
                  - Of
                  - An
                  - Instrument.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                summary: Compliance properties of an instrument.
                description: Compliance properties of an instrument.
            /instrument/composite/get:
              get:
                tags:
                  - Composite
                  - Instrument
                  - And
                  - Its
                  - Components.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                summary: Composite instrument and its components.
                description: Composite instrument and its components.
            /instrument/coupon/list:
              get:
                tags:
                  - List
                  - Of
                  - Coupons
                  - For
                  - An
                  - Interest-bearing
                  - Instrument.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                summary: List of coupons for an interest-bearing instrument.
                description: >-
                  List of coupons for an interest-bearing instrument; any other
                  instrument yields empty values. The endpoint provides details
                  regarding the coupon period, the respective interest rate, and
                  payable amount (the latter only for instruments with a fixed
                  nominal value). The list of coupons is generally not available
                  for a perpetual, i.e. without a predefined maturity date,
                  interst-bearing instrument. 


                  If there is no entitled provider supplying a full list of
                  coupons, the list will be synthesized from summary data
                  available from entitled suppliers (if any). Since the exact
                  product terms are not known, e.g. the handling of holidays and
                  weekends, the list may be imprecise.
            /instrument/coupon/dayCountConvention/type/list:
              get:
                tags:
                  - List
                  - Of
                  - Day
                  - Count
                  - Convention
                  - Types.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                summary: List of day count convention types.
                description: List of day count convention types.
            /instrument/coupon/interestRate/type/list:
              get:
                tags:
                  - List
                  - Of
                  - Interest
                  - Rate
                  - Types.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                summary: List of interest rate types.
                description: List of interest rate types.
            /instrument/coupon/keyData/get:
              get:
                tags:
                  - Interest
                  - Rate
                  - Details
                  - For
                  - Selected
                  - Periods
                  - Of
                  - An
                  - Interest-bearing
                  - Instrument.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                summary: >-
                  Interest rate details for selected periods of an
                  interest-bearing instrument.
                description: >-
                  Interest rate details for selected periods of an
                  interest-bearing instrument; any other instrument yields empty
                  values.
            /instrument/crossReference/getByISIN:
              get:
                tags:
                  - Translate
                  - To
                  - Instrument.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                description: >-
                  Translate a given ISIN to the respective most recent
                  instrument identifier, retrieved from the Cross Reference
                  Service.
                summary: Translate ISIN to instrument.
            /instrument/crossReference/getByWKN:
              get:
                tags:
                  - Translate
                  - To
                  - Instrument.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                description: >-
                  Translate a given WKN to the respective most recent instrument
                  identifier, retrieved from the Cross Reference Service.
                summary: Translate WKN to instrument.
            /instrument/crossReference/listByISIN:
              post:
                tags:
                  - Translate
                  - List
                  - Of
                  - Ns
                  - To
                  - Instruments.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                description: >-
                  Translate a given list of ISINs to the respective most recent
                  instrument identifiers, retrieved from the Cross Reference
                  Service.
                summary: Translate a list of ISINs to instruments.
            /instrument/crossReference/listByWKN:
              post:
                tags:
                  - Translate
                  - List
                  - Of
                  - Ns
                  - To
                  - Instruments.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                description: >-
                  Translate a given list of WKNs to the respective most recent
                  instrument identifiers, retrieved from the Cross Reference
                  Service.
                summary: Translate a list of WKNs to instruments.
            /instrument/crossReference/history/getByISIN:
              get:
                tags:
                  - To
                  - Instrument
                  - Translation
                  - History.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                description: >-
                  Retrieve the complete translation history of a given ISIN to
                  the respective instrument association from the Cross Reference
                  Service. The results are sorted in descending order, starting
                  with the most recent.
                summary: ISIN to instrument translation history.
            /instrument/crossReference/history/getByWKN:
              get:
                tags:
                  - To
                  - Instrument
                  - Translation
                  - History.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                description: >-
                  Retrieve the complete translation history of a given WKN to
                  the respective instrument association from the Cross Reference
                  Service. The results are sorted in descending order, starting
                  with the most recent.
                summary: WKN to instrument translation history.
            /instrument/exchangeRate/get:
              get:
                tags:
                  - Retrieve
                  - An
                  - Exchange
                  - Rate
                  - Instrument
                  - Identifier.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                description: >-
                  Retrieve an exchange rate instrument identifier using the
                  identifier of the main currencies represented by that exchange
                  rate. 

                   An error is returned if one of the provided parameters is invalid or if no instrument is associated with the given combination of parameters.
                summary: Retrieve an exchange rate instrument identifier.
            /instrument/exchangeRate/getByISOCode:
              get:
                tags:
                  - Retrieve
                  - An
                  - Exchange
                  - Rate
                  - Instrument
                  - Identifier.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                description: >-
                  Retrieve an exchange rate instrument identifier using the ISO
                  4217 code of the main currencies represented by that exchange
                  rate. 


                  An error is returned if one of the provided parameters is
                  invalid or if no instrument is associated with the given
                  combination of parameters.
                summary: Retrieve an exchange rate instrument identifier.
            /instrument/legalEntity/backgroundText/list:
              get:
                tags:
                  - Role-specific
                  - Background
                  - Texts
                  - Of
                  - Legal
                  - Entities
                  - Related
                  - To
                  - An
                  - Instrument.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                summary: >-
                  Role-specific background texts of legal entities related to an
                  instrument.
                description: >-
                  Role-specific background texts of legal entities related to an
                  instrument.
            /instrument/legalEntity/complianceProperty/list:
              get:
                tags:
                  - Role-specific
                  - Compliance
                  - Properties
                  - Of
                  - Legal
                  - Entities
                  - Related
                  - To
                  - An
                  - Instrument.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                summary: >-
                  Role-specific compliance properties of legal entities related
                  to an instrument.
                description: >-
                  Role-specic compliance properties of legal entities related to
                  an instrument.
            /instrument/mifid/get:
              get:
                tags:
                  - Mi
                  - Data
                  - For
                  - Financial
                  - Instrument.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                description: >-
                  MiFID II data for a specified financial instrument. The
                  instruments governed by MiFID II are called "investment
                  products".
                summary: MiFID II data for a financial instrument.
            /instrument/notation/list:
              post:
                tags:
                  - List
                  - Of
                  - Active,
                  - Entitled
                  - Notations
                  - For
                  - Set
                  - Instruments.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                summary: List of active, entitled notations for a set of instruments.
                description: >-
                  List of active, entitled notations for a set of instruments.
                  By default the list of notations (per instrument) is sorted
                  descending by the trading volume, averaged over one month. All
                  identifiers used as parameters must be valid and entitled.
            /instrument/rating/grade/list:
              post:
                tags:
                  - List
                  - Of
                  - Rating
                  - Grades
                  - For
                  - Instruments.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                description: >-
                  List of rating grades for a list of instruments. The list can
                  be restricted to rating grades belonging to particular rating
                  systems.
                summary: List of rating grades for a list of instruments.
            /instrument/selectionList/list:
              get:
                tags:
                  - Set
                  - Of
                  - Custom
                  - Instrument-level
                  - Selection
                  - Lists.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                description: Set of custom instrument-level selection lists.
                summary: Set of custom instrument-level selection lists.
            /instrument/selectionList/listByInstrument:
              get:
                tags:
                  - For
                  - Each
                  - Given
                  - Instrument,
                  - Returns
                  - The
                  - Instrument-level
                  - Selection
                  - Lists
                  - Of
                  - Which
                  - Instrument
                  - Is
                  - Member.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                description: >-
                  For each given instrument, returns the instrument-level
                  selection lists of which the instrument is a member.
                summary: >-
                  For each given instrument, returns the instrument-level
                  selection lists of which the instrument is a member.
            /instrument/selectionList/members/list:
              post:
                tags:
                  - List
                  - Of
                  - Instruments
                  - Belonging
                  - To
                  - An
                  - Instrument-level
                  - Selection
                  - List.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                summary: >-
                  List of instruments belonging to an instrument-level selection
                  list.
                description: >-
                  List of instruments belonging to an instrument-level selection
                  list.
            /notation/get:
              get:
                tags:
                  - Basic
                  - Data
                  - For
                  - Notation.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                description: Basic data for a notation.
                summary: Basic data for a notation.
            /notation/list:
              get:
                tags:
                  - Basic
                  - Data
                  - For
                  - List
                  - Of
                  - Notations.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                description: Basic data for a list of notations.
                summary: Basic data for a list of notations.
            /notation/category/list:
              post:
                tags:
                  - List
                  - Of
                  - Categories
                  - Assigned
                  - To
                  - Specific
                  - Notation
                  - The
                  - Application
                  - Is
                  - Entitled
                  - See.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                description: >-
                  List of categories assigned to a specific notation the
                  application is entitled to see. Optionally it is possible to
                  restrict the output to only list those for a specific category
                  dataset.
                summary: >-
                  List of categories assigned to a specific notation the
                  application is entitled to see.
            /notation/crossReference/getByFactSetMarketSymbol:
              get:
                tags:
                  - Translate
                  - Fact
                  - Set
                  - Market
                  - Symbol
                  - To
                  - Notation.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                summary: Translate a FactSet market symbol to a notation.
                description: >-
                  Translate a FactSet market symbol to a notation. This symbol
                  is also known as TICKER_EXCHANGE.
            /notation/crossReference/listByInstrument:
              post:
                tags:
                  - List
                  - Of
                  - Entitled
                  - Notations.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                summary: List of entitled notations.
                description: List of entitled notations.
            /notation/crossReference/listByISIN:
              post:
                tags:
                  - List
                  - Of
                  - Entitled
                  - Notations.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                summary: List of entitled notations.
                description: List of entitled notations.
            /notation/crossReference/listBySymbol:
              post:
                tags:
                  - List
                  - Of
                  - Entitled
                  - Notations.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                summary: List of entitled notations.
                description: >-
                  List of entitled notations. Symbols are not globally unique;
                  therefore, a given symbol interpreted in different markets
                  might refer to different instruments.
            /notation/crossReference/factSetIdentifier/get:
              get:
                tags:
                  - Retrieve
                  - Fact
                  - Set
                  - Identifiers
                  - For
                  - Given
                  - Notation.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                summary: Retrieve FactSet identifiers for a given notation.
                description: >-
                  <p>Retrieve FactSet identifiers for a given notation. Security
                  and listing-level identifiers are always included, regional
                  level identifiers are included, if available.
            /notation/crossReference/factSetIdentifier/listByFactSetIdentifier:
              post:
                tags:
                  - Retrieve
                  - List
                  - Of
                  - Notations
                  - For
                  - Given
                  - Fact
                  - Set
                  - Identifier.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                summary: Retrieve a list of notations for a given FactSet identifier.
                description: >-
                  <p>Retrieve a list of notations for a given FactSet
                  identifier, grouped by regional identifiers, if available.
                  Listings without a regional identifier are grouped at the end
                  of the response.</p><p>The notation corresponding to the
                  security's primary listing has the attributes
                  <big><tt>regional.isPrimary</tt></big> and
                  <big><tt>regional.listing.isPrimary</tt></big> both set to
                  true.The security's primary listing might not be among the
                  results depending on the entitlement.</p><p>See the group
                  description for more information about the security's primary
                  listing.</p>
            /notation/crossReference/factSetIdentifier/listByInstrument:
              post:
                tags:
                  - Retrieve
                  - List
                  - Of
                  - Fact
                  - Set
                  - Identifiers
                  - For
                  - Given
                  - Instrument.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                summary: Retrieve a list of FactSet identifiers for a given instrument.
                description: >-
                  <p>Retrieve a list of FactSet identifiers for a given
                  instrument, grouped by regional identifiers, if available.
                  Listings without a regional identifier are grouped at the end
                  of the response.</p><p>The notation corresponding to the
                  security's primary listing has the attributes
                  <big><tt>regional.isPrimary</tt></big> and
                  <big><tt>regional.listing.isPrimary</tt></big> both set to
                  true.The security's primary listing might not be among the
                  results depending on the entitlement.</p><p>The result
                  contains only notations that have at least one FactSet
                  identifier (see
                  <big><tt>listing.permanentIdentifier</tt></big>,
                  <big><tt>listing.tickerExchange</tt></big>).</p><p>See the
                  group description for more information about the security's
                  primary listing.</p>
            /notation/keyFigures/year/10/get:
              get:
                tags:
                  - End-of-day
                  - D)
                  - Key
                  - Figures
                  - For
                  - The
                  - Time
                  - Range
                  - Of
                  - Ten
                  - Years.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                summary: End-of-day (EOD) key figures for the time range of ten years.
                description: End-of-day (EOD) key figures for the time range of ten years.
            /notation/keyFigures/year/10/list:
              get:
                tags:
                  - End-of-day
                  - D)
                  - Key
                  - Figures
                  - For
                  - The
                  - Time
                  - Range
                  - Of
                  - Ten
                  - Years,
                  - List
                  - Notations.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                summary: >-
                  End-of-day (EOD) key figures for the time range of ten years,
                  for a list of notations.
                description: >-
                  End-of-day (EOD) key figures for the time range of ten years,
                  for a list of notations.
            /notation/keyFigures/month/1/get:
              get:
                tags:
                  - End-of-day
                  - D)
                  - Key
                  - Figures
                  - For
                  - The
                  - Time
                  - Range
                  - Of
                  - One
                  - Month.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                summary: End-of-day (EOD) key figures for the time range of one month.
                description: End-of-day (EOD) key figures for the time range of one month.
            /notation/keyFigures/month/1/list:
              get:
                tags:
                  - End-of-day
                  - D)
                  - Key
                  - Figures
                  - For
                  - The
                  - Time
                  - Range
                  - Of
                  - One
                  - Month,
                  - List
                  - Notations.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                summary: >-
                  End-of-day (EOD) key figures for the time range of one month,
                  for a list of notations.
                description: >-
                  End-of-day (EOD) key figures for the time range of one month,
                  for a list of notations.
            /notation/keyFigures/week/1/get:
              get:
                tags:
                  - End-of-day
                  - D)
                  - Key
                  - Figures
                  - For
                  - The
                  - Time
                  - Range
                  - Of
                  - One
                  - Week.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                summary: End-of-day (EOD) key figures for the time range of one week.
                description: End-of-day (EOD) key figures for the time range of one week.
            /notation/keyFigures/week/1/list:
              get:
                tags:
                  - End-of-day
                  - D)
                  - Key
                  - Figures
                  - For
                  - The
                  - Time
                  - Range
                  - Of
                  - One
                  - Week,
                  - List
                  - Notations.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                summary: >-
                  End-of-day (EOD) key figures for the time range of one week,
                  for a list of notations.
                description: >-
                  End-of-day (EOD) key figures for the time range of one week,
                  for a list of notations.
            /notation/keyFigures/year/1/get:
              get:
                tags:
                  - End-of-day
                  - D)
                  - Key
                  - Figures
                  - For
                  - The
                  - Time
                  - Range
                  - Of
                  - One
                  - Year.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                summary: End-of-day (EOD) key figures for the time range of one year.
                description: End-of-day (EOD) key figures for the time range of one year.
            /notation/keyFigures/year/1/list:
              get:
                tags:
                  - End-of-day
                  - D)
                  - Key
                  - Figures
                  - For
                  - The
                  - Time
                  - Range
                  - Of
                  - One
                  - Year,
                  - List
                  - Notations.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                summary: >-
                  End-of-day (EOD) key figures for the time range of one year,
                  for a list of notations.
                description: >-
                  End-of-day (EOD) key figures for the time range of one year,
                  for a list of notations.
            /notation/keyFigures/month/3/get:
              get:
                tags:
                  - End-of-day
                  - D)
                  - Key
                  - Figures
                  - For
                  - The
                  - Time
                  - Range
                  - Of
                  - Three
                  - Months.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                summary: >-
                  End-of-day (EOD) key figures for the time range of three
                  months.
                description: >-
                  End-of-day (EOD) key figures for the time range of three
                  months.
            /notation/keyFigures/month/3/list:
              get:
                tags:
                  - End-of-day
                  - D)
                  - Key
                  - Figures
                  - For
                  - The
                  - Time
                  - Range
                  - Of
                  - Three
                  - Months,
                  - List
                  - Notations.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                summary: >-
                  End-of-day (EOD) key figures for the time range of three
                  months, for a list of notations.
                description: >-
                  End-of-day (EOD) key figures for the time range of three
                  months, for a list of notations.
            /notation/keyFigures/year/3/get:
              get:
                tags:
                  - End-of-day
                  - D)
                  - Key
                  - Figures
                  - For
                  - The
                  - Time
                  - Range
                  - Of
                  - Three
                  - Years.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                summary: >-
                  End-of-day (EOD) key figures for the time range of three
                  years.
                description: >-
                  End-of-day (EOD) key figures for the time range of three
                  years.
            /notation/keyFigures/year/3/list:
              get:
                tags:
                  - End-of-day
                  - D)
                  - Key
                  - Figures
                  - For
                  - The
                  - Time
                  - Range
                  - Of
                  - Three
                  - Years,
                  - List
                  - Notations.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                summary: >-
                  End-of-day (EOD) key figures for the time range of three
                  years, for a list of notations.
                description: >-
                  End-of-day (EOD) key figures for the time range of three
                  years, for a list of notations.
            /notation/keyFigures/year/5/get:
              get:
                tags:
                  - End-of-day
                  - D)
                  - Key
                  - Figures
                  - For
                  - The
                  - Time
                  - Range
                  - Of
                  - Five
                  - Years.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                summary: End-of-day (EOD) key figures for the time range of five years.
                description: End-of-day (EOD) key figures for the time range of five years.
            /notation/keyFigures/year/5/list:
              get:
                tags:
                  - End-of-day
                  - D)
                  - Key
                  - Figures
                  - For
                  - The
                  - Time
                  - Range
                  - Of
                  - Five
                  - Years,
                  - List
                  - Notations.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                summary: >-
                  End-of-day (EOD) key figures for the time range of five years,
                  for a list of notations.
                description: >-
                  End-of-day (EOD) key figures for the time range of five years,
                  for a list of notations.
            /notation/keyFigures/month/6/get:
              get:
                tags:
                  - End-of-day
                  - D)
                  - Key
                  - Figures
                  - For
                  - The
                  - Time
                  - Range
                  - Of
                  - Six
                  - Months.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                summary: End-of-day (EOD) key figures for the time range of six months.
                description: End-of-day (EOD) key figures for the time range of six months.
            /notation/keyFigures/month/6/list:
              get:
                tags:
                  - End-of-day
                  - D)
                  - Key
                  - Figures
                  - For
                  - The
                  - Time
                  - Range
                  - Of
                  - Six
                  - Months,
                  - List
                  - Notations.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                summary: >-
                  End-of-day (EOD) key figures for the time range of six months,
                  for a list of notations.
                description: >-
                  End-of-day (EOD) key figures for the time range of six months,
                  for a list of notations.
            /notation/keyFigures/year/7/get:
              get:
                tags:
                  - End-of-day
                  - D)
                  - Key
                  - Figures
                  - For
                  - The
                  - Time
                  - Range
                  - Of
                  - Seven
                  - Years.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                summary: >-
                  End-of-day (EOD) key figures for the time range of seven
                  years.
                description: >-
                  End-of-day (EOD) key figures for the time range of seven
                  years.
            /notation/keyFigures/year/7/list:
              get:
                tags:
                  - End-of-day
                  - D)
                  - Key
                  - Figures
                  - For
                  - The
                  - Time
                  - Range
                  - Of
                  - Seven
                  - Years,
                  - List
                  - Notations.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                summary: >-
                  End-of-day (EOD) key figures for the time range of seven
                  years, for a list of notations.
                description: >-
                  End-of-day (EOD) key figures for the time range of seven
                  years, for a list of notations.
            /notation/keyFigures/yearToDate/get:
              get:
                tags:
                  - End-of-day
                  - D)
                  - Key
                  - Figures
                  - For
                  - The
                  - Time
                  - Range
                  - Year-to-date
                  - D)..
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                  - To
                  - Date
                summary: >-
                  End-of-day (EOD) key figures for the time range year-to-date
                  (YTD)..
                description: >-
                  End-of-day (EOD) key figures for the time range year-to-date
                  (YTD). The time range YTD begins with the last trading day of
                  the previous calendar year for which EOD prices are available
                  and ends with the most recent trading day of the current
                  calendar year for which EOD prices are available..
            /notation/keyFigures/yearToDate/list:
              get:
                tags:
                  - End-of-day
                  - D)
                  - Key
                  - Figures
                  - For
                  - The
                  - Time
                  - Range
                  - Year-to-date
                  - D),
                  - List
                  - Of
                  - Notations..
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                  - To
                  - Date
                summary: >-
                  End-of-day (EOD) key figures for the time range year-to-date
                  (YTD), for a list of notations..
                description: >-
                  End-of-day (EOD) key figures for the time range year-to-date
                  (YTD), for a list of notations. The time range YTD begins with
                  the last trading day of the previous calendar year for which
                  EOD prices are available and ends with the most recent
                  tradingday of the current calendar year for which EOD prices
                  are available..
            /notation/keyFigures/tradingDay/average/get:
              get:
                tags:
                  - Average
                  - End-of-day
                  - D)
                  - Key
                  - Figures
                  - For
                  - Different
                  - Trading
                  - Days
                  - Periods.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                  - To
                  - Date
                  - Trading
                  - Day
                  - Average
                description: >-
                  Average end-of-day (EOD) key figures for different trading
                  days periods. A trading day is a calendar day on that trading
                  of the notation was possible.
                summary: >-
                  Average end-of-day (EOD) key figures for different trading
                  days periods.
            /notation/market/list:
              post:
                tags:
                  - List
                  - Of
                  - Markets
                  - With
                  - Entitled
                  - Notations.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                  - To
                  - Date
                  - Trading
                  - Day
                  - Average
                description: >-
                  List of markets with entitled notations. The list contains
                  only markets with at least one active and entitled notation. 

                  All identifiers used as parameters must be valid and entitled.
                summary: List of markets with entitled notations.
            /notation/selectionList/list:
              get:
                tags:
                  - Set
                  - Of
                  - Custom
                  - Notation-level
                  - Selection
                  - Lists.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                  - To
                  - Date
                  - Trading
                  - Day
                  - Average
                description: Set of custom notation-level selection lists.
                summary: Set of custom notation-level selection lists.
            /notation/selectionList/listByNotation:
              get:
                tags:
                  - For
                  - Each
                  - Given
                  - Notation,
                  - Returns
                  - The
                  - Notation-level
                  - Selection
                  - Lists
                  - Of
                  - Which
                  - Notation
                  - Is
                  - Member.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                  - To
                  - Date
                  - Trading
                  - Day
                  - Average
                description: >-
                  For each given notation, returns the notation-level selection
                  lists of which the notation is a member.
                summary: >-
                  For each given notation, returns the notation-level selection
                  lists of which the notation is a member.
            /notation/selectionList/members/list:
              post:
                tags:
                  - List
                  - Of
                  - Notations
                  - Belonging
                  - To
                  - Notation-level
                  - Selection
                  - List.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                  - To
                  - Date
                  - Trading
                  - Day
                  - Average
                summary: >-
                  List of notations belonging to a notation-level selection
                  list.
                description: >-
                  List of notations belonging to a notation-level selection
                  list.
            /notation/status/get:
              get:
                tags:
                  - Intraday
                  - Trading
                  - Status
                  - Of
                  - Notation.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                  - To
                  - Date
                  - Trading
                  - Day
                  - Average
                  - Status
                description: >-
                  Intraday trading status of a notation.<br>The endpoint is
                  subscribable to provide push updates. See attribute
                  `_subscriptionMinimalInterval` for valid update rates.
                summary: Intraday trading status of a notation.
            /prices/get:
              get:
                tags:
                  - Overview
                  - Of
                  - Trading
                  - 'On'
                  - The
                  - Most
                  - Recent
                  - Day,
                  - Including
                  - Latest
                  - Price,
                  - For
                  - Notation.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                  - To
                  - Date
                  - Trading
                  - Day
                  - Average
                  - Status
                  - Prices
                summary: >-
                  Overview of trading on the most recent trading day, including
                  the latest price, for a notation.
                description: >-
                  Overview of trading on the most recent trading day, including
                  the latest price, for a notation.


                  The endpoint is subscribable to provide push updates. See
                  attribute `_subscriptionMinimalInterval` for valid update
                  rates.
            /prices/list:
              get:
                tags:
                  - Overview
                  - Of
                  - Trading
                  - 'On'
                  - The
                  - Most
                  - Recent
                  - Day,
                  - Including
                  - Latest
                  - Price,
                  - For
                  - List
                  - Notations.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                  - To
                  - Date
                  - Trading
                  - Day
                  - Average
                  - Status
                  - Prices
                summary: >-
                  Overview of trading on the most recent trading day, including
                  the latest price, for a list of notations.
                description: >-
                  Overview of trading on the most recent trading day, including
                  the latest price, for a list of notations.
            /prices/bidAsk/get:
              get:
                tags:
                  - Most
                  - Recent
                  - Bid
                  - And
                  - Ask
                  - Prices
                  - (best
                  - Offer)
                  - For
                  - Notation.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                  - To
                  - Date
                  - Trading
                  - Day
                  - Average
                  - Status
                  - Prices
                  - Ask
                summary: >-
                  Most recent bid and ask prices (best bid / offer) for a
                  notation.
                description: >-
                  Most recent bid and ask prices (best bid / offer) for a
                  notation.


                  The endpoint is subscribable to provide push updates. See
                  attribute `_subscriptionMinimalInterval` for valid update
                  rates.
            /prices/bidAsk/list:
              get:
                tags:
                  - Most
                  - Recent
                  - Bid
                  - And
                  - Ask
                  - Prices
                  - (best
                  - Offer)
                  - For
                  - List
                  - Of
                  - Notations.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                  - To
                  - Date
                  - Trading
                  - Day
                  - Average
                  - Status
                  - Prices
                  - Ask
                summary: >-
                  Most recent bid and ask prices (best bid / offer) for a list
                  of notations.
                description: >-
                  Most recent bid and ask prices (best bid / offer) for a list
                  of notations.
            /prices/orderbook/aggregated/get:
              get:
                tags:
                  - Orderbook
                  - Aggregated
                  - By
                  - Price.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                  - To
                  - Date
                  - Trading
                  - Day
                  - Average
                  - Status
                  - Prices
                  - Ask
                  - Orderbook
                  - Aggregated
                summary: Orderbook aggregated by price.
                description: Orderbook aggregated by price.
            /prices/orderbook/full/get:
              get:
                tags:
                  - Full
                  - Orderbook
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                  - To
                  - Date
                  - Trading
                  - Day
                  - Average
                  - Status
                  - Prices
                  - Ask
                  - Orderbook
                  - Aggregated
                  - Full
                summary: Full orderbook
                description: Full orderbook
            /prices/tradingSchedule/event/list:
              post:
                tags:
                  - Sequence
                  - Of
                  - Market-related
                  - Events.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                  - To
                  - Date
                  - Trading
                  - Day
                  - Average
                  - Status
                  - Prices
                  - Ask
                  - Orderbook
                  - Aggregated
                  - Full
                  - Schedule
                  - Event
                summary: Sequence of market-related events.
                description: >-
                  Sequence of market-related events like the opening time or
                  closing time of a market of a specific
                  notation.<br><br>Pagination to a previous page is not
                  supported and `pagination.previous` is always `null`.
            /prices/tradingSchedule/event/type/list:
              get:
                tags:
                  - Trading
                  - Schedule
                  - Event
                  - Types.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                  - To
                  - Date
                  - Trading
                  - Day
                  - Average
                  - Status
                  - Prices
                  - Ask
                  - Orderbook
                  - Aggregated
                  - Full
                  - Schedule
                  - Event
                summary: Trading schedule event types.
                description: >-
                  Trading schedule event types define the events which may occur
                  during any period of trading. Types of trading schedule events
                  are for instance OPEN, CLOSE, END_OF_DAY.
            /instrument/search/basic:
              get:
                tags:
                  - Basic
                  - Search
                  - For
                  - Instruments.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                  - To
                  - Date
                  - Trading
                  - Day
                  - Average
                  - Status
                  - Prices
                  - Ask
                  - Orderbook
                  - Aggregated
                  - Full
                  - Schedule
                  - Event
                  - Search
                summary: Basic search for instruments.
                description: >-
                  Search for instruments whose ISIN, specified NSINs, or name
                  match the search value according to a tolerant full-text match
                  algorithm. Better matching results appear in the response
                  before less relevant matches.
            /notation/search/basic:
              get:
                tags:
                  - Basic
                  - Search
                  - For
                  - Notations.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                  - To
                  - Date
                  - Trading
                  - Day
                  - Average
                  - Status
                  - Prices
                  - Ask
                  - Orderbook
                  - Aggregated
                  - Full
                  - Schedule
                  - Event
                  - Search
                summary: Basic search for notations.
                description: >-
                  Search for a notation whose ISIN, specified NSINs, name, or
                  symbol match the search value according to a tolerant
                  full-text match algorithm. If more than one notation of an
                  instrument matches, only the notation with the highest
                  monetary trading volume, averaged over one month, is
                  considered. Better matching results appear in the response
                  before less relevant matches. If the parameter popularity is
                  set to true, the popularity of the notation is the primary
                  sort criterion. Popularity is affected mostly by the request
                  frequency of the notation.
            /notation/searchByText:
              post:
                tags:
                  - Text-based
                  - Search
                  - For
                  - Notations.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                  - To
                  - Date
                  - Trading
                  - Day
                  - Average
                  - Status
                  - Prices
                  - Ask
                  - Orderbook
                  - Aggregated
                  - Full
                  - Schedule
                  - Event
                  - Search
                summary: Text-based search for notations.
                description: >-
                  Text-based search for notations in selected identifier and
                  name attributes according to a tolerant full-text match
                  algorithm. The results satisfy all selected filters; sorting
                  by various attributes is possible. If more than one notation
                  of an instrument matches, only the notation with the best
                  market priority (according to the parameter `market.priority`)
                  or, in the absence of market priorities, only the notation
                  with the highest trading volume, averaged over one month, is
                  considered.     
                   All identifiers used as parameters must be valid and entitled.
          tags:
            - name: basic
              description: basic endpoints
            - name: category
              description: category endpoints
            - name: instrument
              description: instrument endpoints
            - name: notation
              description: notation endpoints
            - name: prices
              description: prices endpoints
          externalDocs:
            description: API Documentation
            url: https://developer.factset.com/api-catalog/
          x-interface-version: 2
          x-documenter-version: 6.3.9
          x-api-version: null
    overlays:
      - type: APIs.io Search
        url: overlays/real-time-quotes-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/real-time-quotes-openapi-api-evangelist-ratings.yml
    aid: factset:factset-real-time-quotes-api
  - aid: twilio:twilio-messaging-api
    name: Twilio Messaging API
    description: >-
      Send and receive messages via SMS, MMS, WhatsApp, Facebook Messenger, and
      more through our Messaging and Conversations APIs.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://www.twilio.com/en-us/ahoy
    baseURL: https:/api.twilio.com
    tags: []
    properties:
      - type: Documentation
        url: https://www.twilio.com/en-us/messaging
      - type: Pricing
        url: https://www.twilio.com/en-us/sms/pricing/us
      - type: OpenAPI
        data:
          info:
            title: Twilio - Messaging
            license:
              name: Apache 2.0
              url: https://www.apache.org/licenses/LICENSE-2.0.html
          openapi: 3.0.1
          paths:
            /v1/Services/{ServiceSid}/AlphaSenders:
              description: >-
                A Messaging Service resource to add, fetch or remove an Alpha
                Sender ID from a Messaging Service.
              post:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
            /v1/Services/{ServiceSid}/AlphaSenders/{Sid}:
              description: >-
                A Messaging Service resource to add, fetch or remove an Alpha
                Sender ID from a Messaging Service.
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
              delete:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
            /v1/a2p/BrandRegistrations/{BrandRegistrationSid}/SmsOtp:
              description: >-
                A Messaging Service resource to retry OTP verification for Sole
                Proprietor Brand Registrations.
              post:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
            /v1/a2p/BrandRegistrations/{Sid}:
              description: >-
                A Messaging Service resource to add and fetch Brand
                Registrations.
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
              post:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
            /v1/a2p/BrandRegistrations:
              description: >-
                A Messaging Service resource to add and fetch Brand
                Registrations.
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
              post:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
            /v1/a2p/BrandRegistrations/{BrandSid}/Vettings:
              description: A Messaging Service resource to add and get Brand Vettings.
              post:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
            /v1/a2p/BrandRegistrations/{BrandSid}/Vettings/{BrandVettingSid}:
              description: A Messaging Service resource to add and get Brand Vettings.
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
            /v1/Services/{MessagingServiceSid}/ChannelSenders:
              description: >-
                A Messaging Service resource to read, fetch all Channel Senders
                associated with a Messaging Service.
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
            /v1/Services/{MessagingServiceSid}/ChannelSenders/{Sid}:
              description: >-
                A Messaging Service resource to read, fetch all Channel Senders
                associated with a Messaging Service.
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
            /v1/Deactivations:
              description: >-
                A Deactivation resource to retrieve a list of United States
                phone numbers that have been deactivated by mobile carriers on a
                specific date.
              get:
                description: >-
                  Fetch a list of all United States numbers that have been
                  deactivated on a specific date.
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
            /v1/LinkShortening/Domains/{DomainSid}/Certificate:
              description: 'TODO: Resource-level docs'
              post:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
              delete:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
            /v1/LinkShortening/Domains/{DomainSid}/Config:
              description: 'TODO: Resource-level docs'
              post:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
            /v1/LinkShortening/MessagingService/{MessagingServiceSid}/DomainConfig:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
            /v1/Services/PreregisteredUsa2p:
              description: >-
                Resource to associate preregistered campaign with Messaging
                Service.
              post:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
                  - Preregistered
                  - Usa2p
            /v1/LinkShortening/Domains/{DomainSid}/MessagingServices/{MessagingServiceSid}:
              description: 'TODO: Resource-level docs'
              post:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
                  - Preregistered
                  - Usa2p
              delete:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
                  - Preregistered
                  - Usa2p
            /v1/LinkShortening/MessagingServices/{MessagingServiceSid}/Domain:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
                  - Preregistered
                  - Usa2p
            /v1/Services/{ServiceSid}/PhoneNumbers:
              description: >-
                A Messaging Service resource to add, fetch or remove phone
                numbers from a Messaging Service.
              post:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
                  - Preregistered
                  - Usa2p
                  - Phone
                  - Numbers
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
                  - Preregistered
                  - Usa2p
                  - Phone
                  - Numbers
            /v1/Services/{ServiceSid}/PhoneNumbers/{Sid}:
              description: >-
                A Messaging Service resource to add, fetch or remove phone
                numbers from a Messaging Service.
              delete:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
                  - Preregistered
                  - Usa2p
                  - Phone
                  - Numbers
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
                  - Preregistered
                  - Usa2p
                  - Phone
                  - Numbers
            /v1/Services:
              description: >-
                A Messaging Service resource to create, fetch, update, delete or
                add/remove senders from Messaging Services.
              post:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
                  - Preregistered
                  - Usa2p
                  - Phone
                  - Numbers
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
                  - Preregistered
                  - Usa2p
                  - Phone
                  - Numbers
            /v1/Services/{Sid}:
              description: >-
                A Messaging Service resource to create, fetch, update, delete or
                add/remove senders from Messaging Services.
              post:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
                  - Preregistered
                  - Usa2p
                  - Phone
                  - Numbers
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
                  - Preregistered
                  - Usa2p
                  - Phone
                  - Numbers
              delete:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
                  - Preregistered
                  - Usa2p
                  - Phone
                  - Numbers
            /v1/Services/{ServiceSid}/ShortCodes:
              description: >-
                A Messaging Service resource to add, fetch or remove short code
                numbers from a Messaging Service.
              post:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
                  - Preregistered
                  - Usa2p
                  - Phone
                  - Numbers
                  - Short
                  - Codes
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
                  - Preregistered
                  - Usa2p
                  - Phone
                  - Numbers
                  - Short
                  - Codes
            /v1/Services/{ServiceSid}/ShortCodes/{Sid}:
              description: >-
                A Messaging Service resource to add, fetch or remove short code
                numbers from a Messaging Service.
              delete:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
                  - Preregistered
                  - Usa2p
                  - Phone
                  - Numbers
                  - Short
                  - Codes
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
                  - Preregistered
                  - Usa2p
                  - Phone
                  - Numbers
                  - Short
                  - Codes
            /v1/Tollfree/Verifications/{Sid}:
              description: A Messaging resource to add and fetch Tollfree Verifications.
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
                  - Preregistered
                  - Usa2p
                  - Phone
                  - Numbers
                  - Short
                  - Codes
                  - Tollfree
                  - Verifications
              post:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
                  - Preregistered
                  - Usa2p
                  - Phone
                  - Numbers
                  - Short
                  - Codes
                  - Tollfree
                  - Verifications
              delete:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
                  - Preregistered
                  - Usa2p
                  - Phone
                  - Numbers
                  - Short
                  - Codes
                  - Tollfree
                  - Verifications
            /v1/Tollfree/Verifications:
              description: A Messaging resource to add and fetch Tollfree Verifications.
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
                  - Preregistered
                  - Usa2p
                  - Phone
                  - Numbers
                  - Short
                  - Codes
                  - Tollfree
                  - Verifications
              post:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
                  - Preregistered
                  - Usa2p
                  - Phone
                  - Numbers
                  - Short
                  - Codes
                  - Tollfree
                  - Verifications
            /v1/Services/{MessagingServiceSid}/Compliance/Usa2p:
              description: >-
                A service for (fetch/create/delete) A2P Campaign for a Messaging
                Service
              post:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
                  - Preregistered
                  - Usa2p
                  - Phone
                  - Numbers
                  - Short
                  - Codes
                  - Tollfree
                  - Verifications
                  - Compliance
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
                  - Preregistered
                  - Usa2p
                  - Phone
                  - Numbers
                  - Short
                  - Codes
                  - Tollfree
                  - Verifications
                  - Compliance
            /v1/Services/{MessagingServiceSid}/Compliance/Usa2p/{Sid}:
              description: >-
                A service for (fetch/create/delete) A2P Campaign for a Messaging
                Service
              delete:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
                  - Preregistered
                  - Usa2p
                  - Phone
                  - Numbers
                  - Short
                  - Codes
                  - Tollfree
                  - Verifications
                  - Compliance
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
                  - Preregistered
                  - Usa2p
                  - Phone
                  - Numbers
                  - Short
                  - Codes
                  - Tollfree
                  - Verifications
                  - Compliance
            /v1/Services/{MessagingServiceSid}/Compliance/Usa2p/Usecases:
              description: >-
                Messaging Service Use Case resource. Fetch possible use cases
                for service. The Use Cases API returns an empty list if there is
                an issue with the customer's A2P brand registration. This Brand
                cannot register any campaign use cases. Customers are requested
                to contact support with their A2P brand information.
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
                  - Preregistered
                  - Usa2p
                  - Phone
                  - Numbers
                  - Short
                  - Codes
                  - Tollfree
                  - Verifications
                  - Compliance
                  - Usecases
            /v1/Services/Usecases:
              description: >-
                Use Case resource. Fetch possible use cases for a Messaging
                Service.
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
                  - Preregistered
                  - Usa2p
                  - Phone
                  - Numbers
                  - Short
                  - Codes
                  - Tollfree
                  - Verifications
                  - Compliance
                  - Usecases
          tags:
            - name: MessagingV1AlphaSender
            - name: MessagingV1BrandRegistration
            - name: MessagingV1BrandRegistrationOtp
            - name: MessagingV1BrandVetting
            - name: MessagingV1ChannelSender
            - name: MessagingV1Deactivations
            - name: MessagingV1DomainCerts
            - name: MessagingV1DomainConfig
            - name: MessagingV1DomainConfigMessagingService
            - name: MessagingV1ExternalCampaign
            - name: MessagingV1LinkshorteningMessagingService
            - name: MessagingV1LinkshorteningMessagingServiceDomainAssociation
            - name: MessagingV1PhoneNumber
            - name: MessagingV1Service
            - name: MessagingV1ShortCode
            - name: MessagingV1TollfreeVerification
            - name: MessagingV1UsAppToPerson
            - name: MessagingV1UsAppToPersonUsecase
            - name: MessagingV1Usecase
          x-maturity:
            - name: GA
              description: This product is Generally Available.
            - name: Beta
              description: >-
                PLEASE NOTE that this is a Beta product that is subject to
                change. U
    overlays:
      - type: APIs.io Search
        url: overlays/messaging-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/messaging-openapi-api-evangelist-ratings.yml
  - aid: twilio:twilio-numbers-api
    name: Twilio Numbers API
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
            title: Twilio - Numbers
            license:
              name: Apache 2.0
              url: https://www.apache.org/licenses/LICENSE-2.0.html
          openapi: 3.0.1
          paths:
            /v2/HostedNumber/AuthorizationDocuments/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: Fetch a specific AuthorizationDocument.
                tags:
                  - Hosted
                  - Number
                  - Authorization
                  - Documents
                  - Sid
              delete:
                description: Cancel the AuthorizationDocument request.
                tags:
                  - Hosted
                  - Number
                  - Authorization
                  - Documents
                  - Sid
            /v2/HostedNumber/AuthorizationDocuments:
              description: 'TODO: Resource-level docs'
              get:
                description: >-
                  Retrieve a list of AuthorizationDocuments belonging to the
                  account initiating the request.
                tags:
                  - Hosted
                  - Number
                  - Authorization
                  - Documents
                  - Sid
              post:
                description: >-
                  Create an AuthorizationDocument for authorizing the hosting of
                  phone number capabilities on Twilio's platform.
                tags:
                  - Hosted
                  - Number
                  - Authorization
                  - Documents
                  - Sid
            /v2/HostedNumber/Orders/Bulk/{BulkHostingSid}:
              description: 'TODO: Resource-level docs'
              get:
                description: Fetch a specific BulkHostedNumberOrder.
                tags:
                  - Hosted
                  - Number
                  - Authorization
                  - Documents
                  - Sid
                  - Orders
                  - Bulk
                  - Hosting
            /v2/HostedNumber/Orders/Bulk:
              description: 'TODO: Resource-level docs'
            /v2/RegulatoryCompliance/Bundles:
              description: 'TODO: Resource-level docs'
              post:
                description: Create a new Bundle.
                tags:
                  - Hosted
                  - Number
                  - Authorization
                  - Documents
                  - Sid
                  - Orders
                  - Bulk
                  - Hosting
                  - Regulatory
                  - Compliance
                  - Bundles
              get:
                description: Retrieve a list of all Bundles for an account.
                tags:
                  - Hosted
                  - Number
                  - Authorization
                  - Documents
                  - Sid
                  - Orders
                  - Bulk
                  - Hosting
                  - Regulatory
                  - Compliance
                  - Bundles
            /v2/RegulatoryCompliance/Bundles/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: Fetch a specific Bundle instance.
                tags:
                  - Hosted
                  - Number
                  - Authorization
                  - Documents
                  - Sid
                  - Orders
                  - Bulk
                  - Hosting
                  - Regulatory
                  - Compliance
                  - Bundles
              post:
                description: Updates a Bundle in an account.
                tags:
                  - Hosted
                  - Number
                  - Authorization
                  - Documents
                  - Sid
                  - Orders
                  - Bulk
                  - Hosting
                  - Regulatory
                  - Compliance
                  - Bundles
              delete:
                description: Delete a specific Bundle.
                tags:
                  - Hosted
                  - Number
                  - Authorization
                  - Documents
                  - Sid
                  - Orders
                  - Bulk
                  - Hosting
                  - Regulatory
                  - Compliance
                  - Bundles
            /v2/RegulatoryCompliance/Bundles/{BundleSid}/Copies:
              description: 'TODO: Resource-level docs'
              post:
                description: >-
                  Creates a new copy of a Bundle. It will internally create
                  copies of all the bundle items (identities and documents) of
                  the original bundle
                tags:
                  - Hosted
                  - Number
                  - Authorization
                  - Documents
                  - Sid
                  - Orders
                  - Bulk
                  - Hosting
                  - Regulatory
                  - Compliance
                  - Bundles
                  - Bundle
                  - Copies
              get:
                description: Retrieve a list of all Bundles Copies for a Bundle.
                tags:
                  - Hosted
                  - Number
                  - Authorization
                  - Documents
                  - Sid
                  - Orders
                  - Bulk
                  - Hosting
                  - Regulatory
                  - Compliance
                  - Bundles
                  - Bundle
                  - Copies
            /v2/HostedNumber/AuthorizationDocuments/{SigningDocumentSid}/DependentHostedNumberOrders:
              description: 'TODO: Resource-level docs'
              get:
                description: >-
                  Retrieve a list of dependent HostedNumberOrders belonging to
                  the AuthorizationDocument.
                tags:
                  - Hosted
                  - Number
                  - Authorization
                  - Documents
                  - Sid
                  - Orders
                  - Bulk
                  - Hosting
                  - Regulatory
                  - Compliance
                  - Bundles
                  - Bundle
                  - Copies
                  - Signing
                  - Document
                  - Dependent
            /v2/RegulatoryCompliance/EndUsers:
              description: 'TODO: Resource-level docs'
              post:
                description: Create a new End User.
                tags:
                  - Hosted
                  - Number
                  - Authorization
                  - Documents
                  - Sid
                  - Orders
                  - Bulk
                  - Hosting
                  - Regulatory
                  - Compliance
                  - Bundles
                  - Bundle
                  - Copies
                  - Signing
                  - Document
                  - Dependent
                  - End
                  - Users
              get:
                description: Retrieve a list of all End User for an account.
                tags:
                  - Hosted
                  - Number
                  - Authorization
                  - Documents
                  - Sid
                  - Orders
                  - Bulk
                  - Hosting
                  - Regulatory
                  - Compliance
                  - Bundles
                  - Bundle
                  - Copies
                  - Signing
                  - Document
                  - Dependent
                  - End
                  - Users
            /v2/RegulatoryCompliance/EndUsers/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: Fetch specific End User Instance.
                tags:
                  - Hosted
                  - Number
                  - Authorization
                  - Documents
                  - Sid
                  - Orders
                  - Bulk
                  - Hosting
                  - Regulatory
                  - Compliance
                  - Bundles
                  - Bundle
                  - Copies
                  - Signing
                  - Document
                  - Dependent
                  - End
                  - Users
              post:
                description: Update an existing End User.
                tags:
                  - Hosted
                  - Number
                  - Authorization
                  - Documents
                  - Sid
                  - Orders
                  - Bulk
                  - Hosting
                  - Regulatory
                  - Compliance
                  - Bundles
                  - Bundle
                  - Copies
                  - Signing
                  - Document
                  - Dependent
                  - End
                  - Users
              delete:
                description: Delete a specific End User.
                tags:
                  - Hosted
                  - Number
                  - Authorization
                  - Documents
                  - Sid
                  - Orders
                  - Bulk
                  - Hosting
                  - Regulatory
                  - Compliance
                  - Bundles
                  - Bundle
                  - Copies
                  - Signing
                  - Document
                  - Dependent
                  - End
                  - Users
            /v2/RegulatoryCompliance/EndUserTypes:
              description: 'TODO: Resource-level docs'
              get:
                description: Retrieve a list of all End-User Types.
                tags:
                  - Hosted
                  - Number
                  - Authorization
                  - Documents
                  - Sid
                  - Orders
                  - Bulk
                  - Hosting
                  - Regulatory
                  - Compliance
                  - Bundles
                  - Bundle
                  - Copies
                  - Signing
                  - Document
                  - Dependent
                  - End
                  - Users
                  - User
                  - Types
            /v2/RegulatoryCompliance/EndUserTypes/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: Fetch a specific End-User Type Instance.
                tags:
                  - Hosted
                  - Number
                  - Authorization
                  - Documents
                  - Sid
                  - Orders
                  - Bulk
                  - Hosting
                  - Regulatory
                  - Compliance
                  - Bundles
                  - Bundle
                  - Copies
                  - Signing
                  - Document
                  - Dependent
                  - End
                  - Users
                  - User
                  - Types
            /v2/RegulatoryCompliance/Bundles/{BundleSid}/Evaluations:
              description: 'TODO: Resource-level docs'
              post:
                description: Creates an evaluation for a bundle
                tags:
                  - Hosted
                  - Number
                  - Authorization
                  - Documents
                  - Sid
                  - Orders
                  - Bulk
                  - Hosting
                  - Regulatory
                  - Compliance
                  - Bundles
                  - Bundle
                  - Copies
                  - Signing
                  - Document
                  - Dependent
                  - End
                  - Users
                  - User
                  - Types
                  - Evaluations
              get:
                description: >-
                  Retrieve a list of Evaluations associated to the Bundle
                  resource.
                tags:
                  - Hosted
                  - Number
                  - Authorization
                  - Documents
                  - Sid
                  - Orders
                  - Bulk
                  - Hosting
                  - Regulatory
                  - Compliance
                  - Bundles
                  - Bundle
                  - Copies
                  - Signing
                  - Document
                  - Dependent
                  - End
                  - Users
                  - User
                  - Types
                  - Evaluations
            /v2/RegulatoryCompliance/Bundles/{BundleSid}/Evaluations/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: Fetch specific Evaluation Instance.
                tags:
                  - Hosted
                  - Number
                  - Authorization
                  - Documents
                  - Sid
                  - Orders
                  - Bulk
                  - Hosting
                  - Regulatory
                  - Compliance
                  - Bundles
                  - Bundle
                  - Copies
                  - Signing
                  - Document
                  - Dependent
                  - End
                  - Users
                  - User
                  - Types
                  - Evaluations
            /v2/HostedNumber/Orders/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: Fetch a specific HostedNumberOrder.
                tags:
                  - Hosted
                  - Number
                  - Authorization
                  - Documents
                  - Sid
                  - Orders
                  - Bulk
                  - Hosting
                  - Regulatory
                  - Compliance
                  - Bundles
                  - Bundle
                  - Copies
                  - Signing
                  - Document
                  - Dependent
                  - End
                  - Users
                  - User
                  - Types
                  - Evaluations
              delete:
                description: >-
                  Cancel the HostedNumberOrder (only available when the status
                  is in `received`).
                tags:
                  - Hosted
                  - Number
                  - Authorization
                  - Documents
                  - Sid
                  - Orders
                  - Bulk
                  - Hosting
                  - Regulatory
                  - Compliance
                  - Bundles
                  - Bundle
                  - Copies
                  - Signing
                  - Document
                  - Dependent
                  - End
                  - Users
                  - User
                  - Types
                  - Evaluations
            /v2/HostedNumber/Orders:
              description: 'TODO: Resource-level docs'
              get:
                description: >-
                  Retrieve a list of HostedNumberOrders belonging to the account
                  initiating the request.
                tags:
                  - Hosted
                  - Number
                  - Authorization
                  - Documents
                  - Sid
                  - Orders
                  - Bulk
                  - Hosting
                  - Regulatory
                  - Compliance
                  - Bundles
                  - Bundle
                  - Copies
                  - Signing
                  - Document
                  - Dependent
                  - End
                  - Users
                  - User
                  - Types
                  - Evaluations
              post:
                description: Host a phone number's capability on Twilio's platform.
                tags:
                  - Hosted
                  - Number
                  - Authorization
                  - Documents
                  - Sid
                  - Orders
                  - Bulk
                  - Hosting
                  - Regulatory
                  - Compliance
                  - Bundles
                  - Bundle
                  - Copies
                  - Signing
                  - Document
                  - Dependent
                  - End
                  - Users
                  - User
                  - Types
                  - Evaluations
            /v2/RegulatoryCompliance/Bundles/{BundleSid}/ItemAssignments:
              description: 'TODO: Resource-level docs'
              post:
                description: Create a new Assigned Item.
                tags:
                  - Hosted
                  - Number
                  - Authorization
                  - Documents
                  - Sid
                  - Orders
                  - Bulk
                  - Hosting
                  - Regulatory
                  - Compliance
                  - Bundles
                  - Bundle
                  - Copies
                  - Signing
                  - Document
                  - Dependent
                  - End
                  - Users
                  - User
                  - Types
                  - Evaluations
                  - Item
                  - Assignments
              get:
                description: Retrieve a list of all Assigned Items for an account.
                tags:
                  - Hosted
                  - Number
                  - Authorization
                  - Documents
                  - Sid
                  - Orders
                  - Bulk
                  - Hosting
                  - Regulatory
                  - Compliance
                  - Bundles
                  - Bundle
                  - Copies
                  - Signing
                  - Document
                  - Dependent
                  - End
                  - Users
                  - User
                  - Types
                  - Evaluations
                  - Item
                  - Assignments
            /v2/RegulatoryCompliance/Bundles/{BundleSid}/ItemAssignments/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: Fetch specific Assigned Item Instance.
                tags:
                  - Hosted
                  - Number
                  - Authorization
                  - Documents
                  - Sid
                  - Orders
                  - Bulk
                  - Hosting
                  - Regulatory
                  - Compliance
                  - Bundles
                  - Bundle
                  - Copies
                  - Signing
                  - Document
                  - Dependent
                  - End
                  - Users
                  - User
                  - Types
                  - Evaluations
                  - Item
                  - Assignments
              delete:
                description: Remove an Assignment Item Instance.
                tags:
                  - Hosted
                  - Number
                  - Authorization
                  - Documents
                  - Sid
                  - Orders
                  - Bulk
                  - Hosting
                  - Regulatory
                  - Compliance
                  - Bundles
                  - Bundle
                  - Copies
                  - Signing
                  - Document
                  - Dependent
                  - End
                  - Users
                  - User
                  - Types
                  - Evaluations
                  - Item
                  - Assignments
            /v2/RegulatoryCompliance/Regulations:
              description: 'TODO: Resource-level docs'
              get:
                description: Retrieve a list of all Regulations.
                tags:
                  - Hosted
                  - Number
                  - Authorization
                  - Documents
                  - Sid
                  - Orders
                  - Bulk
                  - Hosting
                  - Regulatory
                  - Compliance
                  - Bundles
                  - Bundle
                  - Copies
                  - Signing
                  - Document
                  - Dependent
                  - End
                  - Users
                  - User
                  - Types
                  - Evaluations
                  - Item
                  - Assignments
                  - Regulations
            /v2/RegulatoryCompliance/Regulations/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: Fetch specific Regulation Instance.
                tags:
                  - Hosted
                  - Number
                  - Authorization
                  - Documents
                  - Sid
                  - Orders
                  - Bulk
                  - Hosting
                  - Regulatory
                  - Compliance
                  - Bundles
                  - Bundle
                  - Copies
                  - Signing
                  - Document
                  - Dependent
                  - End
                  - Users
                  - User
                  - Types
                  - Evaluations
                  - Item
                  - Assignments
                  - Regulations
            /v2/RegulatoryCompliance:
              description: 'TODO: Resource-level docs'
            /v2/RegulatoryCompliance/Bundles/{BundleSid}/ReplaceItems:
              description: 'TODO: Resource-level docs'
              post:
                description: >-
                  Replaces all bundle items in the target bundle (specified in
                  the path) with all the bundle items of the source bundle
                  (specified by the from_bundle_sid body param)
                tags:
                  - Hosted
                  - Number
                  - Authorization
                  - Documents
                  - Sid
                  - Orders
                  - Bulk
                  - Hosting
                  - Regulatory
                  - Compliance
                  - Bundles
                  - Bundle
                  - Copies
                  - Signing
                  - Document
                  - Dependent
                  - End
                  - Users
                  - User
                  - Types
                  - Evaluations
                  - Item
                  - Assignments
                  - Regulations
                  - Replace
                  - Items
            /v2/RegulatoryCompliance/SupportingDocuments:
              description: 'TODO: Resource-level docs'
              post:
                description: Create a new Supporting Document.
                tags:
                  - Hosted
                  - Number
                  - Authorization
                  - Documents
                  - Sid
                  - Orders
                  - Bulk
                  - Hosting
                  - Regulatory
                  - Compliance
                  - Bundles
                  - Bundle
                  - Copies
                  - Signing
                  - Document
                  - Dependent
                  - End
                  - Users
                  - User
                  - Types
                  - Evaluations
                  - Item
                  - Assignments
                  - Regulations
                  - Replace
                  - Items
                  - Supporting
              get:
                description: Retrieve a list of all Supporting Document for an account.
                tags:
                  - Hosted
                  - Number
                  - Authorization
                  - Documents
                  - Sid
                  - Orders
                  - Bulk
                  - Hosting
                  - Regulatory
                  - Compliance
                  - Bundles
                  - Bundle
                  - Copies
                  - Signing
                  - Document
                  - Dependent
                  - End
                  - Users
                  - User
                  - Types
                  - Evaluations
                  - Item
                  - Assignments
                  - Regulations
                  - Replace
                  - Items
                  - Supporting
            /v2/RegulatoryCompliance/SupportingDocuments/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: Fetch specific Supporting Document Instance.
                tags:
                  - Hosted
                  - Number
                  - Authorization
                  - Documents
                  - Sid
                  - Orders
                  - Bulk
                  - Hosting
                  - Regulatory
                  - Compliance
                  - Bundles
                  - Bundle
                  - Copies
                  - Signing
                  - Document
                  - Dependent
                  - End
                  - Users
                  - User
                  - Types
                  - Evaluations
                  - Item
                  - Assignments
                  - Regulations
                  - Replace
                  - Items
                  - Supporting
              post:
                description: Update an existing Supporting Document.
                tags:
                  - Hosted
                  - Number
                  - Authorization
                  - Documents
                  - Sid
                  - Orders
                  - Bulk
                  - Hosting
                  - Regulatory
                  - Compliance
                  - Bundles
                  - Bundle
                  - Copies
                  - Signing
                  - Document
                  - Dependent
                  - End
                  - Users
                  - User
                  - Types
                  - Evaluations
                  - Item
                  - Assignments
                  - Regulations
                  - Replace
                  - Items
                  - Supporting
              delete:
                description: Delete a specific Supporting Document.
                tags:
                  - Hosted
                  - Number
                  - Authorization
                  - Documents
                  - Sid
                  - Orders
                  - Bulk
                  - Hosting
                  - Regulatory
                  - Compliance
                  - Bundles
                  - Bundle
                  - Copies
                  - Signing
                  - Document
                  - Dependent
                  - End
                  - Users
                  - User
                  - Types
                  - Evaluations
                  - Item
                  - Assignments
                  - Regulations
                  - Replace
                  - Items
                  - Supporting
            /v2/RegulatoryCompliance/SupportingDocumentTypes:
              description: 'TODO: Resource-level docs'
              get:
                description: Retrieve a list of all Supporting Document Types.
                tags:
                  - Hosted
                  - Number
                  - Authorization
                  - Documents
                  - Sid
                  - Orders
                  - Bulk
                  - Hosting
                  - Regulatory
                  - Compliance
                  - Bundles
                  - Bundle
                  - Copies
                  - Signing
                  - Document
                  - Dependent
                  - End
                  - Users
                  - User
                  - Types
                  - Evaluations
                  - Item
                  - Assignments
                  - Regulations
                  - Replace
                  - Items
                  - Supporting
            /v2/RegulatoryCompliance/SupportingDocumentTypes/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: Fetch a specific Supporting Document Type Instance.
                tags:
                  - Hosted
                  - Number
                  - Authorization
                  - Documents
                  - Sid
                  - Orders
                  - Bulk
                  - Hosting
                  - Regulatory
                  - Compliance
                  - Bundles
                  - Bundle
                  - Copies
                  - Signing
                  - Document
                  - Dependent
                  - End
                  - Users
                  - User
                  - Types
                  - Evaluations
                  - Item
                  - Assignments
                  - Regulations
                  - Replace
                  - Items
                  - Supporting
          tags:
            - name: NumbersV2AuthorizationDocument
            - name: NumbersV2BulkHostedNumberOrder
            - name: NumbersV2Bundle
            - name: NumbersV2BundleCopy
            - name: NumbersV2DependentHostedNumberOrder
            - name: NumbersV2EndUser
            - name: NumbersV2EndUserType
            - name: NumbersV2Evaluation
            - name: NumbersV2HostedNumberOrder
            - name: NumbersV2ItemAssignment
            - name: NumbersV2Regulation
            - name: NumbersV2ReplaceItems
            - name: NumbersV2SupportingDocument
            - name: NumbersV2SupportingDocumentType
          x-maturity:
            - name: GA
              description: This product is Generally Available.
            - name: Beta
              description: >-
                PLEASE NOTE that this is a Beta product that is subject to
                change. U
    overlays:
      - type: APIs.io Search
        url: overlays/numbers-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/numbers-openapi-api-evangelist-ratings.yml
  - aid: twilio:twilio-trust-hub-api
    name: Twilio Trust Hub API
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
            title: Twilio - Trusthub
            license:
              name: Apache 2.0
              url: https://www.apache.org/licenses/LICENSE-2.0.html
          openapi: 3.0.1
          paths:
            /v1/ComplianceInquiries/Customers/Initialize:
              description: 'TODO: Resource-level docs'
              post:
                description: >-
                  Create a new Compliance Inquiry for the authenticated account.
                  This is necessary to start a new embedded session.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
            /v1/ComplianceInquiries/Customers/{CustomerId}/Initialize:
              description: 'TODO: Resource-level docs'
              post:
                description: >-
                  Resume a specific Compliance Inquiry that has expired, or
                  re-open a rejected Compliance Inquiry for editing.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
            /v1/ComplianceInquiries/Tollfree/Initialize:
              description: 'TODO: Resource-level docs'
              post:
                description: >-
                  Create a new Compliance Tollfree Verification Inquiry for the
                  authenticated account. This is necessary to start a new
                  embedded session.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
            /v1/CustomerProfiles:
              description: 'TODO: Resource-level docs'
              post:
                description: Create a new Customer-Profile.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
              get:
                description: Retrieve a list of all Customer-Profiles for an account.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
            /v1/CustomerProfiles/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: Fetch a specific Customer-Profile instance.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
              post:
                description: Updates a Customer-Profile in an account.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
              delete:
                description: Delete a specific Customer-Profile.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
            /v1/CustomerProfiles/{CustomerProfileSid}/ChannelEndpointAssignments:
              description: 'TODO: Resource-level docs'
              post:
                description: Create a new Assigned Item.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
                  - Profile
                  - Channel
                  - Endpoint
                  - Assignments
              get:
                description: Retrieve a list of all Assigned Items for an account.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
                  - Profile
                  - Channel
                  - Endpoint
                  - Assignments
            /v1/CustomerProfiles/{CustomerProfileSid}/ChannelEndpointAssignments/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: Fetch specific Assigned Item Instance.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
                  - Profile
                  - Channel
                  - Endpoint
                  - Assignments
              delete:
                description: Remove an Assignment Item Instance.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
                  - Profile
                  - Channel
                  - Endpoint
                  - Assignments
            /v1/CustomerProfiles/{CustomerProfileSid}/EntityAssignments:
              description: 'TODO: Resource-level docs'
              post:
                description: Create a new Assigned Item.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
                  - Profile
                  - Channel
                  - Endpoint
                  - Assignments
                  - Entity
              get:
                description: Retrieve a list of all Assigned Items for an account.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
                  - Profile
                  - Channel
                  - Endpoint
                  - Assignments
                  - Entity
            /v1/CustomerProfiles/{CustomerProfileSid}/EntityAssignments/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: Fetch specific Assigned Item Instance.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
                  - Profile
                  - Channel
                  - Endpoint
                  - Assignments
                  - Entity
              delete:
                description: Remove an Assignment Item Instance.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
                  - Profile
                  - Channel
                  - Endpoint
                  - Assignments
                  - Entity
            /v1/CustomerProfiles/{CustomerProfileSid}/Evaluations:
              description: 'TODO: Resource-level docs'
              post:
                description: Create a new Evaluation
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
                  - Profile
                  - Channel
                  - Endpoint
                  - Assignments
                  - Entity
                  - Evaluations
              get:
                description: >-
                  Retrieve a list of Evaluations associated to the
                  customer_profile resource.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
                  - Profile
                  - Channel
                  - Endpoint
                  - Assignments
                  - Entity
                  - Evaluations
            /v1/CustomerProfiles/{CustomerProfileSid}/Evaluations/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: Fetch specific Evaluation Instance.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
                  - Profile
                  - Channel
                  - Endpoint
                  - Assignments
                  - Entity
                  - Evaluations
            /v1/EndUsers:
              description: 'TODO: Resource-level docs'
              post:
                description: Create a new End User.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
                  - Profile
                  - Channel
                  - Endpoint
                  - Assignments
                  - Entity
                  - Evaluations
                  - End
                  - Users
              get:
                description: Retrieve a list of all End User for an account.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
                  - Profile
                  - Channel
                  - Endpoint
                  - Assignments
                  - Entity
                  - Evaluations
                  - End
                  - Users
            /v1/EndUsers/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: Fetch specific End User Instance.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
                  - Profile
                  - Channel
                  - Endpoint
                  - Assignments
                  - Entity
                  - Evaluations
                  - End
                  - Users
              post:
                description: Update an existing End User.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
                  - Profile
                  - Channel
                  - Endpoint
                  - Assignments
                  - Entity
                  - Evaluations
                  - End
                  - Users
              delete:
                description: Delete a specific End User.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
                  - Profile
                  - Channel
                  - Endpoint
                  - Assignments
                  - Entity
                  - Evaluations
                  - End
                  - Users
            /v1/EndUserTypes:
              description: 'TODO: Resource-level docs'
              get:
                description: Retrieve a list of all End-User Types.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
                  - Profile
                  - Channel
                  - Endpoint
                  - Assignments
                  - Entity
                  - Evaluations
                  - End
                  - Users
                  - User
                  - Types
            /v1/EndUserTypes/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: Fetch a specific End-User Type Instance.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
                  - Profile
                  - Channel
                  - Endpoint
                  - Assignments
                  - Entity
                  - Evaluations
                  - End
                  - Users
                  - User
                  - Types
            /v1/Policies:
              description: 'TODO: Resource-level docs'
              get:
                description: Retrieve a list of all Policys.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
                  - Profile
                  - Channel
                  - Endpoint
                  - Assignments
                  - Entity
                  - Evaluations
                  - End
                  - Users
                  - User
                  - Types
                  - Policies
            /v1/Policies/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: Fetch specific Policy Instance.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
                  - Profile
                  - Channel
                  - Endpoint
                  - Assignments
                  - Entity
                  - Evaluations
                  - End
                  - Users
                  - User
                  - Types
                  - Policies
            /v1/SupportingDocuments:
              description: 'TODO: Resource-level docs'
              post:
                description: Create a new Supporting Document.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
                  - Profile
                  - Channel
                  - Endpoint
                  - Assignments
                  - Entity
                  - Evaluations
                  - End
                  - Users
                  - User
                  - Types
                  - Policies
                  - Supporting
                  - Documents
              get:
                description: Retrieve a list of all Supporting Document for an account.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
                  - Profile
                  - Channel
                  - Endpoint
                  - Assignments
                  - Entity
                  - Evaluations
                  - End
                  - Users
                  - User
                  - Types
                  - Policies
                  - Supporting
                  - Documents
            /v1/SupportingDocuments/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: Fetch specific Supporting Document Instance.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
                  - Profile
                  - Channel
                  - Endpoint
                  - Assignments
                  - Entity
                  - Evaluations
                  - End
                  - Users
                  - User
                  - Types
                  - Policies
                  - Supporting
                  - Documents
              post:
                description: Update an existing Supporting Document.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
                  - Profile
                  - Channel
                  - Endpoint
                  - Assignments
                  - Entity
                  - Evaluations
                  - End
                  - Users
                  - User
                  - Types
                  - Policies
                  - Supporting
                  - Documents
              delete:
                description: Delete a specific Supporting Document.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
                  - Profile
                  - Channel
                  - Endpoint
                  - Assignments
                  - Entity
                  - Evaluations
                  - End
                  - Users
                  - User
                  - Types
                  - Policies
                  - Supporting
                  - Documents
            /v1/SupportingDocumentTypes:
              description: 'TODO: Resource-level docs'
              get:
                description: Retrieve a list of all Supporting Document Types.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
                  - Profile
                  - Channel
                  - Endpoint
                  - Assignments
                  - Entity
                  - Evaluations
                  - End
                  - Users
                  - User
                  - Types
                  - Policies
                  - Supporting
                  - Documents
                  - Document
            /v1/SupportingDocumentTypes/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: Fetch a specific Supporting Document Type Instance.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
                  - Profile
                  - Channel
                  - Endpoint
                  - Assignments
                  - Entity
                  - Evaluations
                  - End
                  - Users
                  - User
                  - Types
                  - Policies
                  - Supporting
                  - Documents
                  - Document
            /v1/TrustProducts:
              description: 'TODO: Resource-level docs'
              post:
                description: Create a new Customer-Profile.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
                  - Profile
                  - Channel
                  - Endpoint
                  - Assignments
                  - Entity
                  - Evaluations
                  - End
                  - Users
                  - User
                  - Types
                  - Policies
                  - Supporting
                  - Documents
                  - Document
                  - Trust
                  - Products
              get:
                description: Retrieve a list of all Customer-Profiles for an account.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
                  - Profile
                  - Channel
                  - Endpoint
                  - Assignments
                  - Entity
                  - Evaluations
                  - End
                  - Users
                  - User
                  - Types
                  - Policies
                  - Supporting
                  - Documents
                  - Document
                  - Trust
                  - Products
            /v1/TrustProducts/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: Fetch a specific Customer-Profile instance.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
                  - Profile
                  - Channel
                  - Endpoint
                  - Assignments
                  - Entity
                  - Evaluations
                  - End
                  - Users
                  - User
                  - Types
                  - Policies
                  - Supporting
                  - Documents
                  - Document
                  - Trust
                  - Products
              post:
                description: Updates a Customer-Profile in an account.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
                  - Profile
                  - Channel
                  - Endpoint
                  - Assignments
                  - Entity
                  - Evaluations
                  - End
                  - Users
                  - User
                  - Types
                  - Policies
                  - Supporting
                  - Documents
                  - Document
                  - Trust
                  - Products
              delete:
                description: Delete a specific Customer-Profile.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
                  - Profile
                  - Channel
                  - Endpoint
                  - Assignments
                  - Entity
                  - Evaluations
                  - End
                  - Users
                  - User
                  - Types
                  - Policies
                  - Supporting
                  - Documents
                  - Document
                  - Trust
                  - Products
            /v1/TrustProducts/{TrustProductSid}/ChannelEndpointAssignments:
              description: 'TODO: Resource-level docs'
              post:
                description: Create a new Assigned Item.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
                  - Profile
                  - Channel
                  - Endpoint
                  - Assignments
                  - Entity
                  - Evaluations
                  - End
                  - Users
                  - User
                  - Types
                  - Policies
                  - Supporting
                  - Documents
                  - Document
                  - Trust
                  - Products
                  - Product
              get:
                description: Retrieve a list of all Assigned Items for an account.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
                  - Profile
                  - Channel
                  - Endpoint
                  - Assignments
                  - Entity
                  - Evaluations
                  - End
                  - Users
                  - User
                  - Types
                  - Policies
                  - Supporting
                  - Documents
                  - Document
                  - Trust
                  - Products
                  - Product
            /v1/TrustProducts/{TrustProductSid}/ChannelEndpointAssignments/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: Fetch specific Assigned Item Instance.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
                  - Profile
                  - Channel
                  - Endpoint
                  - Assignments
                  - Entity
                  - Evaluations
                  - End
                  - Users
                  - User
                  - Types
                  - Policies
                  - Supporting
                  - Documents
                  - Document
                  - Trust
                  - Products
                  - Product
              delete:
                description: Remove an Assignment Item Instance.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
                  - Profile
                  - Channel
                  - Endpoint
                  - Assignments
                  - Entity
                  - Evaluations
                  - End
                  - Users
                  - User
                  - Types
                  - Policies
                  - Supporting
                  - Documents
                  - Document
                  - Trust
                  - Products
                  - Product
            /v1/TrustProducts/{TrustProductSid}/EntityAssignments:
              description: 'TODO: Resource-level docs'
              post:
                description: Create a new Assigned Item.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
                  - Profile
                  - Channel
                  - Endpoint
                  - Assignments
                  - Entity
                  - Evaluations
                  - End
                  - Users
                  - User
                  - Types
                  - Policies
                  - Supporting
                  - Documents
                  - Document
                  - Trust
                  - Products
                  - Product
              get:
                description: Retrieve a list of all Assigned Items for an account.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
                  - Profile
                  - Channel
                  - Endpoint
                  - Assignments
                  - Entity
                  - Evaluations
                  - End
                  - Users
                  - User
                  - Types
                  - Policies
                  - Supporting
                  - Documents
                  - Document
                  - Trust
                  - Products
                  - Product
            /v1/TrustProducts/{TrustProductSid}/EntityAssignments/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: Fetch specific Assigned Item Instance.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
                  - Profile
                  - Channel
                  - Endpoint
                  - Assignments
                  - Entity
                  - Evaluations
                  - End
                  - Users
                  - User
                  - Types
                  - Policies
                  - Supporting
                  - Documents
                  - Document
                  - Trust
                  - Products
                  - Product
              delete:
                description: Remove an Assignment Item Instance.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
                  - Profile
                  - Channel
                  - Endpoint
                  - Assignments
                  - Entity
                  - Evaluations
                  - End
                  - Users
                  - User
                  - Types
                  - Policies
                  - Supporting
                  - Documents
                  - Document
                  - Trust
                  - Products
                  - Product
            /v1/TrustProducts/{TrustProductSid}/Evaluations:
              description: 'TODO: Resource-level docs'
              post:
                description: Create a new Evaluation
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
                  - Profile
                  - Channel
                  - Endpoint
                  - Assignments
                  - Entity
                  - Evaluations
                  - End
                  - Users
                  - User
                  - Types
                  - Policies
                  - Supporting
                  - Documents
                  - Document
                  - Trust
                  - Products
                  - Product
              get:
                description: >-
                  Retrieve a list of Evaluations associated to the trust_product
                  resource.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
                  - Profile
                  - Channel
                  - Endpoint
                  - Assignments
                  - Entity
                  - Evaluations
                  - End
                  - Users
                  - User
                  - Types
                  - Policies
                  - Supporting
                  - Documents
                  - Document
                  - Trust
                  - Products
                  - Product
            /v1/TrustProducts/{TrustProductSid}/Evaluations/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: Fetch specific Evaluation Instance.
                tags:
                  - Compliance
                  - Inquiries
                  - Customers
                  - Initialize
                  - Customer
                  - Id
                  - Tollfree
                  - Profiles
                  - Sid
                  - Profile
                  - Channel
                  - Endpoint
                  - Assignments
                  - Entity
                  - Evaluations
                  - End
                  - Users
                  - User
                  - Types
                  - Policies
                  - Supporting
                  - Documents
                  - Document
                  - Trust
                  - Products
                  - Product
          tags:
            - name: TrusthubV1ComplianceInquiries
            - name: TrusthubV1ComplianceTollfreeInquiries
            - name: TrusthubV1CustomerProfiles
            - name: TrusthubV1CustomerProfilesChannelEndpointAssignment
            - name: TrusthubV1CustomerProfilesEntityAssignments
            - name: TrusthubV1CustomerProfilesEvaluations
            - name: TrusthubV1EndUser
            - name: TrusthubV1EndUserType
            - name: TrusthubV1Policies
            - name: TrusthubV1SupportingDocument
            - name: TrusthubV1SupportingDocumentType
            - name: TrusthubV1TrustProducts
            - name: TrusthubV1TrustProductsChannelEndpointAssignment
            - name: TrusthubV1TrustProductsEntityAssignments
            - name: TrusthubV1TrustProductsEvaluations
          x-maturity:
            - name: GA
              description: This product is G
    overlays:
      - type: APIs.io Search
        url: overlays/trust-hub-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/trust-hub-openapi-api-evangelist-ratings.yml
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---