---
name: Based
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/based.png
url: https://example.com/apis/based.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Based
apis:
  - name: customer-profiles
    description: >-
      <fullname>Amazon Connect Customer Profiles</fullname> <p>Amazon Connect
      Customer Profiles is a unified customer profile for your contact center
      that has pre-built connectors powered by AppFlow that make it easy to
      combine customer information from third party applications, such as
      Salesforce (CRM), ServiceNow (ITSM), and your enterprise resource planning
      (ERP), with contact history from your Amazon Connect contact center. If
      you're new to Amazon Connect, you might find it helpful to review the <a
      href="https://docs.aws.amazon.com/connect/latest/adminguide/">Amazon
      Connect Administrator Guide</a>.</p>
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
            title: customer-profiles
          paths:
            /domains/{DomainName}/profiles/keys:
              POST:
                summary: AddProfileKey
                description: >-
                  <p>Associates a new key value with a specific profile, such as
                  a Contact Record ContactId.</p> <p>A profile object can have a
                  single unique key and any number of additional keys that can
                  be used to identify the profile that it belongs to.</p>
                tags:
                  - Add
                  - Profiles
                  - Keys
                  - Domains
                  - Names
                  - Profiles
                  - Keys
            /domains/{DomainName}/calculated-attributes/{CalculatedAttributeName}:
              PUT:
                summary: UpdateCalculatedAttributeDefinition
                description: >-
                  <p>Updates an existing calculated attribute definition. When
                  updating the Conditions, note that increasing the date range
                  of a calculated attribute will not trigger inclusion of
                  historical data greater than the current date range.</p>
                tags:
                  - Update
                  - Calculated
                  - Attributes
                  - Definitions
                  - Domains
                  - Names
                  - Profiles
                  - Keys
                  - Calculated
                  - Attributes
                  - Attributes
            /domains/{DomainName}:
              PUT:
                summary: UpdateDomain
                description: >-
                  <p>Updates the properties of a domain, including creating or
                  selecting a dead letter queue or an encryption key.</p>
                  <p>After a domain is created, the name can’t be changed.</p>
                  <p>Use this API or <a
                  href="https://docs.aws.amazon.com/customerprofiles/latest/APIReference/API_CreateDomain.html">CreateDomain</a>
                  to enable <a
                  href="https://docs.aws.amazon.com/customerprofiles/latest/APIReference/API_GetMatches.html">identity
                  resolution</a>: set <code>Matching</code> to true.</p> <p>To
                  prevent cross-service impersonation when you call this API,
                  see <a
                  href="https://docs.aws.amazon.com/connect/latest/adminguide/cross-service-confused-deputy-prevention.html">Cross-service
                  confused deputy prevention</a> for sample policies that you
                  should apply. </p> <p>To add or remove tags on an existing
                  Domain, see <a
                  href="https://docs.aws.amazon.com/customerprofiles/latest/APIReference/API_TagResource.html">TagResource</a>/<a
                  href="https://docs.aws.amazon.com/customerprofiles/latest/APIReference/API_UntagResource.html">UntagResource</a>.</p>
                tags:
                  - Update
                  - Domains
                  - Domains
                  - Names
                  - Profiles
                  - Keys
                  - Calculated
                  - Attributes
                  - Attributes
            /domains/{DomainName}/event-streams/{EventStreamName}:
              GET:
                summary: GetEventStream
                description: >-
                  <p>Returns information about the specified event stream in a
                  specific domain.</p>
                tags:
                  - Get
                  - Events
                  - Stream
                  - Domains
                  - Names
                  - Profiles
                  - Keys
                  - Calculated
                  - Attributes
                  - Attributes
                  - Events
                  - Streams
                  - Stream
            /domains/{DomainName}/workflows/integrations:
              POST:
                summary: CreateIntegrationWorkflow
                description: >-
                  <p> Creates an integration workflow. An integration workflow
                  is an async process which ingests historic data and sets up an
                  integration for ongoing updates. The supported Amazon AppFlow
                  sources are Salesforce, ServiceNow, and Marketo. </p>
                tags:
                  - Create
                  - Integrations
                  - Workflows
                  - Domains
                  - Names
                  - Profiles
                  - Keys
                  - Calculated
                  - Attributes
                  - Attributes
                  - Events
                  - Streams
                  - Stream
                  - Workflows
                  - Integrations
            /domains/{DomainName}/profiles:
              PUT:
                summary: UpdateProfile
                description: >-
                  <p>Updates the properties of a profile. The ProfileId is
                  required for updating a customer profile.</p> <p>When calling
                  the UpdateProfile API, specifying an empty string value means
                  that any existing value will be removed. Not specifying a
                  string value means that any value already there will be
                  kept.</p>
                tags:
                  - Update
                  - Profiles
                  - Domains
                  - Names
                  - Profiles
                  - Keys
                  - Calculated
                  - Attributes
                  - Attributes
                  - Events
                  - Streams
                  - Stream
                  - Workflows
                  - Integrations
            /domains/{DomainName}/integrations/delete:
              POST:
                summary: DeleteIntegration
                description: <p>Removes an integration from a specific domain.</p>
                tags:
                  - Delete
                  - Integrations
                  - Domains
                  - Names
                  - Profiles
                  - Keys
                  - Calculated
                  - Attributes
                  - Attributes
                  - Events
                  - Streams
                  - Stream
                  - Workflows
                  - Integrations
                  - Delete
            /domains/{DomainName}/profiles/delete:
              POST:
                summary: DeleteProfile
                description: >-
                  <p>Deletes the standard customer profile and all data
                  pertaining to the profile.</p>
                tags:
                  - Delete
                  - Profiles
                  - Domains
                  - Names
                  - Profiles
                  - Keys
                  - Calculated
                  - Attributes
                  - Attributes
                  - Events
                  - Streams
                  - Stream
                  - Workflows
                  - Integrations
                  - Delete
            /domains/{DomainName}/profiles/keys/delete:
              POST:
                summary: DeleteProfileKey
                description: <p>Removes a searchable key from a customer profile.</p>
                tags:
                  - Delete
                  - Profiles
                  - Keys
                  - Domains
                  - Names
                  - Profiles
                  - Keys
                  - Calculated
                  - Attributes
                  - Attributes
                  - Events
                  - Streams
                  - Stream
                  - Workflows
                  - Integrations
                  - Delete
            /domains/{DomainName}/profiles/objects/delete:
              POST:
                summary: DeleteProfileObject
                description: >-
                  <p>Removes an object associated with a profile of a given
                  ProfileObjectType.</p>
                tags:
                  - Delete
                  - Profiles
                  - Objects
                  - Domains
                  - Names
                  - Profiles
                  - Keys
                  - Calculated
                  - Attributes
                  - Attributes
                  - Events
                  - Streams
                  - Stream
                  - Workflows
                  - Integrations
                  - Delete
                  - Objects
            /domains/{DomainName}/object-types/{ObjectTypeName}:
              PUT:
                summary: PutProfileObjectType
                description: >-
                  <p>Defines a ProfileObjectType.</p> <p>To add or remove tags
                  on an existing ObjectType, see <a
                  href="https://docs.aws.amazon.com/customerprofiles/latest/APIReference/API_TagResource.html">
                  TagResource</a>/<a
                  href="https://docs.aws.amazon.com/customerprofiles/latest/APIReference/API_UntagResource.html">UntagResource</a>.</p>
                tags:
                  - Put
                  - Profiles
                  - Objects
                  - Types
                  - Domains
                  - Names
                  - Profiles
                  - Keys
                  - Calculated
                  - Attributes
                  - Attributes
                  - Events
                  - Streams
                  - Stream
                  - Workflows
                  - Integrations
                  - Delete
                  - Objects
                  - Objects
                  - Types
                  - Types
            /domains/{DomainName}/workflows/{WorkflowId}:
              GET:
                summary: GetWorkflow
                description: <p>Get details of specified workflow.</p>
                tags:
                  - Get
                  - Workflows
                  - Domains
                  - Names
                  - Profiles
                  - Keys
                  - Calculated
                  - Attributes
                  - Attributes
                  - Events
                  - Streams
                  - Stream
                  - Workflows
                  - Integrations
                  - Delete
                  - Objects
                  - Objects
                  - Types
                  - Types
                  - Workflows
                  - Identifiers
            /domains/{DomainName}/detect/object-types:
              POST:
                summary: DetectProfileObjectType
                description: >-
                  <p>The process of detecting profile object type mapping by
                  using given objects.</p>
                tags:
                  - Detect
                  - Profiles
                  - Objects
                  - Types
                  - Domains
                  - Names
                  - Profiles
                  - Keys
                  - Calculated
                  - Attributes
                  - Attributes
                  - Events
                  - Streams
                  - Stream
                  - Workflows
                  - Integrations
                  - Delete
                  - Objects
                  - Objects
                  - Types
                  - Types
                  - Workflows
                  - Identifiers
                  - Detect
            /domains/{DomainName}/identity-resolution-jobs/auto-merging-preview:
              POST:
                summary: GetAutoMergingPreview
                description: >-
                  <p>Tests the auto-merging settings of your Identity Resolution
                  Job without merging your data. It randomly selects a sample of
                  matching groups from the existing matching results, and
                  applies the automerging settings that you provided. You can
                  then view the number of profiles in the sample, the number of
                  matches, and the number of profiles identified to be merged.
                  This enables you to evaluate the accuracy of the attributes in
                  your matching list. </p> <p>You can't view which profiles are
                  matched and would be merged.</p> <important> <p>We strongly
                  recommend you use this API to do a dry run of the automerging
                  process before running the Identity Resolution Job. Include
                  <b>at least</b> two matching attributes. If your matching list
                  includes too few attributes (such as only
                  <code>FirstName</code> or only <code>LastName</code>), there
                  may be a large number of matches. This increases the chances
                  of erroneous merges.</p> </important>
                tags:
                  - Get
                  - Auto
                  - Merging
                  - Preview
                  - Domains
                  - Names
                  - Profiles
                  - Keys
                  - Calculated
                  - Attributes
                  - Attributes
                  - Events
                  - Streams
                  - Stream
                  - Workflows
                  - Integrations
                  - Delete
                  - Objects
                  - Objects
                  - Types
                  - Types
                  - Workflows
                  - Identifiers
                  - Detect
                  - Identity
                  - Resolutions
                  - Jobs
                  - Auto
                  - Merging
                  - Preview
            /domains/{DomainName}/profile/{ProfileId}/calculated-attributes/{CalculatedAttributeName}:
              GET:
                summary: GetCalculatedAttributeForProfile
                description: <p>Retrieve a calculated attribute for a customer profile.</p>
                tags:
                  - Get
                  - Calculated
                  - Attributes
                  - For
                  - Profiles
                  - Domains
                  - Names
                  - Profiles
                  - Keys
                  - Calculated
                  - Attributes
                  - Attributes
                  - Events
                  - Streams
                  - Stream
                  - Workflows
                  - Integrations
                  - Delete
                  - Objects
                  - Objects
                  - Types
                  - Types
                  - Workflows
                  - Identifiers
                  - Detect
                  - Identity
                  - Resolutions
                  - Jobs
                  - Auto
                  - Merging
                  - Preview
                  - Profiles
            /domains/{DomainName}/identity-resolution-jobs/{JobId}:
              GET:
                summary: GetIdentityResolutionJob
                description: >-
                  <p>Returns information about an Identity Resolution Job in a
                  specific domain. </p> <p>Identity Resolution Jobs are set up
                  using the Amazon Connect admin console. For more information,
                  see <a
                  href="https://docs.aws.amazon.com/connect/latest/adminguide/use-identity-resolution.html">Use
                  Identity Resolution to consolidate similar profiles</a>.</p>
                tags:
                  - Get
                  - Identity
                  - Resolutions
                  - Jobs
                  - Domains
                  - Names
                  - Profiles
                  - Keys
                  - Calculated
                  - Attributes
                  - Attributes
                  - Events
                  - Streams
                  - Stream
                  - Workflows
                  - Integrations
                  - Delete
                  - Objects
                  - Objects
                  - Types
                  - Types
                  - Workflows
                  - Identifiers
                  - Detect
                  - Identity
                  - Resolutions
                  - Jobs
                  - Auto
                  - Merging
                  - Preview
                  - Profiles
                  - Jobs
            /domains/{DomainName}/integrations:
              PUT:
                summary: PutIntegration
                description: >-
                  <p>Adds an integration between the service and a third-party
                  service, which includes Amazon AppFlow and Amazon Connect.</p>
                  <p>An integration can belong to only one domain.</p> <p>To add
                  or remove tags on an existing Integration, see <a
                  href="https://docs.aws.amazon.com/customerprofiles/latest/APIReference/API_TagResource.html">
                  TagResource </a>/<a
                  href="https://docs.aws.amazon.com/customerprofiles/latest/APIReference/API_UntagResource.html">
                  UntagResource</a>.</p>
                tags:
                  - Put
                  - Integrations
                  - Domains
                  - Names
                  - Profiles
                  - Keys
                  - Calculated
                  - Attributes
                  - Attributes
                  - Events
                  - Streams
                  - Stream
                  - Workflows
                  - Integrations
                  - Delete
                  - Objects
                  - Objects
                  - Types
                  - Types
                  - Workflows
                  - Identifiers
                  - Detect
                  - Identity
                  - Resolutions
                  - Jobs
                  - Auto
                  - Merging
                  - Preview
                  - Profiles
                  - Jobs
            /domains/{DomainName}/matches:
              POST:
                summary: GetSimilarProfiles
                description: >-
                  <p>Returns a set of profiles that belong to the same matching
                  group using the <code>matchId</code> or
                  <code>profileId</code>. You can also specify the type of
                  matching that you want for finding similar profiles using
                  either <code>RULE_BASED_MATCHING</code> or
                  <code>ML_BASED_MATCHING</code>.</p>
                tags:
                  - Get
                  - Similar
                  - Profiles
                  - Domains
                  - Names
                  - Profiles
                  - Keys
                  - Calculated
                  - Attributes
                  - Attributes
                  - Events
                  - Streams
                  - Stream
                  - Workflows
                  - Integrations
                  - Delete
                  - Objects
                  - Objects
                  - Types
                  - Types
                  - Workflows
                  - Identifiers
                  - Detect
                  - Identity
                  - Resolutions
                  - Jobs
                  - Auto
                  - Merging
                  - Preview
                  - Profiles
                  - Jobs
                  - Matches
            /templates/{TemplateId}:
              GET:
                summary: GetProfileObjectTypeTemplate
                description: >-
                  <p>Returns the template information for a specific object
                  type.</p> <p>A template is a predefined ProfileObjectType,
                  such as “Salesforce-Account” or “Salesforce-Contact.” When a
                  user sends a ProfileObject, using the PutProfileObject API,
                  with an ObjectTypeName that matches one of the TemplateIds, it
                  uses the mappings from the template.</p>
                tags:
                  - Get
                  - Profiles
                  - Objects
                  - Types
                  - Templates
                  - Domains
                  - Names
                  - Profiles
                  - Keys
                  - Calculated
                  - Attributes
                  - Attributes
                  - Events
                  - Streams
                  - Stream
                  - Workflows
                  - Integrations
                  - Delete
                  - Objects
                  - Objects
                  - Types
                  - Types
                  - Workflows
                  - Identifiers
                  - Detect
                  - Identity
                  - Resolutions
                  - Jobs
                  - Auto
                  - Merging
                  - Preview
                  - Profiles
                  - Jobs
                  - Matches
                  - Templates
            /domains/{DomainName}/workflows/{WorkflowId}/steps:
              GET:
                summary: GetWorkflowSteps
                description: <p>Get granular list of steps in workflow.</p>
                tags:
                  - Get
                  - Workflows
                  - Steps
                  - Domains
                  - Names
                  - Profiles
                  - Keys
                  - Calculated
                  - Attributes
                  - Attributes
                  - Events
                  - Streams
                  - Stream
                  - Workflows
                  - Integrations
                  - Delete
                  - Objects
                  - Objects
                  - Types
                  - Types
                  - Workflows
                  - Identifiers
                  - Detect
                  - Identity
                  - Resolutions
                  - Jobs
                  - Auto
                  - Merging
                  - Preview
                  - Profiles
                  - Jobs
                  - Matches
                  - Templates
                  - Steps
            /integrations:
              POST:
                summary: ListAccountIntegrations
                description: >-
                  <p>Lists all of the integrations associated to a specific URI
                  in the AWS account.</p>
                tags:
                  - Lists
                  - Account
                  - Integrations
                  - Domains
                  - Names
                  - Profiles
                  - Keys
                  - Calculated
                  - Attributes
                  - Attributes
                  - Events
                  - Streams
                  - Stream
                  - Workflows
                  - Integrations
                  - Delete
                  - Objects
                  - Objects
                  - Types
                  - Types
                  - Workflows
                  - Identifiers
                  - Detect
                  - Identity
                  - Resolutions
                  - Jobs
                  - Auto
                  - Merging
                  - Preview
                  - Profiles
                  - Jobs
                  - Matches
                  - Templates
                  - Steps
            /domains/{DomainName}/calculated-attributes:
              GET:
                summary: ListCalculatedAttributeDefinitions
                description: >-
                  <p>Lists calculated attribute definitions for Customer
                  Profiles</p>
                tags:
                  - Lists
                  - Calculated
                  - Attributes
                  - Definitions
                  - Domains
                  - Names
                  - Profiles
                  - Keys
                  - Calculated
                  - Attributes
                  - Attributes
                  - Events
                  - Streams
                  - Stream
                  - Workflows
                  - Integrations
                  - Delete
                  - Objects
                  - Objects
                  - Types
                  - Types
                  - Workflows
                  - Identifiers
                  - Detect
                  - Identity
                  - Resolutions
                  - Jobs
                  - Auto
                  - Merging
                  - Preview
                  - Profiles
                  - Jobs
                  - Matches
                  - Templates
                  - Steps
            /domains/{DomainName}/profile/{ProfileId}/calculated-attributes:
              GET:
                summary: ListCalculatedAttributesForProfile
                description: >-
                  <p>Retrieve a list of calculated attributes for a customer
                  profile.</p>
                tags:
                  - Lists
                  - Calculated
                  - Attributes
                  - For
                  - Profiles
                  - Domains
                  - Names
                  - Profiles
                  - Keys
                  - Calculated
                  - Attributes
                  - Attributes
                  - Events
                  - Streams
                  - Stream
                  - Workflows
                  - Integrations
                  - Delete
                  - Objects
                  - Objects
                  - Types
                  - Types
                  - Workflows
                  - Identifiers
                  - Detect
                  - Identity
                  - Resolutions
                  - Jobs
                  - Auto
                  - Merging
                  - Preview
                  - Profiles
                  - Jobs
                  - Matches
                  - Templates
                  - Steps
            /domains:
              GET:
                summary: ListDomains
                description: >-
                  <p>Returns a list of all the domains for an AWS account that
                  have been created.</p>
                tags:
                  - Lists
                  - Domains
                  - Domains
                  - Names
                  - Profiles
                  - Keys
                  - Calculated
                  - Attributes
                  - Attributes
                  - Events
                  - Streams
                  - Stream
                  - Workflows
                  - Integrations
                  - Delete
                  - Objects
                  - Objects
                  - Types
                  - Types
                  - Workflows
                  - Identifiers
                  - Detect
                  - Identity
                  - Resolutions
                  - Jobs
                  - Auto
                  - Merging
                  - Preview
                  - Profiles
                  - Jobs
                  - Matches
                  - Templates
                  - Steps
                  - Domains
            /domains/{DomainName}/event-streams:
              GET:
                summary: ListEventStreams
                description: >-
                  <p>Returns a list of all the event streams in a specific
                  domain.</p>
                tags:
                  - Lists
                  - Events
                  - Streams
                  - Domains
                  - Names
                  - Profiles
                  - Keys
                  - Calculated
                  - Attributes
                  - Attributes
                  - Events
                  - Streams
                  - Stream
                  - Workflows
                  - Integrations
                  - Delete
                  - Objects
                  - Objects
                  - Types
                  - Types
                  - Workflows
                  - Identifiers
                  - Detect
                  - Identity
                  - Resolutions
                  - Jobs
                  - Auto
                  - Merging
                  - Preview
                  - Profiles
                  - Jobs
                  - Matches
                  - Templates
                  - Steps
                  - Domains
            /domains/{DomainName}/identity-resolution-jobs:
              GET:
                summary: ListIdentityResolutionJobs
                description: >-
                  <p>Lists all of the Identity Resolution Jobs in your domain.
                  The response sorts the list by <code>JobStartTime</code>.</p>
                tags:
                  - Lists
                  - Identity
                  - Resolutions
                  - Jobs
                  - Domains
                  - Names
                  - Profiles
                  - Keys
                  - Calculated
                  - Attributes
                  - Attributes
                  - Events
                  - Streams
                  - Stream
                  - Workflows
                  - Integrations
                  - Delete
                  - Objects
                  - Objects
                  - Types
                  - Types
                  - Workflows
                  - Identifiers
                  - Detect
                  - Identity
                  - Resolutions
                  - Jobs
                  - Auto
                  - Merging
                  - Preview
                  - Profiles
                  - Jobs
                  - Matches
                  - Templates
                  - Steps
                  - Domains
            /templates:
              GET:
                summary: ListProfileObjectTypeTemplates
                description: <p>Lists all of the template information for object types.</p>
                tags:
                  - Lists
                  - Profiles
                  - Objects
                  - Types
                  - Templates
                  - Domains
                  - Names
                  - Profiles
                  - Keys
                  - Calculated
                  - Attributes
                  - Attributes
                  - Events
                  - Streams
                  - Stream
                  - Workflows
                  - Integrations
                  - Delete
                  - Objects
                  - Objects
                  - Types
                  - Types
                  - Workflows
                  - Identifiers
                  - Detect
                  - Identity
                  - Resolutions
                  - Jobs
                  - Auto
                  - Merging
                  - Preview
                  - Profiles
                  - Jobs
                  - Matches
                  - Templates
                  - Steps
                  - Domains
                  - Templates
            /domains/{DomainName}/object-types:
              GET:
                summary: ListProfileObjectTypes
                description: >-
                  <p>Lists all of the templates available within the
                  service.</p>
                tags:
                  - Lists
                  - Profiles
                  - Objects
                  - Types
                  - Domains
                  - Names
                  - Profiles
                  - Keys
                  - Calculated
                  - Attributes
                  - Attributes
                  - Events
                  - Streams
                  - Stream
                  - Workflows
                  - Integrations
                  - Delete
                  - Objects
                  - Objects
                  - Types
                  - Types
                  - Workflows
                  - Identifiers
                  - Detect
                  - Identity
                  - Resolutions
                  - Jobs
                  - Auto
                  - Merging
                  - Preview
                  - Profiles
                  - Jobs
                  - Matches
                  - Templates
                  - Steps
                  - Domains
                  - Templates
            /domains/{DomainName}/profiles/objects:
              PUT:
                summary: PutProfileObject
                description: >-
                  <p>Adds additional objects to customer profiles of a given
                  ObjectType.</p> <p>When adding a specific profile object, like
                  a Contact Record, an inferred profile can get created if it is
                  not mapped to an existing profile. The resulting profile will
                  only have a phone number populated in the standard
                  ProfileObject. Any additional Contact Records with the same
                  phone number will be mapped to the same inferred profile.</p>
                  <p>When a ProfileObject is created and if a ProfileObjectType
                  already exists for the ProfileObject, it will provide data to
                  a standard profile depending on the ProfileObjectType
                  definition.</p> <p>PutProfileObject needs an ObjectType, which
                  can be created using PutProfileObjectType.</p>
                tags:
                  - Put
                  - Profiles
                  - Objects
                  - Domains
                  - Names
                  - Profiles
                  - Keys
                  - Calculated
                  - Attributes
                  - Attributes
                  - Events
                  - Streams
                  - Stream
                  - Workflows
                  - Integrations
                  - Delete
                  - Objects
                  - Objects
                  - Types
                  - Types
                  - Workflows
                  - Identifiers
                  - Detect
                  - Identity
                  - Resolutions
                  - Jobs
                  - Auto
                  - Merging
                  - Preview
                  - Profiles
                  - Jobs
                  - Matches
                  - Templates
                  - Steps
                  - Domains
                  - Templates
            /domains/{DomainName}/profiles/ruleBasedMatches:
              GET:
                summary: ListRuleBasedMatches
                description: >-
                  <p>Returns a set of <code>MatchIds</code> that belong to the
                  given domain.</p>
                tags:
                  - Lists
                  - Rules
                  - Based
                  - Matches
                  - Domains
                  - Names
                  - Profiles
                  - Keys
                  - Calculated
                  - Attributes
                  - Attributes
                  - Events
                  - Streams
                  - Stream
                  - Workflows
                  - Integrations
                  - Delete
                  - Objects
                  - Objects
                  - Types
                  - Types
                  - Workflows
                  - Identifiers
                  - Detect
                  - Identity
                  - Resolutions
                  - Jobs
                  - Auto
                  - Merging
                  - Preview
                  - Profiles
                  - Jobs
                  - Matches
                  - Templates
                  - Steps
                  - Domains
                  - Templates
                  - Rules
                  - Based
            /tags/{resourceArn}:
              DELETE:
                summary: UntagResource
                description: >-
                  <p>Removes one or more tags from the specified Amazon Connect
                  Customer Profiles resource. In Connect Customer Profiles,
                  domains, profile object types, and integrations can be
                  tagged.</p>
                tags:
                  - Untag
                  - Resources
                  - Domains
                  - Names
                  - Profiles
                  - Keys
                  - Calculated
                  - Attributes
                  - Attributes
                  - Events
                  - Streams
                  - Stream
                  - Workflows
                  - Integrations
                  - Delete
                  - Objects
                  - Objects
                  - Types
                  - Types
                  - Workflows
                  - Identifiers
                  - Detect
                  - Identity
                  - Resolutions
                  - Jobs
                  - Auto
                  - Merging
                  - Preview
                  - Profiles
                  - Jobs
                  - Matches
                  - Templates
                  - Steps
                  - Domains
                  - Templates
                  - Rules
                  - Based
                  - ARN
            /domains/{DomainName}/workflows:
              POST:
                summary: ListWorkflows
                description: <p>Query to list all workflows.</p>
                tags:
                  - Lists
                  - Workflows
                  - Domains
                  - Names
                  - Profiles
                  - Keys
                  - Calculated
                  - Attributes
                  - Attributes
                  - Events
                  - Streams
                  - Stream
                  - Workflows
                  - Integrations
                  - Delete
                  - Objects
                  - Objects
                  - Types
                  - Types
                  - Workflows
                  - Identifiers
                  - Detect
                  - Identity
                  - Resolutions
                  - Jobs
                  - Auto
                  - Merging
                  - Preview
                  - Profiles
                  - Jobs
                  - Matches
                  - Templates
                  - Steps
                  - Domains
                  - Templates
                  - Rules
                  - Based
                  - ARN
            /domains/{DomainName}/profiles/objects/merge:
              POST:
                summary: MergeProfiles
                description: >-
                  <p>Runs an AWS Lambda job that does the following:</p> <ol>
                  <li> <p>All the profileKeys in the
                  <code>ProfileToBeMerged</code> will be moved to the main
                  profile.</p> </li> <li> <p>All the objects in the
                  <code>ProfileToBeMerged</code> will be moved to the main
                  profile.</p> </li> <li> <p>All the
                  <code>ProfileToBeMerged</code> will be deleted at the end.</p>
                  </li> <li> <p>All the profileKeys in the
                  <code>ProfileIdsToBeMerged</code> will be moved to the main
                  profile.</p> </li> <li> <p>Standard fields are merged as
                  follows:</p> <ol> <li> <p>Fields are always "union"-ed if
                  there are no conflicts in standard fields or
                  attributeKeys.</p> </li> <li> <p>When there are conflicting
                  fields:</p> <ol> <li> <p>If no <code>SourceProfileIds</code>
                  entry is specified, the main Profile value is always taken.
                  </p> </li> <li> <p>If a <code>SourceProfileIds</code> entry is
                  specified, the specified profileId is always taken, even if it
                  is a NULL value.</p> </li> </ol> </li> </ol> </li> </ol>
                  <p>You can use MergeProfiles together with <a
                  href="https://docs.aws.amazon.com/customerprofiles/latest/APIReference/API_GetMatches.html">GetMatches</a>,
                  which returns potentially matching profiles, or use it with
                  the results of another matching system. After profiles have
                  been merged, they cannot be separated (unmerged).</p>
                tags:
                  - Merge
                  - Profiles
                  - Domains
                  - Names
                  - Profiles
                  - Keys
                  - Calculated
                  - Attributes
                  - Attributes
                  - Events
                  - Streams
                  - Stream
                  - Workflows
                  - Integrations
                  - Delete
                  - Objects
                  - Objects
                  - Types
                  - Types
                  - Workflows
                  - Identifiers
                  - Detect
                  - Identity
                  - Resolutions
                  - Jobs
                  - Auto
                  - Merging
                  - Preview
                  - Profiles
                  - Jobs
                  - Matches
                  - Templates
                  - Steps
                  - Domains
                  - Templates
                  - Rules
                  - Based
                  - ARN
                  - Merge
            /domains/{DomainName}/profiles/search:
              POST:
                summary: SearchProfiles
                description: >-
                  <p>Searches for profiles within a specific domain using one or
                  more predefined search keys (e.g., _fullName, _phone, _email,
                  _account, etc.) and/or custom-defined search keys. A search
                  key is a data type pair that consists of a
                  <code>KeyName</code> and <code>Values</code> list.</p> <p>This
                  operation supports searching for profiles with a minimum of 1
                  key-value(s) pair and up to 5 key-value(s) pairs using either
                  <code>AND</code> or <code>OR</code> 
                tags:
                  - Search
                  - Profiles
                  - Domains
                  - Names
                  - Profiles
                  - Keys
                  - Calculated
                  - Attributes
                  - Attributes
                  - Events
                  - Streams
                  - Stream
                  - Workflows
                  - Integrations
                  - Delete
                  - Objects
                  - Objects
                  - Types
                  - Types
                  - Workflows
                  - Identifiers
                  - Detect
                  - Identity
                  - Resolutions
                  - Jobs
                  - Auto
                  - Merging
                  - Preview
                  - Profiles
                  - Jobs
                  - Matches
                  - Templates
                  - Steps
                  - Domains
                  - Templates
                  - Rules
                  - Based
                  - ARN
                  - Merge
                  - Search
    overlays:
      - type: APIs.io Search
        url: overlays/customer-profiles-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/customer-profiles-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:customer-profiles
  - name: Confluence API
    description: >-
      This is the reference for the Confluence Cloud REST API. This API is the
      primary way to get and modify data in Confluence Cloud, whether you are
      developing an app or any other integration. Use it to interact with
      Confluence entities, like pages and blog posts, spaces, users, groups, and
      more.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.atlassian.com/cloud/confluence/rest/v1/intro/
    baseURL: https://api.example.com
    tags: []
    properties:
      - type: Documentation
        url: https://developer.atlassian.com/cloud/confluence/rest/v1/intro/
      - type: OpenAPI
        data:
          openapi: 3.0.1
          info:
            title: The Confluence Cloud REST API
          externalDocs:
            description: >-
              The online and complete version of the Confluence Cloud REST API
              docs.
            url: https://developer.atlassian.com/cloud/confluence/rest/
          tags:
            - name: Audit
              description: ''
            - name: Analytics
              description: ''
            - name: Content
              description: ''
            - name: Content - attachments
              description: ''
            - name: Content body
              description: ''
            - name: Content - children and descendants
              description: ''
            - name: Content - macro body
              description: ''
            - name: Content comments
              description: ''
            - name: Content labels
              description: ''
            - name: Content permissions
              description: ''
            - name: Content properties
              description: ''
            - name: Content restrictions
              description: ''
            - name: Content states
              description: ''
            - name: Content versions
              description: ''
            - name: Content watches
              description: ''
            - name: Dynamic modules
              description: ''
            - name: Experimental
              description: >-
                APIs in this section can change without any prior deprecation
                notice.
            - name: Group
              description: >-
                **[WARNING](https://support.atlassian.com/user-management/docs/create-and-update-groups/)
                The standard Atlassian group names are default names only and
                can be edited or deleted.**  For example, an admin or Atlassian
                support could delete the default group jira-software-users or
                rename it to jsw-users at any point.
            - name: Inline tasks
              description: ''
            - name: Label info
              description: ''
            - name: Long-running task
              description: ''
            - name: Relation
              description: ''
            - name: Search
              description: ''
            - name: Settings
              description: ''
            - name: Space
              description: ''
            - name: Space permissions
              description: ''
            - name: Space properties
              description: ''
            - name: Space settings
              description: ''
            - name: Templates
              description: ''
            - name: Themes
              description: ''
            - name: Users
              description: ''
            - name: User properties
              description: ''
          paths:
            /wiki/rest/api/audit:
              get:
                tags:
                  - Get
                  - Audit
                  - Records
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                summary: Get audit records
                description: >-
                  Returns all records in the audit log, optionally for a certain
                  date range.

                  This contains information about events like space exports,
                  group membership

                  changes, app installations, etc. For more information, see

                  [Audit
                  log](https://confluence.atlassian.com/confcloud/audit-log-802164269.html)

                  in the Confluence administrator's guide.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Confluence Administrator' global permission.
              post:
                tags:
                  - Create
                  - Audit
                  - Record
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                summary: Create audit record
                description: >-
                  Creates a record in the audit log.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Confluence Administrator' global permission.
            /wiki/rest/api/audit/export:
              get:
                tags:
                  - Export
                  - Audit
                  - Records
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                summary: Export audit records
                description: >-
                  Exports audit records as a CSV file or ZIP file.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Confluence Administrator' global permission.
            /wiki/rest/api/audit/retention:
              get:
                tags:
                  - Get
                  - Retention
                  - Period
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                summary: Get retention period
                description: >-
                  Returns the retention period for records in the audit log. The
                  retention

                  period is how long an audit record is kept for, from creation
                  date until

                  it is deleted.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Confluence Administrator' global permission.
              put:
                tags:
                  - Sets
                  - Retention
                  - Period
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                summary: Set retention period
                description: >-
                  Sets the retention period for records in the audit log. The
                  retention period

                  can be set to a maximum of 1 year.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Confluence Administrator' global permission.
            /wiki/rest/api/audit/since:
              get:
                tags:
                  - Get
                  - Audit
                  - Records
                  - For
                  - Time
                  - Period
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                summary: Get audit records for time period
                description: >-
                  Returns records from the audit log, for a time period back
                  from the current

                  date. For example, you can use this method to get the last 3
                  months of records.


                  This contains information about events like space exports,
                  group membership

                  changes, app installations, etc. For more information, see

                  [Audit
                  log](https://confluence.atlassian.com/confcloud/audit-log-802164269.html)

                  in the Confluence administrator's guide.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Confluence Administrator' global permission.
            /wiki/rest/api/content:
              get:
                tags:
                  - Get
                  - Content
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                summary: Get content
                description: >-
                  Deprecated, use [Confluence's v2
                  API](https://developer.atlassian.com/cloud/confluence/rest/v2/intro/).


                  Returns all content in a Confluence instance.


                  By default, the following objects are expanded: `space`,
                  `history`, `version`.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission).

                  Only content that the user has permission to view will be
                  returned.
              post:
                tags:
                  - Create
                  - Content
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                summary: Create content
                description: >-
                  Deprecated, use [Confluence's v2
                  API](https://developer.atlassian.com/cloud/confluence/rest/v2/intro/).


                  Creates a new piece of content or publishes an existing draft.


                  To publish a draft, add the `id` and `status` properties to
                  the body of the request.

                  Set the `id` to the ID of the draft and set the `status` to
                  'current'. When the

                  request is sent, a new piece of content will be created and
                  the metadata from the

                  draft will be transferred into it.


                  By default, the following objects are expanded: `space`,
                  `history`, `version`.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**: 'Add' permission for the

                  space that the content will be created in, and permission to
                  view the draft if publishing a draft.
            /wiki/rest/api/content/archive:
              post:
                tags:
                  - Archive
                  - Pages
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                summary: Archive pages
                description: >-
                  Archives a list of pages. The pages to be archived are
                  specified as a list of content IDs.

                  This API accepts the archival request and returns a task ID.

                  The archival process happens asynchronously.

                  Use the /longtask/<taskId> REST API to get the copy task
                  status.


                  Each content ID needs to resolve to page objects that are not
                  already in an archived state.

                  The content IDs need not belong to the same space.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Archive' permission for each of the pages in the
                  corresponding space it belongs to.
            /wiki/rest/api/content/blueprint/instance/{draftId}:
              put:
                tags:
                  - Publish
                  - Shared
                  - Draft
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                summary: Publish shared draft
                description: >-
                  Publishes a shared draft of a page created from a blueprint.


                  By default, the following objects are expanded:
                  `body.storage`, `history`, `space`, `version`, `ancestors`.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to view the draft and 'Add' permission for the
                  space that

                  the content will be created in.
              post:
                tags:
                  - Publish
                  - Legacy
                  - Draft
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                summary: Publish legacy draft
                description: >-
                  Publishes a legacy draft of a page created from a blueprint.
                  Legacy drafts

                  will eventually be removed in favor of shared drafts. For now,
                  this method

                  works the same as [Publish shared
                  draft](#api-content-blueprint-instance-draftId-put).


                  By default, the following objects are expanded:
                  `body.storage`, `history`, `space`, `version`, `ancestors`.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to view the draft and 'Add' permission for the
                  space that

                  the content will be created in.
            /wiki/rest/api/content/search:
              get:
                tags:
                  - Search
                  - Content
                  - By
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                summary: Search content by CQL
                description: >-
                  Returns the list of content that matches a Confluence Query
                  Language

                  (CQL) query. For information on CQL, see:

                  [Advanced searching using
                  CQL](https://developer.atlassian.com/cloud/confluence/advanced-searching-using-cql/).


                  Example initial call:

                  ```

                  /wiki/rest/api/content/search?cql=type=page&limit=25

                  ```


                  Example response:

                  ```

                  {
                    "results": [
                      { ... },
                      { ... },
                      ...
                      { ... }
                    ],
                    "limit": 25,
                    "size": 25,
                    ...
                    "_links": {
                      "base": "<url>",
                      "context": "<url>",
                      "next": "/rest/api/content/search?cql=type=page&limit=25&cursor=raNDoMsTRiNg",
                      "self": "<url>"
                    }
                  }

                  ```


                  When additional results are available, returns `next` and
                  `prev` URLs to retrieve them in subsequent calls. The URLs
                  each contain a cursor that points to the appropriate set of
                  results. Use `limit` to specify the number of results returned
                  in each call.

                  Example subsequent call (taken from example response):

                  ```

                  /wiki/rest/api/content/search?cql=type=page&limit=25&cursor=raNDoMsTRiNg

                  ```

                  The response to this will have a `prev` URL similar to the
                  `next` in the example response.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission).

                  Only content that the user has permission to view will be
                  returned.
            /wiki/rest/api/content/{id}:
              get:
                tags:
                  - Get
                  - Content
                  - By
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                summary: Get content by ID
                description: >-
                  Deprecated, use [Confluence's v2
                  API](https://developer.atlassian.com/cloud/confluence/rest/v2/intro/).


                  Returns a single piece of content, like a page or a blog post.


                  By default, the following objects are expanded: `space`,
                  `history`, `version`.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to view the content. If the content is a blog post,
                  'View' permission

                  for the space is required.
              put:
                tags:
                  - Update
                  - Content
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                summary: Update content
                description: >-
                  Deprecated, use [Confluence's v2
                  API](https://developer.atlassian.com/cloud/confluence/rest/v2/intro/).


                  Updates a piece of content. Use this method to update the
                  title or body

                  of a piece of content, change the status, change the parent
                  page, and more.


                  Note, updating draft content is currently not supported.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to update the content.
              delete:
                tags:
                  - Delete
                  - Content
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                summary: Delete content
                description: >-
                  Deprecated, use [Confluence's v2
                  API](https://developer.atlassian.com/cloud/confluence/rest/v2/intro/).


                  Moves a piece of content to the space's trash or purges it
                  from the trash,

                  depending on the content's type and status:


                  - If the content's type is `page`,`blogpost`, or `attachment`
                  and its status is `current`,

                  it will be trashed.

                  - If the content's type is `page`,`blogpost`, or `attachment`
                  and its status is `trashed`,

                  the content will be purged from the trash and deleted
                  permanently. Note,

                  you must also set the `status` query parameter to `trashed` in
                  your request.

                  - If the content's type is `comment`, it will be deleted

                  permanently without being trashed.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Delete' permission for the space that the content is in.
            /wiki/rest/api/content/{id}/pageTree:
              delete:
                tags:
                  - Delete
                  - Page
                  - Trees
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                summary: Delete page tree
                description: >-
                  Moves a pagetree rooted at a page to the space's trash:


                  - If the content's type is `page` and its status is `current`,
                  it will be trashed including

                  all its descendants.

                  - For every other combination of content type and status, this
                  API is not supported.


                  This API accepts the pageTree delete request and returns a
                  task ID.

                  The delete process happens asynchronously.

                   Response example:
                   <pre><code>
                   {
                        "id" : "1180606",
                        "links" : {
                             "status" : "/rest/api/longtask/1180606"
                        }
                   }
                   </code></pre>
                   Use the `/longtask/<taskId>` REST API to get the copy task status.

                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Delete' permission for the space that the content is in.
            /wiki/rest/api/content/{id}/child:
              get:
                tags:
                  - Get
                  - Content
                  - Children
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                summary: Get content children
                description: >-
                  Deprecated, use [Confluence's v2
                  API](https://developer.atlassian.com/cloud/confluence/rest/v2/intro/).


                  Returns a map of the direct children of a piece of content. A
                  piece of content

                  has different types of child content, depending on its type.
                  These are

                  the default parent-child content type relationships:


                  - `page`: child content is `page`, `comment`, `attachment`

                  - `blogpost`: child content is `comment`, `attachment`

                  - `attachment`: child content is `comment`

                  - `comment`: child content is `attachment`


                  Apps can override these default relationships. Apps can also
                  introduce

                  new content types that create new parent-child content
                  relationships.


                  Note, the map will always include all child content types that
                  are valid

                  for the content. However, if the content has no instances of a
                  child content

                  type, the map will contain an empty array for that child
                  content type.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**: 'View' permission for the space,

                  and permission to view the content if it is a page.
            /wiki/rest/api/content/{pageId}/move/{position}/{targetId}:
              put:
                tags:
                  - Move
                  - Page
                  - To
                  - New
                  - Locations
                  - Relative
                  - Target
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                summary: Move a page to a new location relative to a target page
                description: >-
                  Move a page to a new location relative to a target page:


                  * `before` - move the page under the same parent as the
                  target, before the target in the list of children

                  * `after` - move the page under the same parent as the target,
                  after the target in the list of children

                  * `append` - move the page to be a child of the target


                  Caution: This API can move pages to the top level of a space.
                  Top-level pages are difficult to find in the UI

                  because they do not show up in the page tree display. To avoid
                  this, never use `before` or `after` positions

                  when the `targetId` is a top-level page.
            /wiki/rest/api/content/{id}/child/attachment:
              get:
                tags:
                  - Get
                  - Attachments
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                summary: Get attachments
                description: >-
                  Deprecated, use [Confluence's v2
                  API](https://developer.atlassian.com/cloud/confluence/rest/v2/intro/).


                  Returns the attachments for a piece of content.


                  By default, the following objects are expanded: `metadata`.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to view the content. If the content is a blog post,
                  'View' permission

                  for the space is required.
              put:
                tags:
                  - Create
                  - Or
                  - Update
                  - Attachment
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                summary: Create or update attachment
                description: >-
                  Adds an attachment to a piece of content. If the attachment
                  already exists

                  for the content, then the attachment is updated (i.e. a new
                  version of the

                  attachment is created).


                  Note, you must set a `X-Atlassian-Token: nocheck` header on
                  the request

                  for this method, otherwise it will be blocked. This protects
                  against XSRF

                  attacks, which is necessary as this method accepts
                  multipart/form-data.


                  The media type 'multipart/form-data' is defined in [RFC
                  7578](https://www.ietf.org/rfc/rfc7578.txt).

                  Most client libraries have classes that make it easier to
                  implement

                  multipart posts, like the
                  [MultipartEntityBuilder](https://hc.apache.org/httpcomponents-client-5.1.x/current/httpclient5/apidocs/)

                  Java class provided by Apache HTTP Components.


                  Note, according to [RFC
                  7578](https://tools.ietf.org/html/rfc7578#section-4.5),

                  in the case where the form data is text,

                  the charset parameter for the "text/plain" Content-Type may be
                  used to

                  indicate the character encoding used in that part. In the case
                  of this

                  API endpoint, the `comment` body parameter should be sent with
                  `type=text/plain`

                  and `charset=utf-8` values. This will force the charset to be
                  UTF-8.


                  Example: This curl command attaches a file ('example.txt') to
                  a piece of

                  content (id='123') with a comment and `minorEdits`=true. If
                  the 'example.txt'

                  file already exists, it will update it with a new version of
                  the attachment.


                  ``` bash

                  curl -D- \
                    -u admin:admin \
                    -X PUT \
                    -H 'X-Atlassian-Token: nocheck' \
                    -F 'file=@"example.txt"' \
                    -F 'minorEdit="true"' \
                    -F 'comment="Example attachment comment"; type=text/plain; charset=utf-8' \
                    http://myhost/rest/api/content/123/child/attachment
                  ```

                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to update the content.
              post:
                tags:
                  - Create
                  - Attachment
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                summary: Create attachment
                description: >-
                  Adds an attachment to a piece of content. This method only
                  adds a new

                  attachment. If you want to update an existing attachment, use

                  [Create or update
                  attachments](#api-content-id-child-attachment-put).


                  Note, you must set a `X-Atlassian-Token: nocheck` header on
                  the request

                  for this method, otherwise it will be blocked. This protects
                  against XSRF

                  attacks, which is necessary as this method accepts
                  multipart/form-data.


                  The media type 'multipart/form-data' is defined in [RFC
                  7578](https://www.ietf.org/rfc/rfc7578.txt).

                  Most client libraries have classes that make it easier to
                  implement

                  multipart posts, like the
                  [MultipartEntityBuilder](https://hc.apache.org/httpcomponents-client-5.1.x/current/httpclient5/apidocs/)

                  Java class provided by Apache HTTP Components.


                  Note, according to [RFC
                  7578](https://tools.ietf.org/html/rfc7578#section-4.5),

                  in the case where the form data is text,

                  the charset parameter for the "text/plain" Content-Type may be
                  used to

                  indicate the character encoding used in that part. In the case
                  of this

                  API endpoint, the `comment` body parameter should be sent with
                  `type=text/plain`

                  and `charset=utf-8` values. This will force the charset to be
                  UTF-8.


                  Example: This curl command attaches a file ('example.txt') to
                  a container

                  (id='123') with a comment and `minorEdits`=true.


                  ``` bash

                  curl -D- \
                    -u admin:admin \
                    -X POST \
                    -H 'X-Atlassian-Token: nocheck' \
                    -F 'file=@"example.txt"' \
                    -F 'minorEdit="true"' \
                    -F 'comment="Example attachment comment"; type=text/plain; charset=utf-8' \
                    http://myhost/rest/api/content/123/child/attachment
                  ```

                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to update the content.
            /wiki/rest/api/content/{id}/child/attachment/{attachmentId}:
              put:
                tags:
                  - Update
                  - Attachment
                  - Properties
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                summary: Update attachment properties
                description: >-
                  Updates the attachment properties, i.e. the non-binary data of
                  an attachment

                  like the filename, media-type, comment, and parent container.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to update the content.
            /wiki/rest/api/content/{id}/child/attachment/{attachmentId}/data:
              post:
                tags:
                  - Update
                  - Attachment
                  - Data
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                summary: Update attachment data
                description: >-
                  Updates the binary data of an attachment, given the attachment
                  ID, and

                  optionally the comment and the minor edit field.


                  This method is essentially the same as [Create or update
                  attachments](#api-content-id-child-attachment-put),

                  except that it matches the attachment ID rather than the name.


                  Note, you must set a `X-Atlassian-Token: nocheck` header on
                  the request

                  for this method, otherwise it will be blocked. This protects
                  against XSRF

                  attacks, which is necessary as this method accepts
                  multipart/form-data.


                  The media type 'multipart/form-data' is defined in [RFC
                  7578](https://www.ietf.org/rfc/rfc7578.txt).

                  Most client libraries have classes that make it easier to
                  implement

                  multipart posts, like the
                  [MultipartEntityBuilder](https://hc.apache.org/httpcomponents-client-5.1.x/current/httpclient5/apidocs/)

                  Java class provided by Apache HTTP Components.


                  Note, according to [RFC
                  7578](https://tools.ietf.org/html/rfc7578#section-4.5),

                  in the case where the form data is text,

                  the charset parameter for the "text/plain" Content-Type may be
                  used to

                  indicate the character encoding used in that part. In the case
                  of this

                  API endpoint, the `comment` body parameter should be sent with
                  `type=text/plain`

                  and `charset=utf-8` values. This will force the charset to be
                  UTF-8.


                  Example: This curl command updates an attachment (id='att456')
                  that is attached

                  to a piece of content (id='123') with a comment and
                  `minorEdits`=true.


                  ``` bash

                  curl -D- \
                    -u admin:admin \
                    -X POST \
                    -H 'X-Atlassian-Token: nocheck' \
                    -F 'file=@"example.txt"' \
                    -F 'minorEdit="true"' \
                    -F 'comment="Example attachment comment"; type=text/plain; charset=utf-8' \
                    http://myhost/rest/api/content/123/child/attachment/att456/data
                  ```

                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to update the content.
            /wiki/rest/api/content/{id}/child/attachment/{attachmentId}/download:
              get:
                tags:
                  - Get
                  - To
                  - Download
                  - Attachment
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                summary: Get URI to download attachment
                description: >-
                  Redirects the client to a URL that serves an attachment's
                  binary data.
            /wiki/rest/api/content/{id}/child/comment:
              get:
                tags:
                  - Get
                  - Content
                  - Comments
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                summary: Get content comments
                description: >-
                  Deprecated, use [Confluence's v2
                  API](https://developer.atlassian.com/cloud/confluence/rest/v2/intro/).


                  Returns the comments on a piece of content.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**: 'View' permission for the space,

                  and permission to view the content if it is a page.
            /wiki/rest/api/content/{id}/child/{type}:
              get:
                tags:
                  - Get
                  - Content
                  - Children
                  - By
                  - Types
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                summary: Get content children by type
                description: >-
                  Deprecated, use [Confluence's v2
                  API](https://developer.atlassian.com/cloud/confluence/rest/v2/intro/).


                  Returns all children of a given type, for a piece of content.

                  A piece of content has different types of child content,
                  depending on its type:


                  - `page`: child content is `page`, `comment`, `attachment`

                  - `blogpost`: child content is `comment`, `attachment`

                  - `attachment`: child content is `comment`

                  - `comment`: child content is `attachment`


                  Custom content types that are provided by apps can also be
                  returned.


                  Note, this method only returns direct children. To return
                  children at all

                  levels, use [Get descendants by
                  type](#api-content-id-descendant-type-get).


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**: 'View' permission for the space,

                  and permission to view the content if it is a page.
            /wiki/rest/api/content/{id}/descendant:
              get:
                tags:
                  - Get
                  - Content
                  - Descendants
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                summary: Get content descendants
                description: >-
                  Returns a map of the descendants of a piece of content. This
                  is similar

                  to [Get content children](#api-content-id-child-get), except
                  that this

                  method returns child pages at all levels, rather than just the
                  direct

                  child pages.


                  A piece of content has different types of descendants,
                  depending on its type:


                  - `page`: descendant is `page`, `comment`, `attachment`

                  - `blogpost`: descendant is `comment`, `attachment`

                  - `attachment`: descendant is `comment`

                  - `comment`: descendant is `attachment`


                  The map will always include all descendant types that are
                  valid for the content.

                  However, if the content has no instances of a descendant type,
                  the map will

                  contain an empty array for that descendant type.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'View' permission for the space, and permission to view the
                  content if it

                  is a page.
            /wiki/rest/api/content/{id}/descendant/{type}:
              get:
                tags:
                  - Get
                  - Content
                  - Descendants
                  - By
                  - Types
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                summary: Get content descendants by type
                description: >-
                  Returns all descendants of a given type, for a piece of
                  content. This is

                  similar to [Get content children by
                  type](#api-content-id-child-type-get),

                  except that this method returns child pages at all levels,
                  rather than just

                  the direct child pages.


                  A piece of content has different types of descendants,
                  depending on its type:


                  - `page`: descendant is `page`, `comment`, `attachment`

                  - `blogpost`: descendant is `comment`, `attachment`

                  - `attachment`: descendant is `comment`

                  - `comment`: descendant is `attachment`


                  Custom content types that are provided by apps can also be
                  returned.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'View' permission for the space, and permission to view the
                  content if it

                  is a page.
            /wiki/rest/api/content/{id}/history:
              get:
                tags:
                  - Get
                  - Content
                  - History
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                summary: Get content history
                description: >-
                  Deprecated, use [Confluence's v2
                  API](https://developer.atlassian.com/cloud/confluence/rest/v2/intro/).


                  Returns the most recent update for a piece of content.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**: Permission to view the content.
            /wiki/rest/api/content/{id}/history/{version}/macro/id/{macroId}:
              get:
                tags:
                  - Get
                  - Macro
                  - Body
                  - By
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                summary: Get macro body by macro ID
                description: >-
                  Returns the body of a macro in storage format, for the given
                  macro ID.

                  This includes information like the name of the macro, the body
                  of the macro,

                  and any macro parameters. This method is mainly used by Cloud
                  apps.


                  About the macro ID: When a macro is created in a new version
                  of content,

                  Confluence will generate a random ID for it, unless an ID is
                  specified

                  (by an app). The macro ID will look similar to this:
                  '50884bd9-0cb8-41d5-98be-f80943c14f96'.

                  The ID is then persisted as new versions of content are
                  created, and is

                  only modified by Confluence if there are conflicting IDs.


                  Note, to preserve backwards compatibility this resource will
                  also match on

                  the hash of the macro body, even if a macro ID is found. This
                  check will

                  eventually become redundant, as macro IDs are generated for
                  pages and

                  transparently propagate out to all instances.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to view the content that the macro is in.
            /wiki/rest/api/content/{id}/history/{version}/macro/id/{macroId}/convert/{to}:
              get:
                tags:
                  - Get
                  - Macro
                  - Body
                  - By
                  - And
                  - Convert
                  - The
                  - Representation
                  - Synchronously
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                summary: >-
                  Get macro body by macro ID and convert the representation
                  synchronously
                description: >-
                  Returns the body of a macro in format specified in path, for
                  the given macro ID.

                  This includes information like the name of the macro, the body
                  of the macro,

                  and any macro parameters.


                  About the macro ID: When a macro is created in a new version
                  of content,

                  Confluence will generate a random ID for it, unless an ID is
                  specified

                  (by an app). The macro ID will look similar to this:
                  '50884bd9-0cb8-41d5-98be-f80943c14f96'.

                  The ID is then persisted as new versions of content are
                  created, and is

                  only modified by Confluence if there are conflicting IDs.


                  Note, to preserve backwards compatibility this resource will
                  also match on

                  the hash of the macro body, even if a macro ID is found. This
                  check will

                  eventually become redundant, as macro IDs are generated for
                  pages and

                  transparently propagate out to all instances.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to view the content that the macro is in.
            /wiki/rest/api/content/{id}/history/{version}/macro/id/{macroId}/convert/async/{to}:
              get:
                tags:
                  - Get
                  - Macro
                  - Body
                  - By
                  - And
                  - Convert
                  - Representation
                  - Asynchronously
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                summary: >-
                  Get macro body by macro ID and convert representation
                  Asynchronously
                description: >-
                  Returns Async Id of the conversion task which will convert the
                  macro into a content body of the desired format.

                  The result will be available for 5 minutes after completion of
                  the conversion.


                  About the macro ID: When a macro is created in a new version
                  of content,

                  Confluence will generate a random ID for it, unless an ID is
                  specified

                  (by an app). The macro ID will look similar to this:
                  '884bd9-0cb8-41d5-98be-f80943c14f96'.

                  The ID is then persisted as new versions of content are
                  created, and is

                  only modified by Confluence if there are conflicting IDs.


                  Note, to preserve backwards compatibility this resource will
                  also match on

                  the hash of the macro body, even if a macro ID is found. This
                  check will

                  eventually become redundant, as macro IDs are generated for
                  pages and

                  transparently propagate out to all instances.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to view the content that the macro is in.
            /wiki/rest/api/content/{id}/label:
              get:
                tags:
                  - Get
                  - Labels
                  - For
                  - Content
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                summary: Get labels for content
                description: >-
                  Deprecated, use [Confluence's v2
                  API](https://developer.atlassian.com/cloud/confluence/rest/v2/intro/).


                  Returns the labels on a piece of content.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'View' permission for the space and permission to view the
                  content if it is a page.
              post:
                tags:
                  - Add
                  - Labels
                  - To
                  - Content
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                summary: Add labels to content
                description: >-
                  Adds labels to a piece of content. Does not modify the
                  existing labels.


                  Notes:


                  - Labels can also be added when creating content ([Create
                  content](#api-content-post)).

                  - Labels can be updated when updating content ([Update
                  content](#api-content-id-put)).

                  This will delete the existing labels and replace them with the
                  labels in

                  the request.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to update the content.
              delete:
                tags:
                  - Removes
                  - Labels
                  - From
                  - Content
                  - Using
                  - Queries
                  - Parameters
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                summary: Remove label from content using query parameter
                description: >-
                  Removes a label from a piece of content. Labels can't be
                  deleted from archived content.

                  This is similar to [Remove label from
                  content](#api-content-id-label-label-delete)

                  except that the label name is specified via a query parameter.


                  Use this method if the label name has "/" characters, as

                  [Remove label from content using query
                  parameter](#api-content-id-label-delete)

                  does not accept "/" characters for the label name.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to update the content.
            /wiki/rest/api/content/{id}/label/{label}:
              delete:
                tags:
                  - Removes
                  - Labels
                  - From
                  - Content
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                summary: Remove label from content
                description: >-
                  Removes a label from a piece of content. Labels can't be
                  deleted from archived content.

                  This is similar to [Remove label from content using query
                  parameter](#api-content-id-label-delete)

                  except that the label name is specified via a path parameter.


                  Use this method if the label name does not have "/"
                  characters, as the path

                  parameter does not accept "/" characters for security reasons.
                  Otherwise,

                  use [Remove label from content using query
                  parameter](#api-content-id-label-delete).


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to update the content.
            /wiki/rest/api/content/{id}/notification/child-created:
              get:
                tags:
                  - Get
                  - Watches
                  - For
                  - Page
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                summary: Get watches for page
                description: >-
                  Returns the watches for a page. A user that watches a page
                  will receive

                  receive notifications when the page is updated.


                  If you want to manage watches for a page, use the following
                  `user` methods:


                  - [Get content watch status for
                  user](#api-user-watch-content-contentId-get)

                  - [Add content watch](#api-user-watch-content-contentId-post)

                  - [Remove content
                  watch](#api-user-watch-content-contentId-delete)


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission).
            /wiki/rest/api/content/{id}/notification/created:
              get:
                tags:
                  - Get
                  - Watches
                  - For
                  - Space
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                summary: Get watches for space
                description: >-
                  Returns all space watches for the space that the content is
                  in. A user that

                  watches a space will receive receive notifications when any
                  content in the

                  space is updated.


                  If you want to manage watches for a space, use the following
                  `user` methods:


                  - [Get space watch status for
                  user](#api-user-watch-space-spaceKey-get)

                  - [Add space watch](#api-user-watch-space-spaceKey-post)

                  - [Remove space watch](#api-user-watch-space-spaceKey-delete)


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission).
            /wiki/rest/api/content/{id}/pagehierarchy/copy:
              post:
                tags:
                  - Copy
                  - Page
                  - Hierarchy
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                summary: Copy page hierarchy
                description: >-
                  Copy page hierarchy allows the copying of an entire hierarchy
                  of pages and their associated properties, permissions and
                  attachments.
                   The id path parameter refers to the content id of the page to copy, and the new parent of this copied page is defined using the destinationPageId in the request body.
                   The titleOptions object defines the rules of renaming page titles during the copy;
                   for example, search and replace can be used in conjunction to rewrite the copied page titles.

                   Response example:
                   <pre><code>
                   {
                        "id" : "1180606",
                        "links" : {
                             "status" : "/rest/api/longtask/1180606"
                        }
                   }
                   </code></pre>
                   Use the /longtask/<taskId> REST API to get the copy task status.
            /wiki/rest/api/content/{id}/copy:
              post:
                tags:
                  - Copy
                  - Single
                  - Page
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                summary: Copy single page
                description: >-
                  Copies a single page and its associated properties,
                  permissions, attachments, and custom contents.
                   The `id` path parameter refers to the content ID of the page to copy. The target of the page to be copied
                   is defined using the `destination` in the request body and can be one of the following types.

                    - `space`: page will be copied to the specified space as a root page on the space
                    - `parent_page`: page will be copied as a child of the specified parent page
                    - `existing_page`: page will be copied and replace the specified page

                  By default, the following objects are expanded: `space`,
                  `history`, `version`.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**: 'Add' permission for the space that the content
                  will be copied in and permission to update the content if
                  copying to an `existing_page`.
            /wiki/rest/api/content/{id}/permission/check:
              post:
                tags:
                  - Checks
                  - Content
                  - Permissions
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                summary: Check content permissions
                description: >-
                  Check if a user or a group can perform an operation to the
                  specified content. The `operation` to check

                  must be provided. The user’s account ID or the ID of the group
                  can be provided in the `subject` to check

                  permissions against a specified user or group. The following
                  permission checks are done to make sure that the

                  user or group has the proper access:


                  - site permissions

                  - space permissions

                  - content restrictions


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission) if checking permission for self,

                  otherwise 'Confluence Administrator' global permission is
                  required.
            /wiki/rest/api/content/{id}/property:
              get:
                tags:
                  - Get
                  - Content
                  - Properties
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                summary: Get content properties
                description: >-
                  Returns the properties for a piece of content. For more
                  information

                  about content properties, see [Confluence entity
                  properties](https://developer.atlassian.com/cloud/confluence/confluence-entity-properties/).


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'View' permission for the space, and permission to view the
                  content if it is a page.
              post:
                tags:
                  - Create
                  - Content
                  - Properties
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                summary: Create content property
                description: >-
                  Creates a property for an existing piece of content. For more
                  information

                  about content properties, see [Confluence entity
                  properties](https://developer.atlassian.com/cloud/confluence/confluence-entity-properties/).


                  This is the same as [Create content property for
                  key](#api-content-id-property-key-post)

                  except that the key is specified in the request body instead
                  of as a

                  path parameter.


                  Content properties can also be added when creating a new piece
                  of content

                  by including them in the `metadata.properties` of the request.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to update the content.
            /wiki/rest/api/content/{id}/property/{key}:
              get:
                tags:
                  - Get
                  - Content
                  - Properties
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                summary: Get content property
                description: >-
                  Returns a content property for a piece of content. For more
                  information, see

                  [Confluence entity
                  properties](https://developer.atlassian.com/cloud/confluence/confluence-entity-properties/).


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'View' permission for the space, and permission to view the
                  content if it is a page.
              put:
                tags:
                  - Update
                  - Content
                  - Properties
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                summary: Update content property
                description: >-
                  Updates an existing content property. This method will also
                  create a new

                  property for a piece of content, if the property key does not
                  exist and

                  the property version is 1. For more information about content
                  properties, see

                  [Confluence entity
                  properties](https://developer.atlassian.com/cloud/confluence/confluence-entity-properties/).


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to update the content.
              post:
                tags:
                  - Create
                  - Content
                  - Properties
                  - For
                  - Keys
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                summary: Create content property for key
                description: >-
                  Creates a property for an existing piece of content. For more
                  information

                  about content properties, see [Confluence entity
                  properties](https://developer.atlassian.com/cloud/confluence/confluence-entity-properties/).


                  This is the same as [Create content
                  property](#api-content-id-property-post)

                  except that the key is specified as a path parameter instead
                  of in the

                  request body.


                  Content properties can also be added when creating a new piece
                  of content

                  by including them in the `metadata.properties` of the request.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to update the content.
              delete:
                tags:
                  - Delete
                  - Content
                  - Properties
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                summary: Delete content property
                description: >-
                  Deletes a content property. For more information about content
                  properties, see

                  [Confluence entity
                  properties](https://developer.atlassian.com/cloud/confluence/confluence-entity-properties/).


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to update the content.
            /wiki/rest/api/content/{id}/restriction:
              get:
                tags:
                  - Get
                  - Restrictions
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                summary: Get restrictions
                description: >-
                  Returns the restrictions on a piece of content.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to view the content.
              put:
                tags:
                  - Update
                  - Restrictions
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                summary: Update restrictions
                description: >-
                  Updates restrictions for a piece of content. For each
                  operation specified in the request, it removes

                  any existing restrictions on the content for that operation,
                  and replaces them with the restrictions in the request.

                  Note: Not specifying an operation will ignore restrictions of
                  that type, and passing an empty list for an operation

                  will remove all existing restrictions of that type.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to edit the content.
              post:
                tags:
                  - Add
                  - Restrictions
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                summary: Add restrictions
                description: >-
                  Adds restrictions to a piece of content. Note, this does not
                  change any

                  existing restrictions on the content.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to edit the content.
              delete:
                tags:
                  - Delete
                  - Restrictions
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                summary: Delete restrictions
                description: >-
                  Removes all restrictions (read and update) on a piece of
                  content.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to edit the content.
            /wiki/rest/api/content/{id}/restriction/byOperation:
              get:
                tags:
                  - Get
                  - Restrictions
                  - By
                  - Operation
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                summary: Get restrictions by operation
                description: >-
                  Returns restrictions on a piece of content by operation. This
                  method is

                  similar to [Get restrictions](#api-content-id-restriction-get)
                  except that

                  the operations are properties of the return object, rather
                  than items in

                  a results array.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to view the content.
            /wiki/rest/api/content/{id}/restriction/byOperation/{operationKey}:
              get:
                tags:
                  - Get
                  - Restrictions
                  - For
                  - Operation
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                summary: Get restrictions for operation
                description: >-
                  Returns the restictions on a piece of content for a given
                  operation (read

                  or update).


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to view the content.
            /wiki/rest/api/content/{id}/restriction/byOperation/{operationKey}/group/{groupName}:
              get:
                tags:
                  - Get
                  - Content
                  - Restrictions
                  - Status
                  - For
                  - Group
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                summary: Get content restriction status for group
                description: >-
                  Deprecated, use [Get content restriction status for group via
                  groupId](https://developer.atlassian.com/cloud/confluence/rest/v1/api-group-content-restrictions/#api-wiki-rest-api-content-id-restriction-byoperation-operationkey-bygroupid-groupid-get).

                  Returns whether the specified content restriction applies to a
                  group.

                  For example, if a page with `id=123` has a `read` restriction
                  for the `admins` group,

                  the following request will return `true`:


                  `/wiki/rest/api/content/123/restriction/byOperation/read/group/admins`


                  Note that a response of `true` does not guarantee that the
                  group can view the page, as it does not account for

                  account-inherited restrictions, space permissions, or even
                  product access. For more

                  information, see [Confluence
                  permissions](https://confluence.atlassian.com/x/_AozKw).


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to view the content.
              put:
                tags:
                  - Add
                  - Group
                  - To
                  - Content
                  - Restrictions
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                summary: Add group to content restriction
                description: >-
                  Deprecated, use [Add group to content restriction via
                  groupId](https://developer.atlassian.com/cloud/confluence/rest/v1/api-group-content-restrictions/#api-wiki-rest-api-content-id-restriction-byoperation-operationkey-bygroupid-groupid-put).

                  Adds a group to a content restriction. That is, grant read or
                  update

                  permission to the group for a piece of content.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to edit the content.
              delete:
                tags:
                  - Removes
                  - Group
                  - From
                  - Content
                  - Restrictions
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                summary: Remove group from content restriction
                description: >-
                  Deprecated, use [Remove group from content restriction by
                  groupId](https://developer.atlassian.com/cloud/confluence/rest/v1/api-group-content-restrictions/#api-wiki-rest-api-content-id-restriction-byoperation-operationkey-user-delete).

                  Removes a group from a content restriction. That is, remove
                  read or update

                  permission for the group for a piece of content.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to edit the content.
            /wiki/rest/api/content/{id}/restriction/byOperation/{operationKey}/byGroupId/{groupId}:
              get:
                tags:
                  - Get
                  - Content
                  - Restrictions
                  - Status
                  - For
                  - Group
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                summary: Get content restriction status for group
                description: >-
                  Returns whether the specified content restriction applies to a
                  group.

                  For example, if a page with `id=123` has a `read` restriction
                  for the `123456` group id,

                  the following request will return `true`:


                  `/wiki/rest/api/content/123/restriction/byOperation/read/byGroupId/123456`


                  Note that a response of `true` does not guarantee that the
                  group can view the page, as it does not account for

                  account-inherited restrictions, space permissions, or even
                  product access. For more

                  information, see [Confluence
                  permissions](https://confluence.atlassian.com/x/_AozKw).


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to view the content.
              put:
                tags:
                  - Add
                  - Group
                  - To
                  - Content
                  - Restrictions
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                summary: Add group to content restriction
                description: >-
                  Adds a group to a content restriction by Group Id. That is,
                  grant read or update

                  permission to the group for a piece of content.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to edit the content.
              delete:
                tags:
                  - Removes
                  - Group
                  - From
                  - Content
                  - Restrictions
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                summary: Remove group from content restriction
                description: >-
                  Removes a group from a content restriction. That is, remove
                  read or update

                  permission for the group for a piece of content.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to edit the content.
            /wiki/rest/api/content/{id}/restriction/byOperation/{operationKey}/user:
              get:
                tags:
                  - Get
                  - Content
                  - Restrictions
                  - Status
                  - For
                  - Users
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                summary: Get content restriction status for user
                description: >-
                  Returns whether the specified content restriction applies to a
                  user.

                  For example, if a page with `id=123` has a `read` restriction
                  for a user with an account ID of

                  `384093:32b4d9w0-f6a5-3535-11a3-9c8c88d10192`, the following
                  request will return `true`:


                  `/wiki/rest/api/content/123/restriction/byOperation/read/user?accountId=384093:32b4d9w0-f6a5-3535-11a3-9c8c88d10192`


                  Note that a response of `true` does not guarantee that the
                  user can view the page, as it does not account for

                  account-inherited restrictions, space permissions, or even
                  product access. For more

                  information, see [Confluence
                  permissions](https://confluence.atlassian.com/x/_AozKw).


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to view the content.
              put:
                tags:
                  - Add
                  - Users
                  - To
                  - Content
                  - Restrictions
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                summary: Add user to content restriction
                description: >-
                  Adds a user to a content restriction. That is, grant read or
                  update

                  permission to the user for a piece of content.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to edit the content.
              delete:
                tags:
                  - Removes
                  - Users
                  - From
                  - Content
                  - Restrictions
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                summary: Remove user from content restriction
                description: >-
                  Removes a group from a content restriction. That is, remove
                  read or update

                  permission for the group for a piece of content.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to edit the content.
            /wiki/rest/api/content/{id}/state:
              get:
                tags:
                  - Get
                  - Content
                  - States
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                summary: Get content state
                description: >-
                  Gets the current content state of the draft or current version
                  of content. To specify the draft version, set

                  the parameter status to draft, otherwise archived or current
                  will get the relevant published state.

                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to view the content.
              put:
                tags:
                  - Sets
                  - The
                  - Content
                  - States
                  - Of
                  - And
                  - Publishes
                  - New
                  - Versions
                  - Content
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                summary: >-
                  Set the content state of a content and publishes a new version
                  of the content.
                description: >-
                  Sets the content state of the content specified and creates a
                  new version

                  (publishes the content without changing the body) of the
                  content with the new state.


                  You may pass in either an id of a state, or the name and color
                  of a desired new state.

                  If all 3 are passed in, id will be used.

                  If the name and color passed in already exist under the
                  current user's existing custom states, the existing state will
                  be reused.

                  If custom states are disabled in the space of the content
                  (which can be determined by getting the content state space
                  settings of the content's space)

                  then this set will fail.


                  You may not remove a content state via this PUT request. You
                  must use the DELETE method. A specified state is required in
                  the body of this request.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to edit the content.
              delete:
                tags:
                  - Removes
                  - The
                  - Content
                  - States
                  - Of
                  - And
                  - Publishes
                  - New
                  - Versions
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                summary: >-
                  Removes the content state of a content and publishes a new
                  version.
                description: >-
                  Removes the content state of the content specified and creates
                  a new version

                  (publishes the content without changing the body) of the
                  content with the new status.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to edit the content.
            /wiki/rest/api/content/{id}/state/available:
              get:
                tags:
                  - Gets
                  - Available
                  - Content
                  - States
                  - For
                  - Content
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                summary: Gets available content states for content.
                description: >-
                  Gets content states that are available for the content to be
                  set as.

                  Will return all enabled Space Content States.

                  Will only return most the 3 most recently published custom
                  content states to match UI editor list.

                  To get all custom content states, use the /content-states
                  endpoint.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to edit the content.
            /wiki/rest/api/content/{id}/version:
              get:
                tags:
                  - Get
                  - Content
                  - Versions
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                summary: Get content versions
                description: >-
                  Deprecated, use [Confluence's v2
                  API](https://developer.atlassian.com/cloud/confluence/rest/v2/intro/).


                  Returns the versions for a piece of content in descending
                  order.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to view the content. If the content is a blog post,
                  'View' permission

                  for the space is required.
              post:
                tags:
                  - Restore
                  - Content
                  - Versions
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                summary: Restore content version
                description: >-
                  Restores a historical version to be the latest version. That
                  is, a new version

                  is created with the content of the historical version.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to update the content.
            /wiki/rest/api/content/{id}/version/{versionNumber}:
              get:
                tags:
                  - Get
                  - Content
                  - Versions
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                summary: Get content version
                description: >-
                  Deprecated, use [Confluence's v2
                  API](https://developer.atlassian.com/cloud/confluence/rest/v2/intro/).


                  Returns a version for a piece of content.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to view the content. If the content is a blog post,
                  'View' permission

                  for the space is required.
              delete:
                tags:
                  - Delete
                  - Content
                  - Versions
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                summary: Delete content version
                description: >-
                  Delete a historical version. This does not delete the changes
                  made to the

                  content in that version, rather the changes for the deleted
                  version are

                  rolled up into the next version. Note, you cannot delete the
                  current version.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to update the content.
            /wiki/rest/api/content-states:
              put:
                tags:
                  - Bulk
                  - Sets
                  - Content
                  - States
                  - Of
                  - Many
                  - Contents
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                summary: Bulk set content state of many contents
                description: >-
                  Creates a long running task that sets content state of draft
                  or published versions of pages specified.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**

                  Content Edit Permission for a content to have its state set
                  via this endpoint.
              get:
                tags:
                  - Get
                  - Custom
                  - Content
                  - States
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                summary: Get Custom Content States
                description: >-
                  Get custom content states that authenticated user has created.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**

                  Must have user authentication.
            /wiki/rest/api/content-states/delete:
              post:
                tags:
                  - Bulk
                  - Removes
                  - Content
                  - States
                  - From
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                summary: Bulk remove content states from content
                description: >-
                  Creates a long running task that Removes content state from
                  draft or published versions of pages specified.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**

                  Content Edit Permission for a content to have its state
                  removed via this endpoint.
            /wiki/rest/api/content-states/task/{taskId}:
              get:
                tags:
                  - Get
                  - Update
                  - 'On'
                  - Long
                  - Running
                  - Tasks
                  - For
                  - Settings
                  - Of
                  - Content
                  - States
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                summary: Get update on long running task for setting of content state.
                description: >-
                  Get Status of long running task that was previously created to
                  set or remove content states from content.

                  User must first create a task by passing in details to
                  /wiki/rest/api/content-states PUT or DELETE endpoints.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**

                  Must have created long running task
            /wiki/rest/api/contentbody/convert/{to}:
              post:
                tags:
                  - Convert
                  - Content
                  - Body
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                summary: Convert content body
                description: >-
                  Converts a content body from one format to another format.


                  Supported conversions:


                  - storage: view, export_view, styled_view, editor

                  - editor: storage

                  - view: none

                  - export_view: none

                  - styled_view: none


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  If request specifies 'contentIdContext', 'View' permission for
                  the space, and permission to view the content.
            /wiki/rest/api/contentbody/convert/async/{to}:
              post:
                tags:
                  - Asynchronously
                  - Convert
                  - Content
                  - Body
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                summary: Asynchronously convert content body
                description: >-
                  Converts a content body from one format to another format
                  asynchronously.

                  Returns the asyncId for the asynchronous task.


                  Supported conversions:


                  - storage: export_view


                  No other conversions are supported at the moment.

                  Once a conversion is completed, it will be available for 5
                  minutes at the result endpoint.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  If request specifies 'contentIdContext', 'View' permission for
                  the space, and permission to view the content.
            /wiki/rest/api/contentbody/convert/async/{id}:
              get:
                tags:
                  - Get
                  - Asynchronously
                  - Converted
                  - Content
                  - Body
                  - From
                  - The
                  - Identifiers
                  - Or
                  - Current
                  - Status
                  - Of
                  - Tasks
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                summary: >-
                  Get asynchronously converted content body from the id or the
                  current status of the task.
                description: >-
                  Returns the asynchronous content body for the corresponding id
                  if the task is complete 

                  or returns the status of the task.


                  After the task is completed, the result can be obtained for 5
                  minutes, or until an identical conversion request is made
                  again,

                  with allowCache query param set to false.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  If request specifies 'contentIdContext', 'View' permission for
                  the space, and permission to view the content.
            /wiki/rest/api/inlinetasks/search:
              get:
                tags:
                  - Get
                  - Inline
                  - Tasks
                  - Based
                  - 'On'
                  - Search
                  - Parameters
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                summary: Get inline tasks based on search parameters
                description: >-
                  Deprecated, use [Confluence's v2
                  API](https://developer.atlassian.com/cloud/confluence/rest/v2/intro/).


                  Returns inline tasks based on the search query.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission). Only tasks

                  in contents that the user has permission to view are returned.
            /wiki/rest/api/inlinetasks/{inlineTaskId}:
              get:
                tags:
                  - Get
                  - Inline
                  - Tasks
                  - Based
                  - 'On'
                  - Global
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                summary: Get inline task based on global ID
                description: >-
                  Deprecated, use [Confluence's v2
                  API](https://developer.atlassian.com/cloud/confluence/rest/v2/intro/).


                  Returns inline task based on the global ID.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to view the content associated with the task.
              put:
                tags:
                  - Update
                  - Inline
                  - Tasks
                  - Given
                  - Global
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                summary: Update inline task given global ID
                description: >-
                  Updates an inline tasks status given its global ID


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to update the content associated with the task.
            /wiki/rest/api/label:
              get:
                tags:
                  - Get
                  - Labels
                  - Information
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                summary: Get label information
                description: >-
                  Returns label information and a list of contents associated
                  with the label.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission). Only contents

                  that the user is permitted to view is returned.
            /wiki/rest/api/group:
              get:
                tags:
                  - Get
                  - Groups
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                summary: Get groups
                description: >-
                  Returns all user groups. The returned groups are ordered
                  alphabetically in

                  ascending order by group name.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission).
              post:
                tags:
                  - Create
                  - New
                  - Users
                  - Group
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                summary: Create new user group
                description: >-
                  Creates a new user group.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  User must be a site admin.
              delete:
                tags:
                  - Delete
                  - Users
                  - Group
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                summary: Delete user group
                description: >-
                  Delete user group.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  User must be a site admin.
            /wiki/rest/api/group/by-name:
              get:
                tags:
                  - Get
                  - Group
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                summary: Get group
                description: >-
                  Returns a user group for a given group name.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission).
            /wiki/rest/api/group/by-id:
              get:
                tags:
                  - Get
                  - Group
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                summary: Get group
                description: >-
                  Returns a user group for a given group id.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission).
              delete:
                tags:
                  - Delete
                  - Users
                  - Group
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                summary: Delete user group
                description: >-
                  Delete user group.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  User must be a site admin.
            /wiki/rest/api/group/{groupName}:
              get:
                tags:
                  - Get
                  - Group
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                summary: Get group
                description: >-
                  Returns a user group for a given group name.


                  Use updated Get group API


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission).
            /wiki/rest/api/group/member:
              get:
                tags:
                  - Get
                  - Group
                  - Members
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                summary: Get group members
                description: >-
                  Returns the users that are members of a group.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission).
            /wiki/rest/api/group/{groupName}/member:
              get:
                tags:
                  - Get
                  - Group
                  - Members
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                summary: Get group members
                description: >-
                  Returns the users that are members of a group.


                  Use updated Get group API


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission).
            /wiki/rest/api/group/picker:
              get:
                tags:
                  - Search
                  - Groups
                  - By
                  - Partial
                  - Queries
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                summary: Search groups by partial query
                description: Get search results of groups by partial query provided.
            /wiki/rest/api/group/userByGroupId:
              post:
                tags:
                  - Add
                  - Members
                  - To
                  - Group
                  - By
                  - Identifiers
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                summary: Add member to group by groupId
                description: >-
                  Adds a user as a member in a group represented by its groupId


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  User must be a site admin.
              delete:
                tags:
                  - Removes
                  - Members
                  - From
                  - Group
                  - Using
                  - Identifiers
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                summary: Remove member from group using group id
                description: >-
                  Remove user as a member from a group.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  User must be a site admin.
            /wiki/rest/api/group/{groupId}/membersByGroupId:
              get:
                tags:
                  - Get
                  - Group
                  - Members
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                summary: Get group members
                description: >-
                  Returns the users that are members of a group.


                  Use updated Get group API


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission).
            /wiki/rest/api/group/user:
              post:
                tags:
                  - Add
                  - Members
                  - To
                  - Group
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                summary: Add member to group
                description: >-
                  Adds a user as a member in a group.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  User must be a site admin.
              delete:
                tags:
                  - Removes
                  - Members
                  - From
                  - Group
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                summary: Remove member from group
                description: >-
                  Remove user as a member from a group.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  User must be a site admin.
            /wiki/rest/api/longtask:
              get:
                tags:
                  - Get
                  - Long-running
                  - Tasks
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                summary: Get long-running tasks
                description: >-
                  Returns information about all active long-running tasks (e.g.
                  space export),

                  such as how long each task has been running and the percentage
                  of each task

                  that has completed.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission).
            /wiki/rest/api/longtask/{id}:
              get:
                tags:
                  - Get
                  - Long-running
                  - Tasks
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                summary: Get long-running task
                description: >-
                  Returns information about an active long-running task (e.g.
                  space export),

                  such as how long it has been running and the percentage of the
                  task that

                  has completed.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission).
            /wiki/rest/api/relation/{relationName}/from/{sourceType}/{sourceKey}/to/{targetType}:
              get:
                tags:
                  - Find
                  - Target
                  - Entities
                  - Related
                  - To
                  - Source
                  - Entities
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                summary: Find target entities related to a source entity
                description: >-
                  Returns all target entities that have a particular
                  relationship to the

                  source entity. Note, relationships are one way.


                  For example, the following method finds all content that the
                  current user

                  has an 'ignore' relationship with:

                  `GET
                  /wiki/rest/api/relation/ignore/from/user/current/to/content`

                  Note, 'ignore' is an example custom relationship type.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to view both the target entity and source entity.
            /wiki/rest/api/relation/{relationName}/from/{sourceType}/{sourceKey}/to/{targetType}/{targetKey}:
              get:
                tags:
                  - Find
                  - Relationships
                  - From
                  - Source
                  - To
                  - Target
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                summary: Find relationship from source to target
                description: >-
                  Find whether a particular type of relationship exists from a
                  source

                  entity to a target entity. Note, relationships are one way.


                  For example, you can use this method to find whether the
                  current user has

                  selected a particular page as a favorite (i.e. 'save for
                  later'):

                  `GET
                  /wiki/rest/api/relation/favourite/from/user/current/to/content/123`


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to view both the target entity and source entity.
              put:
                tags:
                  - Create
                  - Relationships
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                summary: Create relationship
                description: >-
                  Creates a relationship between two entities (user, space,
                  content). The

                  'favourite' relationship is supported by default, but you can
                  use this method

                  to create any type of relationship between two entities.


                  For example, the following method creates a 'sibling'
                  relationship between

                  two pieces of content:

                  `GET
                  /wiki/rest/api/relation/sibling/from/content/123/to/content/456`


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission).
              delete:
                tags:
                  - Delete
                  - Relationships
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                summary: Delete relationship
                description: >-
                  Deletes a relationship between two entities (user, space,
                  content).


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission).

                  For favourite relationships, the current user can only delete
                  their own

                  favourite relationships. A space administrator can delete
                  favourite

                  relationships for any user.
            /wiki/rest/api/relation/{relationName}/to/{targetType}/{targetKey}/from/{sourceType}:
              get:
                tags:
                  - Find
                  - Source
                  - Entities
                  - Related
                  - To
                  - Target
                  - Entities
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                summary: Find source entities related to a target entity
                description: >-
                  Returns all target entities that have a particular
                  relationship to the

                  source entity. Note, relationships are one way.


                  For example, the following method finds all users that have a
                  'collaborator'

                  relationship to a piece of content with an ID of '1234':

                  `GET
                  /wiki/rest/api/relation/collaborator/to/content/1234/from/user`

                  Note, 'collaborator' is an example custom relationship type.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to view both the target entity and source entity.
            /wiki/rest/api/search:
              get:
                tags:
                  - Search
                  - Content
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                summary: Search content
                description: >-
                  Searches for content using the

                  [Confluence Query Language
                  (CQL)](https://developer.atlassian.com/cloud/confluence/advanced-searching-using-cql/).


                  **Note that CQL input queries submitted through the
                  `/wiki/rest/api/search` endpoint no longer support
                  user-specific fields like `user`, `user.fullname`,
                  `user.accountid`, and `user.userkey`.** 

                  See this [deprecation
                  notice](https://developer.atlassian.com/cloud/confluence/deprecation-notice-search-api/)
                  for more details.


                  Example initial call:

                  ```

                  /wiki/rest/api/search?cql=type=page&limit=25

                  ```


                  Example response:

                  ```

                  {
                    "results": [
                      { ... },
                      { ... },
                      ...
                      { ... }
                    ],
                    "limit": 25,
                    "size": 25,
                    ...
                    "_links": {
                      "base": "<url>",
                      "context": "<url>",
                      "next": "/rest/api/search?cql=type=page&limit=25&cursor=raNDoMsTRiNg",
                      "self": "<url>"
                    }
                  }

                  ```


                  When additional results are available, returns `next` and
                  `prev` URLs to retrieve them in subsequent calls. The URLs
                  each contain a cursor that points to the appropriate set of
                  results. Use `limit` to specify the number of results returned
                  in each call.


                  Example subsequent call (taken from example response):

                  ```

                  /wiki/rest/api/search?cql=type=page&limit=25&cursor=raNDoMsTRiNg

                  ```

                  The response to this will have a `prev` URL similar to the
                  `next` in the example response.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to view the entities. Note, only entities that the
                  user has

                  permission to view will be returned.
            /wiki/rest/api/search/user:
              get:
                tags:
                  - Search
                  - Users
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                summary: Search users
                description: >-
                  Searches for users using user-specific queries from the

                  [Confluence Query Language
                  (CQL)](https://developer.atlassian.com/cloud/confluence/advanced-searching-using-cql/).


                  Note that CQL input queries submitted through the
                  `/wiki/rest/api/search/user` endpoint only support
                  user-specific fields like `user`, `user.fullname`,
                  `user.accountid`, and `user.userkey`.


                  Note that some user fields may be set to null depending on the
                  user's privacy settings.

                  These are: email, profilePicture, displayName, and timeZone.
            /wiki/rest/api/settings/lookandfeel:
              get:
                tags:
                  - Get
                  - Look
                  - And
                  - Feel
                  - Settings
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                summary: Get look and feel settings
                description: >-
                  Returns the look and feel settings for the site or a single
                  space. This

                  includes attributes such as the color scheme, padding, and
                  border radius.


                  The look and feel settings for a space can be inherited from
                  the global

                  look and feel settings or provided by a theme.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  None
              put:
                tags:
                  - Select
                  - Look
                  - And
                  - Feel
                  - Settings
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                summary: Select look and feel settings
                description: >-
                  Sets the look and feel settings to the default (global)
                  settings, the

                  custom settings, or the current theme's settings for a space.

                  The custom and theme settings can only be selected if there is
                  already

                  a theme set for a space. Note, the default space settings are
                  inherited

                  from the current global settings.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Admin' permission for the space.
            /wiki/rest/api/settings/lookandfeel/custom:
              post:
                tags:
                  - Update
                  - Look
                  - And
                  - Feel
                  - Settings
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                summary: Update look and feel settings
                description: >-
                  Updates the look and feel settings for the site or for a
                  single space.

                  If custom settings exist, they are updated. If no custom
                  settings exist,

                  then a set of custom settings is created.


                  Note, if a theme is selected for a space, the space look and
                  feel settings

                  are provided by the theme and cannot be overridden.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Admin' permission for the space.
              delete:
                tags:
                  - Reset
                  - Look
                  - And
                  - Feel
                  - Settings
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                summary: Reset look and feel settings
                description: >-
                  Resets the custom look and feel settings for the site or a
                  single space.

                  This changes the values of the custom settings to be the same
                  as the

                  default settings. It does not change which settings (default
                  or custom)

                  are selected. Note, the default space settings are inherited
                  from the

                  current global settings.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Admin' permission for the space.
            /wiki/rest/api/settings/lookandfeel/selected:
              put:
                tags:
                  - Sets
                  - Look
                  - And
                  - Feel
                  - Settings
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                summary: Set look and feel settings
                description: >-
                  Sets the look and feel settings to either the default settings
                  or the

                  custom settings, for the site or a single space. Note, the
                  default

                  space settings are inherited from the current global settings.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Admin' permission for the space.
            /wiki/rest/api/settings/systemInfo:
              get:
                tags:
                  - Get
                  - Systems
                  - Info
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                summary: Get system info
                description: >-
                  Returns the system information for the Confluence Cloud
                  tenant. This

                  information is used by Atlassian.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission).
            /wiki/rest/api/settings/theme:
              get:
                tags:
                  - Get
                  - Themes
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                summary: Get themes
                description: >-
                  Returns all themes, not including the default theme.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**: None
            /wiki/rest/api/settings/theme/selected:
              get:
                tags:
                  - Get
                  - Global
                  - Theme
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                summary: Get global theme
                description: >-
                  Returns the globally assigned theme.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**: None
            /wiki/rest/api/settings/theme/{themeKey}:
              get:
                tags:
                  - Get
                  - Theme
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                summary: Get theme
                description: >-
                  Returns a theme. This includes information about the theme
                  name,

                  description, and icon.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**: None
            /wiki/rest/api/space:
              get:
                tags:
                  - Get
                  - Spaces
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                summary: Get spaces
                description: >-
                  Deprecated, use [Confluence's v2
                  API](https://developer.atlassian.com/cloud/confluence/rest/v2/intro/).


                  Returns all spaces. The returned spaces are ordered
                  alphabetically in

                  ascending order by space key.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission).

                  Note, the returned list will only contain spaces that the
                  current user

                  has permission to view.
              post:
                tags:
                  - Create
                  - Space
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                summary: Create space
                description: >-
                  Creates a new space. Note, currently you cannot set space
                  labels when

                  creating a space.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Create Space(s)' global permission.
            /wiki/rest/api/space/_private:
              post:
                tags:
                  - Create
                  - Private
                  - Space
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                summary: Create private space
                description: >-
                  Creates a new space that is only visible to the creator. This
                  method is

                  the same as the [Create space](#api-space-post) method with
                  permissions

                  set to the current user only. Note, currently you cannot set
                  space

                  labels when creating a space.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Create Space(s)' global permission.
            /wiki/rest/api/space/{spaceKey}:
              get:
                tags:
                  - Get
                  - Space
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                summary: Get space
                description: >-
                  Deprecated, use [Confluence's v2
                  API](https://developer.atlassian.com/cloud/confluence/rest/v2/intro/).


                  Returns a space. This includes information like the name,
                  description,

                  and permissions, but not the content in the space.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'View' permission for the space.
              put:
                tags:
                  - Update
                  - Space
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                summary: Update space
                description: >-
                  Updates the name, description, or homepage of a space.


                  -   For security reasons, permissions cannot be updated via
                  the API and

                  must be changed via the user interface instead.

                  -   Currently you cannot set space labels when updating a
                  space.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Admin' permission for the space.
              delete:
                tags:
                  - Delete
                  - Space
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                summary: Delete space
                description: >-
                  Deletes a space. Note, the space will be deleted in a long
                  running task.

                  Therefore, the space may not be deleted yet when this method
                  has

                  returned. Clients should poll the status link that is returned
                  in the

                  response until the task completes.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Admin' permission for the space.
            /wiki/rest/api/space/{spaceKey}/content:
              get:
                tags:
                  - Get
                  - Content
                  - For
                  - Space
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                summary: Get content for space
                description: >-
                  Deprecated, use [Confluence's v2
                  API](https://developer.atlassian.com/cloud/confluence/rest/v2/intro/).


                  Returns all content in a space. The returned content is
                  grouped by type

                  (pages then blogposts), then ordered by content ID in
                  ascending order.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'View' permission for the space. Note, the returned list will
                  only

                  contain content that the current user has permission to view.
            /wiki/rest/api/space/{spaceKey}/permission:
              post:
                tags:
                  - Add
                  - New
                  - Permission
                  - To
                  - Space
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                summary: Add new permission to space
                description: >-
                  Adds new permission to space.


                  If the permission to be added is a group permission, the group
                  can be identified

                  by its group name or group id.


                  Note: Apps cannot access this REST resource - including when
                  utilizing user impersonation.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Admin' permission for the space.
            /wiki/rest/api/space/{spaceKey}/permission/custom-content:
              post:
                tags:
                  - Add
                  - New
                  - Custom
                  - Content
                  - Permission
                  - To
                  - Space
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                summary: Add new custom content permission to space
                description: >-
                  Adds new custom content permission to space.


                  If the permission to be added is a group permission, the group
                  can be identified

                  by its group name or group id.


                  Note: Only apps can access this REST resource and only make
                  changes to the respective app permissions.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Admin' permission for the space.
            /wiki/rest/api/space/{spaceKey}/permission/{id}:
              delete:
                tags:
                  - Removes
                  - Space
                  - Permission
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                summary: Remove a space permission
                description: >-
                  Removes a space permission. Note that removing Read Space
                  permission for a user or group will remove all

                  the space permissions for that user or group.


                  Note: Apps cannot access this REST resource - including when
                  utilizing user impersonation.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Admin' permission for the space.
            /wiki/rest/api/space/{spaceKey}/content/{type}:
              get:
                tags:
                  - Get
                  - Content
                  - By
                  - Types
                  - For
                  - Space
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                summary: Get content by type for space
                description: >-
                  Deprecated, use [Confluence's v2
                  API](https://developer.atlassian.com/cloud/confluence/rest/v2/intro/).


                  Returns all content of a given type, in a space. The returned
                  content is

                  ordered by content ID in ascending order.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'View' permission for the space. Note, the returned list will
                  only

                  contain content that the current user has permission to view.
            /wiki/rest/api/space/{spaceKey}/property:
              get:
                tags:
                  - Get
                  - Space
                  - Properties
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                summary: Get space properties
                description: >-
                  Deprecated, use [Confluence's v2
                  API](https://developer.atlassian.com/cloud/confluence/rest/v2/intro/).


                  Returns all properties for the given space. Space properties
                  are a key-value storage associated with a space.


                  **[Permissions
                  required](https://confluence.atlassian.com/x/_AozKw)**: ‘View’
                  permission for the space.
              post:
                tags:
                  - Create
                  - Space
                  - Properties
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                summary: Create space property
                description: >-
                  Deprecated, use [Confluence's v2
                  API](https://developer.atlassian.com/cloud/confluence/rest/v2/intro/).


                  Creates a new space property.


                  **[Permissions
                  required](https://confluence.atlassian.com/x/_AozKw)**:

                  ‘Admin’ permission for the space.
            /wiki/rest/api/space/{spaceKey}/property/{key}:
              get:
                tags:
                  - Get
                  - Space
                  - Properties
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                summary: Get space property
                description: >-
                  Deprecated, use [Confluence's v2
                  API](https://developer.atlassian.com/cloud/confluence/rest/v2/intro/).


                  Returns a space property.


                  **[Permissions
                  required](https://confluence.atlassian.com/x/_AozKw)**: ‘View’
                  permission for the space.
              put:
                tags:
                  - Update
                  - Space
                  - Properties
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                summary: Update space property
                description: >-
                  Deprecated, use [Confluence's v2
                  API](https://developer.atlassian.com/cloud/confluence/rest/v2/intro/).


                  Updates a space property. Note, you cannot update the key of a
                  space

                  property, only the value.


                  **[Permissions
                  required](https://confluence.atlassian.com/x/_AozKw)**:

                  ‘Admin’ permission for the space.
              post:
                tags:
                  - Create
                  - Space
                  - Properties
                  - For
                  - Keys
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                summary: Create space property for key
                description: >-
                  Deprecated, use [Confluence's v2
                  API](https://developer.atlassian.com/cloud/confluence/rest/v2/intro/).


                  Creates a new space property. This is the same as `POST

                  /wiki/rest/api/space/{spaceKey}/property` but the key for the
                  property is passed as a

                  path parameter, rather than in the request body.


                  **[Permissions
                  required](https://confluence.atlassian.com/x/_AozKw)**:

                  ‘Admin’ permission for the space.
              delete:
                tags:
                  - Delete
                  - Space
                  - Properties
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                summary: Delete space property
                description: >-
                  Deprecated, use [Confluence's v2
                  API](https://developer.atlassian.com/cloud/confluence/rest/v2/intro/).


                  Deletes a space property.


                  **[Permissions
                  required](https://confluence.atlassian.com/x/_AozKw)**:

                  ‘Admin’ permission for the space.
            /wiki/rest/api/space/{spaceKey}/settings:
              get:
                tags:
                  - Get
                  - Space
                  - Settings
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                summary: Get space settings
                description: >-
                  Returns the settings of a space. Currently only the

                  `routeOverrideEnabled` setting can be returned.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'View' permission for the space.
              put:
                tags:
                  - Update
                  - Space
                  - Settings
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                summary: Update space settings
                description: >-
                  Updates the settings for a space. Currently only the

                  `routeOverrideEnabled` setting can be updated.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Admin' permission for the space.
            /wiki/rest/api/space/{spaceKey}/state:
              get:
                tags:
                  - Get
                  - Space
                  - Suggested
                  - Content
                  - States
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                summary: Get space suggested content states
                description: >-
                  Get content states that are suggested in the space.

                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Space view permission
            /wiki/rest/api/space/{spaceKey}/state/settings:
              get:
                tags:
                  - Get
                  - Content
                  - States
                  - Settings
                  - For
                  - Space
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                summary: Get content state settings for space
                description: >-
                  Get object describing whether content states are allowed at
                  all, if custom content states or space content states

                  are restricted, and a list of space content states allowed for
                  the space if they are not restricted.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Space admin permission
            /wiki/rest/api/space/{spaceKey}/state/content:
              get:
                tags:
                  - Get
                  - Content
                  - In
                  - Space
                  - With
                  - Given
                  - States
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                summary: Get content in space with given content state
                description: >-
                  Finds paginated content with 


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Space View Permission
            /wiki/rest/api/space/{spaceKey}/theme:
              get:
                tags:
                  - Get
                  - Space
                  - Theme
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                summary: Get space theme
                description: >-
                  Returns the theme selected for a space, if one is set. If no
                  space

                  theme is set, this means that the space is inheriting the
                  global look

                  and feel settings.


                  **[Permissions
                  required](https://confluence.atlassian.com/x/_AozKw)**: ‘View’
                  permission for the space.
              put:
                tags:
                  - Sets
                  - Space
                  - Theme
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                summary: Set space theme
                description: >-
                  Sets the theme for a space. Note, if you want to reset the
                  space theme to

                  the default Confluence theme, use the 'Reset space theme'
                  method instead

                  of this method.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Admin' permission for the space.
              delete:
                tags:
                  - Reset
                  - Space
                  - Theme
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                summary: Reset space theme
                description: >-
                  Resets the space theme. This means that the space will inherit
                  the

                  global look and feel settings


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Admin' permission for the space.
            /wiki/rest/api/space/{spaceKey}/watch:
              get:
                tags:
                  - Get
                  - Space
                  - Watchers
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                summary: Get space watchers
                description: Returns a list of watchers of a space
            /wiki/rest/api/space/{spaceKey}/label:
              get:
                tags:
                  - Get
                  - Space
                  - Labels
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                summary: Get Space Labels
                description: >-
                  Returns a list of labels associated with a space. Can provide
                  a prefix as well as other filters to

                  select different types of labels.
              post:
                tags:
                  - Add
                  - Labels
                  - To
                  - Space
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                summary: Add labels to a space
                description: >-
                  Adds labels to a piece of content. Does not modify the
                  existing labels.


                  Notes:


                  - Labels can also be added when creating content ([Create
                  content](#api-content-post)).

                  - Labels can be updated when updating content ([Update
                  content](#api-content-id-put)).

                  This will delete the existing labels and replace them with the
                  labels in

                  the request.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to update the content.
              delete:
                tags:
                  - Removes
                  - Labels
                  - From
                  - Space
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                summary: Remove label from a space
                description: ''
            /wiki/rest/api/template:
              put:
                tags:
                  - Update
                  - Content
                  - Templates
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                summary: Update content template
                description: >-
                  Updates a content template. Note, blueprint templates cannot
                  be updated

                  via the REST API.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Admin' permission for the space to update a space template or
                  'Confluence Administrator'

                  global permission to update a global template.
              post:
                tags:
                  - Create
                  - Content
                  - Templates
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                summary: Create content template
                description: >-
                  Creates a new content template. Note, blueprint templates
                  cannot be created via the REST API.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Admin' permission for the space to create a space template or
                  'Confluence Administrator'

                  global permission to create a global template.
            /wiki/rest/api/template/blueprint:
              get:
                tags:
                  - Get
                  - Blueprints
                  - Templates
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                  - Blueprints
                summary: Get blueprint templates
                description: >-
                  Returns all templates provided by blueprints. Use this method
                  to retrieve

                  all global blueprint templates or all blueprint templates in a
                  space.


                  Note, all global blueprints are inherited by each space. Space
                  blueprints

                  can be customised without affecting the global blueprints.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'View' permission for the space to view blueprints for the
                  space and permission

                  to access the Confluence site ('Can use' global permission) to
                  view global blueprints.
            /wiki/rest/api/template/page:
              get:
                tags:
                  - Get
                  - Content
                  - Templates
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                  - Blueprints
                  - Page
                summary: Get content templates
                description: >-
                  Returns all content templates. Use this method to retrieve all
                  global

                  content templates or all content templates in a space.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'View' permission for the space to view space templates and
                  permission to

                  access the Confluence site ('Can use' global permission) to
                  view global templates.
            /wiki/rest/api/template/{contentTemplateId}:
              get:
                tags:
                  - Get
                  - Content
                  - Templates
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                  - Blueprints
                  - Page
                summary: Get content template
                description: >-
                  Returns a content template. This includes information about
                  template,

                  like the name, the space or blueprint that the template is in,
                  the body

                  of the template, and more.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'View' permission for the space to view space templates and
                  permission to

                  access the Confluence site ('Can use' global permission) to
                  view global templates.
              delete:
                tags:
                  - Removes
                  - Templates
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                  - Blueprints
                  - Page
                summary: Remove template
                description: >-
                  Deletes a template. This results in different actions
                  depending on the

                  type of template:


                  - If the template is a content template, it is deleted.

                  - If the template is a modified space-level blueprint
                  template, it reverts

                  to the template inherited from the global-level blueprint
                  template.

                  - If the template is a modified global-level blueprint
                  template, it reverts

                  to the default global-level blueprint template.

                   Note, unmodified blueprint templates cannot be deleted.

                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:
                          'Admin' permission for the space to delete a space template or 'Confluence Administrator'
                          global permission to delete a global template.
            /wiki/rest/api/user:
              get:
                tags:
                  - Get
                  - Users
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                  - Blueprints
                  - Page
                summary: Get user
                description: >-
                  Returns a user. This includes information about the user, such
                  as the

                  display name, account ID, profile picture, and more. The
                  information returned may be

                  restricted by the user's profile visibility settings.


                  **Note:** to add, edit, or delete users in your organization,
                  see the

                  [user management REST
                  API](/cloud/admin/user-management/about/).


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission).
            /wiki/rest/api/user/anonymous:
              get:
                tags:
                  - Get
                  - Anonymous
                  - Users
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                  - Blueprints
                  - Page
                  - Anonymous
                summary: Get anonymous user
                description: >-
                  Returns information about how anonymous users are represented,
                  like the

                  profile picture and display name.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission).
            /wiki/rest/api/user/current:
              get:
                tags:
                  - Get
                  - Current
                  - Users
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                  - Blueprints
                  - Page
                  - Anonymous
                  - Current
                summary: Get current user
                description: >-
                  Returns the currently logged-in user. This includes
                  information about

                  the user, like the display name, userKey, account ID, profile
                  picture,

                  and more.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission).
            /wiki/rest/api/user/memberof:
              get:
                tags:
                  - Get
                  - Group
                  - Memberships
                  - For
                  - Users
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                  - Blueprints
                  - Page
                  - Anonymous
                  - Current
                  - Members
                summary: Get group memberships for user
                description: >-
                  Returns the groups that a user is a member of.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission).
            /wiki/rest/api/user/bulk:
              get:
                tags:
                  - Get
                  - Multiple
                  - Users
                  - Using
                  - Ids
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                  - Blueprints
                  - Page
                  - Anonymous
                  - Current
                  - Members
                  - Bulk
                summary: Get multiple users using ids
                description: >-
                  Returns user details for the ids provided in request.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission).
            /wiki/rest/api/user/watch/content/{contentId}:
              get:
                tags:
                  - Get
                  - Content
                  - Watch
                  - Status
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                  - Blueprints
                  - Page
                  - Anonymous
                  - Current
                  - Members
                  - Bulk
                summary: Get content watch status
                description: >-
                  Returns whether a user is watching a piece of content. Choose
                  the user by

                  doing one of the following:


                  - Specify a user via a query parameter: Use the `accountId` to
                  identify the user.

                  - Do not specify a user: The currently logged-in user will be
                  used.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Confluence Administrator' global permission if specifying a
                  user, otherwise

                  permission to access the Confluence site ('Can use' global
                  permission).
              post:
                tags:
                  - Add
                  - Content
                  - Watchers
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                  - Blueprints
                  - Page
                  - Anonymous
                  - Current
                  - Members
                  - Bulk
                summary: Add content watcher
                description: >-
                  Adds a user as a watcher to a piece of content. Choose the
                  user by doing

                  one of the following:


                  - Specify a user via a query parameter: Use the `accountId` to
                  identify the user.

                  - Do not specify a user: The currently logged-in user will be
                  used.


                  Note, you must add the `X-Atlassian-Token: no-check` header
                  when making a

                  request, as this operation has XSRF protection.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Confluence Administrator' global permission if specifying a
                  user, otherwise

                  permission to access the Confluence site ('Can use' global
                  permission).
              delete:
                tags:
                  - Removes
                  - Content
                  - Watchers
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                  - Blueprints
                  - Page
                  - Anonymous
                  - Current
                  - Members
                  - Bulk
                summary: Remove content watcher
                description: >-
                  Removes a user as a watcher from a piece of content. Choose
                  the user by

                  doing one of the following:


                  - Specify a user via a query parameter: Use the `accountId` to
                  identify the user.

                  - Do not specify a user: The currently logged-in user will be
                  used.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Confluence Administrator' global permission if specifying a
                  user, otherwise

                  permission to access the Confluence site ('Can use' global
                  permission).
            /wiki/rest/api/user/watch/label/{labelName}:
              get:
                tags:
                  - Get
                  - Labels
                  - Watch
                  - Status
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                  - Blueprints
                  - Page
                  - Anonymous
                  - Current
                  - Members
                  - Bulk
                summary: Get label watch status
                description: >-
                  Returns whether a user is watching a label. Choose the user by
                  doing one

                  of the following:


                  - Specify a user via a query parameter: Use the `accountId` to
                  identify the user.

                  - Do not specify a user: The currently logged-in user will be
                  used.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Confluence Administrator' global permission if specifying a
                  user, otherwise

                  permission to access the Confluence site ('Can use' global
                  permission).
              post:
                tags:
                  - Add
                  - Labels
                  - Watchers
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                  - Blueprints
                  - Page
                  - Anonymous
                  - Current
                  - Members
                  - Bulk
                summary: Add label watcher
                description: >-
                  Adds a user as a watcher to a label. Choose the user by doing
                  one of the

                  following:


                  - Specify a user via a query parameter: Use the `accountId` to
                  identify the user.

                  - Do not specify a user: The currently logged-in user will be
                  used.


                  Note, you must add the `X-Atlassian-Token: no-check` header
                  when making a

                  request, as this operation has XSRF protection.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Confluence Administrator' global permission if specifying a
                  user, otherwise

                  permission to access the Confluence site ('Can use' global
                  permission).
              delete:
                tags:
                  - Removes
                  - Labels
                  - Watchers
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                  - Blueprints
                  - Page
                  - Anonymous
                  - Current
                  - Members
                  - Bulk
                summary: Remove label watcher
                description: >-
                  Removes a user as a watcher from a label. Choose the user by
                  doing one of

                  the following:


                  - Specify a user via a query parameter: Use the `accountId` to
                  identify the user.

                  - Do not specify a user: The currently logged-in user will be
                  used.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Confluence Administrator' global permission if specifying a
                  user, otherwise

                  permission to access the Confluence site ('Can use' global
                  permission).
            /wiki/rest/api/user/watch/space/{spaceKey}:
              get:
                tags:
                  - Get
                  - Space
                  - Watch
                  - Status
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                  - Blueprints
                  - Page
                  - Anonymous
                  - Current
                  - Members
                  - Bulk
                summary: Get space watch status
                description: >-
                  Returns whether a user is watching a space. Choose the user by

                  doing one of the following:


                  - Specify a user via a query parameter: Use the `accountId` to
                  identify the user.

                  - Do not specify a user: The currently logged-in user will be
                  used.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Confluence Administrator' global permission if specifying a
                  user, otherwise

                  permission to access the Confluence site ('Can use' global
                  permission).
              post:
                tags:
                  - Add
                  - Space
                  - Watchers
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                  - Blueprints
                  - Page
                  - Anonymous
                  - Current
                  - Members
                  - Bulk
                summary: Add space watcher
                description: >-
                  Adds a user as a watcher to a space. Choose the user by doing
                  one of the

                  following:


                  - Specify a user via a query parameter: Use the `accountId` to
                  identify the user.

                  - Do not specify a user: The currently logged-in user will be
                  used.


                  Note, you must add the `X-Atlassian-Token: no-check` header
                  when making a

                  request, as this operation has XSRF protection.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Confluence Administrator' global permission if specifying a
                  user, otherwise

                  permission to access the Confluence site ('Can use' global
                  permission).
              delete:
                tags:
                  - Removes
                  - Space
                  - Watch
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                  - Blueprints
                  - Page
                  - Anonymous
                  - Current
                  - Members
                  - Bulk
                summary: Remove space watch
                description: >-
                  Removes a user as a watcher from a space. Choose the user by
                  doing one of

                  the following:


                  - Specify a user via a query parameter: Use the `accountId` to
                  identify the user.

                  - Do not specify a user: The currently logged-in user will be
                  used.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  'Confluence Administrator' global permission if specifying a
                  user, otherwise

                  permission to access the Confluence site ('Can use' global
                  permission).
            /wiki/rest/api/user/email:
              get:
                tags:
                  - Get
                  - Users
                  - Email
                  - Addresses
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                  - Blueprints
                  - Page
                  - Anonymous
                  - Current
                  - Members
                  - Bulk
                  - Email
                summary: Get user email address
                description: >-
                  Returns a user's email address. This API is only available to
                  apps approved by

                  Atlassian, according to these
                  [guidelines](https://community.developer.atlassian.com/t/guidelines-for-requesting-access-to-email-address/27603).


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission).
            /wiki/rest/api/user/email/bulk:
              get:
                tags:
                  - Get
                  - Users
                  - Email
                  - Addresses
                  - In
                  - Batches
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                  - Blueprints
                  - Page
                  - Anonymous
                  - Current
                  - Members
                  - Bulk
                  - Email
                summary: Get user email addresses in batch
                description: >-
                  Returns user email addresses for a set of accountIds. This API
                  is only available to apps approved by

                  Atlassian, according to these
                  [guidelines](https://community.developer.atlassian.com/t/guidelines-for-requesting-access-to-email-address/27603).


                  Any accounts which are not available will not be included in
                  the result.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission).
            /atlassian-connect/1/app/module/dynamic:
              get:
                tags:
                  - Get
                  - Modules
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                  - Blueprints
                  - Page
                  - Anonymous
                  - Current
                  - Members
                  - Bulk
                  - Email
                  - Atlassian
                  - Connect
                  - Applications
                  - Modules
                  - Dynamic
                summary: Get modules
                description: >-
                  Returns all modules registered dynamically by the calling app.


                  **[Permissions](#permissions) required:** Only Connect apps
                  can make this request.
              post:
                tags:
                  - Register
                  - Modules
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                  - Blueprints
                  - Page
                  - Anonymous
                  - Current
                  - Members
                  - Bulk
                  - Email
                  - Atlassian
                  - Connect
                  - Applications
                  - Modules
                  - Dynamic
                summary: Register modules
                description: >-
                  Registers a list of modules. For the list of modules that
                  support dynamic registration, see [Dynamic
                  modules](https://developer.atlassian.com/cloud/confluence/dynamic-modules/).


                  **[Permissions](#permissions) required:** Only Connect apps
                  can make this request.
              delete:
                tags:
                  - Removes
                  - Modules
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                  - Blueprints
                  - Page
                  - Anonymous
                  - Current
                  - Members
                  - Bulk
                  - Email
                  - Atlassian
                  - Connect
                  - Applications
                  - Modules
                  - Dynamic
                summary: Remove modules
                description: >-
                  Remove all or a list of modules registered by the calling app.


                  **[Permissions](#permissions) required:** Only Connect apps
                  can make this request.
            /wiki/rest/api/analytics/content/{contentId}/views:
              get:
                tags:
                  - Get
                  - Views
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                  - Blueprints
                  - Page
                  - Anonymous
                  - Current
                  - Members
                  - Bulk
                  - Email
                  - Atlassian
                  - Connect
                  - Applications
                  - Modules
                  - Dynamic
                  - Views
                summary: Get views
                description: Get the total number of views a piece of content has.
            /wiki/rest/api/analytics/content/{contentId}/viewers:
              get:
                tags:
                  - Get
                  - Viewers
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                  - Blueprints
                  - Page
                  - Anonymous
                  - Current
                  - Members
                  - Bulk
                  - Email
                  - Atlassian
                  - Connect
                  - Applications
                  - Modules
                  - Dynamic
                  - Views
                  - Viewers
                summary: Get viewers
                description: >-
                  Get the total number of distinct viewers a piece of content
                  has.
            /wiki/rest/api/user/{userId}/property:
              get:
                tags:
                  - Get
                  - Users
                  - Properties
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                  - Blueprints
                  - Page
                  - Anonymous
                  - Current
                  - Members
                  - Bulk
                  - Email
                  - Atlassian
                  - Connect
                  - Applications
                  - Modules
                  - Dynamic
                  - Views
                  - Viewers
                summary: Get user properties
                description: >-
                  Returns the properties for a user as list of property keys.
                  For more information

                  about user properties, see [Confluence entity
                  properties](https://developer.atlassian.com/cloud/confluence/confluence-entity-properties/).

                  `Note`, these properties stored against a user are on a
                  Confluence site level and not space/content level.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission).
            /wiki/rest/api/user/{userId}/property/{key}:
              get:
                tags:
                  - Get
                  - Users
                  - Properties
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                  - Blueprints
                  - Page
                  - Anonymous
                  - Current
                  - Members
                  - Bulk
                  - Email
                  - Atlassian
                  - Connect
                  - Applications
                  - Modules
                  - Dynamic
                  - Views
                  - Viewers
                summary: Get user property
                description: >-
                  Returns the property corresponding to `key` for a user. For
                  more information

                  about user properties, see [Confluence entity
                  properties](https://developer.atlassian.com/cloud/confluence/confluence-entity-properties/).

                  `Note`, these properties stored against a user are on a
                  Confluence site level and not space/content level.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission).
              put:
                tags:
                  - Update
                  - Users
                  - Properties
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                  - Blueprints
                  - Page
                  - Anonymous
                  - Current
                  - Members
                  - Bulk
                  - Email
                  - Atlassian
                  - Connect
                  - Applications
                  - Modules
                  - Dynamic
                  - Views
                  - Viewers
                summary: Update user property
                description: >-
                  Updates a property for the given user. Note, you cannot update
                  the key of a user property, only the value.

                  For more information about user properties, see

                  [Confluence entity
                  properties](https://developer.atlassian.com/cloud/confluence/confluence-entity-properties/).

                  `Note`, these properties stored against a user are on a
                  Confluence site level and not space/content level.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission).
              post:
                tags:
                  - Create
                  - Users
                  - Properties
                  - By
                  - Keys
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                  - Blueprints
                  - Page
                  - Anonymous
                  - Current
                  - Members
                  - Bulk
                  - Email
                  - Atlassian
                  - Connect
                  - Applications
                  - Modules
                  - Dynamic
                  - Views
                  - Viewers
                summary: Create user property by key
                description: >-
                  Creates a property for a user. For more information  about
                  user properties, see [Confluence entity properties]

                  (https://developer.atlassian.com/cloud/confluence/confluence-entity-properties/).

                  `Note`, these properties stored against a user are on a
                  Confluence site level and not space/content level.


                  `Note:` the number of properties which could be created per
                  app in a tenant for each user might be

                  restricted by fixed system limits.

                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission).
              delete:
                tags:
                  - Delete
                  - Users
                  - Properties
                  - Wiki
                  - Rest
                  - APIs
                  - Audit
                  - Export
                  - Retention
                  - Since
                  - Content
                  - Archive
                  - Identifiers
                  - Search
                  - Trees
                  - Child
                  - Move
                  - Positions
                  - Target
                  - Attachment
                  - Data
                  - Download
                  - Comments
                  - Types
                  - Descendants
                  - History
                  - Convert
                  - To
                  - Async
                  - Labels
                  - Notifications
                  - Created
                  - Page Hierarchy
                  - Copy
                  - Permission
                  - Checks
                  - Properties
                  - Keys
                  - Restrictions
                  - Operation
                  - Group
                  - Names
                  - By
                  - Users
                  - States
                  - Available
                  - Versions
                  - Numbers
                  - States
                  - Delete
                  - Content Body
                  - Inline Tasks
                  - Tasks
                  - Members
                  - Picker
                  - Members
                  - Longtask
                  - From
                  - Source
                  - Settings
                  - Lookandfeel
                  - Custom
                  - Selected
                  - Info
                  - Theme
                  - Space
                  - _private
                  - Watch
                  - Templates
                  - Blueprints
                  - Page
                  - Anonymous
                  - Current
                  - Members
                  - Bulk
                  - Email
                  - Atlassian
                  - Connect
                  - Applications
                  - Modules
                  - Dynamic
                  - Views
                  - Viewers
                summary: Delete user property
                description: >-
                  Deletes a property for the given user.

                  For more information about user properties, see

                  [Confluence entity
                  properties](https://developer.atlassian.com/cloud/confluence/confluence-entity-properties/).

                  `Note`, these properties stored against a user are on a
                  Confluence site level and not space/content level.


                  **[Permissions](https://confluence.atlassian.com/x/_AozKw)
                  required**:

                  Permission to access the Confluence site ('Can use' global
                  permission).
          x-atlassian-narrative:
            documents:
              - title: About
                anchor: about
                body: >-
                  This is the reference for the Confluence Cloud REST API. This
                  API is the primary way to get and

                  modify data in Confluence Cloud, whether you are developing an
                  app or any other integration.

                  Use it to interact with Confluence entities, like pages and
                  blog posts, spaces, users, groups,

                  and more.
              - title: Authentication and authorization
                anchor: auth
                body: >-
                  **Authentication:** If you are building a Cloud app,
                  authentication is implemented via JWT or OAuth 2.0, depending
                  on what you are building (see [Security
                  overview](https://developer.atlassian.com/cloud/confluence/security-overview/)).
                  Otherwise, if you are authenticating directly against the REST
                  API, the REST API supports basic auth (see [Basic auth for
                  REST
                  APIs](https://developer.atlassian.com/cloud/confluence/basic-auth-for-rest-apis/)).


                  **Authorization:** If you are building a Cloud app,
                  authorization can be implemented by
                  [scopes](https://developer.atlassian.com/cloud/confluence/scopes/)
                  or by [OAuth 2.0 user
                  impersonation](https://developer.atlassian.com/cloud/confluence/oauth-2-jwt-bearer-tokens-for-apps).
                  Otherwise, if you are making calls directly against the REST
                  API, authorization is based on the user used in the
                  authentication process.


                  See [Security
                  overview](https://developer.atlassian.com/cloud/confluence/security-overview/)
                  for more details on authentication and authorization.
              - title: Status codes
                anchor: status-code
                body: >-
                  The Confluence REST API uses the [standard HTTP status
                  codes](https://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html).


                  Responses that return an error status code will also return a
                  response body, similar to the following:

                  ```json

                  {
                    "statusCode": 404,
                    "data": {
                      "authorized": false,
                      "valid": false,
                      "errors": [
                        {
                          "message": {
                            "translation": "This is an example error message.",
                            "args": []
                          }
                        }
                      ],
                      "successful": false
                    },
                    "message": "This is an example error message."
                  }

                  ```
              - title: Using the REST API
                anchor: using
                body: >-
                  **Expansion:** The Confluence REST API uses resource
                  expansion: some parts of a resource are not returned unless
                  explicitly specified. This simplifies responses and minimizes
                  network traffic.


                  To expand part of a resource in a request, use the `expand`
                  query parameter and specify the entities to be expanded. If
                  you need to expand nested entities, use the `.` dot notation.
                  For example, the following request will expand information
                  about the requested content's space and labels:

                  ```

                  GET /wiki/rest/api/content/{id}?expand=space,metadata.labels

                  ```

                  **Pagination:** The Confluence REST API uses pagination: a
                  method that returns a response with multiple objects can only
                  return a limited number at one time. This limits the size of
                  responses and conserves server resources.


                  Use the 'limit' and 'start' query parameters to specify
                  pagination:


                  - `limit` is the number of objects to return per page. This
                  may be restricted by system limits.

                  - `start` is the index of the first item returned in the page
                  of results. The base index is 0.


                  For example, the following request will return ten content
                  objects, starting from the fifth object.

                  ```

                  GET /wiki/rest/api/content?start=4&limit=10

                  ```

                  **Special headers:**


                  - `X-Atlassian-Token: no-check` request header must be
                  specified for methods

                  that are protected from Cross Site Request Forgery (XSRF/CSRF)
                  attacks. This is

                  stated in the method description, if required. For more
                  information, see this

                  [KB
                  article](https://confluence.atlassian.com/cloudkb/xsrf-check-failed-when-calling-cloud-apis-826874382.html).
              - title: Capabilities
                anchor: capabilities
                body: >-
                  **Webhooks:** A webhook is a user-defined callback over HTTP.
                  You can use Confluence webhooks to notify your app or web
                  application when certain events occur in Confluence. For
                  example, when a page is created or updated. To learn more, see
                  [Webhooks](https://developer.atlassian.com/cloud/confluence/modules/webhook/).


                  **Content properties:** Content properties are a key-value
                  storage associated with a piece of Confluence content. If you
                  are building an app, this is one form of persistence that you
                  can use. You can use the Confluence REST API to get, update,
                  and delete content properties. To learn more, see [Content
                  properties in the REST
                  API](https://developer.atlassian.com/cloud/confluence/content-properties/).


                  **CQL:** The Confluence Query Language (CQL) allows you to
                  perform complex searches for content using an SQL-like syntax
                  in the `search` resource. To learn more, see [Advanced
                  searching using
                  CQL](https://developer.atlassian.com/cloud/confluence/advanced-
      - type: Postman Collection
        url: >-
          https://developer.atlassian.com/cloud/confluence/confcloud.1.postman.json
      - type: Authentication
        url: https://developer.atlassian.com/cloud/confluence/rest/v1/intro/#auth
      - type: Status Codes
        url: >-
          https://developer.atlassian.com/cloud/confluence/rest/v1/intro/#status-code
      - type: Capabilities
        url: >-
          https://developer.atlassian.com/cloud/confluence/rest/v1/intro/#capabilities
    overlays:
      - type: APIs.io Search
        url: >-
          overlays/https://dac-static.atlassian.com/cloud/confluence/swagger.v3.json?_v=1.6660.0-0.1294.0-openapi-search.yml
      - type: APIs.io Search
        url: overlays/confluence-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/confluence-openapi-api-evangelist-ratings.yml
    aid: atlassian:confluence-api
  - aid: box:box-workflows-api
    name: Box Workflows API
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
            title: Box Workflows API
          paths:
            /workflows:
              get:
                summary: List workflows
                tags:
                  - List
                  - Workflows
                  - Workflows
                description: >-
                  Returns list of workflows that act on a given `folder ID`, and

                  have a flow with a trigger type of `WORKFLOW_MANUAL_START`.


                  You application must be authorized to use the `Manage Box
                  Relay` application

                  scope within the developer console in to use this endpoint.
            /workflows/{workflow_id}/start:
              post:
                summary: Starts workflow based on request body
                tags:
                  - Starts
                  - Workflow
                  - Based
                  - 'On'
                  - Request
                  - Body
                  - Workflows
                  - Workflow_id
                  - Start
                description: >-
                  Initiates a flow with a trigger type of
                  `WORKFLOW_MANUAL_START`.


                  You application must be authorized to use the `Manage Box
                  Relay` application

                  scope within the develo
    overlays:
      - type: APIs.io Search
        url: overlays/workflows-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/workflows-openapi-api-evangelist-ratings.yml
  - name: FactSet ESG API
    description: FactSet ESG API giving access to SASB & SDG Score data
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.factset.com/api-catalog/factset-esg-api
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: https://developer.factset.com/api-catalog/factset-esg-api#overview
      - type: SDKs
        url: https://developer.factset.com/api-catalog/factset-esg-api#sdkLibrary
      - type: Jupyter Notebooks
        url: https://developer.factset.com/api-catalog/factset-esg-api#notebooks
      - type: Code Snippets
        url: https://developer.factset.com/api-catalog/factset-esg-api#codeSnippet
      - type: Change Log
        url: https://developer.factset.com/api-catalog/factset-esg-api#changelog
      - type: OpenAPI
        data:
          openapi: 3.0.0
          info:
            title: FactSet ESG API
            license:
              name: Apache License, Version 2.0
              url: https://www.apache.org/licenses/LICENSE-2.0
          externalDocs:
            description: API Documentation
            url: https://developer.factset.com/api-catalog/factset-esg-api
          tags:
            - name: SASB
              description: >-
                Get scores and ranks based on the 26 SASB categories for a
                requested list of symbols and date range.
            - name: SDG
              description: >-
                Get scores and ranks based on the 16 SDG goals for a requested
                list of symbols and date range.
            - name: SFDR
              description: >-
                Get the Principle Adverse Impact PAI data supporting the SFDR
                reporting.
            - name: Spotlights
              description: >-
                Get Spotlight data for the most important positive and negative
                ESG events
            - name: Articles
              description: >-
                Get Articles data for the most important positive and negative
                ESG events
          paths:
            /factset-esg/v1/sasb-scores:
              get:
                tags:
                  - Gets
                  - Short-term,
                  - Long-term,
                  - And
                  - Momentum
                  - Scores
                  - Based
                  - 'On'
                  - The
                  - '26'
                  - Categories
                  - Defined
                  - By
                  - Sustainability
                  - Accounting
                  - Standards
                  - Board
                  - B).
                  - Factset
                  - Esg
                  - V1
                  - Sasb
                  - Scores
                summary: >-
                  Gets short-term, long-term, and momentum scores based on the
                  26 ESG categories defined by the Sustainability Accounting
                  Standards Board (SASB).
                description: >
                  FactSet Truvalue Labs SASB Scores provides short-term,
                  long-term, and momentum scores that are generated for 26 ESG
                  categories defined by the Sustainability Accounting Standards
                  Board. FactSet Truvalue also calculates a custom overall score
                  called ALLCATEGORIES, can indicate data volume flow, and the
                  Dynamic Materiality of that data flow.
              post:
                tags:
                  - For
                  - Large
                  - List
                  - Of
                  - Ids,
                  - Gets
                  - Short-term,
                  - Long-term,
                  - And
                  - Momentum
                  - Scores
                  - Based
                  - 'On'
                  - The
                  - '26'
                  - Categories
                  - Defined
                  - By
                  - Sustainability
                  - Accounting
                  - Standards
                  - Board
                  - B).
                  - Factset
                  - Esg
                  - V1
                  - Sasb
                  - Scores
                summary: >-
                  For a large list of ids, gets short-term, long-term, and
                  momentum scores based on the 26 ESG categories defined by the
                  Sustainability Accounting Standards Board (SASB).
                description: >
                  FactSet Truvalue Labs SASB Scores provides short-term,
                  long-term, and momentum scores that are generated for 26 ESG
                  categories defined by the Sustainability Accounting Standards
                  Board. FactSet Truvalue also calculates a custom overall score
                  called ALLCATEGORIES, can indicate data volume flow, and the
                  Dynamic Materiality of that data flow.
            /factset-esg/v1/sasb-ranks:
              get:
                tags:
                  - Gets
                  - Rankings
                  - For
                  - Requested
                  - List
                  - Of
                  - Ids
                  - And
                  - Dates.
                  - Factset
                  - Esg
                  - V1
                  - Sasb
                  - Scores
                  - Ranks
                summary: Gets ESG Rankings for a requested list of ids and dates.
                description: >
                  Indicates if a company is a Leader, Above Average, Average,
                  Below Average, or a Laggard; directly mapping from Industry
                  Percentiles (*request IND_PCTL in scores endpoints*). Mapping
                  of ESG Ranks to Industry Percentile Ranges is as follows - 


                  |Rank|Industry Percentile Range (%)|

                  |||

                  |Leader|90 - 100|

                  |Above Average|70 - 89.9|

                  |Average|30 - 69.9|

                  |Below Average|10 - 29.9|

                  |Laggard|0 - 9.9|


                  Industry classifications follow SICS, SASB's Industry
                  Classification System. Using the Adjusted Insight scores,
                  Industry Percentiles are generated for all companies.
                  Companies with five or more articles in a year get ranked in a
                  first pass, then companies with filled-in values are
                  interpolated without forcing the ranking of higher-volume
                  companies up or down.  In the case where a company falls into
                  an industry with fewer than 7 high or medium volume companies
                  the Sector Percentile is inserted in the place of the Industry
                  Percentile score.

                  <p>Only Vaild for ALLCATEGORIES and MATERIALITY
                  categories.</p>
              post:
                tags:
                  - Get
                  - Ranks
                  - For
                  - Large
                  - List
                  - Of
                  - Ids
                  - And
                  - Specified
                  - Date
                  - Range.
                  - Factset
                  - Esg
                  - V1
                  - Sasb
                  - Scores
                  - Ranks
                summary: >-
                  Get ESG Ranks for a large list of ids and specified date
                  range.
                description: >
                  Indicates if a company is a Leader, Above Average, Average,
                  Below Average, or a Laggard; directly mapping from Industry
                  Percentiles (*request IND_PCTL in scores endpoints*). Mapping
                  of ESG Ranks to Industry Percentile Ranges is as follows - 


                  |Rank|Industry Percentile Range (%)|

                  |||

                  |Leader|90 - 100|

                  |Above Average|70 - 89.9|

                  |Average|30 - 69.9|

                  |Below Average|10 - 29.9|

                  |Laggard|0 - 9.9|


                  Industry classifications follow SICS, SASB's Industry
                  Classification System. Using the Adjusted Insight scores,
                  Industry Percentiles are generated for all companies.
                  Companies with five or more articles in a year get ranked in a
                  first pass, then companies with filled-in values are
                  interpolated without forcing the ranking of higher-volume
                  companies up or down.  In the case where a company falls into
                  an industry with fewer than 7 high or medium volume companies
                  the Sector Percentile is inserted in the place of the Industry
                  Percentile score.

                  <p>Only Vaild for ALLCATEGORIES and MATERIALITY
                  categories.</p>
            /factset-esg/v1/sasb-scores-all:
              get:
                tags:
                  - Gets
                  - Flat
                  - Key
                  - Value
                  - Array
                  - Of
                  - Scores
                  - For
                  - Named
                  - Categories
                  - The
                  - Input
                  - Score
                  - Type(s).
                  - Factset
                  - Esg
                  - V1
                  - Sasb
                  - Scores
                  - Ranks
                  - All
                summary: >-
                  Gets a flat key value array of scores for named categories of
                  the input scoreType(s).
                description: >
                  **Retrieves a flat array of all categories for the requested
                  scoreType and ids. Unlike the /sasb-scores endpoint the format
                  of the response returns category names as part of the key
                  value.**<p> Gets values for all categories for the selected
                  score type(s) for the requested identifier(s). FactSet
                  Truvalue Labs SASB Scores provides short-term, long-term, and
                  momentum scores that are generated for 26 ESG categories
                  defined by the Sustainability Accounting Standards Board. ESG
                  Ranks are not supported in this Endpoint.
              post:
                tags:
                  - Gets
                  - Flat
                  - Key
                  - Value
                  - Array
                  - Of
                  - Scores
                  - For
                  - Named
                  - Categories
                  - The
                  - Input
                  - Score
                  - Type(s).
                  - Factset
                  - Esg
                  - V1
                  - Sasb
                  - Scores
                  - Ranks
                  - All
                summary: >-
                  Gets a flat key value array of scores for named categories of
                  the input score type(s).
                description: >
                  **Retrieves a flat array of all categories for the requested
                  scoreType and ids. Unlike the /sasb-scores endpoint the format
                  of the response returns category names as part of the key
                  value.**<p> Gets values for all categories for the selected
                  score type(s) for the requested identifier(s). FactSet
                  Truvalue Labs SASB Scores provides short-term, long-term, and
                  momentum scores that are generated for 26 ESG categories
                  defined by the Sustainability Accounting Standards Board. ESG
                  Ranks are not supported in this Endpoint.
            /factset-esg/v1/sdg-scores:
              get:
                tags:
                  - Gets
                  - Short-term,
                  - Long-term,
                  - And
                  - Momentum
                  - Scores
                  - Based
                  - 'On'
                  - The
                  - '16'
                  - Sustainable
                  - Development
                  - Goals
                  - Categories
                  - Defined
                  - By
                  - United
                  - Nations.
                  - Factset
                  - Esg
                  - V1
                  - Sasb
                  - Scores
                  - Ranks
                  - All
                  - Sdg
                summary: >-
                  Gets short-term, long-term, and momentum scores based on the
                  16 Sustainable Development Goals categories defined by the
                  United Nations.
                description: >
                  Truvalue Labs SDG Scores provides short-term, long-term, and
                  momentum scores that are generated for 16 Sustainable
                  Development Goals categories defined by the United Nations.
              post:
                tags:
                  - Gets
                  - Short-term,
                  - Long-term,
                  - And
                  - Momentum
                  - Scores
                  - Based
                  - 'On'
                  - The
                  - '16'
                  - Sustainable
                  - Development
                  - Goals
                  - Categories
                  - Defined
                  - By
                  - United
                  - Nations.
                  - Factset
                  - Esg
                  - V1
                  - Sasb
                  - Scores
                  - Ranks
                  - All
                  - Sdg
                summary: >-
                  Gets short-term, long-term, and momentum scores based on the
                  16 Sustainable Development Goals categories defined by United
                  Nations.
                description: >
                  Truvalue Labs SDG Scores provides short-term, long-term, and
                  momentum scores that are generated for 16 Sustainable
                  Development Goals categories defined by the United Nations.*
            /factset-esg/v1/sfdr-pai:
              get:
                tags:
                  - Gets
                  - Principle
                  - Adverse
                  - Impact
                  - I)
                  - Data
                  - To
                  - Support
                  - Compliant
                  - Sustainable
                  - Finance
                  - Disclosure
                  - Regulation
                  - R)
                  - Reporting
                  - Factset
                  - Esg
                  - V1
                  - Sasb
                  - Scores
                  - Ranks
                  - All
                  - Sdg
                  - Sfdr
                  - Pai
                summary: >-
                  Gets Principle Adverse Impact (PAI) data to support compliant
                  SFDR Sustainable Finance Disclosure Regulation (SFDR)
                  reporting
                description: >
                  SFDR Principle Adverse Impact (PAI) data is built specifically
                  to support compliant Sustainable Finance Disclosure Regulation
                  (SFDR) reporting. FactSet collects PAI data items from
                  publicly available company-reported information and FactSet
                  databases, such as FactSet Fundamentals, FactSet RBICS with
                  Revenue and FactSet People, which are also based on
                  company-disclosures. FactSet uses Truvalue Labs SASB
                  Spotlights for supplemental OECD & UNGC violation checks where
                  company reporting is sparse. 
              post:
                tags:
                  - Gets
                  - Principle
                  - Adverse
                  - Impact
                  - I)
                  - Data
                  - To
                  - Support
                  - Compliant
                  - Sustainable
                  - Finance
                  - Disclosure
                  - Regulation
                  - R)
                  - Reporting
                  - Factset
                  - Esg
                  - V1
                  - Sasb
                  - Scores
                  - Ranks
                  - All
                  - Sdg
                  - Sfdr
                  - Pai
                summary: >-
                  Gets Principle Adverse Impact (PAI) data to support compliant
                  SFDR Sustainable Finance Disclosure Regulation (SFDR)
                  reporting
                description: >
                  SFDR Principle Adverse Impact (PAI) data is built specifically
                  to support compliant Sustainable Finance Disclosure Regulation
                  (SFDR) reporting. FactSet collects PAI data items from
                  publicly available company-reported information and FactSet
                  databases, such as FactSet Fundamentals, FactSet RBICS with
                  Revenue and FactSet People, which are also based on
                  company-disclosures. FactSet uses Truvalue Labs SASB
                  Spotlights for supplemental OECD & UNGC violation checks where
                  company reporting is sparse.
            /factset-esg/v1/sasb-spotlights:
              get:
                tags:
                  - Gets
                  - Spotlight
                  - Data
                  - For
                  - The
                  - Most
                  - Important
                  - Positive
                  - And
                  - Negative
                  - Events
                  - To
                  - Enable
                  - Timely
                  - Systematic
                  - Trading
                  - Strategies
                  - Portfolio
                  - Management
                  - Factset
                  - Esg
                  - V1
                  - Sasb
                  - Scores
                  - Ranks
                  - All
                  - Sdg
                  - Sfdr
                  - Pai
                  - Spotlights
                summary: >-
                  Gets Spotlight data for the most important positive and
                  negative ESG events to enable timely and systematic trading
                  strategies and portfolio management
                description: >
                  FactSet ESG by Truvalue Labs’ Spotlight Data solutions are a
                  daily collection of the most important positive and negative
                  ESG events detected by our algorithms, with a variety of
                  quantitative metadata to enable timely and systematic trading
                  strategies and portfolio management. Qualitive informational
                  data points such as the headline and key bullet points for
                  articles is also included. 
              post:
                tags:
                  - Gets
                  - Spotlight
                  - Data
                  - For
                  - The
                  - Most
                  - Important
                  - Positive
                  - And
                  - Negative
                  - Events
                  - To
                  - Enable
                  - Timely
                  - Systematic
                  - Trading
                  - Strategies
                  - Portfolio
                  - Management
                  - Factset
                  - Esg
                  - V1
                  - Sasb
                  - Scores
                  - Ranks
                  - All
                  - Sdg
                  - Sfdr
                  - Pai
                  - Spotlights
                summary: >-
                  Gets Spotlight data for the most important positive and
                  negative ESG events to enable timely and systematic trading
                  strategies and portfolio management
                description: >
                  FactSet ESG by Truvalue Labs’ Spotlight Data solutions are a
                  daily collection of the most important positive and negative
                  ESG events detected by our algorithms, with a variety of
                  quantitative metadata to enable timely and systematic trading
                  strategies and portfolio management. Qualitive informational
                  data points such as the headline and key bullet points for
                  articles is also included. reporting is sparse.
            /factset-esg/v1/sdg-spotlights:
              get:
                tags:
                  - Gets
                  - Spotlight
                  - Data
                  - For
                  - The
                  - Most
                  - Important
                  - Positive
                  - And
                  - Negative
                  - Events
                  - To
                  - Enable
                  - Timely
                  - Systematic
                  - Trading
                  - Strategies
                  - Portfolio
                  - Management
                  - Factset
                  - Esg
                  - V1
                  - Sasb
                  - Scores
                  - Ranks
                  - All
                  - Sdg
                  - Sfdr
                  - Pai
                  - Spotlights
                summary: >-
                  Gets Spotlight data for the most important positive and
                  negative ESG events to enable timely and systematic trading
                  strategies and portfolio management
                description: >
                  FactSet ESG by Truvalue Labs’ Spotlight Data solutions are a
                  daily collection of the most important positive and negative
                  ESG events detected by our algorithms, with a variety of
                  quantitative metadata to enable timely and systematic trading
                  strategies and portfolio management. Qualitive informational
                  data points such as the headline and key bullet points for
                  articles is also included. 
              post:
                tags:
                  - Gets
                  - Spotlight
                  - Data
                  - For
                  - The
                  - Most
                  - Important
                  - Positive
                  - And
                  - Negative
                  - Events
                  - To
                  - Enable
                  - Timely
                  - Systematic
                  - Trading
                  - Strategies
                  - Portfolio
                  - Management
                  - Factset
                  - Esg
                  - V1
                  - Sasb
                  - Scores
                  - Ranks
                  - All
                  - Sdg
                  - Sfdr
                  - Pai
                  - Spotlights
                summary: >-
                  Gets Spotlight data for the most important positive and
                  negative ESG events to enable timely and systematic trading
                  strategies and portfolio management
                description: >
                  FactSet ESG by Truvalue Labs’ Spotlight Data solutions are a
                  daily collection of the most important positive and negative
                  ESG events detected by our algorithms, with a variety of
                  quantitative metadata to enable timely and systematic trading
                  strategies and portfolio management. Qualitive informational
                  data points such as the headline and key bullet points for
                  articles is also included. reporting is sparse.
            /factset-esg/v1/sasb-articles:
              get:
                tags:
                  - Request
                  - Articles
                  - Tagged
                  - With
                  - Lens
                  - Categories
                  - From
                  - '2016-01-01'
                  - To
                  - Previous
                  - Day.
                  - Factset
                  - Esg
                  - V1
                  - Sasb
                  - Scores
                  - Ranks
                  - All
                  - Sdg
                  - Sfdr
                  - Pai
                  - Spotlights
                  - Articles
                summary: >-
                  Request articles tagged with SASB lens categories from
                  2016-01-01 to previous day.
                description: >
                  Articles endpoint allows to retrieve underlying news articles
                  used by the AI engine to calculate the ESG Scores of companies
                  and therefore provides ESG relevant news and also transparency
                  into the ESG Scores.
              post:
                tags:
                  - Request
                  - Articles
                  - Tagged
                  - With
                  - Lens
                  - Categories
                  - From
                  - '2016-01-01'
                  - To
                  - Previous
                  - Day
                  - Factset
                  - Esg
                  - V1
                  - Sasb
                  - Scores
                  - Ranks
                  - All
                  - Sdg
                  - Sfdr
                  - Pai
                  - Spotlights
                  - Articles
                summary: >-
                  Request articles tagged with SASB lens categories from
                  2016-01-01 to previous day
                description: >
                  Articles endpoint allows to retrieve underlying news articles
                  used by the AI engine to calculate the ESG Scores of companies
                  and therefore provides ESG relevant news and also transparency
                  into the ESG Scores.
            /factset-esg/v1/sdg-articles:
              get:
                tags:
                  - Request
                  - Articles
                  - Tagged
                  - With
                  - Lens
                  - Categories
                  - From
                  - '2016-01-01'
                  - To
                  - Previous
                  - Day.
                  - Factset
                  - Esg
                  - V1
                  - Sasb
                  - Scores
                  - Ranks
                  - All
                  - Sdg
                  - Sfdr
                  - Pai
                  - Spotlights
                  - Articles
                summary: >-
                  Request articles tagged with SDG lens categories from
                  2016-01-01 to previous day.
                description: >
                  Articles endpoint allows to retrieve underlying news articles
                  used by the AI engine to calculate the ESG Scores of companies
                  and therefore provides ESG relevant news and also transparency
                  into the ESG Scores.
              post:
                tags:
                  - Request
                  - Articles
                  - Tagged
                  - With
                  - Lens
                  - Categories
                  - From
                  - '2016-01-01'
                  - To
                  - Previous
                  - Day
                  - Factset
                  - Esg
                  - V1
                  - Sasb
                  - Scores
                  - Ranks
                  - All
                  - Sdg
                  - Sfdr
                  - Pai
                  - Spotlights
                  - Articles
                summary: >-
                  Request articles tagged with SDG lens categories from
                  2016-01-01 to previous day
                description: >
                  Articles endpoint allows to retrieve underlying news articles
                  used by the AI engine to calculate the ESG Scores of companies
                  and therefore provides ESG relevant news and also
                  transparency 
    overlays:
      - type: APIs.io Search
        url: overlays/esg-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/esg-openapi-api-evangelist-ratings.yml
    aid: factset:factset-esg-api
  - name: FactSet Vermilion API
    description: >-
      The Vermilion API, enables users to programmatically access FactSet's
      Vermilion Reporting Suite (VRS) and seamlessly integrate into customer's
      3rd party applications. The API is referred to as two key product
      initiatives, the REST API and the SCIM API.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.factset.com/api-catalog/vermilion-api
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: https://developer.factset.com/api-catalog/vermilion-api#overview
      - type: SDKs
        url: https://developer.factset.com/api-catalog/vermilion-api#sdkLibrary
      - type: Jupyter Notebooks
        url: https://developer.factset.com/api-catalog/vermilion-api#notebooks
      - type: Code Snippets
        url: https://developer.factset.com/api-catalog/vermilion-api#codeSnippet
      - type: Change Log
        url: https://developer.factset.com/api-catalog/vermilion-api#changelog
      - type: OpenAPI
        data:
          openapi: 3.0.0
          info:
            title: VRS API documentation
            license:
              name: Apache License, Version 2.0
              url: https://www.apache.org/licenses/LICENSE-2.0
          externalDocs:
            description: API Documentation
            url: https://developer.factset.com/api-catalog/vermilion-api
          tags:
            - name: Datasource
            - name: Entities
            - name: Reports
            - name: Report instance
            - name: SCIM
          paths:
            /v1/{tenant}/data-sources:
              get:
                tags:
                  - Lists
                  - All
                  - Datasources
                  - V1
                  - Tenant
                  - Data
                  - Sources
                summary: Lists all datasources
                description: List all datasources the user has permission to see
            /v1/{tenant}/data-sources/{dataSourceCode}:
              get:
                tags:
                  - Gets
                  - Datasource
                  - V1
                  - Tenant
                  - Data
                  - Sources
                  - Source
                  - Code
                summary: Gets a datasource
                description: Gets a datasource based on the code passed
            /v1/{tenant}/data-sources/{dataSourceCode}/data:
              get:
                tags:
                  - Gets
                  - The
                  - Data
                  - For
                  - Datasource
                  - V1
                  - Tenant
                  - Data
                  - Sources
                  - Source
                  - Code
                summary: Gets the data for the datasource
                description: >-
                  Gets the data for the datasource. There are optional query
                  parameters to filter the data
            /v1/{tenant}/entities/{entityCode}/values:
              get:
                tags:
                  - Gets
                  - The
                  - Entity
                  - Values
                  - V1
                  - Tenant
                  - Data
                  - Sources
                  - Source
                  - Code
                  - Values
                summary: Gets the entity values
                description: Gets the entity values for the specified entity
            /v1/{tenant}/reports:
              get:
                tags:
                  - Gets
                  - All
                  - Report
                  - Definitions
                  - V1
                  - Tenant
                  - Data
                  - Sources
                  - Source
                  - Code
                  - Values
                  - Reports
                summary: Gets all report definitions
                description: Gets all report definitions the user has permissions for
            /v1/{tenant}/reports/{reportDefinitionCode}:
              get:
                tags:
                  - Gets
                  - Report
                  - Definition
                  - V1
                  - Tenant
                  - Data
                  - Sources
                  - Source
                  - Code
                  - Values
                  - Reports
                  - Definition
                summary: Gets a report definition
                description: Gets a report defintion based on the code specified
            /v1/report-instances/generate:
              post:
                tags:
                  - Generates
                  - Report
                  - V1
                  - Tenant
                  - Data
                  - Sources
                  - Source
                  - Code
                  - Values
                  - Reports
                  - Definition
                  - Report
                  - Instances
                  - Generate
                summary: Generates a report
                description: >-
                  Generates a report using the specified ID and the JSON in the
                  request body
            /v1/{tenant}/report-instances/{reportInstanceId}:
              delete:
                tags:
                  - Cancels
                  - Report
                  - Generation
                  - V1
                  - Tenant
                  - Data
                  - Sources
                  - Source
                  - Code
                  - Values
                  - Reports
                  - Definition
                  - Report
                  - Instances
                  - Generate
                  - Instance
                  - Id
                summary: Cancels a report generation
                description: >-
                  Sends a request to cancel a report generation based on the
                  report instance id passed
              get:
                tags:
                  - Gets
                  - Report
                  - Instance
                  - Based
                  - 'On'
                  - The
                  - V1
                  - Tenant
                  - Data
                  - Sources
                  - Source
                  - Code
                  - Values
                  - Reports
                  - Definition
                  - Report
                  - Instances
                  - Generate
                  - Instance
                  - Id
                summary: Gets a report instance based on the ID
                description: Gets a report instance object based on the ID passed
            /v1/{tenant}/report-instances:
              get:
                tags:
                  - Gets
                  - List
                  - Of
                  - Report
                  - Instances
                  - V1
                  - Tenant
                  - Data
                  - Sources
                  - Source
                  - Code
                  - Values
                  - Reports
                  - Definition
                  - Report
                  - Instances
                  - Generate
                  - Instance
                  - Id
                summary: Gets a list of report instances
                description: >-
                  Gets a list of report instances. This can be filtered down
                  further by including query parameters in the URL. For example,
                  a report definition id can be added so the only report
                  instances returned are the ones with a matching id
            /v1/{tenant}/report-instances/{reportInstanceId}/results/{reportFileName}:
              get:
                tags:
                  - Gets
                  - The
                  - Generated
                  - File
                  - V1
                  - Tenant
                  - Data
                  - Sources
                  - Source
                  - Code
                  - Values
                  - Reports
                  - Definition
                  - Report
                  - Instances
                  - Generate
                  - Instance
                  - Id
                  - Results
                  - File
                  - Name
                summary: Gets the generated file
                description: >-
                  Get the generated file for a report instance. Users can fetch
                  the generated report once the genration is finished. The
                  report instance id and the report file name are passed in as
                  path paramters
            /v1/{tenant}/report-instances/{reportInstanceId}/logs:
              get:
                tags:
                  - Gets
                  - List
                  - Of
                  - Logs
                  - For
                  - The
                  - Report
                  - Instance
                  - Generation
                  - V1
                  - Tenant
                  - Data
                  - Sources
                  - Source
                  - Code
                  - Values
                  - Reports
                  - Definition
                  - Report
                  - Instances
                  - Generate
                  - Instance
                  - Id
                  - Results
                  - File
                  - Name
                  - Logs
                summary: Gets a list of logs for the report instance generation
                description: >-
                  Gets a list of logs for the generated report instance. Allows
                  the user to sort on log message, type and date. Also allows
                  for retrieving of just the errors & warnings'
            /scim/v2/Users:
              get:
                tags:
                  - Retrieves
                  - List
                  - Of
                  - Users
                  - V1
                  - Tenant
                  - Data
                  - Sources
                  - Source
                  - Code
                  - Values
                  - Reports
                  - Definition
                  - Report
                  - Instances
                  - Generate
                  - Instance
                  - Id
                  - Results
                  - File
                  - Name
                  - Logs
                  - Users
                summary: Retrieves a list of VRS users
                description: Retrieves a list of VRS users
              post:
                tags:
                  - Creates
                  - User
                  - V1
                  - Tenant
                  - Data
                  - Sources
                  - Source
                  - Code
                  - Values
                  - Reports
                  - Definition
                  - Report
                  - Instances
                  - Generate
                  - Instance
                  - Id
                  - Results
                  - File
                  - Name
                  - Logs
                  - Users
                summary: Creates a user
                description: Creates a VRS user
            /scim/v2/Users/{userId}:
              get:
                tags:
                  - Retrieves
                  - User
                  - V1
                  - Tenant
                  - Data
                  - Sources
                  - Source
                  - Code
                  - Values
                  - Reports
                  - Definition
                  - Report
                  - Instances
                  - Generate
                  - Instance
                  - Id
                  - Results
                  - File
                  - Name
                  - Logs
                  - Users
                  - User
                summary: Retrieves a VRS User
                description: Retrieves a VRS user based on their ID
              delete:
                tags:
                  - Deletes
                  - User
                  - V1
                  - Tenant
                  - Data
                  - Sources
                  - Source
                  - Code
                  - Values
                  - Reports
                  - Definition
                  - Report
                  - Instances
                  - Generate
                  - Instance
                  - Id
                  - Results
                  - File
                  - Name
                  - Logs
                  - Users
                  - User
                summary: Deletes a VRS user
                description: >-
                  Deletes a VRS user (this marks them as 'Deleted' in the
                  database)
              patch:
                tags:
                  - Add
                  - Or
                  - Remove
                  - User
                  - Attributes
                  - V1
                  - Tenant
                  - Data
                  - Sources
                  - Source
                  - Code
                  - Values
                  - Reports
                  - Definition
                  - Report
                  - Instances
                  - Generate
                  - Instance
                  - Id
                  - Results
                  - File
                  - Name
                  - Logs
                  - Users
                  - User
                summary: Add or remove VRS user attributes
                description: >-
                  Adds or removes VRS user attributes based on the JSON
                  properties
              put:
                tags:
                  - Updates
                  - User
                  - V1
                  - Tenant
                  - Data
                  - Sources
                  - Source
                  - Code
                  - Values
                  - Reports
                  - Definition
                  - Report
                  - Instances
                  - Generate
                  - Instance
                  - Id
                  - Results
                  - File
                  - Name
                  - Logs
                  - Users
                  - User
                summary: Updates a VRS user
                description: Updates (replaces) a VRS user with the properties in the JSON
            /scim/v2/Groups:
              get:
                tags:
                  - Retrieves
                  - List
                  - Of
                  - Role
                  - V1
                  - Tenant
                  - Data
                  - Sources
                  - Source
                  - Code
                  - Values
                  - Reports
                  - Definition
                  - Report
                  - Instances
                  - Generate
                  - Instance
                  - Id
                  - Results
                  - File
                  - Name
                  - Logs
                  - Users
                  - User
                  - Groups
                summary: Retrieves a list of VRS role
                description: Retrieves a VRS roles
              post:
                tags:
                  - Creates
                  - Role
                  - V1
                  - Tenant
                  - Data
                  - Sources
                  - Source
                  - Code
                  - Values
                  - Reports
                  - Definition
                  - Report
                  - Instances
                  - Generate
                  - Instance
                  - Id
                  - Results
                  - File
                  - Name
                  - Logs
                  - Users
                  - User
                  - Groups
                summary: Creates a role
                description: Creates a VRS role
            /scim/v2/Groups/{groupId}:
              get:
                tags:
                  - Retrieves
                  - Role
                  - V1
                  - Tenant
                  - Data
                  - Sources
                  - Source
                  - Code
                  - Values
                  - Reports
                  - Definition
                  - Report
                  - Instances
                  - Generate
                  - Instance
                  - Id
                  - Results
                  - File
                  - Name
                  - Logs
                  - Users
                  - User
                  - Groups
                  - Group
                summary: Retrieves a VRS role
                description: Retrieves a VRS role based on the ID
              delete:
                tags:
                  - Deletes
                  - Role
                  - V1
                  - Tenant
                  - Data
                  - Sources
                  - Source
                  - Code
                  - Values
                  - Reports
                  - Definition
                  - Report
                  - Instances
                  - Generate
                  - Instance
                  - Id
                  - Results
                  - File
                  - Name
                  - Logs
                  - Users
                  - User
                  - Groups
                  - Group
                summary: Deletes a VRS role
                description: Deletes a VRS role
              patch:
                tags:
                  - Add
                  - Or
                  - Remove
                  - User
                  - To/from
                  - Group
                  - V1
                  - Tenant
                  - Data
                  - Sources
                  - Source
                  - Code
                  - Values
                  - Reports
                  - Definition
                  - Report
                  - Instances
                  - Generate
                  - Instance
                  - Id
                  - Results
                  - File
                  - Name
                  - Logs
                  - Users
                  - User
                  - Groups
                  - Group
                summary: Add or remove a user to/from a group
                description: Adds or removes a VRS user to/from a VRS role
              put:
                tags:
                  - Updates
                  - Group
                  - V1
                  - Tenant
                  - Data
                  - Sources
                  - Source
                  - Code
                  - Values
                  - Reports
                  - Definition
                  - Report
                  - Instances
                  - Generate
                  - Instance
                  - Id
                  - Results
                  - File
                  - Name
                  - Logs
                  - Users
                  - User
                  - Groups
                  - Group
                summary: Updates a VRS Group
                description: Updates (replaces) a VRS Group with the pr
    overlays:
      - type: APIs.io Search
        url: overlays/vermilion-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/vermilion-openapi-api-evangelist-ratings.yml
    aid: factset:factset-vermilion-api
  - name: FactSet Analytics Datastore API
    description: >-
      Request pre-calculated Portfolio Analytics data saved in FactSet's
      Analytics Datastore, via deterministic URLs.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.factset.com/api-catalog/analytics-datastore-api
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: >-
          https://developer.factset.com/api-catalog/analytics-datastore-api#overview
      - type: SDKs
        url: >-
          https://developer.factset.com/api-catalog/analytics-datastore-api#sdkLibrary
      - type: Jupyter Notebooks
        url: >-
          https://developer.factset.com/api-catalog/analytics-datastore-api#notebooks
      - type: Code Snippets
        url: >-
          https://developer.factset.com/api-catalog/analytics-datastore-api#codeSnippet
      - type: Change Log
        url: >-
          https://developer.factset.com/api-catalog/analytics-datastore-api#changelog
      - type: OpenAPI
        data:
          openapi: 3.0.3
          info:
            title: Analytics Datastore API
            license:
              name: Apache License, Version 2.0
              url: https://www.apache.org/licenses/LICENSE-2.0
          externalDocs:
            url: https://developer.factset.com/api-catalog/analytics-datastore-api
            description: API Documentation
          tags:
            - name: Mappings
              description: >-
                Retrieves a mapping with a Location header to redirect to the
                underlying data
            - name: Objects
              description: Retrieves Objects and their underlying data
            - name: Documents
              description: Retrieves Document metadata and URL locations to underlying data
          paths:
            /analytics/pub-datastore/swivel/v1/{document}/{accountId}/{date}:
              get:
                tags:
                  - Redirects
                  - To
                  - The
                  - Raw
                  - T/
                  - Output
                  - Created
                  - By
                  - Publisher
                  - Service.
                  - Id
                  - Date
                summary: >-
                  Redirects to the raw PPT/PDF output created by the Publisher
                  service.
                description: "Takes report parameter inputs and returns the object location for the specified report via a 302 redirect.\r\n\r\nNote: Due to Swagger UI functionality, the redirect is automatically followed when using 'Try it out', so instead of the 302 Header response, a 200 is returned with the Cargo response Body."
            /analytics/pub-datastore/swivel/v1/{document}/{assetName}/{reportId}/{tileId}/{accountId}:
              get:
                tags:
                  - Redirects
                  - To
                  - The
                  - Underlying
                  - A/
                  - Data
                  - Represented
                  - In
                  - Stach
                  - Format,
                  - With
                  - 'No'
                  - As
                  - Of
                  - Date
                  - Specified.
                  - Id
                  - Date
                  - Name
                  - Report
                  - Tile
                  - Account
                summary: >-
                  Redirects to the underlying PA/SPAR data represented in a
                  Stach format, with no as of date specified.
                description: "Takes report parameter inputs and returns the object location for the specified report via a 302 redirect.\r\n\r\nNote: Due to Swagger UI functionality, the redirect is automatically followed when using 'Try it out', so instead of the 302 Header response, a 200 is returned with the Cargo response Body."
            /analytics/pub-datastore/swivel/v1/{document}/{assetName}/{reportId}/{tileId}/{accountId}/{date}:
              get:
                tags:
                  - Redirects
                  - To
                  - The
                  - Underlying
                  - A/
                  - Data
                  - Represented
                  - In
                  - Stach
                  - Format.
                  - Id
                  - Date
                  - Name
                  - Report
                  - Tile
                  - Account
                summary: >-
                  Redirects to the underlying PA/SPAR data represented in a
                  Stach format.
                description: "Takes report parameter inputs and returns the object location for the specified report via a 302 redirect.\r\n\r\nNote: Due to Swagger UI functionality, the redirect is automatically followed when using 'Try it out', so instead of the 302 Header response, a 200 is returned with the Cargo response Body."
            /analytics/pub-datastore/swivel/v1/{document}/{assetName}/{reportId}/{tileId}/{accountId}/{configId}/{date}:
              get:
                tags:
                  - Redirects
                  - To
                  - The
                  - Underlying
                  - Insight/
                  - Vault
                  - Data
                  - In
                  - Stach
                  - Format.
                  - Id
                  - Date
                  - Name
                  - Report
                  - Tile
                  - Account
                  - Config
                summary: >-
                  Redirects to the underlying Insight/Vault data in a Stach
                  format.
                description: "The inclusion of a configId in the path indicates this is for Insight/Vault mappings only, as PA/SPAR mappings do not support the concept of configuration id.\r\n\r\nTakes report parameter inputs and returns the object location for the specified report via a 302 redirect.\r\n\r\nNote: Due to Swagger UI functionality, the redirect is automatically followed when using 'Try it out', so instead of the 302 Header response, a 200 is returned with the Cargo response Body."
            /analytics/pub-datastore/cargo/v1/groups/{groupId}/objects/{objectId}:
              get:
                tags:
                  - Gets
                  - An
                  - Object
                  - Given
                  - D.
                  - In
                  - This
                  - Case
                  - Retrieved
                  - From
                  - Mapping
                  - Location
                  - Header,
                  - Data
                  - Response
                  - Body.
                  - Id
                  - Date
                  - Name
                  - Report
                  - Tile
                  - Account
                  - Config
                  - Objects
                  - Object
                summary: >-
                  Gets an object given an ID. In this case ID retrieved from
                  mapping Location header, object data in response body.
                description: "Raw object data can be found in the response body. This can be either the mapped PDF/PPT or STACH json, depending on the mapping. https://pages.github.factset.com/analytics-reporting/stachschema/#/ \r\n\nOptional request header \"accept-encoding\", with allowed values of \"br\" and \"gzip\". If accept-encoding is passed, the response is compressed."
            /analytics/pub-datastore/tag-search/v1/documents/search:
              post:
                tags:
                  - Gets
                  - List
                  - Of
                  - Documents
                  - That
                  - User
                  - Has
                  - Access
                  - To.
                  - Id
                  - Date
                  - Name
                  - Report
                  - Tile
                  - Account
                  - Config
                  - Objects
                  - Object
                  - Analytics
                  - Pub
                  - Datastore
                  - Tag
                  - Search
                  - V1
                  - Documents
                summary: Gets a list of Documents that a user has access to.
                description: "Retrieves metadata around documents stored in the Analytics Datastore Service. Each Document will have a 'url' property which will act as a re-direct to the underlying document data\r\n\r\nThis end point supports pagination and filtering through the use of the request body listed below.\r\n\r\nTo discover what tags are available to filter on, see GET /tags and GET /tags/{name}/values to retrieve these filter values.\r\n\r\nSimilarly, to discover what product types are available to filter on, see POST /product-types/search to retrieve a list of product types."
            /analytics/pub-datastore/tag-search/v1/tags:
              get:
                tags:
                  - Gets
                  - List
                  - Of
                  - Tag
                  - Definitions
                  - For
                  - The
                  - User.
                  - Id
                  - Date
                  - Name
                  - Report
                  - Tile
                  - Account
                  - Config
                  - Objects
                  - Object
                  - Analytics
                  - Pub
                  - Datastore
                  - Tag
                  - Search
                  - V1
                  - Documents
                  - Tags
                summary: Gets a list of tag definitions for the user.
                description: >-
                  Tag definitions consist of a name and a type. Use this end
                  point to see a list of pre-existing tags that can be used to
                  filter on the Documents end point.
            /analytics/pub-datastore/tag-search/v1/tags/{name}:
              get:
                tags:
                  - Get
                  - Single
                  - Tag
                  - Definition
                  - Based
                  - 'On'
                  - Its
                  - Name
                  - Id
                  - Date
                  - Name
                  - Report
                  - Tile
                  - Account
                  - Config
                  - Objects
                  - Object
                  - Analytics
                  - Pub
                  - Datastore
                  - Tag
                  - Search
                  - V1
                  - Documents
                  - Tags
                summary: Get a single tag definition based on its name
                description: Retrieve a tag definition based on its name
            /analytics/pub-datastore/tag-search/v1/tags/{name}/values:
              post:
                tags:
                  - Gets
                  - List
                  - Of
                  - Tag
                  - Values
                  - For
                  - The
                  - Given
                  - Name
                  - Id
                  - Date
                  - Name
                  - Report
                  - Tile
                  - Account
                  - Config
                  - Objects
                  - Object
                  - Analytics
                  - Pub
                  - Datastore
                  - Tag
                  - Search
                  - V1
                  - Documents
                  - Tags
                  - Values
                summary: Gets a list of tag values for the given name
                description: >-
                  Returns a list of tag values depending on the name provided.
                  Supports filtering on additional tag name value pairs, which
                  operates as an 'AND' where the Document must have the tag name
                  specified in the path AND the filtered parameter.
            /analytics/pub-datastore/tag-search/v1/product-types/search:
              post:
                tags:
                  - Gets
                  - List
                  - Of
                  - Product
                  - Types
                  - That
                  - User
                  - Has
                  - Access
                  - To.
                  - Id
                  - Date
                  - Name
                  - Report
                  - Tile
                  - Account
                  - Config
                  - Objects
                  - Object
                  - Analytics
                  - Pub
                  - Datastore
                  - Tag
                  - Search
                  - V1
                  - Documents
                  - Tags
                  - Values
                  - Product
                  - Types
                summary: Gets a list of product types that a user has access to.
                description: >-
                  Retrieves a list of product types that have been specified
                  across all documents th
    overlays:
      - type: APIs.io Search
        url: overlays/analytics-datastore-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/analytics-datastore-openapi-api-evangelist-ratings.yml
    aid: factset:factset-analytics-datastore-api
  - name: FactSet Options API
    description: >-
      The FactSet Options API provides Chains and related pricing data such as
      mid bid-ask price, reference data (e.g., strike price), and risk measures
      (e.g., Greeks and implied volatility).
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.factset.com/api-catalog/factset-options-api
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: https://developer.factset.com/api-catalog/factset-options-api#overview
      - type: SDKs
        url: >-
          https://developer.factset.com/api-catalog/factset-options-api#sdkLibrary
      - type: Jupyter Notebooks
        url: >-
          https://developer.factset.com/api-catalog/factset-options-api#notebooks
      - type: Code Snippets
        url: >-
          https://developer.factset.com/api-catalog/factset-options-api#codeSnippet
      - type: Change Log
        url: >-
          https://developer.factset.com/api-catalog/factset-options-api#changelog
      - type: OpenAPI
        data:
          openapi: 3.0.0
          info:
            title: FactSet Options API
          tags:
            - name: Option Chains & Screening
              description: >-
                Generate a list or universe of options ids based on underlying
                securities or other conditions
            - name: Snapshot
              description: >-
                A generic profile for a list of option securities as of a
                specific date
            - name: Reference
              description: Option Reference Information and Dates
            - name: Prices & Volume
              description: >-
                Option Prices & Volume information for a requested time-range
                for the option security or aggregated for all options associated
                to the underlying security
            - name: Risk Measures
              description: >-
                Option Risk measures such as Greeks, Implied Volatilities, and
                Calculators
          paths:
            /factset-options/v1/chains:
              post:
                tags:
                  - Returns
                  - All
                  - The
                  - Underlying
                  - Option
                  - Identifiers
                  - For
                  - Specified
                  - Security
                  - Identifier
                  - Factset
                  - Options
                  - V1
                  - Chains
                summary: >-
                  Returns all the underlying option identifiers for the
                  specified underlying Security identifier
                description: >
                  Returns all the underlying option identifiers for the
                  underlying security identifier. Specify the date and or
                  exhcange for the list of options associated to the id. 

                    *Currently only OPRA Exchange is supported with exchange ISO "USA"*
            /factset-options/v1/option-screening:
              post:
                tags:
                  - Returns
                  - All
                  - The
                  - Option
                  - Identifiers
                  - Based
                  - 'On'
                  - Conditions
                  - Provided
                  - As
                  - Input
                  - In
                  - Request
                  - Factset
                  - Options
                  - V1
                  - Chains
                  - Option
                  - Screening
                summary: >-
                  Returns all the option identifiers based on the conditions
                  provided as input in the request
                description: >
                  Returns all the option identifiers based on the conditions
                  provided as input in the request. Conditions are as follows
                  and will follow "AND" logic if more than one condition is
                  applied and allows up to **three conditions** using AND
                  Logic.If a condition is used the accompanying value MUST be
                  used - 

                  |conditions|description|

                  |||

                  |P_OPT_UNDERLYING_SECURITY_E|Underlying Security Equal To|

                  |P_OPT_STRIKE_PRICE_E|Strike Price Equal To|

                  |P_OPT_EXP_DATEN_E|Expiration Date (YYYYMMDD) Equal To|

                  |P_OPT_VOLUME_G|Volume Greater Than|

                  |P_OPT_VOLUME_GE|Volume Greater Than or Equal To|

                  |P_OPT_VOLUME_L|Volume Less Than|

                  |P_OPT_VOLUME_LE|Volume Less Than or Equal To|

                  |P_OPT_VOLUME_E|Volume Equal To|

                  |P_OPT_OPTION_TYPE_E|Option Type (1= Equity, 2=Index)|

                  |P_OPT_CALL_OR_PUT_E|Call or Put (0=Call, 1=Put)|

                    *Currently only OPRA Exchange is supported with exchange ISO "USA"*
            /factset-options/v1/snapshot:
              post:
                tags:
                  - Returns
                  - All
                  - The
                  - Profile
                  - Information
                  - For
                  - List
                  - Of
                  - Identifiers
                  - As
                  - Specific
                  - Date
                  - Factset
                  - Options
                  - V1
                  - Chains
                  - Option
                  - Screening
                  - Snapshot
                summary: >-
                  Returns all the profile information for the list of
                  identifiers as of a specific date
                description: >
                  Returns all the profile information for the list of
                  identifiers for a specific date. The data includes - 

                  * Expiration Date

                  * Greek - Delta

                  * Implied Volatility

                  * Price 

                  * Style

                  * Type

                  * Underlying Security

                  * Underlying Security Price

                  * Open Interest

                  * Name

                    *Currently only OPRA Exchange is supported with exchange ISO "USA"*
            /factset-options/v1/references:
              post:
                tags:
                  - Returns
                  - Basic
                  - Reference
                  - Details
                  - For
                  - The
                  - Options
                  - Such
                  - As
                  - Currency,
                  - Exchange,
                  - Symbols,
                  - Flags
                  - And
                  - More
                  - Factset
                  - Options
                  - V1
                  - Chains
                  - Option
                  - Screening
                  - Snapshot
                  - References
                summary: >-
                  Returns basic reference details for the options such as
                  currency, exchange, symbols, flags and more
                description: >
                  Returns basic reference details for the options. Data items
                  include - 

                  * Name

                  * Exchange

                  * Call or Put Flag

                  * Call or Put Pair Symbol

                  * Other symbols such as OPRA17 and OCC21

                  * Currency

                  * Underlying Security Symbols

                  * Expiration Month, Dates, and Frequency


                  *For details or definitions of all available response fields
                  visit the associated schema.*

                    *Currently only OPRA Exchange is supported with exchange ISO "USA"*
            /factset-options/v1/dates:
              post:
                tags:
                  - Returns
                  - Option
                  - Security
                  - Dates
                  - Such
                  - As
                  - Expiration
                  - And
                  - Trade.
                  - Factset
                  - Options
                  - V1
                  - Chains
                  - Option
                  - Screening
                  - Snapshot
                  - References
                  - Dates
                summary: Returns option security dates such as expiration and trade.
                description: >
                  Returns all relevant dates such as  for the specified Option
                  identifier. Data Items include - 

                  * Expiration Date

                  * First Dates for Ask, Bid, Settlement, and Trade

                  * Last Dates for Ask, Bid, Settlement, and Trade

                    *Currently only OPRA Exchange is supported with exchange ISO "USA"*
            /factset-options/v1/prices:
              post:
                tags:
                  - Returns
                  - The
                  - Pricing
                  - Related
                  - Information
                  - For
                  - Specified
                  - Option
                  - Identifier
                  - Factset
                  - Options
                  - V1
                  - Chains
                  - Option
                  - Screening
                  - Snapshot
                  - References
                  - Dates
                  - Prices
                summary: >-
                  Returns the pricing related information for the specified
                  option identifier
                description: >
                  Returns the pricing related information for the specified
                  option identifier. Items include - 

                  * Ask

                  * Bid

                  * Mid

                  * Mid Bid Ask

                  * Settlement

                  * Last Price Type (Settlement or MidBidAsk)

                  * Last Price

                  * Strike Price

                  * Underlying Security Price

                  * 52 Week High/Low

                  * Open, High, Low for day. Note securities must be trading for
                  day requested.

                    *Currently only OPRA Exchange is supported with exchange ISO "USA"*
            /factset-options/v1/underlying-volume:
              post:
                tags:
                  - Returns
                  - The
                  - Aggregate
                  - Volume
                  - And
                  - Open
                  - Interest
                  - For
                  - List
                  - Of
                  - Options
                  - Under
                  - Specified
                  - Security
                  - Identifier
                  - Factset
                  - Options
                  - V1
                  - Chains
                  - Option
                  - Screening
                  - Snapshot
                  - References
                  - Dates
                  - Prices
                  - Underlying
                  - Volume
                summary: >-
                  Returns the aggregate volume and open interest for the list of
                  the options under the specified security identifier
                description: >
                  Return the Volume and Open Interest details for list of the
                  options for the specified underlying security identifier. The
                  data is aggregated for all options contracts associated to the
                  underlying id, or specified in the request only the contracts
                  listed on a specific exchange. Data Includes - 

                  * Put Call Ratio 

                  * Total Put Volume & Open Interest

                  * Total Call Volume & Open Interest

                  * Total Put & Call Volume & Open Interest

                    *Currently only OPRA Exchange is supported with exchange ISO "USA"*
            /factset-options/v1/volume:
              post:
                tags:
                  - Returns
                  - The
                  - Volume
                  - Details
                  - For
                  - Specified
                  - Option
                  - Identifier
                  - Factset
                  - Options
                  - V1
                  - Chains
                  - Option
                  - Screening
                  - Snapshot
                  - References
                  - Dates
                  - Prices
                  - Underlying
                  - Volume
                summary: Returns the volume details for the specified option identifier
                description: >
                  Returns the volume details for the specified option identifier
                  for a specified exchange. Data items include - 

                  * Open Interest

                  * Volume

                    *Currently only OPRA Exchange is supported with exchange ISO "USA"*
            /factset-options/v1/greeks:
              post:
                tags:
                  - Returns
                  - All
                  - The
                  - Greeks
                  - Details
                  - For
                  - Specified
                  - Option
                  - Identifier
                  - Factset
                  - Options
                  - V1
                  - Chains
                  - Option
                  - Screening
                  - Snapshot
                  - References
                  - Dates
                  - Prices
                  - Underlying
                  - Volume
                  - Greeks
                summary: >-
                  Returns all the Greeks details for the specified option
                  identifier
                description: >
                  Returns all the greeks details for the specified option
                  identifier. Greeks provide quantifiable factors for measuring
                  the option's price sensativity. Greeks include -


                  |Greek|Description|

                  |||

                  |Delta| The ratio comparing the change in the price of the
                  underlying asset to the corresponding change in the price of a
                  derivative. Sometimes referred to as the "hedge ratio". For
                  example, with respect to call options, a delta of 0.7 means
                  that for every $1 the underlying stock increases, the call
                  option will increase by $0.70. Put option deltas, on the other
                  hand, will be negative, because as the underlying security
                  increases, the value of the option will decrease. So a put
                  option with a delta of -0.7 will decrease by $0.70 for every
                  $1 the underlying increases in price. As an in-the-money call
                  option nears expiration, it will approach a delta of 1.00, and
                  as an in-the-money put option nears expiration, it will
                  approach a delta of -1.00.|

                  |Gamma| The rate of change for delta with respect to the
                  underlying asset's price. Mathematically, gamma is the first
                  derivative of delta and is used when trying to gauge the price
                  of an option relative to the amount it is in or out of the
                  money. When the option being measured is deep in or out of the
                  money, gamma is small. When the option is near the money,
                  gamma is largest.|

                  |Rho|The rate at which the price of a derivative changes
                  relative to a change in the risk-free rate of interest. Rho
                  measures the sensitivity of an option or options portfolio to
                  a change in interest rate.|

                  |Theta|A measure of the rate of decline in the value of an
                  option due to the passage of time. Theta can also be referred
                  to as the time decay on the value of an option. If everything
                  is held constant, then the option will lose value as time
                  moves closer to the maturity of the option. For example, if
                  the strike price of an option is $1,150 and theta is 53.80,
                  then in theory the value of the option will drop $53.80 per
                  day. The measure of theta quantifies the risk that time
                  imposes on options as options are only exercisable for a
                  certain period of time.|

                  |Vega|The amount that the price of an option changes compared
                  to a 1% change in volatility. Vega changes when there are
                  large price movements in the underlying asset and vega falls
                  as the option gets closer to maturity. Vega can change even if
                  there is no change in the price of the underlying asset, this
                  would happen if there is a change in expected volatility. For
                  example, if the vega of an option is -96.94 and if implied
                  volatility were to rise by 1% then the option value would fall
                  by $96.94.|


                  Note
                    * Each step in the binomial model represents a change in time, therefore, point estimates of the Greeks can be calculated for American options. The following can be used to calculate the Greeks for the Binomial Option Pricing Model (BOPM) pricing model, using the notation fstep,node so f1,1 represents the option price at the first step, top node (nodes are counted at each step starting with 0 at the bottom. See [Constructing the Tree](https://my.apps.factset.com/oa/pages/17735#tree) for more information).
                    
                  For more detials on calculation methodologies, visit [OA
                  14933](https://my.apps.factset.com/oa/pages/14933). 

                    *Currently only OPRA Exchange is supported with exchange ISO "USA"*
            /factset-options/v1/implied-volatility:
              post:
                tags:
                  - Returns
                  - The
                  - Implied
                  - Volatility
                  - Information
                  - For
                  - Specified
                  - Option
                  - Identifier
                  - Factset
                  - Options
                  - V1
                  - Chains
                  - Option
                  - Screening
                  - Snapshot
                  - References
                  - Dates
                  - Prices
                  - Underlying
                  - Volume
                  - Greeks
                  - Implied
                  - Volatility
                summary: >-
                  Returns the implied volatility information for the specified
                  option identifier
                description: >
                  Returns the Implied Volatility for the specified option across
                  European and American contracts. For more details regarding
                  Implied Volatility calculations visit - [OA
                  14932](https://my.apps.factset.com/oa/pages/14932)


                  *Currently the following exchanges are not supported for API
                  use cases - CME, CMEE, CBT, CBTE, NYM, NYME*
            /factset-options/v1/atm-implied-volatility:
              post:
                tags:
                  - Returns
                  - The
                  - At-the-money
                  - M)
                  - Implied
                  - Volatility
                  - Details
                  - For
                  - Specified
                  - Underlying
                  - Security
                  - Identifier
                  - Factset
                  - Options
                  - V1
                  - Chains
                  - Option
                  - Screening
                  - Snapshot
                  - References
                  - Dates
                  - Prices
                  - Underlying
                  - Volume
                  - Greeks
                  - Implied
                  - Volatility
                  - Atm
                summary: >-
                  Returns the at-the-money (ATM) implied volatility details for
                  the specified underlying security identifier
                description: >
                  Returns weighted average of the implied volatilities from the
                  options listed for a specified security identifier. 


                  There are three different methods available for calculating
                  at-the-money implied volatility (ATM IV), which gives a
                  weighted average of the implied volatilities from the options
                  listed on a given stock. They are ATM IV (Filtered), ATM IV
                  (Filtered with Smoothing), and ATM IV (Market). Each of these
                  ATM IV calculations is available for just the calls on a given
                  stock, just the puts, or the composite of both the calls and
                  puts.

                  This at-the-money implied volatility market can calculated for
                  different periods -

                  * One Month

                  * Two Months

                  * Three Months

                  * Four Months

                  * Five Months

                  * Six Months


                  *For more details regarding ATM Volatility calculations, visit
                  [OA 16276](https://my.apps.factset.com/oa/pages/16276)*

                    *Currently only OPRA Exchange traded op
    overlays:
      - type: APIs.io Search
        url: overlays/options-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/options-openapi-api-evangelist-ratings.yml
    aid: factset:factset-options-api
  - name: Symphony Pod API
    description: >-
      The Symphony Pod API is used to build tools in order to manage and
      administer Symphony for your organization. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://docs.developers.symphony.com/bots/overview-of-rest-api/pod-api
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: https://docs.developers.symphony.com/bots/overview-of-rest-api/pod-api
      - type: OpenAPI
        data:
          swagger: '2.0'
          info:
            title: Pod API
          host: yourpodURL.symphony.com
          basePath: /pod
          paths:
            /v1/companycert/list:
              get:
                summary: List all trusted certs
                tags:
                  - List
                  - All
                  - Trusted
                  - Certs
                  - V1
                  - Companycert
                  - List
            /v2/companycert/create:
              post:
                summary: >-
                  Create a company trusted or untrusted certificate. Different
                  from V1 in that we reject expired certificates.
                tags:
                  - Create
                  - Company
                  - Trusted
                  - Or
                  - Untrusted
                  - Certificate.
                  - Different
                  - From
                  - V1
                  - In
                  - That
                  - We
                  - Reject
                  - Expired
                  - Certificates.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
            /v1/companycert/delete:
              post:
                summary: Delete a company certificate
                tags:
                  - Delete
                  - Company
                  - Certificate
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
            /v1/companycert/{fingerPrint}/get:
              get:
                summary: Get the details of a company certificate
                tags:
                  - Get
                  - The
                  - Details
                  - Of
                  - Company
                  - Certificate
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
            /v1/companycert/{fingerPrint}/update:
              post:
                summary: Update a company certificate
                tags:
                  - Update
                  - Company
                  - Certificate
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
            /v1/companycert/{fingerPrint}/issuedBy:
              get:
                summary: >
                  Return a list of all certificates which were verified to the
                  cert whose

                  fingerprint is passed.
                tags:
                  - Return
                  - List
                  - Of
                  - All
                  - Certificates
                  - Which
                  - Were
                  - Verified
                  - To
                  - The
                  - Cert
                  - |-
                    Whose
                    fingerprint
                  - Is
                  - |
                    Passed.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
            /v1/companycert/podmanaged/list:
              get:
                summary: List all trusted certs
                tags:
                  - List
                  - All
                  - Trusted
                  - Certs
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
            /v1/companycert/type/list:
              post:
                summary: List all certs of the given types
                tags:
                  - List
                  - All
                  - Certs
                  - Of
                  - The
                  - Given
                  - Types
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
            /v1/podcert:
              get:
                summary: >
                  Retrieve the pod certificate that can be use to validate
                  signed JWT tokens generated from the pod
                tags:
                  - Retrieve
                  - The
                  - Pod
                  - Certificate
                  - That
                  - Can
                  - Be
                  - Use
                  - To
                  - Validate
                  - Signed
                  - Tokens
                  - Generated
                  - From
                  - |
                    Pod
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
            /v1/connection/list:
              get:
                summary: List of requesting user's connection
                description: >
                  This retrieves all connections of the requesting user. (i.e.
                  both connections in which the requesting user is the sender
                  and those

                  in which the requesting user is the inivtee) By default, if
                  you haven't specified the connection status to filter on, this
                  call will only

                  return results for both "pending_incoming" and
                  "pending_outgoing". You can optionally filter by userIds to
                  further restrict the results of

                  a specific connection status. If the users are in the same
                  private pod, the users have an implicit connection status of
                  "accepted". Those

                  users will not be returned in the response if you don't
                  specify the connection status as "accepted" (default is
                  "pending")

                  and the explicit userIds in the request.
                tags:
                  - List
                  - Of
                  - Requesting
                  - User's
                  - Connection
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
            /v1/connection/create:
              post:
                summary: Sends an invitation to connect with another user
                tags:
                  - Sends
                  - An
                  - Invitation
                  - To
                  - Connect
                  - With
                  - Another
                  - User
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
            /v1/connection/accept:
              post:
                summary: Accept the connection request for the requesting user
                tags:
                  - Accept
                  - The
                  - Connection
                  - Request
                  - For
                  - Requesting
                  - User
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
            /v1/connection/reject:
              post:
                summary: Reject the connection request for the requesting user.
                description: >
                  Reject the connection between the requesting user and request
                  sender. If both users are in the same private pod,

                  an error will be returned because both users have an implicit
                  connection which cannot be rejected.
                tags:
                  - Reject
                  - The
                  - Connection
                  - Request
                  - For
                  - Requesting
                  - User.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
            /v1/connection/user/{userId}/info:
              get:
                summary: The status of the connection invitation to another user.
                tags:
                  - The
                  - Status
                  - Of
                  - Connection
                  - Invitation
                  - To
                  - Another
                  - User.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
            /v1/connection/user/{uid}/remove:
              post:
                summary: Removes a connection with a user.
                tags:
                  - Removes
                  - Connection
                  - With
                  - User.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
            /v1/im/create:
              post:
                summary: >-
                  Create a new single or multi party instant message
                  conversation between the caller and specified users.
                description: >
                  At least one user ID must be provided or

                  an error response will be sent.


                  The caller is implicitly included in the members of the

                  created chat.


                  Duplicate users will be included in the membership of the chat
                  but

                  the duplication will be silently ignored.


                  If there is an existing IM conversation with the same set of
                  participants then

                  the id of that existing stream will be returned.


                  This method was incorrectly specified to take a query
                  parameter in

                  version 1.0 of this specification but now expects a JSON array
                  of

                  user IDs in the body of the request.
                tags:
                  - Create
                  - New
                  - Single
                  - Or
                  - Multi
                  - Party
                  - Instant
                  - Message
                  - Conversation
                  - Between
                  - The
                  - Caller
                  - And
                  - Specified
                  - Users.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
            /v1/im/{id}/update:
              post:
                summary: Update the attributes of an existing IM.
                tags:
                  - Update
                  - The
                  - Attributes
                  - Of
                  - An
                  - Existing
                  - M.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
            /v1/im/{id}/info:
              get:
                summary: Get information about a partcular IM.
                tags:
                  - Get
                  - Information
                  - About
                  - Partcular
                  - M.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
            /v1/presence/feed/create:
              post:
                summary: Create Presence status feed.
                description: >
                  Create a new stream capturing presence status changes
                  ("presence feed").

                  When read from, the feed will return the current presence
                  status of company (pod) users

                  if it has changed since the last read.


                  Returns the ID of the presence feed to be used in subsequent
                  read operations.
                tags:
                  - Create
                  - Presence
                  - Status
                  - Feed.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
            /v1/presence/feed/{feedId}/read:
              get:
                summary: Read a presence status feed.
                description: >
                  Returns the current presence status of company (pod) users

                  if it has changed since the last read. Returns up to 500
                  records at a time.
                tags:
                  - Read
                  - Presence
                  - Status
                  - Feed.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
            /v1/presence/feed/{feedId}/delete:
              post:
                summary: Delete a presence status feed.
                description: |
                  Returns the ID of the deleted feed.
                tags:
                  - Delete
                  - Presence
                  - Status
                  - Feed.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
            /v3/room/create:
              post:
                summary: Create a new chatroom.
                description: >
                  Create a new chatroom.


                  If no  attributes are specified, the room is created as a
                  private chatroom.
                tags:
                  - Create
                  - New
                  - Chatroom.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
            /v3/room/search:
              post:
                summary: Search rooms according to the specified criteria.
                tags:
                  - Search
                  - Rooms
                  - According
                  - To
                  - The
                  - Specified
                  - Criteria.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
            /v3/room/{id}/info:
              get:
                summary: Get information about a partcular chatroom.
                tags:
                  - Get
                  - Information
                  - About
                  - Partcular
                  - Chatroom.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
            /v1/room/{id}/setActive:
              post:
                summary: >-
                  Deactivate or reactivate a chatroom. At creation, a new
                  chatroom is active.
                tags:
                  - Deactivate
                  - Or
                  - Reactivate
                  - Chatroom.
                  - At
                  - Creation,
                  - New
                  - Chatroom
                  - Is
                  - Active.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
            /v3/room/{id}/update:
              post:
                summary: Update the attributes of an existing chatroom.
                tags:
                  - Update
                  - The
                  - Attributes
                  - Of
                  - An
                  - Existing
                  - Chatroom.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
            /v1/room/{id}/membership/add:
              post:
                summary: Adds new member to an existing room.
                tags:
                  - Adds
                  - New
                  - Member
                  - To
                  - An
                  - Existing
                  - Room.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
            /v1/room/{id}/membership/remove:
              post:
                summary: Removes member from an existing room.
                tags:
                  - Removes
                  - Member
                  - From
                  - An
                  - Existing
                  - Room.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
            /v1/room/{id}/membership/promoteOwner:
              post:
                summary: Promotes user to owner.
                tags:
                  - Promotes
                  - User
                  - To
                  - Owner.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
            /v1/room/{id}/membership/demoteOwner:
              post:
                summary: Demotes room owner.
                tags:
                  - Demotes
                  - Room
                  - Owner.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
            /v2/room/{id}/membership/list:
              get:
                summary: Lists current members of an existing room.
                tags:
                  - Lists
                  - Current
                  - Members
                  - Of
                  - An
                  - Existing
                  - Room.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
            /v2/sessioninfo:
              get:
                summary: Get information about the current user's session.
                tags:
                  - Get
                  - Information
                  - About
                  - The
                  - Current
                  - User's
                  - Session.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
            /v2/user:
              get:
                summary: Get user information
                tags:
                  - Get
                  - User
                  - Information
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
            /v3/users:
              get:
                summary: |
                  Search users by emails or ids.
                  Only one of the search lists should be informed at a time.
                  Search lists may containt up to 100 elements.
                tags:
                  - Search
                  - Users
                  - By
                  - Emails
                  - Or
                  - |
                    Ids.
                  - Only
                  - One
                  - Of
                  - The
                  - Lists
                  - Should
                  - Be
                  - Informed
                  - At
                  - |
                    Time.
                  - May
                  - Containt
                  - Up
                  - To
                  - '100'
                  - |
                    Elements.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
            /v1/user/presence/register:
              post:
                summary: Register interest in a user's presence status
                tags:
                  - Register
                  - Interest
                  - In
                  - User's
                  - Presence
                  - Status
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
            /v2/user/presence:
              get:
                summary: Get presence information about the requesting user.
                tags:
                  - Get
                  - Presence
                  - Information
                  - About
                  - The
                  - Requesting
                  - User.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
              post:
                summary: Set the presence of the requesting user.
                tags:
                  - Set
                  - The
                  - Presence
                  - Of
                  - Requesting
                  - User.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
            /v3/user/{uid}/presence:
              get:
                summary: Get presence information about a particular user.
                tags:
                  - Get
                  - Presence
                  - Information
                  - About
                  - Particular
                  - User.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
            /v2/users/presence:
              get:
                summary: Get presence information about all company (pod) users.
                description: >
                  The returned data is taken from the in-memory cache for
                  performance

                  reasons which means inactive users may be omitted from the
                  response.


                  All non-inactive users WILL be returned and some inactive
                  users MAY

                  be included. Any omitted user IS inactive.


                  Returned records are sorted by user ID, ascending.


                  This method is expensive. It pulls ALL records from the cache,
                  sorts them and then only uses a subset.

                  For large numbers of users, this can be very inefficient both
                  due to sorting

                  and due to the cache being distributed across many nodes.


                  Addiionally, there is the potential to miss users if they
                  become active

                  after the page in which their user ID falls has already been
                  read by the client.

                  To avoid this situation, a presence feed should be created
                  (and optionally read from)

                  first to capture presence changes of users who get reactivated
                  during a paged call to this endpoint.
                tags:
                  - Get
                  - Presence
                  - Information
                  - About
                  - All
                  - Company
                  - (pod)
                  - Users.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
            /v3/user/presence:
              post:
                summary: Set presence information for a particular user.
                tags:
                  - Set
                  - Presence
                  - Information
                  - For
                  - Particular
                  - User.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
            /v1/user/search:
              post:
                summary: Search for users by name or email address
                tags:
                  - Search
                  - For
                  - Users
                  - By
                  - Name
                  - Or
                  - Email
                  - Address
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
            /v1/streams/list:
              post:
                summary: >
                  Retrieve a list of all streams of which the requesting user is
                  a member,

                  sorted by creation date (ascending).
                tags:
                  - Retrieve
                  - List
                  - Of
                  - All
                  - Streams
                  - Which
                  - The
                  - Requesting
                  - User
                  - Is
                  - |-
                    Member,
                    sorted
                  - By
                  - Creation
                  - Date
                  - |
                    (ascending).
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
            /v1/admin/user/{uid}/streams/list:
              post:
                summary: |
                  Retrieve a list of all streams of which this user is a member,
                  sorted by creation date (ascending). Since SBE 20.16.
                tags:
                  - Retrieve
                  - List
                  - Of
                  - All
                  - Streams
                  - Which
                  - This
                  - User
                  - Is
                  - |-
                    Member,
                    sorted
                  - By
                  - Creation
                  - Date
                  - (ascending).
                  - Since
                  - |
                    20.16.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
            /v2/streams/{sid}/info:
              get:
                summary: Get information about a partcular stream.
                tags:
                  - Get
                  - Information
                  - About
                  - Partcular
                  - Stream.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
            /v1/streams/{sid}/attachments:
              get:
                summary: Get attachments in a particular stream.
                tags:
                  - Get
                  - Attachments
                  - In
                  - Particular
                  - Stream.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
            /v1/admin/app/entitlement/list:
              get:
                summary: Get the list of application entitlements for the company
                tags:
                  - Get
                  - The
                  - List
                  - Of
                  - Application
                  - Entitlements
                  - For
                  - Company
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
              post:
                summary: Update the application entitlements for the company
                tags:
                  - Update
                  - The
                  - Application
                  - Entitlements
                  - For
                  - Company
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
            /v1/admin/disclaimer/{did}:
              get:
                summary: Get a disclaimer by disclaimer id
                tags:
                  - Get
                  - Disclaimer
                  - By
                  - Id
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
            /v1/admin/disclaimer/list:
              get:
                summary: List all disclaimers for the company (pod)
                tags:
                  - List
                  - All
                  - Disclaimers
                  - For
                  - The
                  - Company
                  - (pod)
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
            /v1/admin/disclaimer/{did}/users:
              get:
                summary: List all users assigned to this disclaimer
                tags:
                  - List
                  - All
                  - Users
                  - Assigned
                  - To
                  - This
                  - Disclaimer
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
            /v1/admin/group/list:
              get:
                summary: Get a list of all Information Barrier Groups
                tags:
                  - Get
                  - List
                  - Of
                  - All
                  - Information
                  - Barrier
                  - Groups
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
            /v1/admin/group/{gid}/membership/list:
              get:
                summary: Get the list of userids in this Information Barrier Group
                tags:
                  - Get
                  - The
                  - List
                  - Of
                  - Userids
                  - In
                  - This
                  - Information
                  - Barrier
                  - Group
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
            /v1/admin/group/{gid}/membership/add:
              post:
                summary: Add members to an Information Barrier group.
                tags:
                  - Add
                  - Members
                  - To
                  - An
                  - Information
                  - Barrier
                  - Group.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
            /v1/admin/group/{gid}/membership/remove:
              post:
                summary: Remove members from an Information Barrier group
                tags:
                  - Remove
                  - Members
                  - From
                  - An
                  - Information
                  - Barrier
                  - Group
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
            /v1/admin/im/create:
              post:
                summary: >-
                  Create a new single or multi party instant message
                  conversation
                description: >
                  At least two user IDs must be provided or

                  an error response will be sent.


                  The caller is not included in the members of the

                  created chat.


                  Duplicate users will be included in the membership of the chat
                  but

                  the duplication will be silently ignored.


                  If there is an existing IM conversation with the same set of
                  participants then

                  the id of that existing stream will be returned.
                tags:
                  - Create
                  - New
                  - Single
                  - Or
                  - Multi
                  - Party
                  - Instant
                  - Message
                  - Conversation
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
            /v1/admin/messagesuppression/{id}/suppress:
              post:
                summary: Suppress a message
                tags:
                  - Suppress
                  - Message
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
            /v1/admin/policy/list:
              get:
                summary: Get all Information Policies
                tags:
                  - Get
                  - All
                  - Information
                  - Policies
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
            /v1/admin/room/{id}/setActive:
              post:
                summary: Deactivate or reactivate a chatroom via AC Portal.
                tags:
                  - Deactivate
                  - Or
                  - Reactivate
                  - Chatroom
                  - Via
                  - Portal.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
            /v1/admin/room/{id}/membership/list:
              get:
                summary: Lists current and previous members of an existing room.
                tags:
                  - Lists
                  - Current
                  - And
                  - Previous
                  - Members
                  - Of
                  - An
                  - Existing
                  - Room.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
            /v1/admin/room/{id}/membership/add:
              post:
                summary: Add a member to an existing room.
                tags:
                  - Add
                  - Member
                  - To
                  - An
                  - Existing
                  - Room.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
            /v1/admin/room/{id}/membership/remove:
              post:
                summary: Remove a member from a room.
                tags:
                  - Remove
                  - Member
                  - From
                  - Room.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
            /v2/admin/user/list:
              get:
                summary: Retrieve a list of all users in the company (pod)
                tags:
                  - Retrieve
                  - List
                  - Of
                  - All
                  - Users
                  - In
                  - The
                  - Company
                  - (pod)
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
            /v1/admin/user/find:
              post:
                summary: Find a user based on attributes
                tags:
                  - Find
                  - User
                  - Based
                  - 'On'
                  - Attributes
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
            /v1/admin/user/{uid}/roles/add:
              post:
                summary: Add a role to a user
                tags:
                  - Add
                  - Role
                  - To
                  - User
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
            /v1/admin/user/{uid}/roles/remove:
              post:
                summary: Remove a role from a user
                tags:
                  - Remove
                  - Role
                  - From
                  - User
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
            /v1/admin/user/{uid}/app/entitlement/list:
              get:
                summary: Get the list of application entitlements for this user
                tags:
                  - Get
                  - The
                  - List
                  - Of
                  - Application
                  - Entitlements
                  - For
                  - This
                  - User
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
              post:
                summary: Update the application entitlements for this user
                tags:
                  - Update
                  - The
                  - Application
                  - Entitlements
                  - For
                  - This
                  - User
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
              patch:
                summary: >-
                  Update unique entitlement of an app for this user. Entitlement
                  can be installation, visibility or product
                tags:
                  - Update
                  - Unique
                  - Entitlement
                  - Of
                  - An
                  - App
                  - For
                  - This
                  - User.
                  - Can
                  - Be
                  - Installation,
                  - Visibility
                  - Or
                  - Product
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
            /v1/admin/user/{uid}/avatar:
              get:
                summary: Get the URL of the avatar of a particular user
                tags:
                  - Get
                  - The
                  - Of
                  - Avatar
                  - Particular
                  - User
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
            /v1/admin/user/{uid}/avatar/update:
              post:
                summary: Update the avatar of a particular user
                tags:
                  - Update
                  - The
                  - Avatar
                  - Of
                  - Particular
                  - User
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
            /v1/admin/user/{uid}/disclaimer:
              get:
                summary: Get the disclaimer assigned to a user
                tags:
                  - Get
                  - The
                  - Disclaimer
                  - Assigned
                  - To
                  - User
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
              delete:
                summary: Unassign a disclaimer from a user
                tags:
                  - Unassign
                  - Disclaimer
                  - From
                  - User
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
            /v1/admin/user/{uid}/disclaimer/update:
              post:
                summary: Assign a disclaimer to a user
                tags:
                  - Assign
                  - Disclaimer
                  - To
                  - User
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
            /v1/admin/user/{uid}/delegates:
              get:
                summary: Get the delegates assigned to a user
                tags:
                  - Get
                  - The
                  - Delegates
                  - Assigned
                  - To
                  - User
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
            /v1/admin/user/{uid}/delegates/update:
              post:
                summary: Update the delegates assigned to a user
                tags:
                  - Update
                  - The
                  - Delegates
                  - Assigned
                  - To
                  - User
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
            /v1/admin/user/{uid}/features:
              get:
                summary: >-
                  Get the list of Symphony feature entitlements enabled for a
                  particular user
                tags:
                  - Get
                  - The
                  - List
                  - Of
                  - Symphony
                  - Feature
                  - Entitlements
                  - Enabled
                  - For
                  - Particular
                  - User
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
            /v1/admin/user/{uid}/features/update:
              post:
                summary: >-
                  Update the list of Symphony feature entitlements for a
                  particular user
                tags:
                  - Update
                  - The
                  - List
                  - Of
                  - Symphony
                  - Feature
                  - Entitlements
                  - For
                  - Particular
                  - User
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
            /v1/user/{uid}/follow:
              post:
                summary: Make a list of users start following a specific user
                tags:
                  - Make
                  - List
                  - Of
                  - Users
                  - Start
                  - Following
                  - Specific
                  - User
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
            /v1/user/{uid}/unfollow:
              post:
                summary: Make a list of users unfollowing a specific user
                tags:
                  - Make
                  - List
                  - Of
                  - Users
                  - Unfollowing
                  - Specific
                  - User
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
            /v1/user/{uid}/followers:
              get:
                summary: Returns the list of followers for a specific user
                tags:
                  - Returns
                  - The
                  - List
                  - Of
                  - Followers
                  - For
                  - Specific
                  - User
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
            /v1/user/{uid}/following:
              get:
                summary: Returns the list of users that a specific user is following
                tags:
                  - Returns
                  - The
                  - List
                  - Of
                  - Users
                  - That
                  - Specific
                  - User
                  - Is
                  - Following
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
                  - Following
            /v1/user/manifest/own:
              post:
                summary: Update own service account manifest
                tags:
                  - Update
                  - Own
                  - Service
                  - Account
                  - Manifest
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
                  - Following
                  - Manifest
                  - Own
              get:
                summary: Get own service account manifest
                tags:
                  - Get
                  - Own
                  - Service
                  - Account
                  - Manifest
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
                  - Following
                  - Manifest
                  - Own
            /v1/admin/user/{uid}/status:
              get:
                summary: Get the status, active or inactive, for a particular user
                tags:
                  - Get
                  - The
                  - Status,
                  - Active
                  - Or
                  - Inactive,
                  - For
                  - Particular
                  - User
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
                  - Following
                  - Manifest
                  - Own
                  - Status
            /v1/admin/user/{uid}/status/update:
              post:
                summary: Update the status of a particular user
                tags:
                  - Update
                  - The
                  - Status
                  - Of
                  - Particular
                  - User
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
                  - Following
                  - Manifest
                  - Own
                  - Status
            /v2/admin/streams/list:
              post:
                summary: >
                  Retrieve all the streams across the enterprise where the
                  membership of the stream has been modified between a given
                  time range
                tags:
                  - Retrieve
                  - All
                  - The
                  - Streams
                  - Across
                  - Enterprise
                  - Where
                  - Membership
                  - Of
                  - Stream
                  - Has
                  - Been
                  - Modified
                  - Between
                  - Given
                  - Time
                  - |
                    Range
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
                  - Following
                  - Manifest
                  - Own
                  - Status
            /v1/admin/stream/{id}/membership/list:
              get:
                summary: >-
                  List the current members of an existing stream.  The stream
                  can be of type IM, MIM, or ROOM
                tags:
                  - List
                  - The
                  - Current
                  - Members
                  - Of
                  - An
                  - Existing
                  - Stream.
                  - Stream
                  - Can
                  - Be
                  - Type
                  - M,
                  - Or
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
                  - Following
                  - Manifest
                  - Own
                  - Status
                  - Stream
            /v1/admin/system/features/list:
              get:
                summary: Get the full set of Symphony features available for this pod
                tags:
                  - Get
                  - The
                  - Full
                  - Set
                  - Of
                  - Symphony
                  - Features
                  - Available
                  - For
                  - This
                  - Pod
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
                  - Following
                  - Manifest
                  - Own
                  - Status
                  - Stream
                  - System
            /v1/admin/system/protocols/list:
              get:
                summary: Get a list of all URI protocols supported by the company (pod)
                tags:
                  - Get
                  - List
                  - Of
                  - All
                  - Protocols
                  - Supported
                  - By
                  - The
                  - Company
                  - (pod)
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
                  - Following
                  - Manifest
                  - Own
                  - Status
                  - Stream
                  - System
                  - Protocols
            /v2/system/protocols:
              get:
                summary: Get a list of URI protocols supported by the company (pod)
                tags:
                  - Get
                  - List
                  - Of
                  - Protocols
                  - Supported
                  - By
                  - The
                  - Company
                  - (pod)
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
                  - Following
                  - Manifest
                  - Own
                  - Status
                  - Stream
                  - System
                  - Protocols
            /v1/admin/system/protocols:
              post:
                summary: Add an entry to URI protocols supported by the company (pod)
                tags:
                  - Add
                  - An
                  - Entry
                  - To
                  - Protocols
                  - Supported
                  - By
                  - The
                  - Company
                  - (pod)
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
                  - Following
                  - Manifest
                  - Own
                  - Status
                  - Stream
                  - System
                  - Protocols
            /v1/admin/system/protocols/{scheme}:
              delete:
                summary: >-
                  Remove an entry from URI protocols supported by the company
                  (pod)
                tags:
                  - Remove
                  - An
                  - Entry
                  - From
                  - Protocols
                  - Supported
                  - By
                  - The
                  - Company
                  - (pod)
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
                  - Following
                  - Manifest
                  - Own
                  - Status
                  - Stream
                  - System
                  - Protocols
                  - Scheme
            /v1/admin/system/roles/list:
              get:
                summary: Get a list of all roles available in the company (pod)
                tags:
                  - Get
                  - List
                  - Of
                  - All
                  - Roles
                  - Available
                  - In
                  - The
                  - Company
                  - (pod)
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
                  - Following
                  - Manifest
                  - Own
                  - Status
                  - Stream
                  - System
                  - Protocols
                  - Scheme
            /v1/message/{mid}/status:
              get:
                summary: Get the read status of a particular message.
                tags:
                  - Get
                  - The
                  - Read
                  - Status
                  - Of
                  - Particular
                  - Message.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
                  - Following
                  - Manifest
                  - Own
                  - Status
                  - Stream
                  - System
                  - Protocols
                  - Scheme
                  - Message
                  - Mid
            /v1/admin/app/create:
              post:
                summary: Creates a new app
                tags:
                  - Creates
                  - New
                  - App
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
                  - Following
                  - Manifest
                  - Own
                  - Status
                  - Stream
                  - System
                  - Protocols
                  - Scheme
                  - Message
                  - Mid
            /v1/admin/app/{id}/update:
              post:
                summary: Updates a app
                tags:
                  - Updates
                  - App
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
                  - Following
                  - Manifest
                  - Own
                  - Status
                  - Stream
                  - System
                  - Protocols
                  - Scheme
                  - Message
                  - Mid
            /v1/admin/app/{id}/delete:
              post:
                summary: Deletes a app
                tags:
                  - Deletes
                  - App
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
                  - Following
                  - Manifest
                  - Own
                  - Status
                  - Stream
                  - System
                  - Protocols
                  - Scheme
                  - Message
                  - Mid
            /v1/admin/app/{id}/get:
              get:
                summary: Gets a app
                tags:
                  - Gets
                  - App
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
                  - Following
                  - Manifest
                  - Own
                  - Status
                  - Stream
                  - System
                  - Protocols
                  - Scheme
                  - Message
                  - Mid
            /v1/admin/messages:
              post:
                summary: Fetch message details
                tags:
                  - Fetch
                  - Message
                  - Details
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
                  - Following
                  - Manifest
                  - Own
                  - Status
                  - Stream
                  - System
                  - Protocols
                  - Scheme
                  - Message
                  - Mid
                  - Messages
            /v2/admin/user/create:
              post:
                summary: Create a new V2 User
                tags:
                  - Create
                  - New
                  - V2
                  - User
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
                  - Following
                  - Manifest
                  - Own
                  - Status
                  - Stream
                  - System
                  - Protocols
                  - Scheme
                  - Message
                  - Mid
                  - Messages
            /v2/admin/user/{uid}/update:
              post:
                summary: Update an existing V2 User
                tags:
                  - Update
                  - An
                  - Existing
                  - V2
                  - User
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
                  - Following
                  - Manifest
                  - Own
                  - Status
                  - Stream
                  - System
                  - Protocols
                  - Scheme
                  - Message
                  - Mid
                  - Messages
            /v2/admin/user/{uid}:
              get:
                summary: Retrieve V2 User details for a particular user
                tags:
                  - Retrieve
                  - V2
                  - User
                  - Details
                  - For
                  - Particular
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
                  - Following
                  - Manifest
                  - Own
                  - Status
                  - Stream
                  - System
                  - Protocols
                  - Scheme
                  - Message
                  - Mid
                  - Messages
            /v1/files/allowedTypes:
              get:
                summary: Get supported attachment types for the pod
                tags:
                  - Get
                  - Supported
                  - Attachment
                  - Types
                  - For
                  - The
                  - Pod
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
                  - Following
                  - Manifest
                  - Own
                  - Status
                  - Stream
                  - System
                  - Protocols
                  - Scheme
                  - Message
                  - Mid
                  - Messages
                  - Types
            /file_ext/v1/allowed_extensions:
              get:
                summary: Allows iteration of all file extensions supported for upload
                description: >
                  Provides a RESTful API to iterate all file extensions
                  configured by the tenant admin

                  that are allowed for the upload.  Pagination of this list is
                  managed through a

                  combination of the optional request parameters and
                  service-side managed maximums.


                  Pagination of the results is provided through the before or
                  after input paramters

                  and presented through the opaque cursor values provided as
                  output from a previous

                  response.  Only one of before or after or neither may be
                  provided.


                  DO NOT store cursors. Cursors can quickly become invalid if
                  items are added or deleted.

                  Use them only during a short-period of time that you are
                  traversing the list.
                tags:
                  - Allows
                  - Iteration
                  - Of
                  - All
                  - File
                  - Extensions
                  - Supported
                  - For
                  - Upload
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
                  - Following
                  - Manifest
                  - Own
                  - Status
                  - Stream
                  - System
                  - Protocols
                  - Scheme
                  - Message
                  - Mid
                  - Messages
                  - Types
                  - File_ext
                  - Allowed_extensions
            /file_ext/v1/allowed_extensions/{extension}:
              put:
                summary: >-
                  Allows replacement or creation of a specific file extension
                  supported for upload
                description: >
                  Provides a method to create or replace a specific file
                  extension configured for upload

                  support via an admin. The API treats the file extension in the
                  path case-insensitively

                  by converting it to lowecase.
                tags:
                  - Allows
                  - Replacement
                  - Or
                  - Creation
                  - Of
                  - Specific
                  - File
                  - Extension
                  - Supported
                  - For
                  - Upload
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
                  - Following
                  - Manifest
                  - Own
                  - Status
                  - Stream
                  - System
                  - Protocols
                  - Scheme
                  - Message
                  - Mid
                  - Messages
                  - Types
                  - File_ext
                  - Allowed_extensions
                  - Extension
              delete:
                summary: >-
                  Allows deletion of a specific file extension supported for
                  upload
                description: >
                  Provides a method to delete a specific file extension
                  configured for upload

                  support via an admin. The file extension identifying the
                  resource is treated

                  case-insensitively by the API.
                tags:
                  - Allows
                  - Deletion
                  - Of
                  - Specific
                  - File
                  - Extension
                  - Supported
                  - For
                  - Upload
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
                  - Following
                  - Manifest
                  - Own
                  - Status
                  - Stream
                  - System
                  - Protocols
                  - Scheme
                  - Message
                  - Mid
                  - Messages
                  - Types
                  - File_ext
                  - Allowed_extensions
                  - Extension
            /v1/admin/messages/{messageId}/receipts:
              get:
                summary: Fetch receipts details from a specific message.
                tags:
                  - Fetch
                  - Receipts
                  - Details
                  - From
                  - Specific
                  - Message.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
                  - Following
                  - Manifest
                  - Own
                  - Status
                  - Stream
                  - System
                  - Protocols
                  - Scheme
                  - Message
                  - Mid
                  - Messages
                  - Types
                  - File_ext
                  - Allowed_extensions
                  - Extension
                  - Receipts
            /v1/languages:
              get:
                summary: Lists available languages for the pod.
                tags:
                  - Lists
                  - Available
                  - Languages
                  - For
                  - The
                  - Pod.
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
                  - Following
                  - Manifest
                  - Own
                  - Status
                  - Stream
                  - System
                  - Protocols
                  - Scheme
                  - Message
                  - Mid
                  - Messages
                  - Types
                  - File_ext
                  - Allowed_extensions
                  - Extension
                  - Receipts
                  - Languages
            /v1/admin/messages/{messageId}/metadata/relationships:
              get:
                summary: Get the message metadata relationship
                tags:
                  - Get
                  - The
                  - Message
                  - Metadata
                  - Relationship
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
                  - Following
                  - Manifest
                  - Own
                  - Status
                  - Stream
                  - System
                  - Protocols
                  - Scheme
                  - Message
                  - Mid
                  - Messages
                  - Types
                  - File_ext
                  - Allowed_extensions
                  - Extension
                  - Receipts
                  - Languages
                  - Metadata
                  - Relationships
            /v1/admin/user/{userId}/suspension/update:
              put:
                summary: Update the status of suspension of a particular user
                tags:
                  - Update
                  - The
                  - Status
                  - Of
                  - Suspension
                  - Particular
                  - User
                  - V1
                  - Companycert
                  - List
                  - V2
                  - Create
                  - Delete
                  - Print
                  - Get
                  - Update
                  - Issued
                  - By
                  - Podmanaged
                  - Type
                  - Podcert
                  - Connection
                  - Accept
                  - Reject
                  - Id
                  - Info
                  - User
                  - Uid
                  - Remove
                  - Im
                  - Presence
                  - Feed
                  - Read
                  - V3
                  - Room
                  - Search
                  - Active
                  - Membership
                  - Add
                  - Owner
                  - Sessioninfo
                  - Users
                  - Register
                  - Streams
                  - Admin
                  - Sid
                  - Attachments
                  - App
                  - Entitlement
                  - Disclaimer
                  - Did
                  - Group
                  - Gid
                  - Messagesuppression
                  - Suppress
                  - Policy
                  - Find
                  - Roles
                  - Avatar
                  - Delegates
                  - Features
                  - Follow
                  - Unfollow
                  - Followers
                  - Following
                  - Manifest
                  - Own
                  - Status
                  - Stream
                  - System
                  - Protocols
                  - Scheme
                  - Message
                  - Mid
                  - Messages
                  - Types
                  - File_ext
                  - Allowed_extensions
                  - Extension
                  - Receipts
                  - Languages
                  - Metadata
                  - Relationships
                  - Suspension
          definitions:
            Error:
              type: object
              properties:
                code:
                  type: integer
                  format: int32
                  example: 401
                message:
                  type: string
                  example: Invalid session
            CompanyCert:
              type: object
              properties:
                pem:
                  type: string
                  description: An X509 certificate in PEM format
                  example: '--BEGIN CERTIFICATE--MIIH/TC...p9DBiB/--END CERTIFICATE--'
                attributes:
                  $ref: '#/definitions/CompanyCertAttributes'
            CompanyCertDetail:
              type: object
              properties:
                companyCertAttributes:
                  $ref: '#/definitions/CompanyCertAttributes'
                companyCertInfo:
                  $ref: '#/definitions/CompanyCertInfo'
                certInfo:
                  $ref: '#/definitions/CertInfo'
            CompanyCertInfoList:
              type: array
              items:
                type: object
                properties:
                  companyCertAttributes:
                    $ref: '#/definitions/CompanyCertAttributes'
                  companyCertInfo:
                    $ref: '#/definitions/CompanyCertInfo'
                example:
                  - companyCertAttributes:
                      name: agentservice
                      type:
                        type: USER
                      status:
                        type: TRUSTED
                    companyCertInfo:
                      fingerPrint: 300a...
                      lastSeen: 0
                      updatedAt: 0
                      updatedBy: 0
                      commonName: agentservice
                      expiryDate: 1781886755000
            CompanyCertType:
              type: object
              properties:
                type:
                  type: string
                  enum:
                    - USERSIGNING
                    - USER
                    - OPERATIONSSIGNING
                    - OPERATIONSUSER
                  example: USER
            CompanyCertTypeList:
              type: array
              items:
                $ref: '#/definitions/CompanyCertType'
            CompanyCertStatus:
              type: object
              properties:
                type:
                  type: string
                  enum:
                    - TRUSTED
                    - KNOWN
                    - REVOKED
                    - DISABLED
                  example: TRUSTED
            CompanyCertAttributes:
              type: object
              properties:
                name:
                  type: string
                  description: Friendly name assigned by administrator
                  example: agentservice
                type:
                  $ref: '#/definitions/CompanyCertType'
                status:
                  $ref: '#/definitions/CompanyCertStatus'
            CompanyCertInfo:
              type: object
              properties:
                fingerPrint:
                  type: string
                  description: Unique identifier
                  example: 300a...
                issuerFingerPrint:
                  type: string
                  description: Unique identifier of issuer cert if known
                  example: 450s...
                lastSeen:
                  type: integer
                  format: int64
                  description: Date when we last saw this certificate presented
                  example: 0
                updatedAt:
                  type: integer
                  format: int64
                  description: Date when this cert was last updated by administrator
                  example: 0
                updatedBy:
                  type: integer
                  format: int64
                  description: User ID of administrator who last updated this cert
                  example: 0
                commonName:
                  type: string
                  description: >-
                    The Symphony account name which this certificate
                    authenticates
                  example: agentservice
                expiryDate:
                  type: integer
                  format: int64
                  description: Expiry date of this cert
                  example: 1781886755000
            CertInfo:
              type: array
              items:
                $ref: '#/definitions/CertInfoItem'
              example:
                - name: Validity
                  attributes:
                    - name: Not Before
                      value: Mon Jan 15 20:56:05 UTC 2018
                    - name: Not After
                      value: Thu Jan 15 20:56:05 UTC 2026
                - name: Public Key
                  attributes:
                    - name: Algorithm
                      value: RSA
                    - name: Format
                      value: X.509
            CertInfoItem:
              type: object
              properties:
                name:
                  type: string
                  example: Public Key
                attributes:
                  type: array
                  items:
                    $ref: '#/definitions/NameValuePair'
                  example:
                    - name: Algorithm
                      value: RSA
                    - name: Format
                      value: X.509
            PodCertificate:
              type: object
              properties:
                certificate:
                  description: Certificate in PEM format
                  type: string
                  example: PEM_CERTIFICATE
            NameValuePair:
              type: object
              properties:
                name:
                  type: string
                  example: Algorithm
                value:
                  type: string
                  example: RSA
            Stream:
              type: object
              properties:
                id:
                  type: string
                  example: xhGxbTcvTDK6EIMMrwdOrX___quztr2HdA
            UserError:
              description: User error information
              type: object
              properties:
                error:
                  type: string
                  description: Error code informing what is wrong
                  example: invalid.format
                email:
                  type: string
                  description: >-
                    Email with error. Only one of the following fields should be
                    present: email or id
                  example: notavalidemail
                id:
                  type: string
                  description: >-
                    Id with error. Only one of the following fields should be
                    present: email or id
                  example: notavalidid
            UserV2:
              description: User record version 2
              type: object
              properties:
                id:
                  type: integer
                  format: int64
                  example: 7696581394433
                emailAddress:
                  type: string
                  format: email
                  example: admin@symphony.com
                firstName:
                  type: string
                  example: Symphony
                lastName:
                  type: string
                  example: Admin
                displayName:
                  type: string
                  example: Symphony Admin
                title:
                  type: string
                  example: Administrator
                company:
                  type: string
                  example: Acme
                username:
                  type: string
                  example: admin@symphony.com
                location:
                  type: string
                  example: California
                accountType:
                  type: string
                  enum:
                    - NORMAL
                    - SYSTEM
                    - SDL
                  example: NORMAL
                avatars:
                  $ref: '#/definitions/AvatarList'
                workPhoneNumber:
                  type: string
                  description: >-
                    Note: only available if the application has the extended
                    user or contact permission
                  example: '+33901020304'
                mobilePhoneNumber:
                  type: string
                  description: >-
                    Note: only available if the application has the extended
                    user or contact permission
                  example: '+33601020304'
                jobFunction:
                  type: string
                  description: >-
                    Note: only available if the application has the extended
                    user or contact permission
                  example: Sales
                department:
                  type: string
                  description: >-
                    Note: only available if the application has the extended
                    user or contact permission
                  example: APIs
                division:
                  type: string
                  description: >-
                    Note: only available if the application has the extended
                    user or contact permission
                  example: Partnerships
                roles:
                  $ref: '#/definitions/StringList'
                  example:
                    - INDIVIDUAL
                    - SUPER_ADMINISTRATOR
            V2UserList:
              description: List of User record version 2
              type: object
              properties:
                users:
                  type: array
                  items:
                    $ref: '#/definitions/UserV2'
                  description: List of all users found with the search
                  example:
                    - id: 15942919536460
                      emailAddress: technicalwriter@symphony.com
                      firstName: Technical
                      lastName: Writer
                      displayName: Technical Writer
                      title: Technical Writer
                      company: Symphony
                      department: Marketing // if internal user
                      username: tw
                      accountType: NORMAL
                      location: France // if internal user
                      mobilePhoneNumber: 33601020304
                      avatars:
                        - size: original
                          url: ../avatars/static/150/default.png
                        - size: small
                          url: ../avatars/static/50/default.png
                    - id: 15942919536461
                      emailAddress: serviceaccount@symphony.com
                      firstName: null
                      lastName: null
                      displayName: Service Account
                      title: null
                      company: pod232
                      department: Marketing // if internal user
                      username: SA
                      location: France // if internal user
                      accountType: SYSTEM
                      avatars:
                        - size: original
                          url: ../avatars/static/150/default.png
                        - size: small
                          url: ../avatars/static/50/default.png
                errors:
                  type: array
                  items:
                    $ref: '#/definitions/UserError'
                  description: List of all errors found with the informed search criteria
                  example:
                    - error: invalid.format
                      email: notavalidemail
                    - error: invalid.format
                      id: 654321
            UserSearchResults:
              type: object
              properties:
                count:
                  description: The total number of users which matched the search criteria.
                  type: integer
                  format: int64
                  example: 1
                skip:
                  description: The number of skipped results.
                  type: integer
                  format: int64
                  example: 0
                limit:
                  description: The number of returned results.
                  type: integer
                  format: int64
                  example: 1
                searchQuery:
                  $ref: '#/definitions/UserSearchQuery'
                users:
                  description: A list of users which matched by the search criteria.
                  type: array
                  items:
                    $ref: '#/definitions/UserV2'
                  example:
                    - null
            UserSearchFilter:
              type: object
              properties:
                accountTypes:
                  $ref: '#/definitions/StringList'
                  description: type of user used to search
                  example: NORMAL
                title:
                  type: string
                  description: user's job title
                  example: Sales Manager
                company:
                  type: string
                  description: company name
                  example: Symphony
                location:
                  type: string
                  description: city of the user's job location
                  example: Marseille
                marketCoverage:
                  type: string
                  description: geographic area the user works with
                  example: EMEA
                responsibility:
                  type: string
                  description: user's responsibility
                  example: BAU
                function:
                  type: string
                  description: user's function
                  example: Trade Management
                instrument:
                  type: string
                  description: higher level instrument for the Asset Classes
                  example: Securities
            UserSearchQuery:
              type: object
              properties:
                query:
                  type: string
                  description: >-
                    search / query term.  This can be firstname, lastname,
                    displayname or email
                  example: jane
                filters:
                  $ref: '#/definitions/UserSearchFilter'
            UserNameList:
              type: array
              items:
                type: object
                $ref: '#/definitions/UserName'
            UserName:
              type: object
              properties:
                username:
                  type: string
                  example: dpayet
            UserIdList:
              type: array
              items:
                type: integer
                format: int64
              example:
                - 7215545058313
                - 7215545078461
            UserId:
              type: object
              properties:
                id:
                  type: integer
                  format: int64
                  example: 7215545058313
            StringId:
              type: object
              properties:
                id:
                  type: string
                  example: xhGxbTcvTDK6EIMMrwdOrX___quztr2HdA
            RoomAttributes:
              type: object
              properties:
                name:
                  type: string
                  description: Room name.
                description:
                  type: string
                  description: Room description.
                membersCanInvite:
                  type: boolean
                  description: >-
                    If true, any chatroom participant can add new participants.
                    If false, only owners can add new participants.
                discoverable:
                  type: boolean
                  description: >-
                    If true, this chatroom (name, description and messages) can
                    be searched and listed by non-participants. If false, only
                    participants can search this room.
            V3RoomAttributes:
              type: object
              properties:
                name:
                  type: string
                  description: Room name.
                  example: API room
                keywords:
                  type: array
                  description: Keywords for search to use to find this room
                  items:
                    $ref: '#/definitions/RoomTag'
                  example:
                    - key: region
                      value: EMEA
                    - key: lead
                      value: Daffy Duck
                description:
                  type: string
                  description: Room description.
                  example: Created via the API
                membersCanInvite:
                  type: boolean
                  description: >-
                    If true, any chatroom participant can add new participants.
                    If false, only owners can add new participants.
                  example: true
                discoverable:
                  type: boolean
                  description: >-
                    If true, this chatroom (name, description and messages) can
                    be searched and listed by non-participants. If false, only
                    participants can search this room.
                  example: false
                public:
                  type: boolean
                  description: >-
                    If true, this is a public chatroom. IF false, a private
                    chatroom.
                  example: false
                readOnly:
                  type: boolean
                  description: If true, only stream owners can send messages.
                  example: false
                copyProtected:
                  type: boolean
                  description: >-
                    If true, clients disable the clipboard copy for content in
                    this stream.
                  example: false
                crossPod:
                  type: boolean
                  description: If true, this room is a cross pod room
                  example: false
                viewHistory:
                  type: boolean
                  description: >-
                    If true, new members can view the room chat history of the
                    room.
                  example: false
                multiLateralRoom:
                  type: boolean
                  description: >-
                    If true, this is a multi lateral room where we can find
                    users belonging to more than 2 companies.
                  example: false
                scheduledMeeting:
                  type: boolean
                  description: If true, this room is for a scheduled meeting.
                  example: false
                subType:
                  type: string
                  description: >-
                    This field is ignored when creating a new room as it was
                    only used for email integration which is now sunset.
                pinnedMessageId:
                  type: string
                  description: >-
                    UrlSafe message id of the pinned message inside the room. To
                    perform unpin operation, send an empty string.
                  example: vd7qwNb6hLoUV0BfXXPC43___oPIvkwJbQ
                groupChat:
                  type: boolean
                  description: >-
                    If true, this room is a group chat. Note: this parameter is
                    ignored for creating rooms. Since SBE 20.16.
                  x-since: 20.16
                  example: false
            RoomSearchCriteria:
              description: >-
                Room Query Object. Used to specify the parameters for room
                search.
              properties:
                query:
                  description: The search query. Matches the room name and description.
                  type: string
                  example: automobile
                labels:
                  description: A list of room tag labels whose values will be queried.
                  type: array
                  items:
                    type: string
                  example:
                    - industry
                active:
                  description: >-
                    Restrict the search to active/inactive rooms. If
                    unspecified, search all rooms.
                  type: boolean
                  example: true
                private:
                  description: >-
                    Restrict the search to private rooms. If unspecified, search
                    all rooms.
                  type: boolean
                  example: true
                owner:
                  $ref: '#/definitions/UserId'
                creator:
                  $ref: '#/definitions/UserId'
                member:
                  $ref: '#/definitions/UserId'
                sortOrder:
                  description: >
                    Sort algorithm to be used. Supports two values: "BASIC"
                    (legacy algorithm)

                    and "RELEVANCE" (enhanced algorithm).
                  type: string
                  enum:
                    - BASIC
                    - RELEVANCE
                  example: RELEVANCE
              required:
                - query
            V2RoomSearchCriteria:
              description: >-
                Room Query Object. Used to specify the parameters for room
                search.
              allOf:
                - $ref: '#/definitions/RoomSearchCriteria'
                - type: object
                  properties:
                    subType:
                      description: >-
                        Restrict the search to the specific room subtype. Valid
                        values are: EMAIL
                      type: string
                      example: EMAIL
            V3RoomSearchResults:
              description: A list of search results and counts per search parameter.
              properties:
                count:
                  description: The total number of rooms matched by the search.
                  type: integer
                  format: int64
                  example: 2
                skip:
                  description: The number of skipped results.
                  type: integer
                  example: 0
                limit:
                  description: The number of returned results.
                  type: integer
                  example: 10
                query:
                  $ref: '#/definitions/V2RoomSearchCriteria'
                rooms:
                  description: A list of rooms matched by the query.
                  type: array
                  items:
                    $ref: '#/definitions/V3RoomDetail'
                  example:
                    - roomAttributes:
                        name: Automobile Industry Room
                        description: Room to discuss car companies
                        membersCanInvite: true
                        readOnly: false
                        copyProtected: false
                        crossPod: false
                        viewHistory: false
                        public: false
                        multiLateralRoom: false
                      roomSystemInfo:
                        id: tzwvAZIdDMG3ZPRxv+xsgH///qr+JJkWdA==
                        creationDate: 1464615003895
                        createdByUserId: 7696581411197
                        active: true
                    - roomAttributes:
                        name: Tesla Room
                        keywords:
                          - key: industry
                            value: automobile
                        description: Discussions on TSLA
                        membersCanInvite: true
                        readOnly: false
                        copyProtected: false
                        crossPod: false
                        viewHistory: false
                        public: false
                        multiLateralRoom: false
                      roomSystemInfo:
                        id: o6UkQ1TEmU0Tf/DHUlZrCH///qr+JQowdA==
                        creationDate: 1464614974947
                        createdByUserId: 7696581411197
                        active: true
                facetedMatchCount:
                  description: Detailed counts of matched rooms per search criterion.
                  type: array
                  items:
                    $ref: '#/definitions/FacetedMatchCount'
                  example:
                    - facet: industry
                      count: 1
            RoomTag:
              description: >-
                Room Tag object. A key:value pair describing additional
                properties of the room.
              properties:
                key:
                  description: A unique label of the Tag.
                  type: string
                  example: region
                value:
                  description: The value of this Tag's label.
                  type: string
                  example: EMEA
              required:
                - key
                - value
            FacetedMatchCount:
              description: An object respresenting the result count of faceted search.
              properties:
                facet:
                  description: The matched query.
                  type: string
                count:
                  description: The result count.
                  type: integer
            RoomSystemInfo:
              type: object
              properties:
                id:
                  type: string
                  example: bjHSiY4iz3ar4iIh6-VzCX___peoM7cPdA
                creationDate:
                  type: integer
                  format: int64
                  description: >-
                    The datetime when the stream was originally created.
                    Milliseconds since Jan 1 1970.
                  example: 1547661232368
                createdByUserId:
                  type: integer
                  format: int64
                  example: 14362370637825
                active:
                  type: boolean
                  description: >-
                    If false, no messages can be sent in this stream, and
                    membership is locked.
                  example: true
            ImmutableRoomAttributes:
              type: object
              description: >-
                These attributes cannot be changed once the room has been
                created
              properties:
                public:
                  type: boolean
                  description: >-
                    If true, this is a public chatroom. IF false, a private
                    chatroom.
                readOnly:
                  type: boolean
                  description: If true, only stream owners can send messages.
                copyProtected:
                  type: boolean
                  description: >-
                    If true, clients disable the clipboard copy for content in
                    this stream.
            RoomDetail:
              type: object
              properties:
                roomAttributes:
                  $ref: '#/definitions/RoomAttributes'
                roomSystemInfo:
                  $ref: '#/definitions/RoomSystemInfo'
                immutableRoomAttributes:
                  $ref: '#/definitions/ImmutableRoomAttributes'
            V3RoomDetail:
              type: object
              properties:
                roomAttributes:
                  $ref: '#/definitions/V3RoomAttributes'
                roomSystemInfo:
                  $ref: '#/definitions/RoomSystemInfo'
                groups:
                  description: List of groups (aka SDLs) that were added to the room.
                  type: array
                  items:
                    $ref: '#/definitions/GroupItem'
                  example:
                    - id: 68719476744
                      addedBy: 68719476743
            GroupItem:
              type: object
              properties:
                id:
                  description: The ID of the added group (aka SDL).
                  type: integer
                  format: int64
                  example: 68719476744
                addedBy:
                  description: The user ID who added the group to the room.
                  type: integer
                  format: int64
                  example: 68719476743
            SuccessResponse:
              type: object
              properties:
                format:
                  type: string
                  enum:
                    - TEXT
                    - XML
                  example: TEXT
                message:
                  type: string
                  example: Success
            AvatarUpdate:
              type: object
              properties:
                image:
                  description: Base64 encoded image. Original image must be less than 2MB.
                  type: string
                  example: >-
                    iVBORw0KGgoAAAANSUhEUgAAAJgAAAAoCAMAAAA11sNmAAAAGXRFWHRTb2Z0d2FyZQBBZG9iZSBJbWFnZVJlYWR5ccllPAAAAX1QTFRFAAAAVVVVZmZmc8bmd3d3jMyMmZmZ+cxA////VVVVZmZmc8bmd3d3jMyM8oCZ+cxA////VVVVZmZmc8bmd3d3jMyM////VVVVZmZmc8bmd3d3jMyMmZmZ8oCZ+cxA////ZmZmjMyM////VVVVd3d3jMyM+cxA////VVVVZmZmc8bmd3d3jMyMmZmZnMyB8oCZ+cxA////ZmZmc8bmd3d3jMyMmZmZ+cxA////d3d3jMyM8oCZ+cxA////VVVVZmZmdm1RjMyM8oCZ+cxA////ZmZmmZmZ+cxA////W1tbZmZmc8bmdpGcd3d3jMyMmZmZ8oCZ////d3d3jMyMmZmZx3iJ+cxA////VVVVZmZmc8bmd3d3jMyMuIOVyqpG////VVVVZmZmbW1td3d3jMyMmZmZ+cxA////VVVVX1xUZmZmb46ac8bmdZ+vd3d3fnNQjMyMkpeGlqaWmJyYmZmZnYlMp5FLsZhJvJ9Iz3qM0K5F78VB8oCZ+cxA////9laq9wAAAGh0Uk5TABAQEBAQEBAQICAgICAgICAwMDAwMDBAQEBAQEBAQEBQUFBgYGBgYHBwcHBwcHBwcHCAgICAgICAj4+Pj4+fn5+fn5+fr6+vr7+/v7+/v7+/v8/Pz8/Pz9/f39/f39/f7+/v7+/v7+/qia/hAAADQ0lEQVRYw+2Xa1fTQBCGV0WJCBIvxEq10YoEVNQoaLxURKNWUHRRqYgaUSC1QkWsNzT7252Z3W1TWpCjX+I5fT/ksrM782T2Tc4JYy211NL/oJ50Ot2TRLD5FdTkma6kgU2uSB1PGtiY5HqZuK0ckWAjiQNLS7CdiQPrIq6xpGHtGnr0eRXA0gnjGlqoVCoA9kTe9rfXQob1r8ntv1mUmjlGYBUJdhJv2u9FlzWVHwohAt9kBuc+Dfk8zxjnWRnn3GHM4lKuAUM5nsMIjNETOQVM4NJstQpCzKxL10TjpdJ4B5zvEtg8Wj+zGEVRtwxjVpLFckIAA8sKAVWECBGCeUJ40BI9qwCDXHBqkxDYKT8WwVWWDDFMh5QOpWtURwk0dwE8toBgV2HoeoQ6T2GL6rJsAZ7OCBAGjgUqIbAvptBgNggo/XVgMJQ3mZmHk1wVGArMCPEajrxpwwZLpJkUO4JgXax7mriiaaay1xyWRQhPjsgmAoQGk9uCVeJg1bo+TafW6enxdI26U1Ia3X6psjrJ+hcjJQpjRwLOPYf2DZ7blp2iEhxz14FxCRZ4IB/BbLlflMjDVQVsqprOKZ3HNrKY0tzg09Wzt4Ho59r3NThlKO6E0iLkDTNUe4EloLAb4FGCIUuebrg2HIB5ihgXEJgNZI4Ci6XbDKxUevvp9bcvH98Xi8WvVTAo6no5yBbgtSt0B6AEAoRGM/PXOuZUd0qDgUeFxnWFfEGaaX8q9eyH0qsP998USTczmUx7/BPkqlSByOs6NrwY8EJpMPxa+E51P5XHTL1VLj0RDlm0B6w+XVPd+kV6fHRieWrbwHMEO6FjDr5TMTCuLYElctjGOo+x9WC4r0hrh9RyGsrWwPhGDiOdk1js4tJy+Qpjh24Ui/t0LIceJ/PkG8GM0P4jGPqogFYILQ2GxtsS2F7CYoeXAKzcCwO7B2rBrPrCcqMRrOadjcHgCy/NZ8VW+VsDY9cAi+14QWDv2tZHLcfzXP2tsWxTvRK2oS9gxLBjHrZsmm3oKZbreVbdqur0arpNtGeCwMoPk/czcuDUAwArn07gf9IwgpUPJhVsqi2hYLOdiQSb7Uugx3qH+zpZSy211FJNvwFNoXAncdBvawAAAABJRU5ErkJggg==
            Avatar:
              type: object
              properties:
                size:
                  description: The Avatar Size
                  type: string
                  example: original
                url:
                  description: Url of the image
                  type: string
                  example: ../avatars/izcQTdRVFOK_qhCrYeQOpIuHKuZuMk3J88Uz_bShzM8.png
            AvatarList:
              type: array
              items:
                $ref: '#/definitions/Avatar'
              example:
                - size: original
                  url: ../avatars/izcQTdRVFOK_qhCrYeQOpIuHKuZuMk3J88Uz_bShzM8.png
                - size: small
                  url: >-
                    ../avatars/izcQTdRVFOK_qhCrYeQOpIuHKuZuMk3J88Uz_bShzM8_small.png
            UserStatus:
              type: object
              properties:
                status:
                  type: string
                  enum:
                    - ENABLED
                    - DISABLED
                  example: ENABLED
                suspended:
                  type: boolean
                  description: >-
                    An optional attribute indicating whether the user is
                    temporarily suspended or not. Since SBE 20.14.
                  x-since: 20.14
                  example: true
                suspendedUntil:
                  type: integer
                  format: int64
                  description: >-
                    An optional unix timestamp until which the suspension is
                    effective. Since SBE 20.14.
                  x-since: 20.14
                  example: 1601546400
                suspensionReason:
                  type: string
                  description: >-
                    An optional description of the suspension reason. Since SBE
                    20.14.
                  x-since: 20.14
                  example: The user will be OOO due to a mandatory leave
            UserFilter:
              type: object
              properties:
                role:
                  type: string
                  description: The user role
                  example: INDIVIDUAL
                feature:
                  type: string
                status:
                  type: string
                  enum:
                    - ENABLED
                    - DISABLED
            PasswordReset:
              type: object
              properties:
                type:
                  type: string
                  enum:
                    - EMAIL
                  example: EMAIL
            FeatureList:
              type: array
              items:
                $ref: '#/definitions/Feature'
              example:
                - entitlment: canCreatePublicRoom
                  enabled: true
                - entitlment: isExternalRoomEnabled
                  enabled: false
                - entitlment: canUpdateAvatar
                  enabled: true
            Feature:
              description: Entitlement feature record.
              type: object
              properties:
                entitlment:
                  type: string
                  example: canCreatePublicRoom
                enabled:
                  type: boolean
                  description: Whether this entitlement is enabled for the user.
                  example: true
            Group:
              description: Information Barrier Group record.
              type: object
              properties:
                id:
                  type: string
                  example: 571db1f2e4b027c4f055a594
                name:
                  type: string
                  example: Group 1
                active:
                  type: boolean
                  example: true
                memberCount:
                  type: integer
                  format: int32
                  example: 1
                policies:
                  type: array
                  items:
                    type: string
                  example:
                    - 571db2e4e4b012df6341f393
                createdDate:
                  type: integer
                  format: int64
                  example: 1461563890135
                modifiedDate:
                  type: integer
                  format: int64
                  example: 1461563926812
            Product:
              description: Application Product
              type: object
              required:
                - name
                - type
                - subscribed
              properties:
                appId:
                  type: string
                  description: App ID for the Product
                  maxLength: 256
                  minLength: 1
                  example: selerity
                name:
                  type: string
                  minLength: 1
                  maxLength: 50
                  description: Product Name
                  example: Premium
                sku:
                  type: string
                  minLength: 1
                  maxLength: 100
                  description: Product SKU
                  example: AcDccU53SsY
                subscribed:
                  type: boolean
                  description: indicate whether the product is subscribed or not
                  example: false
                type:
                  type: string
                  description: Product Type (default or premium)
                  example: premium
            ProductList:
              type: array
              items:
                $ref: '#/definitions/Product'
              example:
                - appId: selerity
                  name: Standard
                  subscribed: true
                  type: default
                - appId: selerity
                  name: Premium
                  sku: AcDccU53SsY
                  subscribed: false
                  type: premium
            PolicyList:
              type: array
              items:
                $ref: '#/definitions/Policy'
              example:
                - id: 56e9df05e4b00737e3d3b82d
                  policyType: BLOCK
                  active: true
                  groups:
                    - 56e9def8e4b0b406041812e6
                    - 56e9deffe4b0b406041812e7
                  createdDate: 1458167557358
                  modifiedDate: 1458330606752
                - id: 571cd64de4b042aaf06d2d8b
                  policyType: BLOCK
                  active: true
                  groups:
                    - 571cd646e4b042aaf06d2d84
                    - 571cd64ce4b042aaf06d2d8a
                  createdDate: 1461507661146
                  modifiedDate: 1461507661146
            Policy:
              description: Information Barrier Policy record.
              type: object
              properties:
                id:
                  type: string
                  example: 56e9df05e4b00737e3d3b82d
                policyType:
                  type: string
                  enum:
                    - BLOCK
                    - ALLOW
                  example: BLOCK
                active:
                  type: boolean
                  example: true
                memberCount:
                  type: integer
                  format: int32
                  example: 3
                groups:
                  type: array
                  items:
                    type: string
                  example:
                    - 56e9deffe4b0b406041812e6
                    - 56e9deffe4b0b406041812e7
                createdDate:
                  type: integer
                  format: int64
                  example: 1458167557358
                modifiedDate:
                  type: integer
                  format: int64
                  example: 1458330606752
            UserAppEntitlement:
              description: Application Entitlements for the user
              type: object
              required:
                - appId
                - listed
                - install
              properties:
                appId:
                  type: string
                  description: Unique ID for the Application
                  maxLength: 256
                  minLength: 1
                  example: selerity
                appName:
                  type: string
                  description: Name for this Application
                  maxLength: 50
                  minLength: 1
                  example: Selerity Context
                listed:
                  type: boolean
                  description: >-
                    if true, this application will be listed in the appstore for
                    this user.  Otherwise, this application will be hidden in
                    the appstore.
                  example: true
                install:
                  type: boolean
                  description: >-
                    if true, it indicate this application is installed for this
                    user.  Otherwise, this user does not have this application
                    installed.
                  example: true
                products:
                  $ref: '#/definitions/ProductList'
            PodAppEntitlement:
              description: Application Entitlements for the company
              type: object
              required:
                - appId
                - appName
                - enable
                - listed
                - install
              properties:
                appId:
                  type: string
                  description: Unique ID for the Application
                  maxLength: 256
                  minLength: 1
                  example: djApp
                appName:
                  type: string
                  description: Name for this Application
                  maxLength: 50
                  minLength: 1
                  example: Dow Jones
                enable:
                  type: boolean
                  example: true
                listed:
                  type: boolean
                  description: >-
                    if true, this application will be listed in the appstore for
                    everyone.  Otherwise, this application will be hidden in the
                    appstore.
                  example: true
                install:
                  type: boolean
                  description: >-
                    if true, the entitlement is set to automatic for the
                    company.  Otherwise, it is set to manual.
                  example: true
            Role:
              description: Role record.
              type: object
              properties:
                id:
                  type: string
                  format: long
                name:
                  type: string
                description:
                  type: string
            RoleDetailList:
              type: array
              items:
                $ref: '#/definitions/RoleDetail'
              example:
                - id: CONTENT_MANAGEMENT
                  name: Content Management
                  userTypes:
                    - SYSTEM
                    - NORMAL
                  optionalActions:
                    - MONITOR_ROOMS
                - id: COMPLIANCE_OFFICER
                  name: Compliance Officer
                  userTypes:
                    - NORMAL
                  optionalActions:
                    - BAN_AND_UNBAN_ROOM_MEMBER
                    - LOCK_AND_UNLOCK_ROOM
                    - MONITOR_ROOMS
                    - MONITOR_WALL_POSTS
            RoleDetail:
              description: Role detailed.
              type: object
              properties:
                id:
                  type: string
                  example: CONTENT_MANAGEMENT
                name:
                  type: string
                  example: Content Management
                userTypes:
                  type: array
                  items:
                    type: string
                  example:
                    - NORMAL
                    - SYSTEM
                optionalActions:
                  type: array
                  items:
                    type: string
                  example:
                    - MONITOR_ROOMS
                    - MONITOR_WALL_POSTS
            GroupList:
              type: array
              items:
                $ref: '#/definitions/Group'
              example:
                - id: 571db1f2e4b027c4f055a594
                  name: Group 1
                  active: true
                  memberCount: 1
                  policies:
                    - 571db2e4e4b012df6341f393
                  createdDate: 1461563890135
                  modifiedDate: 1461563926812
                - id: 571db20ae4b012df6341f391
                  name: Group 2
                  active: true
                  memberCount: 1
                  policies:
                    - 571db2e4e4b012df6341f393
                  createdDate: 1461563914581
                  modifiedDate: 1461564112286
            UserAppEntitlementsPatchList:
              description: Array of app entitlements to patch for a user
              type: array
              items:
                $ref: '#/definitions/UserAppEntitlementPatch'
            UserAppEntitlementPatchEnum:
              type: object
              default: KEEP
              description: null
              properties:
                type:
                  type: string
                  enum: &ref_0
                    - 'TRUE'
                    - 'FALSE'
                    - KEEP
                    - REMOVE
                  description: |
                    UserAppEntitlementPatchEnum type :
                     * TRUE - The parameter should be set to true.
                     * FALSE - The parameter should be set to false.
                     * KEEP - The parameter should not be updated, the current value will be kept.
                     * REMOVE - The parameter should be reverted to tenant level's value.
                  example: KEEP
            UserAppEntitlementPatch:
              description: Application Entitlements to patch for the user
              type: object
              required:
                - appId
              properties:
                appId:
                  type: string
                  description: Unique ID for the Application
                  maxLength: 256
                  minLength: 1
                  example: selerity
                listed:
                  type: string
                  enum: *ref_0
                  default: KEEP
                  description: >-
                    If "TRUE", this application will be listed in the appstore
                    for this user. If "FALSE", this application will be hidden
                    in the appstore. If "KEEP" or not set, the current value is
                    kept. If "REMOVE", it will be removed from user settings and
                    the pod level setting's value will be used.
                  example: KEEP
                install:
                  type: string
                  enum: *ref_0
                  default: KEEP
                  description: >-
                    If "TRUE", this application will be installed for this user.
                    If "FALSE", this application will not be installed for this
                    user. If "KEEP" or not set, the current value is kept. If
                    "REMOVE", it will be removed from user settings and the pod
                    level setting's value will be used.
                  example: true
                product:
                  $ref: '#/definitions/Product'
            UserAppEntitlementList:
              type: array
              items:
                $ref: '#/definitions/UserAppEntitlement'
              example:
                - appId: djApp
                  appName: Dow Jones
                  listed: true
                  install: false
                - appId: selerity
                  appName: Selerity Context
                  listed: true
                  install: true
                  products:
                    - appId: selerity
                      name: Standard
                      subscribed: true
                      type: default
                    - appId: selerity
                      name: Premium
                      sku: AcDccU53SsY
                      subscribed: false
                      type: premium
            PodAppEntitlementList:
              type: array
              items:
                $ref: '#/definitions/PodAppEntitlement'
              example:
                - appId: djApp
                  appName: Dow Jones
                  enable: true
                  listed: true
                  install: false
                - appId: selerity
                  appName: Selerity Context
                  enable: false
                  listed: true
                  install: true
            RoleList:
              type: array
              items:
                $ref: '#/definitions/Role'
            IntegerList:
              type: array
              items:
                type: integer
                format: int64
              example:
                - 1461508270000
                - 7215545057281
            StringList:
              type: array
              items:
                type: string
              example:
                - ftp
                - mailto
                - fdsup
                - skype
            DisclaimerList:
              type: array
              items:
                $ref: '#/definitions/Disclaimer'
              example:
                - id: 571d2052e4b042aaf06d2e7a
                  name: Enterprise Disclaimer
                  content: This is a disclaimer for the enterprise.
                  frequencyInHours: 24
                  isDefault: false
                  isActive: true
                  createdDate: 1461526610846
                  modifiedDate: 1461526610846
                - id: 571d20dae4b042aaf06d2e7c
                  name: New Enterprise Disclaimer
                  content: This is a second enterprise disclaimer.
                  frequencyInHours: 168
                  isDefault: false
                  isActive: true
                  createdDate: 1461526746875
                  modifiedDate: 1461526746875
            Disclaimer:
              type: object
              properties:
                id:
                  type: string
                  example: 571d20dae4b042aaf06d2e7c
                name:
                  type: string
                  example: New Enterprise Disclaimer
                content:
                  type: string
                  example: This is a second enterprise disclaimer.
                frequencyInHours:
                  type: integer
                  format: int32
                  example: 168
                isDefault:
                  type: boolean
                  example: false
                isActive:
                  type: boolean
                  example: true
                createdDate:
                  type: integer
                  format: int64
                  example: 1461526746875
                modifiedDate:
                  type: integer
                  format: int64
                  example: 1461526746875
                format:
                  type: string
                  enum:
                    - TEXT
                    - XML
                  example: TEXT
            DelegateAction:
              type: object
              properties:
                userId:
                  type: integer
                  format: int64
                  example: 7215545078461
                action:
                  type: string
                  enum:
                    - ADD
                    - REMOVE
                  example: ADD
            UserInfo:
              description: User record.
              type: object
              properties:
                user:
                  $ref: '#/definitions/UserAttributes'
                userSystemInfo:
                  $ref: '#/definitions/UserSystemInfo'
            UserAttributes:
              description: User record.
              type: object
              properties:
                emailAddress:
                  type: string
                  example: janedoe@symphony.com
                firstName:
                  type: string
                  example: Jane
                lastName:
                  type: string
                  example: Doe
                userName:
                  type: string
                  example: jane.doe
                displayName:
                  type: string
                  example: Jane Doe
                companyName:
                  type: string
                  example: Company
                department:
                  type: string
                  example: Department
                division:
                  type: string
                  example: Division
                title:
                  type: string
                  example: Trader
                workPhoneNumber:
                  type: string
                  example: '+12349999999'
                mobilePhoneNumber:
                  type: string
                  example: '+12349999999'
                smsNumber:
                  type: string
                  example: '+12349999999'
                accountType:
                  type: string
                  enum:
                    - NORMAL
                    - SYSTEM
                    - SDL
                  example: NORMAL
                location:
                  type: string
                  example: New York
                jobFunction:
                  type: string
                  example: Trader
                assetClasses:
                  type: array
                  items:
                    type: string
                  example:
                    - Commodities
                industries:
                  type: array
                  items:
                    type: string
                  example:
                    - Financials
                    - Services
            V2UserDetail:
              description: V2 Detailed User record.
              type: object
              properties:
                userAttributes:
                  $ref: '#/definitions/V2UserAttributes'
                userSystemInfo:
                  $ref: '#/definitions/UserSystemInfo'
                features:
                  $ref: '#/definitions/IntegerList'
                apps:
                  $ref: '#/definitions/IntegerList'
                groups:
                  $ref: '#/definitions/IntegerList'
                roles:
                  $ref: '#/definitions/StringList'
                disclaimers:
                  $ref: '#/definitions/IntegerList'
                avatar:
                  $ref: '#/definitions/Avatar'
            V2UserAttributes:
              description: V2 User record.
              type: object
              properties:
                emailAddress:
                  type: string
                  example: johndoe@symphony.com
                firstName:
                  type: string
                  example: John
                lastName:
                  type: string
                  example: Doe
                userName:
                  type: string
                  example: johndoe
                displayName:
                  type: string
                  example: John Doe
                companyName:
                  type: string
                  example: Company
                department:
                  type: string
                  example: Department
                division:
                  type: string
                  example: Division
                title:
                  type: string
                  example: Trader
                workPhoneNumber:
                  type: string
                  example: '+15419999999'
                mobilePhoneNumber:
                  type: string
                  example: '+15419999999'
                twoFactorAuthPhone:
                  type: string
                  example: '+15419999999'
                smsNumber:
                  type: string
                  example: '+15419999999'
                accountType:
                  type: string
                  enum:
                    - NORMAL
                    - SYSTEM
                    - SDL
                  example: NORMAL
                location:
                  type: string
                  example: New York
                recommendedLanguage:
                  type: string
                  example: english
                jobFunction:
                  type: string
                  example: Trader
                assetClasses:
                  type: array
                  items:
                    type: string
                  example:
                    - Equities
                industries:
                  type: array
                  items:
                    type: string
                  example:
                    - Healthcare
                    - Technology
                marketCoverage:
                  type: array
                  items:
                    type: string
                  example:
                    - EMEA
                responsibility:
                  type: array
                  items:
                    type: string
                  example:
                    - BAU
                function:
                  type: array
                  items:
                    type: string
                  example:
                    - Trade Processing
                instrument:
                  type: array
                  items:
                    type: string
                  example:
                    - Equities
                currentKey:
                  $ref: '#/definitions/V2UserKeyRequest'
                previousKey:
                  $ref: '#/definitions/V2UserKeyRequest'
            V2UserKeyRequest:
              description: User RSA key information.
              type: object
              properties:
                key:
                  description: User RSA public key.
                  type: string
                  example: >-
                    --BEGIN PUBLIC KEY--\nMIICIANBgkqhw0BAQ...cCAwEAAQ==\n--END
                    PUBLIC KEY--
                expirationDate:
                  description: >-
                    RSA key expiration date. This value is set just for rotated
                    keys.
                  type: integer
                  format: int64
                  example: 1467562406219
                action:
                  description: >
                    Action to be performed on the RSA key.

                    The following actions can be performed onto the user's
                    active RSA key:
                      - SAVE
                      - REVOKE
                    The following actions can be performed onto the user's
                    rotated RSA key:
                      - REVOKE
                      - EXTEND
                  type: string
                  example: SAVE
            V2UserCreate:
              description: >
                V2 User Creation Object.

                After creation, modify roles, features etc via the specific API
                calls.
              type: object
              properties:
                userAttributes:
                  $ref: '#/definitions/V2UserAttributes'
                password:
                  $ref: '#/definitions/Password'
                roles:
                  type: array
                  items:
                    type: string
                  example:
                    - INDIVIDUAL
                    - COMPLIANCE_OFFICER
            V2UserDetailList:
              type: array
              items:
                $ref: '#/definitions/V2UserDetail'
              example:
                - userAttributes:
                    emailAddress: nexus.user@email.com
                    userName: nexus.user
                    displayName: nexus.user
                    accountType: SYSTEM
                  userSystemInfo:
                    id: 9826885173290
                    status: ENABLED
                    suspended: false
                    createdDate: 1499375475000
                    createdBy: '9826885173255'
                    lastUpdatedDate: 1499375475852
                    lastLoginDate: 1504899124191
                  roles:
                    - USER_PROVISIONING
                    - CONTENT_MANAGEMENT
                    - INDIVIDUAL
                - userAttributes:
                    emailAddress: admin@mail.com
                    firstName: admin
                    lastName: admin
                    userName: admin@mail.com
                    displayName: Admin Admin
                    companyName: Company Name
                    department: Departament
                    division: Division
                    title: Administrator
                    twoFactorAuthPhone: '+15419999999'
                    workPhoneNumber: '+15419999999'
                    mobilePhoneNumber: '+15419999999'
                    accountType: NORMAL
                    assetClasses:
                      - Currencies
                    industries:
                      - Technology
                  userSystemInfo:
                    id: 7696581394433
                    status: ENABLED
                    suspended: false
                    createdDate: 1438054194000
                    lastUpdatedDate: 1527532171729
                    lastLoginDate: 1523912043015
                  roles:
                    - SUPER_COMPLIANCE_OFFICER
                    - INDIVIDUAL
                    - SUPER_ADMINISTRATOR
            UserSystemInfo:
              description: User Status Information.
              type: object
              properties:
                id:
                  type: integer
                  format: int64
                  example: 7215545078461
                status:
                  type: string
                  enum:
                    - ENABLED
                    - DISABLED
                  example: ENABLED
                suspended:
                  type: boolean
                  description: >-
                    An optional attribute indicating whether the user is
                    temporarily suspended or not. Since SBE 20.14.
                  x-since: 20.14
                  example: true
                suspendedUntil:
                  type: integer
                  format: int64
                  description: >-
                    An optional unix timestamp until which the suspension is
                    effective. Since SBE 20.14.
                  x-since: 20.14
                  example: 1601546400
                suspensionReason:
                  type: string
                  description: >-
                    An optional description of the suspension reason. Since SBE
                    20.14.
                  x-since: 20.14
                  example: The user will be OOO due to a mandatory leave
                createdDate:
                  type: integer
                  format: int64
                  example: 1461508270000
                createdBy:
                  type: string
                  example: '7215545057281'
                lastUpdatedDate:
                  type: integer
                  format: int64
                  example: 1461508270000
                lastLoginDate:
                  type: integer
                  format: int64
                  example: 1461508270000
                lastPasswordReset:
                  type: integer
                  format: int64
                  example: 1461508270000
                deactivatedDate:
                  type: integer
                  format: int64
                  example: 1461508270000
            UserDetailList:
              type: array
              items:
                $ref: '#/definitions/UserDetail'
              example:
                - userAttributes:
                    emailAddress: janedoe@symphony.com
                    firstName: Jane
                    lastName: Doe
                    userName: jane.doe
                    displayName: Jane Doe
                    accountType: NORMAL
                    assetClasses:
                      - Commodities
                    industries:
                      - Financials
                      - Healthcare
                  userSystemInfo:
                    id: 9826885173258
                    status: ENABLED
                    suspended: true
                    suspensionReason: The user will be OOO due to a mandatory leave
                    suspendedUntil: 1601546400
                    createdDate: 1499347606000
                    createdBy: '9826885173252'
                    lastUpdatedDate: 1499348554853
                    lastLoginDate: 1504839044527
                  roles:
                    - INDIVIDUAL
                - userAttributes:
                    emailAddress: nexus.user@email.com
                    userName: nexus.user
                    displayName: nexus.user
                    accountType: SYSTEM
                  userSystemInfo:
                    id: 9826885173290
                    status: ENABLED
                    suspended: false
                    createdDate: 1499375475000
                    createdBy: '9826885173255'
                    lastUpdatedDate: 1499375475852
                    lastLoginDate: 1504899124191
                  roles:
                    - USER_PROVISIONING
                    - CONTENT_MANAGEMENT
                    - INDIVIDUAL
            UserDetail:
              description: Detailed User record.
              type: object
              properties:
                userAttributes:
                  $ref: '#/definitions/UserAttributes'
                userSystemInfo:
                  $ref: '#/definitions/UserSystemInfo'
                features:
                  $ref: '#/definitions/IntegerList'
                apps:
                  $ref: '#/definitions/IntegerList'
                groups:
                  $ref: '#/definitions/IntegerList'
                roles:
                  $ref: '#/definitions/StringList'
                disclaimers:
                  $ref: '#/definitions/IntegerList'
                avatar:
                  $ref: '#/definitions/Avatar'
            Password:
              description: >-
                Password. Stored as derived password in both the Pod and the Key
                Manager using PBKDF2 function. Number of iterations should be
                10000 and desired length 256 bits.
              type: object
              properties:
                hSalt:
                  description: Pod password salt used for PBKDF2 derivation.
                  type: string
                  example: hsalt
                hPassword:
                  description: Pod password derived with PBKDF2.
                  type: string
                  example: hpassword
                khSalt:
                  description: Key Manager password salt used for PBKDF2 derivation.
                  type: string
                  example: khsalt
                khPassword:
                  description: Key Manager password derived with PBKDF2.
                  type: string
                  example: khpassword
            MemberInfo:
              description: Detailed membership record.
              type: object
              properties:
                id:
                  type: integer
                  format: int64
                  example: 7078106103810
                owner:
                  type: boolean
                  example: true
                joinDate:
                  type: integer
                  format: int64
                  example: 1461426797833
                addedThroughGroups:
                  description: >-
                    When the user has been added to the stream through a group
                    (aka SDL), this array contains the group ID which the user
                    belongs to. Since SBE 20.14.
                  x-since: 20.14
                  type: array
                  items:
                    type: integer
                    format: int64
                  example:
                    - 68719476744
            MembershipList:
              description: List of members in a room.
              type: array
              items:
                $ref: '#/definitions/MemberInfo'
              example:
                - id: 7078106103900
                  owner: false
                  joinDate: 1461430710531
                - id: 7078106103809
                  owner: true
                  joinDate: 1461426797875
                - id: 7078106103810
                  owner: true
                  joinDate: 1461426797833
                  addedThroughGroups:
                    - 68719476744
            V2MemberUserDetail:
              description: User detail information for stream membership
              type: object
              properties:
                userId:
                  type: integer
                  format: int64
                  example: 13537736917013
                email:
                  type: string
                  example: dpayet@om.fr
                firstName:
                  type: string
                  example: Dimitri
                lastName:
                  type: string
                  example: Payet
                displayName:
                  type: string
                  description: Display name for the user
                  example: Dimitri Payet
                company:
                  type: string
                  description: Company name
                  example: Mars
                companyId:
                  type: integer
                  description: Company ID
                  example: 13
                isExternal:
                  type: boolean
                  description: true indicate that this user belong to another company
                  example: true
            V2MemberInfo:
              description: Detailed membership record.
              type: object
              properties:
                user:
                  $ref: '#/definitions/V2MemberUserDetail'
                isOwner:
                  type: boolean
                  description: true if this is an owner of the room
                  example: true
                isCreator:
                  type: boolean
                  description: true if this is the creator of the room
                  example: true
                joinDate:
                  description: unix timestamp for join date
                  type: integer
                  format: int64
                  example: 1604494574047
                addedThroughGroups:
                  description: >-
                    When the user has been added to the stream through a group
                    (aka SDL), this array contains the group ID which the user
                    belongs to. Since SBE 20.14.
                  x-since: 20.14
                  type: array
                  items:
                    type: integer
                    format: int64
                  example:
                    - 68719476744
            V2MemberInfoList:
              type: array
              items:
                $ref: '#/definitions/V2MemberInfo'
              example:
                - user:
                    userId: 13537736917000
                    email: john.doe@symphony.com
                    firstName: John
                    lastName: Doe
                    displayName: John Doe
                    company: pod197
                    companyId: 197
                    isExternal: false
                  isOwner: true
                  isCreator: true
                  joinDate: 1604494574047
                - user:
                    userId: 13537736917001
                    email: bot@symphony.com
                    displayName: User Provisioning Bot
                    company: pod197
                    companyId: 197
                    isExternal: false
                  isOwner: false
                  isCreator: false
                  joinDate: 1604494605272
                  addedThroughGroups:
                    - 68719476744
            V2MembershipList:
              description: List of members in the stream.
              type: object
              properties:
                count:
                  type: integer
                  description: total members count
                  example: null
                skip:
                  type: integer
                  description: number of items to skip from the request
                  example: null
                limit:
                  type: integer
                  description: maximum number of items to return
                  example: null
                members:
                  $ref: '#/definitions/V2MemberInfoList'
            MessageSuppressionResponse:
              description: The suppression state of a message
              type: object
              properties:
                messageId:
                  type: string
                  example: _Gj13MiR-5IrVtrmPNl6fn___qvWCYI_dA
                suppressed:
                  type: boolean
                  example: true
                suppressionDate:
                  type: integer
                  format: int64
                  description: The date when this message was suppressed.
                  example: 1461565603191
            BulkActionResult:
              description: >
                The results of list based bulk action. The list contains the
                result messages

                in the same order as submitted. The message will be an empty
                string if the action

                was successful for item in that index.
              properties:
                overallResult:
                  type: string
                  enum:
                    - SUCCESS
                    - FAIL
                  example: SUCCESS
                results:
                  type: array
                  items:
                    type: string
                  example:
                    - ''
            UserConnectionRequest:
              type: object
              description: Request body for the Connection APIs
              properties:
                userId:
                  type: integer
                  format: int64
                  description: user id
                  example: 769658112378
            UserConnection:
              type: object
              description: Connection status between two users
              properties:
                userId:
                  type: integer
                  format: int64
                  description: user id
                  example: 769658112378
                status:
                  type: string
                  description: >-
                    Connection status between the requesting user and the
                    request sender
                  enum:
                    - PENDING_INCOMING
                    - PENDING_OUTGOING
                    - ACCEPTED
                    - REJECTED
                  example: ACCEPTED
                firstRequestedAt:
                  type: integer
                  format: int64
                  description: unix timestamp when the first request was made
                  example: 1470018073812
                updatedAt:
                  type: integer
                  format: int64
                  description: unix timestamp on the last updated date
                  example: 1471018076255
                requestCounter:
                  type: integer
                  format: int32
                  description: number of requests made
                  example: 1
            UserConnectionList:
              type: array
              items:
                $ref: '#/definitions/UserConnection'
              example:
                - userId: 769658112378
                  status: PENDING_OUTGOING
                  firstRequestedAt: 1470018073812
                  updatedAt: 1471018076255
                  requestCounter: 1
                - userId: 7078106103809
                  status: ACCEPTED
            StreamList:
              description: A list of streams of which the requesting user is a member.
              type: array
              items:
                $ref: '#/definitions/StreamAttributes'
            StreamAttributes:
              type: object
              properties:
                id:
                  type: string
                  description: The stream ID.
                crossPod:
                  type: boolean
                  description: If true, this is a cross-pod stream.
                active:
                  type: boolean
                  description: If true, this stream is active.
                streamType:
                  $ref: '#/definitions/StreamType'
                streamAttributes:
                  $ref: '#/definitions/ConversationSpecificStreamAttributes'
                roomAttributes:
                  $ref: '#/definitions/RoomSpecificStreamAttributes'
            StreamType:
              type: object
              properties:
                type:
                  type: string
                  enum:
                    - IM
                    - MIM
                    - ROOM
                    - POST
                  example: ROOM
            ConversationSpecificStreamAttributes:
              type: object
              properties:
                members:
                  $ref: '#/definitions/UserIdList'
            RoomSpecificStreamAttributes:
              type: object
              properties:
                name:
                  type: string
                  description: Room name.
            StreamFilter:
              description: Stream filtering parameters.
              properties:
                streamTypes:
                  description: Types of streams to search for.
                  type: array
                  items:
                    $ref: '#/definitions/StreamType'
                  example:
                    - type: IM
                    - type: ROOM
                includeInactiveStreams:
                  description: Whether to include inactive streams in the list of results.
                  type: boolean
                  example: 'false'
            V2StreamAttributes:
              type: object
              properties:
                id:
                  type: string
                  description: The stream ID.
                  example: BZQYepoT0Zf4vL_jpeMPqn___oEWvVy3dA
                crossPod:
                  type: boolean
                  description: If true, this is a cross-pod stream.
                  example: false
                origin:
                  type: string
                  description: >-
                    INTERNAL if the creator of this stream belongs to the pod,
                    EXTERNAL otherwise
                  example: INTERNAL
                active:
                  type: boolean
                  description: If true, this stream is active.
                  example: true
                lastMessageDate:
                  type: integer
                  format: int64
                  description: unix timestamp of the last message sent in the stream
                  example: 1644590972696
                streamType:
                  description: >-
                    The type of the stream (IM = IM, multi-IM = MIM, chat room =
                    ROOM, user wall = POST).
                  $ref: '#/definitions/V2StreamType'
                streamAttributes:
                  $ref: '#/definitions/V2ConversationSpecificStreamAttributes'
                roomAttributes:
                  $ref: '#/definitions/V2RoomSpecificStreamAttributes'
            V2StreamType:
              type: object
              properties:
                type:
                  type: string
                  example: ROOM
            V2ConversationSpecificStreamAttributes:
              type: object
              properties:
                members:
                  $ref: '#/definitions/UserIdList'
            V2RoomSpecificStreamAttributes:
              type: object
              properties:
                name:
                  type: string
                  description: Room name.
                  example: API room
                groups:
                  description: >-
                    List of groups (aka SDLs) that were added to the room. Since
                    SBE 20.14.
                  x-since: 20.14
                  type: array
                  items:
                    $ref: '#/definitions/GroupItem'
                  example:
                    - id: 68719476744
                      addedBy: 68719476743
            V2AdminStreamFilter:
              description: stream filter criteria
              type: object
              properties:
                streamTypes:
                  description: type of streams to search for
                  type: array
                  items:
                    description: Valid values are IM, MIM or ROOM
                    $ref: '#/definitions/V2AdminStreamType'
                  example:
                    - type: IM
                    - type: ROOM
                scope:
                  description: >
                    Scope of the room. Valid values are INTERNAL or EXTERNAL.

                    If not specified, it will include both Internal and External
                    scope
                  type: string
                  example: INTERNAL
                origin:
                  description: >
                    Origin of the room. It indicates whether the room was
                    created by a user within the company by another company.

                    Valid values are INTERNAL or EXTERNAL.

                    If not specified, it will include both Internal and External
                    origin
                  type: string
                  example: INTERNAL
                status:
                  description: >
                    Status of the room.

                    Valid values are ACTIVE or INACTIVE.

                    If not specified, it will include both Active and Inactive
                    status
                  type: string
                  example: ACTIVE
                privacy:
                  description: >
                    Privacy setting of the stream.

                    Valid values are PUBLIC or PRIVATE.

                    If not specified, it will include both public and private
                    streams
                  type: string
                  example: PRIVATE
                startDate:
                  description: Start date in unix timestamp in millseconds
                  type: integer
                  format: int64
                  example: 1481575056047
                endDate:
                  description: >-
                    End date in unix timestamp in millseconds.  If not
                    specified, it assume to be current time.
                  type: integer
                  format: int64
                  example: 1483038089833
            V2AdminStreamType:
              type: object
              properties:
                type:
                  type: string
                  example: ROOM
            AdminJustifiedUserAction:
              type: object
              properties:
                userId:
                  description: The userId of the target user.
                  type: integer
                  format: int64
                justification:
                  description: The reason for the requested action.
                  type: string
            AdminJustifiedAction:
              type: object
              properties:
                justification:
                  description: The reason for the requested action.
                  type: string
            MessageStatusUser:
              type: object
              properties:
                userId:
                  type: string
                  example: 7078106103901
                firstName:
                  type: string
                  example: Gustav
                lastName:
                  type: string
                  example: Mahler
                displayName:
                  type: string
                  example: Gustav Mahler
                email:
                  type: string
                  example: gustav.mahler@music.org
                userName:
                  type: string
                  example: gmahler
                timestamp:
                  type: string
                  example: 1531968487845
            MessageStatus:
              description: >
                Holds the status of a particular message, indicating which user
                the message has been sent, delivered or read.
              type: object
              properties:
                author:
                  description: User who has sent the message.
                  type: object
                  $ref: '#/definitions/MessageStatusUser'
                read:
                  description: >-
                    All users who have read that message, in any Symphony
                    client.
                  type: array
                  items:
                    $ref: '#/definitions/MessageStatusUser'
                delivered:
                  description: >
                    All users who have at least one Symphony client to which the
                    message has been delivered, and not read yet.
                  type: array
                  items:
                    $ref: '#/definitions/MessageStatusUser'
                sent:
                  description: >
                    All users to whom the message has been sent and received by
                    the Symphony system,

                    but not yet delivered to any user's Symphony client.
                  type: array
                  items:
                    $ref: '#/definitions/MessageStatusUser'
                  example:
                    - userId: 7078106103904
                      firsName: Benjamin
                      lastName: Britten
                      displayName: Benjamin Britten
                      email: benjamin.britten@music.org
                      userName: bbritten
                      timestamp: 1484156123000
                    - userId: 7078106103901
                      firsName: Gustav
                      lastName: Mahler
                      displayName: Gustav Mahler
                      email: gmahler@music.org
                      userName: gmahler
                      timestamp: 1531968487845
            ApplicationInfo:
              description: |
                Required information for creating an application.
              type: object
              properties:
                appId:
                  description: An unique id for the application.
                  type: string
                  maxLength: 256
                  minLength: 1
                name:
                  description: User defined name for the application.
                  type: string
                appUrl:
                  description: The url for the app. Must start with "https://".
                  type: string
                domain:
                  description: Domain for app, that must match app url domain.
                  type: string
                publisher:
                  description: The publisher for this application.
                  type: string
              example:
                appId: my-test-app
                name: my-test-app
                appUrl: https://joe.mydomain.com
                domain: mydomain.com
                publisher: Joe Smith
            ApplicationDetail:
              description: Detailed record of application.
              type: object
              properties:
                applicationInfo:
                  $ref: '#/definitions/ApplicationInfo'
                iconUrl:
                  description: Url to a icon to use for app. Must start with "https://".
                  type: string
                  example: https://myiconUrl.com
                description:
                  description: Description of the application.
                  type: string
                  example: a test app
                allowOrigins:
                  description: >
                    The permitted domains to send or receive a request from.

                    The field is for the purpose of CORS which set the app
                    specific "ALLOW-ORIGIN-DOMAINS" header in HTTP.
                  type: string
                  example: mydomain.com
                permissions:
                  description: >
                    List of application permissions provisioned for the
                    application.

                    In addition to the known ones, custom permissions are
                    accepted.

                    A custom permission should only contain upper case
                    alphanumeric characters and underscore.

                    It should not be empty or only contain spaces and its length
                    is limited to 64 characters.


                    Known permissions:
                      - SEND_MESSAGES
                      - GET_USER_CONNECTIONS
                      - REQUEST_USER_CONNECTIONS
                      - SET_PRESENCE
                      - GET_PRESENCE
                      - GET_BASIC_USER_INFO
                      - GET_EXTENDED_USER_INFO
                      - GET_BASIC_CONTACT_INFO
                      - GET_EXTENDED_CONTACT_INFO
                      - ACT_AS_USER
                      - MANAGE_SIGNALS
                      - MANAGE_USER_FOLLOWING
                      - TRUST_APP
                  type: array
                  items:
                    type: string
                    maxLength: 64
                    minLength: 1
                  example:
                    - ACT_AS_USER
                    - SEND_MESSAGES
                cert:
                  description: The app public certificate in pem format.
                  type: string
                  example: >-
                    --BEGIN PUBLIC KEY--\nMIICIANBgkqhw0BAQ...cCAwEAAQ==\n--END
                    PUBLIC KEY--
                authenticationKeys:
                  $ref: '#/definitions/AppAuthenticationKeys'
                notification:
                  $ref: '#/definitions/AppNotification'
                properties:
                  $ref: '#/definitions/AppProperties'
            V2PresenceList:
              type: array
              items:
                $ref: '#/definitions/V2Presence'
              example:
                - category: AVAILABLE
                  userId: 14568529068038
                  timestamp: 1533928483800
                - category: OFFLINE
                  userId: 974217539631
                  timestamp: 1503286226030
            V2Presence:
              allOf:
                - $ref: '#/definitions/V2UserPresence'
                - type: object
                  properties:
                    timestamp:
                      type: integer
                      format: int64
                      description: >-
                        The time, in milliseconds since Jan 1 1970, when the
                        presence state was set.
                      example: 1533928483800
            V2UserPresence:
              allOf:
                - $ref: '#/definitions/V2PresenceStatus'
                - type: object
                  properties:
                    userId:
                      type: integer
                      format: int64
                      description: The ID of the user to whom the presence state relates.
                      example: 14568529068038
            V2PresenceStatus:
              type: object
              properties:
                category:
                  type: string
                  description: |
                    Presence status. Possible values are:
                      - UNDEFINED
                      - AVAILABLE
                      - BUSY
                      - DO_NOT_DISTURB
                      - ON_THE_PHONE
                      - BE_RIGHT_BACK
                      - IN_A_MEETING
                      - AWAY
                      - OUT_OF_OFFICE
                      - OFF_WORK
                      - OFFLINE
                  example: AWAY
              required:
                - category
            V2AdminStreamList:
              description: list of streams info
              type: object
              properties:
                count:
                  type: integer
                  format: int64
                  description: total number of streams which match the filter criteria
                  example: 4
                skip:
                  type: integer
                  description: number of streams skipped
                  example: 0
                limit:
                  type: integer
                  description: maximum number of streams return
                  example: 50
                filter:
                  $ref: '#/definitions/V2AdminStreamFilter'
                streams:
                  $ref: '#/definitions/V2AdminStreamInfoList'
            V2AdminStreamInfoList:
              type: array
              description: list of stream info
              items:
                $ref: '#/definitions/V2AdminStreamInfo'
              example:
                - id: Q2KYGm7JkljrgymMajYTJ3___qcLPr1UdA
                  isExternal: false
                  isActive: true
                  isPublic: false
                  type: ROOM
                  attributes:
                    roomName: Active Internal Private Room
                    roomDescription: Active Internal Private Room
                    createdByUserId: 8933531975689
                    createdDate: 1481575056047
                    lastModifiedDate: 1481575056047
                    originCompany: Symphony
                    originCompanyId: 130
                    membersCount: 1
                    lastMessageDate: 1516699467959
                - id: _KnoYrMkhEn3H2_8vE0kl3___qb5SANQdA
                  isExternal: true
                  isActive: false
                  isPublic: false
                  type: ROOM
                  attributes:
                    roomName: Inactive External Room
                    roomDescription: Inactive External Room
                    createdByUserId: 8933531975686
                    createdDate: 1481876438194
                    lastModifiedDate: 1481876438194
                    originCompany: Symphony
                    originCompanyId: 130
                    membersCount: 2
                    lastMessageDate: 1516699467959
            V2AdminStreamInfo:
              description: Stream information
              type: object
              properties:
                id:
                  type: string
                  description: stream id
                  example: Q2KYGm7JkljrgymMajYTJ3___qcLPr1UdA
                isExternal:
                  type: boolean
                  description: >-
                    true indicate this stream has the scope of external and
                    false indictate this stream has the scope of internal.
                    Deprecated, use origin
                  example: false
                isActive:
                  type: boolean
                  description: >-
                    true indicate that this stream has the status of active and
                    false indicate this stream has the scope of inactive
                  example: true
                isPublic:
                  type: boolean
                  description: >-
                    true indicate that this stream has a privacy setting of
                    public.  This only apply a ROOM stream type.
                  example: false
                type:
                  type: string
                  description: type of stream (IM, MIM, ROOM)
                  example: ROOM
                crossPod:
                  type: boolean
                  description: If true, this is a cross-pod stream.
                  example: false
                origin:
                  type: string
                  description: >-
                    INTERNAL if the creator of this stream belongs to the pod,
                    EXTERNAL otherwise
                  example: INTERNAL
                attributes:
                  $ref: '#/definitions/V2AdminStreamAttributes'
            V2AdminStreamAttributes:
              description: additional optional properties for the stream
              type: object
              properties:
                roomName:
                  type: string
                  description: room name (room only)
                  example: API room
                roomDescription:
                  type: string
                  description: description of the room (room only)
                  example: Room created via API
                members:
                  type: array
                  description: list of userid who is member of the stream - im or mim only
                  items:
                    type: integer
                    format: int64
                  example:
                    - 8933531975686
                    - 8933531975689
                createdByUserId:
                  type: integer
                  format: int64
                  description: creator user id
                  example: 8933531975689
                createdDate:
                  type: integer
                  format: int64
                  description: created date
                  example: 1481575056047
                lastModifiedDate:
                  type: integer
                  format: int64
                  description: last modified date
                  example: 1481575056047
                originCompany:
                  type: string
                  description: company name of the creator
                  example: Symphony
                originCompanyId:
                  type: integer
                  description: company id of the creator
                  example: 130
                membersCount:
                  type: integer
                  description: total number of members in the stream
                  example: 1
                lastMessageDate:
                  type: integer
                  format: int64
                  description: last date a message was sent in this stream
                  example: 1516699467959
                groupChat:
                  type: boolean
                  description: whether a stream is a group chat or not. Since SBE 20.16.
                  x-since: 20.16
                  example: false
            FileExtension:
              type: object
              required:
                - extension
              properties:
                extension:
                  type: string
                  description: >
                    The file extension that this specific record is for.  This
                    is a unique ID

                    that allows this record to be referenced in the URI.
                  example: .txt
                scope_internal:
                  type: boolean
                  description: |
                    File extension allowed for internal scope
                scope_external:
                  type: boolean
                  description: |
                    File extension allowed for external scope
                scope_xpod:
                  type: boolean
                  description: |
                    File extension allowed to be received from another POD
                  x-since: 24.2
                source:
                  type: string
                  description: >
                    File extension with metadata understood by the system or
                    file extension created by a customer
                  enum:
                    - SYSTEM
                    - CUSTOMER
            Pagination:
              type: object
              required:
                - cursors
              properties:
                cursors:
                  type: object
                  required:
                    - before
                  properties:
                    before:
                      type: string
                      description: >
                        This is the opaque url-safe string that points to the
                        start of the page of data

                        that has been returned.
                      example: MTAxNTExOTQ1MjAwNzI5NDE=
                    after:
                      type: string
                      description: >
                        This is the opaque url-safe string that points to the
                        end of the page of data

                        that has been returned.
                      example: NDMyNzQyODI3OTQw
                previous:
                  type: string
                  description: >
                    API endpoint that will return the previous page of data. If
                    not included, this is

                    the first page of data.
                  example: >-
                    https://tenantapi.d.isym.io/v1/tenantinfo?limit=25&before=MTAxNTExOTQ1MjAwNzI5NDE=
                next:
                  type: string
                  description: >
                    API endpoint that will return the next page of data. If not
                    included, this is the

                    last page of data. Due to how pagination works with
                    visibility and privacy, it is

                    possible that a page may be empty but contain a 'next'
                    paging link. Stop paging when

                    the 'next' link no longer appears.
                  example: >-
                    https://tenantapi.d.isym.io/v1/tenantinfo?limit=25&after=NDMyNzQyODI3OTQw
            FileExtensionsResponse:
              type: object
              required:
                - data
                - paging
              properties:
                data:
                  type: array
                  items:
                    $ref: '#/definitions/FileExtension'
            Protocol:
              type: object
              required:
                - scheme
              properties:
                scheme:
                  type: string
                  description: 'URI protocol scheme (example: http, https, ftp)'
                  example: skype
            AppAuthenticationKeys:
              description: App RSA keys information.
              type: object
              properties:
                current:
                  $ref: '#/definitions/AppAuthenticationKey'
                previous:
                  $ref: '#/definitions/AppAuthenticationKey'
            AppAuthenticationKey:
              description: App RSA key information.
              type: object
              properties:
                key:
                  description: Application RSA public key.
                  type: string
                  example: >-
                    --BEGIN PUBLIC KEY--\nMIICIANBgkqhw0BAQ...cCAwEAAQ==\n--END
                    PUBLIC KEY--
                expirationDate:
                  description: >-
                    RSA key expiration date. This value is set just for rotated
                    keys.
                  type: integer
                  format: int64
                  example: 1700815176000
                action:
                  description: >
                    Action to be performed on the RSA key.

                    The following actions can be performed onto the app's active
                    RSA key:
                      - SAVE
                      - REVOKE
                    The following actions can be performed onto the app's
                    rotated RSA key:
                      - REVOKE
                      - EXTEND
                  type: string
                  example: SAVE
            AppNotification:
              type: object
              description: Application callback information
              properties:
                url:
                  type: string
                  description: callback URL
                  example: https://some.url
                apiKey:
                  type: string
                  description: >-
                    apiKey sent into every callback request, using the X-API-KEY
                    header
                  example: test123456
            AppProperties:
              type: array
              description: >-
                Application configuration properties that are shared with the
                extension application, client side. Do not store sensitive
                information here. Since SBE 20.14.
              x-since: 20.14
              items:
                $ref: '#/definitions/AppProperty'
              example:
                - key: port
                  value: 4000
                - key: url
                  value: https://someother.url
            AppProperty:
              type: object
              description: >-
                Application configuration property that is shared with the
                extension application, client side. Do not store sensitive
                information here.
              properties:
                key:
                  type: string
                  description: >-
                    Name of an application configuration property. It cannot be
                    null or empty and its length is limited to 1024 characters.
                    Keys are unique.
                value:
                  type: string
                  description: >-
                    Value of an application configuration property. It cannot be
                    null and its length is limited to 4096 characters. It can be
                    empty.
              example:
                key: port
                value: 4000
            StreamAttachmentResponse:
              type: array
              items:
                $ref: '#/definitions/StreamAttachmentItem'
            StreamAttachmentItem:
              description: File attachments for a message in a stream
              type: object
              properties:
                messageId:
                  type: string
                  example: PYLHNm/1K6p...peOpj+FbQ
                ingestionDate:
                  type: integer
                  format: int64
                  example: 1548089933946
                userId:
                  type: integer
                  format: int64
                  example: 14568529068038
                fileId:
                  type: string
                  description: The attachment File ID.
                  example: internal_14362
                name:
                  type: string
                  description: The file name.
                  example: butterfly.jpg
                size:
                  type: integer
                  format: int64
                  description: Size in bytes.
                  example: 70186
                content-type:
                  type: string
                  example: image/jpeg
                previews:
                  type: array
                  items:
                    $ref: '#/definitions/AttachmentPreview'
            AttachmentPreview:
              description: Preview file for image attachments
              type: object
              properties:
                fileId:
                  type: string
                  description: The preview file ID
                  example: internal_14362
                width:
                  type: integer
                  description: The preview image width
                  example: 600
            UserGroupCreate:
              description: Body for group creation
              type: object
              properties:
                name:
                  description: Group name
                  type: string
                area:
                  description: Group area
                  type: string
                description:
                  description: Group description
                  type: string
                type:
                  description: Group type
                  type: string
              required:
                - name
                - type
            UserGroupResponse:
              description: Group object response
              type: object
              properties:
                id:
                  description: Group ID
                  type: string
                name:
                  description: Group name
                  type: string
                area:
                  description: An optional string attribute used for categorizing groups
                  type: string
                description:
                  description: Group description
                  type: string
                type:
                  description: Group type
                  type: string
                active:
                  description: Group status
                  type: boolean
                createdDate:
                  description: Date of group creation
                  type: integer
                  format: int64
                modifiedDate:
                  description: Date of group last update
                  type: integer
                  format: int64
                memberCount:
                  description: Number of group members
                  type: integer
                  format: int64
                assigneeCount:
                  description: Number of group assignees
                  type: integer
                  format: int64
            UserGroupResponseList:
              type: object
              properties:
                data:
                  type: array
                  items:
                    $ref: '#/definitions/UserGroupResponse'
                pagination:
                  type: object
                  $ref: '#/definitions/Pagination'
            UserGroupUpdate:
              description: Body for group update
              type: object
              properties:
                name:
                  description: Group name
                  type: string
                area:
                  description: Group area
                  type: string
                description:
                  description: Group description
                  type: string
                active:
                  description: Group status
                  type: boolean
            UserGroupMembershipResponseData:
              description: User object response
              type: object
              properties:
                id:
                  type: string
                groupId:
                  type: string
                group:
                  type: object
                  $ref: '#/definitions/GroupRoleScope'
                userId:
                  type: integer
                  format: int64
                user:
                  type: object
                  $ref: '#/definitions/UserCompp'
                active:
                  type: boolean
                lastAddedDate:
                  type: integer
                  format: int64
                lastRemovedDate:
                  type: integer
                  format: int64
            GroupRoleScope:
              description: User Group info to include in other models
              type: object
              properties:
                id:
                  type: string
                  description: Group ID
                name:
                  type: string
                  description: Group name
                area:
                  type: string
                  description: An optional string attribute used for categorizing groups
                type:
                  type: string
                  description: Group type
                active:
                  type: boolean
                  description: Group status
            UserCompp:
              description: Basic user information to include in other models
              type: object
              properties:
                id:
                  type: integer
                  format: int64
                  description: User ID
                  example: 7215545058329
                username:
                  type: string
                  description: Username
                  example: dpayet
                firstName:
                  type: string
                  description: User first name
                  example: Dimitri
                lastName:
                  type: string
                  description: User last name
                  example: Payet
                emailAddress:
                  type: string
                  description: User email addressIntegrationUserManagerTest
                  example: dpayet@om.fr
            UserGroupMembershipRequest:
              description: Body for user group membership creation
              type: object
              properties:
                active:
                  type: boolean
            UserGroupMembershipData:
              description: Body for user group membership response
              type: object
              properties:
                id:
                  type: string
                groupId:
                  type: string
                userId:
                  type: integer
                  format: int64
                group:
                  type: object
                  $ref: '#/definitions/UserGroupData'
                user:
                  type: object
                  $ref: '#/definitions/MembershipData'
                active:
                  type: boolean
                lastAddedDate:
                  type: integer
                  format: int64
                lastRemovedDate:
                  type: integer
                  format: int64
            MembershipData:
              description: User object response
              type: object
              properties:
                id:
                  type: integer
                  format: int64
                userName:
                  type: string
                firstName:
                  type: string
                lastName:
                  type: string
                emailAddress:
                  type: string
            UserGroupData:
              description: Group object response
              type: object
              properties:
                id:
                  description: Group Id
                  type: string
                name:
                  description: Group name
                  type: string
                area:
                  description: Group area
                  type: string
                type:
                  description: Group type
                  type: string
                active:
                  description: Group Status
                  type: boolean
            UserGroupMembershipResponse:
              type: object
              properties:
                data:
                  type: array
                  items:
                    $ref: '#/definitions/UserGroupMembershipResponseData'
                pagination:
                  type: object
                  $ref: '#/definitions/Pagination'
            UserGroupAssignee:
              description: User group assignee object
              type: object
              properties:
                id:
                  description: Assignee id
                  type: string
                groupId:
                  type: string
                group:
                  description: Group
                  type: object
                  $ref: '#/definitions/GroupRoleScope'
                userId:
                  type: integer
                  format: int64
                user:
                  type: object
                  $ref: '#/definitions/UserCompp'
                userRoles:
                  type: array
                  items:
                    type: string
                active:
                  type: boolean
                lastAddedDate:
                  description: Last added
                  type: integer
                  format: int64
                lastRemovedDate:
                  description: Last removed
                  type: integer
                  format: int64
            UserData:
              description: User object response
              type: object
              properties:
                id:
                  type: integer
                  format: int64
                username:
                  type: string
                firstName:
                  type: string
                lastName:
                  type: string
                emailAddress:
                  type: string
            UserGroupAssigneeResponse:
              description: response
              type: object
              properties:
                data:
                  type: array
                  items:
                    $ref: '#/definitions/UserGroupAssignee'
                pagination:
                  type: object
                  $ref: '#/definitions/Pagination'
            UserGroupAssigneeUpdate:
              description: Body for user group assignee update
              type: object
              properties:
                current:
                  description: Assignee status
                  type: boolean
              required:
                - current
            UserGroupMembershipUpdate:
              description: User Group membership update object
              type: object
              properties:
                active:
                  description: Group membership status
                  type: boolean
            UserGroupAssignmentResponse:
              description: User Group assignment response object
              type: object
              properties:
                id:
                  type: string
                  description: Assignment ID
                groupId:
                  type: string
                  description: Group ID
                group:
                  type: object
                  $ref: '#/definitions/GroupRoleScope'
                userId:
                  type: integer
                  format: int64
                  description: User ID
                user:
                  type: object
                  $ref: '#/definitions/UserCompp'
                userRoles:
                  type: array
                  items:
                    type: string
                active:
                  type: boolean
                  description: Group membership status
                lastAddedDate:
                  type: integer
                  format: int64
                  description: Date of group membership last added
                lastRemovedDate:
                  type: integer
                  format: int64
                  description: Date of group membership last removed
            DownloadReceiptCount:
              type: object
              properties:
                fileName:
                  type: string
                  example: Untitled Document.txt
                timestamp:
                  type: integer
                  format: int64
                  example: 1552999335740
            MessageReceiptDetail:
              description: Message receipt details response object
              type: object
              properties:
                user:
                  $ref: '#/definitions/UserCompp'
                deliveryReceiptTimestamp:
                  description: Timestamp of message delivery receipts
                  type: integer
                  format: int64
                  example: 1552999333784
                readReceiptTimestamp:
                  description: Timestamp of message read receipts
                  type: integer
                  format: int64
                  example: 1552999335114
                emailNotificationTimestamp:
                  description: Timestamp of message email notifications
                  type: integer
                  format: int64
                  example: 1552999335114
                downloadReceiptCounts:
                  type: array
                  items:
                    $ref: '#/definitions/DownloadReceiptCount'
                  example:
                    - fileName: Untitled Document.txt
                      timestamp: 1552999335740
            MessageReceiptDetailResponse:
              description: List of Message receipt details
              type: object
              properties:
                creator:
                  $ref: '#/definitions/MessageUser'
                onBehalfOfUser:
                  $ref: '#/definitions/MessageUser'
                stream:
                  $ref: '#/definitions/MessageStream'
                creationDate:
                  type: integer
                  format: int64
                  example: 1552999333141
                deliveryReceiptCount:
                  type: integer
                  example: 1
                readReceiptCount:
                  type: integer
                  example: 1
                emailNotificationCount:
                  type: integer
                  example: 1
                downloadReceiptCounts:
                  type: array
                  items:
                    $ref: '#/definitions/MessageDownloadReceiptCount'
                  example:
                    - fileName: internal_70781
                      count: 1
                MessageReceiptDetail:
                  type: array
                  items:
                    $ref: '#/definitions/MessageReceiptDetail'
                  example:
                    - user:
                        id: 7215545058329
                        username: dpayet
                        firstName: Dimitri
                        lastName: Payet
                        emailAddress: dpayet@om.fr
                      deliveryReceiptTimestamp: 1552999333784
                      readReceiptTimestamp: 1552999335114
                      emailNotificationTimestamp: 1552999335114
                      downloadReceiptCounts:
                        - fileName: Untitled Document.txt
                          timestamp: 1552999335740
                pagination:
                  $ref: '#/definitions/Pagination'
            MessageUser:
              type: object
              properties:
                id:
                  type: integer
                  format: int64
                  example: 7215545058329
                name:
                  type: string
                  example: User Test
            MessageStream:
              type: object
              properties:
                id:
                  type: string
                  example: lFpyw0ATFmji+Cc/cSzbk3///pZkWpe1dA==
                name:
                  type: string
                  example: Test Room
                streamType:
                  type: string
                  example: ROOM
            MessageDownloadReceiptCount:
              type: object
              properties:
                fileName:
                  type: string
                  example: internal_707810
                count:
                  type: integer
                  format: int64
                  example: 1
            MessageDetail:
              description: Message detail
              type: object
              properties:
                messageId:
                  description: message id
                  type: string
                creator:
                  $ref: '#/definitions/MessageUser'
                onBehalfOfUser:
                  $ref: '#/definitions/MessageUser'
                stream:
                  $ref: '#/definitions/MessageStream'
                creationDate:
                  type: integer
                  format: int64
                deliveryReceiptCount:
                  type: integer
                  format: int64
                readReceiptCount:
                  type: integer
                  format: int64
                emailNotificationCount:
                  type: integer
                  format: int64
                downloadReceiptCounts:
                  type: array
                  items:
                    $ref: '#/definitions/MessageDownloadReceiptCount'
            MessageDetails:
              description: Message details
              type: array
              items:
                $ref: '#/definitions/MessageDetail'
            MessageIds:
              type: object
              properties:
                messageIds:
                  $ref: '#/definitions/StringList'
            AssigneeCandidate:
              description: Assignee Candidate
              type: object
              properties:
                userId:
                  type: integer
                  format: int64
                username:
                  type: string
                firstName:
                  type: string
                surname:
                  type: string
                emailAddress:
                  type: string
                canBeAssigned:
                  type: boolean
                roles:
                  $ref: '#/definitions/StringList'
            AssigneeCandidates:
              description: List of assignee candidate
              type: object
              properties:
                users:
                  type: array
                  items:
                    $ref: '#/definitions/AssigneeCandidate'
                pagination:
                  type: object
                  $ref: '#/definitions/Pagination'
            Languages:
              description: List of languages
              type: object
              properties:
                languages:
                  $ref: '#/definitions/StringList'
            MessageMetadataResponse:
              description: Message metadata
              type: object
              properties:
                messageId:
                  type: string
                parent:
                  type: object
                  properties:
                    messageId:
                      type: string
                      description: Id of the parent message queried
                    relationshipType:
                      type: string
                      enum:
                        - REPLY_FORM
                        - REPLY
                        - FORWARD
                replies:
                  type: array
                  items:
                    type: string
                forwards:
                  type: array
                  items:
                    type: string
                formReplies:
                  type: array
                  items:
                    type: string
            UserSuspension:
              type: object
              properties:
                suspended:
                  type: boolean
                  example: true
                suspendedUntil:
                  type: integer
                  format: int64
                  example: 1601546400
                suspensionReason:
                  type: string
                  example: The user will be OOO due to a mandatory leave
            FollowersList:
              type: object
              properties:
                followers:
                  $ref: '#/definitions/UserIdList'
            FollowersListResponse:
              type: object
              properties:
                count:
                  type: integer
                  format: int64
                  example: 2
                followers:
                  type: array
                  items:
                    type: integer
                    format: int64
                  example:
                    - 13056700579848
                    - 13056700580889
                pagination:
                  $ref: '#/definitions/Pagination'
            FollowingListResponse:
              type: object
              properties:
                count:
                  type: integer
                  format: int64
                  example: 2
                following:
                  type: array
                  items:
                    type: integer
                    format: int64
                  example:
                    - 13056700579848
                    - 13056700580889
                pagination:
                  $ref: '#/definitions/Pagination'
            V1IMAttributes:
              type: object
              properties:
                pinnedMessageId:
                  type: string
                  description: >-
                    UrlSafe message id of the pinned message inside the IM. To
                    perform unpin operation, send an empty string.
                  example: vd7qwNb6hLoUV0BfXXPC43___oPIvkwJbQ
            V1IMDetail:
              type: object
              properties:
                V1IMAttributes:
                  $ref: '#/definitions/V1IMAttributes'
                IMSystemInfo:
                  $ref: '#/definitions/IMSystemInfo'
            IMSystemInfo:
              type: object
              properties:
                id:
                  type: string
                  example: usnBKBkH_BVrGOiVpaupEH___okFfE7QdA
                creationDate:
                  type: integer
                  format: int64
                  description: >-
                    The datetime when the stream was originally created.
                    Milliseconds since Jan 1 1970.
                  example: 1610520703317
                active:
                  type: boolean
                  description: >-
                    If false, no messages can be sent in this stream, and
                    membership is locked.
                  example: true
            ServiceAccountManifest:
              type: object
              properties:
                manifest:
                  type: string
                  maxLength: 6144
                  description: >-
                    Manifest containing commands supported by the service
                    account. Must be valid JSON.
              required:
                - nu
    aid: symphony:symphony-pod-api
    overlays:
      - type: APIs.io Search
        url: overlays/pod-openapi-search.yml
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---